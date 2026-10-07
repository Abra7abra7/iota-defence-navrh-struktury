# IOTA & DELTA DEFENCE: Jediný zdroj pravdy (SSOT) – Architektúra, Pravidlá a Procesy

**Spoločnosť:** IOTA Defence a.s. (projekt Delta Defence)  
**Verzia dokumentu:** 2.0 (Kompletný podnikovorozmerný SSOT systém)  
**Dátum účinnosti:** 7. október 2026  
**Vypracoval:** Márian Stančík  
**Klasifikácia:** Interné riadenie / Dôverné (Pre vnútornú potrebu a orgány spoločnosti)  
**Zákonný rámec:**
* Zákon č. 392/2011 Z. z. o obchodovaní s vojenským materiálom
* Zákon č. 215/2004 Z. z. o ochrane utajovaných skutočností
* Nariadenie Európskeho parlamentu a Rady (EÚ) 2021/821 (Dual-Use export control)
* Zákon č. 54/2019 Z. z. o ochrane oznamovateľov protispoločenskej činnosti (Whistleblowing)
* Nariadenie EÚ o umelej inteligencii (EU AI Act) & Zákon č. 69/2018 Z. z. o kybernetickej bezpečnosti (NIS2)

---

## 🧭 Rýchla navigácia v SSOT systéme

Všetky procesy, perimetre a sekvencie sú prepojené s interaktívnymi, validovanými modelmi v samostatnom HTML formáte. 

> 🌐 **Centrálny vizuálny portál spoločnosti:**  
> **[Otvoriť interaktívny Dashboard modelov](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/index.html)**

---

## 1. Strategický rámec & Poslanie spoločnosti

IOTA Defence a.s. je špecializovaná obranno-technologická spoločnosť zameraná na:
1. **Vývoj a certifikáciu bezpilotných leteckých systémov (UAV).**
2. **Vývoj autonómnych modelov umelej inteligencie (AI)** pre taktické navádzanie, počítačové videnie (Computer Vision) a fúziu senzorických dát v elektronicky rušenom prostredí (GNSS-denied navigation).
3. **Výrobu, montáž a letové testovanie** v režime držiteľa licencie na vojenský materiál a bezpečnostnej previerky priemyselnej bezpečnosti.

### Tri základné piliere riadenia:
1. **Nezávislé VETO Compliance:** Komerčný záujem nikdy neprevažuje nad zákonným súladom. CCO a CISO disponujú zákonnou a internou autoritou zastaviť akúkoľvek zákazku alebo prístup.
2. **Need-to-Know a oddelenie perimetrov:** Každý pracovník vidí len to, čo nevyhnutne potrebuje na výkon svojej práce. Obchodník nevidí kód ani CAD; vývojár nevidí marže; účtovník nevidí taktické algoritmy.
3. **Policy-as-Code & Preukázateľný audit trail:** Rozhodnutia sú zaznamenávané deterministicky s nemennou časovou stopou (vrátane rozhodnutí AI agentov).

---

## 2. Model riadenia a tri línie ochrany (Governance Architecture)

Spoločnosť striktne implementuje medzinárodný štandard **Three Lines of Defense** prispôsobený na podmienky vojenského a utajovaného režimu.

```
                    ┌──────────────────────────────────────────────┐
                    │      Valné zhromaždenie (Akcionári)          │
                    └──────────────────────┬───────────────────────┘
                                           │
                    ┌──────────────────────▼───────────────────────┐
                    │        Dozorná rada (Zákonný dohľad)         │
                    └──────────────┬───────────────────────────────┘
                                   │
              ┌────────────────────┴────────────────────┐
              │                                         │
┌─────────────▼─────────────────────────┐   ┌───────────▼───────────────────────────┐
│       Predstavenstvo (CEO)            │   │  3. LÍNIA: Interný audit (IA)         │
│     Exekutívne riadenie a.s.          │   │  Nezávislé testovanie pre Dozornú radu│
└─────────────┬─────────────────────────┘   └───────────────────────────────────────┘
              │
              ├─────────────────────────────────────────┐
              │                                         │
┌─────────────▼─────────────────────────┐   ┌───────────▼───────────────────────────┐
│ 2. LÍNIA: Nezávislý dohľad & STOP     │   │ 1. LÍNIA: Prevádzka (Vlastníci rizík) │
│ • CCO (Licencie, Sankcie, ABAC, VETO) │   │ • R&D & AI Vývoj (Kód a modely)       │
│ • CISO (Kybernetická bezpečnosť, NBÚ) │   │ • Výroba UAV & Dielňa                 │
│ • ECO (Export Control & EUC)          │   │ • Obchod (Sales & Tendery)            │
│ • Legal & DPO (Zmluvy, GDPR)          │   │ • Financie & Nákup (P2P, Clá)         │
└───────────────────────────────────────┘   └───────────────────────────────────────┘
```

