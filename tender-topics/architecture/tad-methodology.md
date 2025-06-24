# Mindspire TAD módszertan

## Módszertani háttér

A TAD módszertan használata (és folyamatos fejlesztése) közel 10 éves múltra tekint vissza. Az architektúra tervezés során bevált best practice-eket alkalmaz (kérdőívek, sablonok, folyamatleírások), amelyek garantálják a feladatok minőségi elvégzését.

## Jellemzők

* A felmérés során az alkalmazás elemeket **BIAN domain** alapú csoportosítás szerint vizsgáljuk.
* Az alkalmazásokat három kategóriába soroljuk:

  * **Kritikus**
  * **Nem kritikus**
  * **Nem releváns**
* A **kritikus alkalmazások** kerülnek részletes feltérképezésre, mivel ezek adják a jövőbeli architektúra gerincét.
* Kiemelt figyelmet kapnak olyan rendszerek, mint a **Symbols**, **adatárház**, **RTPE**, amelyek más alkalmazásokkal erős kapcsolatban állnak.
* A kritikus alkalmazásokhoz jövőbeli célarchitektúra koncepció készül, míg a nem kritikus elemeket elemzéssel illesztjük a jövőképbe.

## Főbb szakaszok

A feladatvégzés 6 fő szakaszból áll:

1. Előkészítés
2. Adatgyűjtés és feldolgozás
3. Workshopok
4. Részletes elemzés
5. Követő feladatok
6. Lezárás és jóváhagyás

*(A szakaszokhoz tartozó konkrét feladatokat és eredménytermékeket a részletes dokumentáció tartalmazza.)*

## Célok

* Átfogó kép a bank jelenlegi IT architektúrájáról
* Döntés-előkészítő anyagok az alkalmazásokról
* 5 éves jövőkép a banki célarchitektúráról, amely megfelel:

  * az **Erste Group** sztenderdjeinek
  * az iparági elvárásoknak (pl. **cloud képességek**)
* KPI-ok és irányelvek a jövőbeli architektúra nyomon követéséhez

## Referenciák

A módszertant az alábbi intézményeknél alkalmazták:

* MBH Bank
* Raiffeisen Bank Albánia
* OTP Bank: Szlovénia, Albánia, Montenegró, Bulgária, Szerbia, Horvátország, Moldávia, Üzbegisztán
* KDB Bank
* OTP Bank Magyarország CBS projekt
* K\&H Spirit program

## Munkamegosztás a résztvevők között

| Erste Bank IT                          | Erste Bank Business          | Mindspire                                     |
| -------------------------------------- | ---------------------------- | --------------------------------------------- |
| Dokumentumok gyűjtése                  | Egyeztetések / workshopok    | Módszertan                                    |
| Egyeztetések / workshopok              | Részletes elemzés            | Koordináció                                   |
| Részletes elemzésben való közreműködés | Javaslattétel, döntéshozatal | Részletes elemzés és workshopok lebonyolítása |
| Döntéshozatal                          |                              | Dokumentáció                                  |
