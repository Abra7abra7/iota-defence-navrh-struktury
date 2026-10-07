# DELTA DEFENCE: Organizačná štruktúra, matica zodpovedností a procesné toky

**Verzia dokumentu:** 1.0 (Lean Defense Startup)  
**Klasifikácia:** Interné riadenie / Ochrana know-how & Utajované skutočnosti  
**Právny rámec:** Zákon č. 392/2011 Z. z. (Vojenský materiál), Zákon č. 215/2004 Z. z. (Ochrana utajovaných skutočností), Nariadenie EÚ o kontrole položiek s dvojakým použitím (Dual-Use)

---

## 1. Manažérske zhrnutie a bezpečnostný status

Spoločnosť pôsobí v oblasti obranného priemyslu s primárnym zameraním na **vývoj a výrobu bezpilotných leteckých systémov (UAV) a systémov umelej inteligencie (AI)** pre autonómne navádzanie a vyhodnocovanie taktických cieľov.

Firma je **držiteľom povolenia na obchodovanie s vojenským materiálom** a vstupuje do režimu **práce s utajovanými skutočnosťami**. V tomto prostredí nie je možné fungovať ako v bežnom technologickom startupe:
1. **Regulácia a sankčné riziká:** Neoprávnený kontakt, nesprávny export alebo únik špecifikácií znamená okamžitú stratu licencie a trestnoprávnu zodpovednosť.
2. **Need-to-Know princíp:** Každý pracovník vidí striktne iba to, čo bezpodmienečne potrebuje na výkon svojej práce. Účtovník nesmie vidieť algoritmy AI; programátor nesmie vidieť marže a zmluvy; obchodník nesmie vidieť konštrukčné dáta.
3. **Nezávislé VETO:** Compliance Officer disponuje právnou a bezpečnostnou autoritou, ktorá nepodlieha komerčným tlakom a ktorú nemôže zrušiť ani CEO.

---

## 2. ⚠️ KRITICKÉ ZISTENIE Z GRILL-ME: Status externého R&D a IP

> [!CAUTION]
> **AKÚTNA HROZBA PRE BEZPEČNOSŤ A LICENCIU FIRMY:**
> V rámci úvodného auditu bolo identifikované, že **AI programátor je externista**, pričom technológia je v stave Proof-of-Concept **bez zmluvného prevodu duševného vlastníctva (IP assignment)** a bez dedikovaného technického zabezpečenia.

### Okamžité nápravné opatrenia (Fáza 0 - Pred začatím výroby):
1. **Právny prevod majetkových práv (IP Assignment):**
   - Okamžitý podpis *Zmluvy o vytvorení diela s výhradným a neobmedzeným prevodom majetkových autorských práv* a know-how na spoločnosť.
   - Podpis bezpečnostnej zmluvy a doložky o mlčanlivosti (NDA) s vysokou zmluvnou pokutou a sankciami podľa zákona o ochrane utajovaných skutočností.
2. **Izolácia vývojového prostredia (Zero Cloud Leak):**
   - Zákaz ukladania zdrojových kódov a natrénovaných modelov na verejné cloudy (verejný GitHub, Google Drive, AWS bez vojenskej certifikácie).
   - Vytvorenie **lokálneho on-premise šifrovaného repozitára** (napr. GitLab/Gitea na hardvérovo šifrovanom serveri v chránenom priestore firmy).
3. **Previerka personálnej bezpečnosti:**
   - Začatie procesu bezpečnostnej previerky programátora (podľa stupňa utajenia vyžadovaného NBÚ).

---

## 3. Lean organizačná štruktúra (Roly a kompetencie)