### Kľúčové diagramy architektúry riadenia:
* 🏛️ **[FC-01: Organizačná štruktúra & Governance Reporting (HTML)](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/fc01-org-reporting.html)**
* 🛡️ **[FC-02: Model troch línií ochrany & STOP-Right (HTML)](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/fc02-three-lines-of-defense.html)**

### Zásady riadiacich línií:
1. **Zákaz kumulácie:** Žiadny pracovník nesmie kumulovať rolu v 1. línii (výkon) a 2. línii (kontrola).
2. **Oddelenie CISO (Uznesenie U-06):** CISO nie je podriadený vedúcemu IT infraštruktúry.
3. **Notifikácia odvolania:** Ak predstavenstvo navrhne odvolanie CCO, CISO alebo ECO, musí to vopred oznámiť Dozornej rade s odôvodnením.

---

## 3. Bezpečnostná architektúra 4 dátových zón (Data Zones)

Pre zabránenie únikom kľúčového IP (zdrojové kódy, neurónové siete, CAD výkresy) a pre splnenie požiadaviek NBÚ platí striktné rozdelenie do 4 zón:

| Dátová zóna | Klasifikácia dát | Prípustné úložiská & Technológie | Podmienky prístupu | Zákazy (STOP) |
| :--- | :--- | :--- | :--- | :--- |
| **Zóna 1: Verejná** | Verejné / Marketing | Web, sociálne siete, verejné datasheety | Ktokoľvek (publikuje autorizovaný pracovník) | Zákaz zverejnenia tech. parametrov bez previerky Export Control |
| **Zóna 2: Interná** | Bežná interná prevádzka | Firemný cloud tenant v EÚ (M365 / Workspace) | Firemný účet, spravované zariadenie, povinné MFA | Zákaz používania súkromných cloudov a nefiremných zariadení |
| **Zóna 3: Dôverná** | Zmluvy, marže, DD spisy, AI kód, CAD | ERP, CRM, on-premise šifrovaný GitLab / Vault | Need-to-know, schválenie vlastníka dát a CISO | **Zákaz lokálneho sťahovania dát pre externistov (freelancerov)**; zákaz neoverených USB |
| **Zóna 4: Utajovaná** | Utajované skutočnosti (Zák. 215/2004) | Fyzicky certifikovaný chránený priestor NBÚ, Air-gap servery | Platná bezpečnostná previerka NBÚ príslušného stupňa | **Kategorický zákaz bežného cloudu, e-mailu, bežnej siete a verejných AI nástrojov** |

### Kľúčové diagramy dátových zón a perimetrov:
* 🗄️ **[FC-05: Architektúra 4 dátových zón & Perimetrov (HTML)](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/fc05-data-zones.html)**
* 🏢 **[ARCH-01: Celkový bezpečnostný perimeter Delta Defence (HTML)](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/org-security-architecture.html)**

---

## 4. Matica prístupových práv (Need-to-Know) & RACI

Každá rola v spoločnosti má presne limitované prístupy:

