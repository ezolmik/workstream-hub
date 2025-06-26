# Core Banking Stack – Symbols rendszer háttérarchitektúra

Ez a dokumentum összefoglalja a Symbols alapú core banking rendszer fizikai és logikai architektúráját, ahogy az a bankban jellemzően kiépítésre kerül.

---

## 🌟 Szerep

A core banking rendszer biztosítja az alábbiakat:

* Számlák és hitelek vezetése
* Tranzakciók könyvelése
* Kamatképzés, napzárás, főkönyvi szinkron
* Adatok kiszolgálása REST/SOAP adaptereken keresztül

---

## 🧱 Fizikai komponensek

### 1. Oracle RAC (Real Application Cluster)

* **Típus:** tranzakciós adatbázis
* **Működés:** több node párhuzamos írással/olvasással
* **Jellemzők:**

  * ACID garancia
  * Nagy IOPS, SAN háttértár
  * Kétirányú replikáció DR site felé

---

### 2. Application szerverek (Symbols motor)

* **Típus:** Java EE vagy Spring alapú alkalmazás
* **Elrendezés:** Active / Standby (nem aktív/aktív)
* **Funkciók:**

  * SOAP szolgáltatások
  * Ügyintézői GUI kiszolgálás
  * Éjszakai batch feldolgozás (pl. kamatszámítás, zárás)

---

### 3. Load Balancer

* **Típus:** hardveres (pl. F5) vagy szoftveres (pl. HAProxy)
* **Funkciók:**

  * Terheléselosztás az app node-ok között
  * Failover a standby node-ra
  * Session stickiness SOAP hívásoknál

---

## 🗜️ Logikai elrendezés

```
+-------------------+
| Load Balancer     |
+-------------------+
       ↓       ↓
+-------------+ +-------------+
| App Node A  | | App Node B  |
| (Active)    | | (Standby)   |
+-------------+ +-------------+
       ↓             ↓
     +----------------------+
     |   Oracle RAC Cluster |
     +----------------------+
```

---

## 🧠 Jellemző működési minták

* A Symbols rendszer nem konténerizált.
* Telepítése tipikusan VMWare-en vagy fizikai gépen történik.
* REST vagy SOAP adapterek szolgálják ki a peremrendszereket.
* Peremrendszerek gyakran **szatellitként** működnek, és "fordítanak" REST ↔ SOAP vagy fájl ↔ batch kapcsolatot.

---

## 📌 Megjegyzés

Ez a dokumentum nem az alkalmazások funkcionális architektúrájának része, hanem egy stabil referenciapont azok számára, akik Symbols interfészeket vagy adaptereket térképeznek fel.