| Rola | Hlavné poslanie | Kľúčové právomoci | Podlieha / Zodpovedá sa |
| :--- | :--- | :--- | :--- |
| **CEO (Generálny riaditeľ & Štatutár)** | Strategické vedenie, kapitál, podpis zmlúv, celková právna a trestnoprávna zodpovednosť. | Konečný podpis kontraktov, schvaľovanie rozpočtov, personálne rozhodnutia. | Dozorná rada / Vlastníci |
| **Compliance Officer (Bezpečnostný správca)** | Dohľad nad vojenskými licenciami, exportnou kontrolou, styk s NBÚ, MO SR a MH SR. | **ABSOLÚTNE VETO** nad akýmkoľvek obchodom a partnerom. Audit prístupov. | Zo zákona nezávislý; priamy report CEO & NBÚ |
| **Obchodník (Defense Sales & BD)** | Vyhľadávanie zákazníkov (B2G / MoD / zahraniční partneri), zber požiadaviek, príprava tenderov. | Komunikácia s klientom v rámci schválených katalógových listov. | CEO |
| **Účtovník (Financie, Clá & Sklad)** | Finančné toky, kalkulácie marží, colné konania a evidencia položiek s dvojakým použitím (BOM). | Vystavovanie faktúr, colná evidencia dovážaných dielov, daňové priznania. | CEO |
| **Externý Programátor (AI & R&D Lead)** | Vývoj autonómnych modelov, computer vision, navádzania UAV a integrácia senzoriky. | Prístup k dedikovanému vývojovému prostrediu a testovaciemu hardvéru. | CEO / Technický manažér |

---

## 4. Matica bezpečnostných prístupov (Need-to-Know & Access Control)

Každý informačný aktívum v spoločnosti má priradenú úroveň klasifikácie a prísne riadené prístupové práva:

| Informačné aktívum / Systém | Klasifikácia | CEO | Compliance Officer | Obchodník | Účtovník | Programátor (AI R&D) |
| :--- | :--- | :---: | :---: | :---: | :---: | :---: |
| **Zdrojový kód AI & Algoritmy** | Prísne tajné / IP | ❌ (Iba high-level) | 🔍 (Audit prístupov) | ❌ **ZÁKAZ** | ❌ **ZÁKAZ** |  **PLNÝ PRÍSTUP** |
| **CAD výkresy & Konštrukcia UAV** | Obchodné tajomstvo / VM |  (Čítanie) | 🔍 (Audit exportu) | ❌ **ZÁKAZ** | ❌ **ZÁKAZ** |  (Iba rozhrania senzorov) |
| **End-User Certificate (EUC) & Zákazník** | Dôverné (VM režim) |  (Plný) |  **PLNÝ (Vetting)** |  (Zber dát) | ❌ **ZÁKAZ** (Vidí len anonymizované IČO) | ❌ **ZÁKAZ** |
| **Finančné marže, zmluvy & ceny** | Dôverné (Komerčné) |  (Plný) | 🔍 (Audit súladu) |  (Iba predajná cena) |  **PLNÝ (BOM & Náklady)** | ❌ **ZÁKAZ** |
| **Sankčné spisy & Previerky NBÚ** | Vyhradené / Dôverné |  (Informovaný) |  **SPRÁVCA (Veto)** | ❌ **ZÁKAZ** | ❌ **ZÁKAZ** | ❌ **ZÁKAZ** |
| **Zásobovacia BOM & Colná evidencia** | Interné |  (Prehľad) | 🔍 (Kontrola Dual-Use) | ❌ **ZÁKAZ** |  **PLNÝ PRÍSTUP** | 🔍 (Len tech. špecifikácie) |

*Legenda:  Plný prístup | 🔍 Prístup na audit/čítanie | ❌ Prísny zákaz prístupu*

---

## 5. RACI Matica zodpovedností

- **R (Responsible):** Vykonávateľ úlohy.
- **A (Accountable):** Konečný schvaľovateľ nesúci zodpovednosť (len jeden).
- **C (Consulted):** Poskytuje odborné stanovisko pred rozhodnutím.
- **I (Informed):** Je informovaný po vykonaní kroku.