| Informačné aktívum | CEO | CCO / ECO | CISO | Obchodník | Účtovník / Nákup | AI Programátor | Výrobný technik |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **Zdrojový kód AI & Algoritmy** | ❌ (Iba súhrn) | 🔍 (Audit) | 🔍 (Bezpečnosť) | ❌ **ZÁKAZ** | ❌ **ZÁKAZ** | ✅ **PLNÝ PRÍSTUP** | ❌ (Len binárny flash) |
| **CAD výkresy UAV & Avionika** | 🔍 (Prehľad) | 🔍 (Audit) | 🔍 (Bezpečnosť) | ❌ **ZÁKAZ** | ❌ **ZÁKAZ** | 🔍 (Senzorické I/O) | ✅ **PLNÝ (Dielňa)** |
| **End-User Certificate (EUC)** | ✅ (Plný) | ✅ **VETTING** | 🔍 (Audit) | 📝 (Zber podkladov) | ❌ **ZÁKAZ** | ❌ **ZÁKAZ** | ❌ **ZÁKAZ** |
| **Finančné marže & Náklady (BOM)**| ✅ (Plný) | 🔍 (ABAC) | ❌ **ZÁKAZ** | ❌ (Len koncová cena)| ✅ **PLNÝ PRÍSTUP** | ❌ **ZÁKAZ** | ❌ (Len kusovník) |
| **Sankčné spisy & Previerky NBÚ** | 🔍 (Informovaný)| ✅ **SPRÁVCA** | ✅ **SPRÁVCA** | ❌ **ZÁKAZ** | ❌ **ZÁKAZ** | ❌ **ZÁKAZ** | ❌ **ZÁKAZ** |

*Vysvetlivky: ✅ Plný prístup | 🔍 Prístup na audit a čítanie | 📝 Zber podkladov | ❌ Striktný zákaz prístupu*

---

## 5. Podpisový poriadok a finančné limity schvaľovania (L1–L4)

Platí podľa interného predpisu `06_Limity-schvalovania-v1.2` a uznesenia Predstavenstva:

```
[Hodnota záväzku bez DPH kumulatívne za 12 mesiacov]
  │
  ├── Do 1 000 € ────────────── L1 (1-Eye): Vedúci oddelenia / Schválený partner
  │
  ├── 1 001 € až 10 000 € ────── L2 (4-Eyes): Manažér + Finančný úsek
  │
  ├── 10 001 € až 50 000 € ───── L3 (+ CCO): Manažér + Financie + CCO (Mandatórny filter)
  │                                (alebo AKÝKOĽVEK rizikový prípad bez ohľadu na sumu)
  │
  └── Nad 50 000 € ───────────── L4: Predstavenstvo a.s. (Štatutár / bez horného limitu)
```

### Kľúčový diagram sekvencie schvaľovania:
* 💳 **[FC-13: Schvaľovacie limity L1–L4 & Podpisový poriadok (HTML)](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/fc13-approval-limits.html)**

### Záväzné pravidlá:
1. **Zákaz delenia zákaziek:** Úmyselné rozdelenie objednávok s cieľom obísť schvaľovaciu úroveň (napr. 2x 900 € namiesto 1 800 €) je závažným disciplinárnym previnením.
2. **Mandatórny rizikový filter L3:** Každý obchod s verejným činiteľom, zahraničným agentom, rizikovou krajinou, konfliktom záujmov alebo mimo štandardného procesu ide **vždy na L3 (CCO)**, aj keby išlo o sumu 100 €.
3. **Pravidlo 4 očí v banke:** Osoba, ktorá platbu v banke zadá, ju nesmie autorizovať. Platí pre každú transakciu vrátane L1.

---

## 6. Základné procesné toky spoločnosti (Workflows)

### 6.1 Nákup P2P (Procure-to-Pay)
* 🛒 **[FC-04: Nákupný proces P2P & 3-Way Match (HTML)](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/fc04-p2p-procurement.html)**
* **Princíp 3-Way Match:** Účtáreň uhradí faktúru len vtedy, ak sa zhoduje:
  1. Schválená objednávka (PO v ERP)
  2. Príjemka / akceptačný protokol zo skladu / od žiadateľa
  3. Dodávateľská faktúra

### 6.2 Obchod a sankčná kontrola (Lead-to-Contract)
* 🤝 **[PROC-01: Obchodno-licenčný tok (Lead-to-Contract) (HTML)](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/lead-to-contract.html)**
* Žiadna ponuka ani technická špecifikácia nesmie byť odoslaná pred sankčnou previerkou klienta. Compliance drží právo **ABSOLÚTNEHO VETA**.

### 6.3 Vývoj a výroba bezpilotných systémov (R&D to Delivery)
* ✈️ **[PROC-02: R&D vývoj a výroba bezpilotných systémov UAV (HTML)](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/rd-to-delivery.html)**
* Zahŕňa izoláciu vývojového prostredia, testovanie na vojenskom polygóne so schválením MO SR a výstupnú vojenskú kontrolu.

