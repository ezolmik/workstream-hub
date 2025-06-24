# Mindspire TAD módszertan

## Módszertani háttér

A TAD módszertan használata (s folyamatos fejlesztése) közel 10 éves múltra tekint vissza. Az architektúra tervezési gyakorlatban ismert best practice-eket és eszközöket (kérdőívek, sablonok, folyamatleírások) alkalmaz, amelyek garantálják a magas minőségű teljesítést.

## Jellemzők

* A vizsgálat BIAN domain logikán alapul.
* Alkalmazásokat három kategóriába soroljuk: **kritikus**, **nem kritikus**, **nem releváns**.
* Külön figyelmet kapnak: Symbols, CBS, adatárház, RTPE stb.
* Külön értékelési módszertan, kérdőív.

## Célok

* Átfogó kép a bank jelenlegi IT architektúrájáról
* 5 éves jövőkép a banki architektúráról
* KPI-ok, nyomon követés, dokumentált döntések

## Referenciák

* MBH Bank, Raiffeisen Albánia, OTP csoport (Szlovénia, Albánia, stb.), KDB, K\&H CBS, Spirit program

## Részletes fázisleírások és segédletek

* [Fázis 1: Előkészítés](./tad/phase-01-elokeszites.md)
* [Fázis 2: Adatgyűjtés és feldolgozás](./tad/phase-02-adatgyujtes.md)
* [Fázis 3: Onsite workshopok](./tad/phase-03-workshopok.md)
* [Fázis 4: Részletes elemzés](./tad/phase-04-reszletes-elemzes.md)
* [Fázis 5: Követő feladatok](./tad/phase-05-koveto-feladatok.md)
* [Fázis 6: Lezárás és jóváhagyás](./tad/phase-06-lezaras.md)
* [Értékelési szempontok (minta)](./tad/evaluation-criteria.md)
* [To-be architektúra design folyamat](./tad/to-be-design-flow.md)
* [Minta leszállítandók](./tad/sample-deliverables.md)
* [Ütemezés](./tad/planning-timeline.md)
* [Stakeholder szerepkörök](./tad/stakeholder-roles.md)
* [Projekt feltételezések](./tad/project-assumptions.md)

## Testreszabási fázis (2025. július – október)

A módszertan testreszabása során az Erste Bank architecture squad:

* végigmegy a fenti fázisokon és segédleteken,
* kialakítja a bank-specifikus sablonokat, kérdőíveket, értékelési szempontokat,
* összehangolja a belső szereplőkkel (pl. IT vezetők, application ownerök),
* véglegesíti a leszállítandók formátumát,
* és előkészíti a GAP analízis, KPI, roadmap szállítást.

> A testreszabás munkaterülete: [./tad/customization/](./tad/customization/) – itt lesznek az Erste-specifikus anyagok és munkavázlatok.