| Kľúčová aktivita / Proces | CEO | Compliance | Obchodník | Účtovník | Programátor |
| :--- | :---: | :---: | :---: | :---: | :---: |
| Akvizícia klienta a príjem dopytu | I | I | **R / A** | I | I |
| Sankčná kontrola koncového používateľa (Vetting) | I | **R / A (VETO)** | C | I | I |
| Schválenie technického scope (čo je možné vyrobiť) | A | C | I | I | **R** |
| Kalkulácia výrobných nákladov a ceny | A | I | C | **R** | C |
| Žiadosť o exportnú/obchodnú licenciu (MH SR) | I | **R / A** | I | C | I |
| Finálny podpis zmluvy so zákazníkom | **R / A** | C (Potvrdenie) | I | I | I |
| Nákup komponentov podliehajúcich Dual-Use | A | C (Licencia) | I | **R (Colnica)** | C (Výber dielov) |
| Bezpečné uloženie a správa AI kódu | A | C (Audit NBÚ) | I | I | **R** |
| Výroba, montáž a flashovanie softvéru | A | I | I | I | **R** |
| Letové testy na vojenskom polygóne | A | C (Povolenia) | I | I | **R (Vyhodnotenie)** |
| Výstupná vojenská prebierka a expedícia | **R / A** | C (Export check) | I | I | C |

---

## 6. Detailný Proces 1: Obchodno-licenčný tok (Lead-to-Contract)

Tento tok garantuje, že firma neuzavrie obchod so sankcionovaným subjektom a neposkytne technické informácie bez platnej licencie.

```
[Dopyt / Tender] 
       ↓
[Zber údajov o koncovom používateľovi (EUC)] 
       ↓
[BRÁNA 1: Sankčný Vetting & Compliance]
       ├── [Porušenie / Riziko] ──→ ⛔ ABSOLÚTNE VETO (Stop & Archivácia)
       └── [Schválené]
              ↓
[Cenová kalkulácia & Marža (Účtovník)]
       ↓
[Schválenie ponuky (CEO)]
       ↓
[Podpis Zmluvy s doložkou o licencii (Štatutár)]
```

### Podrobný popis krokov:
1. **Dopyt (Sales):** Obchodník zaznamená požiadavku od zákazníka. Nesmie sľúbiť konkrétne neštandardné vojenské modifikácie.
2. **EUC Dossier (Sales):** Obchodník vyžiada identifikačné údaje, End-User Certificate a plánované teritórium nasadenia.
3. **Sankčný Vetting (Compliance - Mandatórna Brána):**
   - Preverenie voči sankčným zoznamom (EÚ, OFAC, OSN).
   - Posúdenie súladu so Zákonom č. 392/2011 Z. z. a zahraničnopolitickými záujmami SR.
   - **VETO Rozhodnutie:** Ak Compliance vydá zamietavé stanovisko, **proces okamžite končí**. Toto veto nie je možné prehlasovať žiadnym orgánom firmy.
4. **Licenčná Zelená (Compliance):** Udelenie predbežného licenčného súhlasu a definícia povoleného rozsahu špecifikácie.
5. **Kalkulácia Ceny (Účtovník & CEO):** Účtovník na základe kusovníka (BOM) a prevádzkových nákladov spočíta cenu; CEO schváli maržu.
6. **Kontrakt (CEO):** Štatutár podpisuje zmluvu. Zmluva povinne obsahuje suspenzívnu doložku viazanú na udelenie konečnej vývoznej licencie.

---

## 7. Detailný Proces 2: Vývojovo-výrobný a dodávateľský tok (R&D-to-Delivery)

Tento tok zabezpečuje bezpečný prechod od vývoja softvéru a nákupu hardvéru až po armádnu prebierku a odovzdanie.

```
[Zmluvný prevod IP & Bezpečnostná doložka (Compliance)]
       ↓
[Presun kódu do On-Prem šifrovaného repozitára (R&D)]
       ↓
[Nákup Dual-Use komponentov & Colná evidencia (Účtovník)]
       ↓
[Montáž UAV v chránenom priestore & Bezpečné flashovanie AI (R&D)]
       ↓
[Letové skúšky na schválenom polygóne (R&D)]
       ↓
[Výstupná armádna prebierka & Protokolárne odovzdanie (CEO)]
```

### Podrobný popis krokov:
1. **IP Prevod & Bezpečnosť (Compliance & R&D):**
   - Podpis prevodu práv a NDA s externým vývojárom.
   - Zavedenie prístupu na základe bezpečnostnej previerky.