### 6.4 Onboarding pracovníkov: TPP vs. Externý vývojár (IP Assignment)
* 👤 **[FC-03: Onboarding & Prístupový model (Freelancer vs. TPP) (HTML)](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/fc03-onboarding-access.html)**
* **Kritická podmienka R&D:** Externý vývojár nesmie napísať ani riadok kódu bez podpísanej zmluvy o výhradnom prevode majetkových autorských práv (IP assignment) a doložky o mlčanlivosti.
* **Offboarding v deň D:** Pri ukončení spolupráce sa v deň D okamžite revokujú všetky IAM identity, tokeny a certifikáty.

### 6.5 Due Diligence partnerov & Pravidlá pre agentov
* 🔍 **[FC-07 & FC-06: Due Diligence partnera & Platba agentovi (HTML)](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/fc07-due-diligence.html)**
* Platba sprostredkovateľovi je povolená len partnerovi v stave **SCHVÁLENÝ**. Platba prebieha výhradne bezhotovostne na bankový účet v krajine sídla agenta. Hotovostné platby a platby tretím stranám sú kategoricky zakázané.

### 6.6 Exportná kontrola, Licencie MH SR & EUC
* 📦 **[FC-09: Sankcie, Licencie MH SR & Exportná kontrola (HTML)](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/fc09-sanctions-export-control.html)**
* Vývoz UAV vyžaduje platnú licenciu Ministerstva hospodárstva SR (MH SR) a overený originál End-User Certificate (EUC). Pred expedíciou prebieha povinná Pre-Shipment inšpekcia.

---

## 7. Bezpečnostné incidenty, SIEM a krízové riadenie (BCP/DR)

### 7.1 Incident Response & Notifikácie orgánom
* 🚨 **[FC-08 & FC-14: Incident Response & SIEM Eskalácia (HTML)](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/fc08-fc14-incident-response.html)**
* Incident kategórie P1 (útok na Zónu 3/4 alebo ransomware) vyžaduje reakciu do 15 minút.
* Zákonná notifikácia Národnému bezpečnostnému úradu (NBÚ) a SK-CERT musí prebehnúť najneskôr **do 72 hodín**.
* Pred akýmkoľvek zásahom do napadnutého stroja je povinné vytvoriť certifikovaný forenzný bitový obraz pre dôkazné konanie.

### 7.2 Plán kontinuity činností (BCP) a obnova po havárii (DR)
* 🔄 **[FC-15: BCP & Disaster Recovery aktivácia krízového štábu (HTML)](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/fc15-bcp-dr.html)**
* **Hierarchia priorít obnovy:**
  1. Priorita 1: Správa identít (IdP/IAM) a zabezpečená núdzová komunikácia (RTO < 4h)
  2. Priorita 2: Bankové platby a kritická komunikácia so štátnymi orgánmi (RTO < 12h)
  3. Priorita 3: ERP, skladové hospodárstvo a výrobná linka (RTO < 24h)
* Zálohy sú ukladané do off-site úložiska s fyzickým oddelením v režime WORM (nemenný zápis).

---

## 8. Integrita, Whistleblowing a etický kódex

* ⚖️ **[FC-10, FC-11 & FC-12: Integrita, Whistleblowing & Konflikt záujmov (HTML)](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/fc10-fc12-ethics-governance.html)**
* **Ochrana oznamovateľov (Zákon 54/2019 Z. z.):** Prijatie podnetu do 7 dní, vyšetrenie do 90 dní. Absolútny zákaz odvetných opatrení. Pri podnete na člena predstavenstva smeruje hlásenie priamo predsedovi Dozornej rady.
* **Register darov a pohostení (FC-11):** Dary do 500 € sa zapisujú do registra do 5 dní. Dary nad 500 € alebo akýkoľvek dar verejnému funkcionárovi podliehajú predchádzajúcemu schváleniu CCO.
* **Konflikt záujmov (FC-12):** Povinné písomné oznámenie vopred. CCO nariadi vylúčenie z rozhodovania, pravidlo 4 očí alebo zastavenie transakcie.

---

## 9. AI Governance & Autonómne rozhodovanie agentov

Pre nasadzovanie AI agentov v interných systémoch spoločnosti platia prísne bezpečnostné zábrany:

* 🤖 **[FC-16: AI Agent Gated Flow & Dual Control Replay (HTML)](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/fc16-ai-agent-decision.html)**