2. **Chránený Repozitár (R&D):**
   - Nasadenie izolovaného git servera bez prístupu z verejného internetu.
   - Správa váh AI modelov a trénovacích dát s kryptografickým podpisom.
3. **Nákup Dual-Use komponentov (Účtovník & Compliance):**
   - Nákup motorov, autopilota, senzorov a výpočtových modulov.
   - Účtovník vedie evidenciu sériových čísel v colnom sklade a sleduje položky s dvojakým použitím.
4. **Montáž a Integrácia (Výroba & R&D):**
   - Fyzická stavba draku UAV v zabezpečenej dielni.
   - Flashovanie autorizovaného firmvéru a AI modelov cez vyhradený servisný terminál.
5. **Letové Skúšky (R&D & Testovací pilot):**
   - Testovanie letovej obálky, autonómneho navádzania a senzorov na vyhradenom polygóne s povolením letovej prevádzky.
   - Vyhotovenie telemetrického a skúšobného protokolu.
6. **Armádna Prebierka & Expedícia (CEO & Zákazník):**
   - Formálna prebierka zástupcom zákazníka (napr. Úrad pre obrannú štandardizáciu / MO SR).
   - Podpis odovzdávacieho protokolu a bezpečná špedícia v súlade s licenciou na prepravu vojenského materiálu.

---

## 8. Interaktívne vizualizácie v Archify & SSOT Portál

Pre celú spoločnosť bol vybudovaný **Jediný zdroj pravdy (SSOT)** s 15 interaktívnymi modelmi a centrálnym portálom:

> 🌐 **Hlavný portál:** [diagrams/index.html](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/index.html)  
> 📑 **Master SSOT dokumentácia:** [docs/SSOT_MASTER_INDEX.md](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/docs/SSOT_MASTER_INDEX.md)

### Prehľad interaktívnych modelov:
* **Architektúra riadenia:** [FC-01 Organizačná štruktúra & reporting](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/fc01-org-reporting.html) | [FC-02 Tri línie ochrany](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/fc02-three-lines-of-defense.html) | [FC-05 Architektúra 4 dátových zón](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/fc05-data-zones.html) | [ARCH-01 Bezpečnostný perimeter](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/org-security-architecture.html)
* **Kľúčové workflowy:** [PROC-01 Lead-to-Contract](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/lead-to-contract.html) | [PROC-02 R&D-to-Delivery UAV](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/rd-to-delivery.html) | [FC-03 Onboarding & IP transfer](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/fc03-onboarding-access.html) | [FC-04 Nákup P2P & 3-Way Match](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/fc04-p2p-procurement.html) | [FC-07 Due Diligence partnerov](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/fc07-due-diligence.html) | [FC-09 Sankcie & Export Control](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/fc09-sanctions-export-control.html)
* **Incidenty a kontinuita:** [FC-08 & FC-14 Incident response & SIEM](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/fc08-fc14-incident-response.html) | [FC-15 BCP & Disaster Recovery](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/fc15-bcp-dr.html) | [FC-10-12 Whistleblowing, Dary & Konflikt](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/fc10-fc12-ethics-governance.html)
* **Sekvencie a AI Governance:** [FC-13 Schvaľovacie limity L1–L4](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/fc13-approval-limits.html) | [FC-16 AI Agent Gated Flow & Replay](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/fc16-ai-agent-decision.html)

---

## 9. Odporúčané ďalšie kroky (Implementačný plán)

1. **Právna dokumentácia k externistovi:** Pripraviť a podpísať zmluvu o prevode práv (IP assignment) a bezpečnostnú dohodu.
2. **Menovanie Bezpečnostného zamestnanca:** Formálne poverenie Compliance Officera funkciou bezpečnostného zamestnanca pre styk s NBÚ.
3. **Zriadenie Chráneného priestoru:** Fyzické vymedzenie montážneho a vývojového priestoru so vstupom na čipové karty a knihou návštev.
4. **Zavedenie On-Prem infraštruktúry:** Inštalácia interného GitLab servera a šifrovaného sieťového úložiska pre CAD a AI modely.