### Záväzné princípy AI:
1. **Agent Register:** Každý AI agent musí byť evidovaný v centrálnom registri s definovaným povoleným rozsahom úloh (`scope`).
2. **Mandatórny Human-in-the-Loop Gate:** Akcie s vysokým dopadom (odoslanie externého e-mailu, zadanie platby, merge kódu do produkcie, zápis do sankčného registra) **vyžadujú vždy ľudské schválenie (Human Gate)**.
3. **Zákaz tichého zlyhania:** Ak Policy Engine akciu zamietne (`DENY`), agent nesmie pokračovať alternatívnou skrytou cestou, ale vygeneruje sa auditovaný bezpečnostný ticket.
4. **Deterministický Replay:** Každý krok agenta ukladá do auditného logu hash vstupov, kontext a rozhodnutie, čo umožňuje 100% spätnú rekonštrukciu činnosti modelu.

---

## 10. Katalóg všetkých artefaktov a súborov v repozitári

| Kód | Názov modelu / procesu | Typ diagramu | Odkaz na interaktívny model |
| :--- | :--- | :---: | :--- |
| **PORTÁL** | **Centrálny prehliadač SSOT** | Web Dashboard | **[diagrams/index.html](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/index.html)** |
| **FC-01** | Organizačná štruktúra & Governance reporting | Architecture | **[fc01-org-reporting.html](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/fc01-org-reporting.html)** |
| **FC-02** | Model troch línií ochrany & STOP-right | Architecture | **[fc02-three-lines-of-defense.html](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/fc02-three-lines-of-defense.html)** |
| **FC-05** | Architektúra 4 dátových zón a perimetrov | Architecture | **[fc05-data-zones.html](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/fc05-data-zones.html)** |
| **ARCH-01**| Bezpečnostný perimeter Delta Defence | Architecture | **[org-security-architecture.html](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/org-security-architecture.html)** |
| **PROC-01**| Obchodno-licenčný tok (Lead-to-Contract) | Workflow | **[lead-to-contract.html](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/lead-to-contract.html)** |
| **PROC-02**| R&D vývoj a výroba bezpilotných systémov UAV | Workflow | **[rd-to-delivery.html](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/rd-to-delivery.html)** |
| **FC-03** | Onboarding & Prístupy (Freelancer vs. TPP) | Workflow | **[fc03-onboarding-access.html](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/fc03-onboarding-access.html)** |
| **FC-04** | Nákupný proces P2P (Procure-to-Pay) | Workflow | **[fc04-p2p-procurement.html](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/fc04-p2p-procurement.html)** |
| **FC-07/06**| Due Diligence partnera & Platba agentovi | Workflow | **[fc07-due-diligence.html](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/fc07-due-diligence.html)** |
| **FC-09** | Sankcie, Licencie MH SR & Export Control | Workflow | **[fc09-sanctions-export-control.html](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/fc09-sanctions-export-control.html)** |
| **FC-08/14**| Incident Response & SIEM eskalácia | Workflow | **[fc08-fc14-incident-response.html](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/fc08-fc14-incident-response.html)** |
| **FC-15** | BCP & Disaster Recovery aktivácia krízového štábu | Workflow | **[fc15-bcp-dr.html](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/fc15-bcp-dr.html)** |
| **FC-10-12**| Integrita, Whistleblowing & Konflikt záujmov | Workflow | **[fc10-fc12-ethics-governance.html](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/fc10-fc12-ethics-governance.html)** |
| **FC-13** | Schvaľovacie limity L1–L4 & Podpisový poriadok | Sequence | **[fc13-approval-limits.html](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/fc13-approval-limits.html)** |
| **FC-16** | AI Agent Gated Flow & Dual Control Replay | Sequence | **[fc16-ai-agent-decision.html](file:///c:/Users/mstancik/Documents/01_Projekty/projekty_a_vyvoj/github/delta-defence-navrh-struktury/diagrams/fc16-ai-agent-decision.html)** |

---

### Záverečné ustanovenia
Tento dokument tvorí záväznú základnú normu pre interné postupy spoločností **IOTA Defence a.s.** a **Delta Defence**. Všetky podriadené smernice, pracovné postupy (SOP), zmluvy a technické implementácie musia byť v plnom súlade s týmto Single Source of Truth rámcom. Zmeny tohto dokumentu schvaľuje Predstavenstvo spoločnosti po prerokovaní v Dozornej rade.
