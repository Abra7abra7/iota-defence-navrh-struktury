# IOTA Defence a.s. – Jediný zdroj pravdy (SSOT)

> **Kompletná organizačná štruktúra, tri línie ochrany, 4 dátové perimetre, procesné toky a AI Governance.**

Tento repozitár slúži ako oficiálny, normatívny a záväzný **Jediný zdroj pravdy (Single Source of Truth – SSOT)** pre akciovú spoločnosť **IOTA Defence a.s.** (v rámci projektového portfólia Delta Defence).

---

## 🌐 Centrálny vizuálny portál

Všetky procesy a architektúry sú spracované do interaktívnych, samostatných HTML modelov (SVG s podporou svetlej/tmavej témy, trace animáciami a exportom):

* **[Otvoriť interaktívny Portál modelov](diagrams/index.html)**
* **[Kompletná metodická dokumentácia (SSOT Master Index)](docs/SSOT_MASTER_INDEX.md)**
* **[Organizačná štruktúra a procesné toky](docs/organizacna_struktura_a_procesy.md)**

---

## 🏛️ Katalóg modelov

### 1. Architektúra riadenia a bezpečnosti
* **[FC-01: Organizačná štruktúra & Governance Reporting](diagrams/fc01-org-reporting.html)** – Valné zhromaždenie, Dozorná rada, Predstavenstvo a nezávislá 2. línia (CCO, CISO, ECO).
* **[FC-02: Model troch línií ochrany & STOP-Right](diagrams/fc02-three-lines-of-defense.html)** – Striktné oddelenie prevádzky, compliance dohľadu a interného auditu pre Dozornú radu.
* **[FC-05: Architektúra 4 dátových zón & Perimetrov](diagrams/fc05-data-zones.html)** – Zero-Trust rozdelenie: Zóna 1 (Verejná), Zóna 2 (Firemný tenant EÚ), Zóna 3 (On-prem Git / CAD trezor), Zóna 4 (Chránený priestor NBÚ / Air-gap).
* **[ARCH-01: Bezpečnostný perimeter spoločnosti](diagrams/org-security-architecture.html)** – Fyzické a digitálne oddelenie komerčnej sféry od R&D vývoja.

### 2. Kľúčové procesné toky (Workflows)
* **[PROC-01: Obchodno-licenčný tok (Lead-to-Contract)](diagrams/lead-to-contract.html)** – Prijatie dopytu, sankčný vetting (EUC) a právo absolútneho VETA Compliance Officera.
* **[PROC-02: R&D vývoj a výroba bezpilotných systémov UAV](diagrams/rd-to-delivery.html)** – Vývoj autonómnych modelov, on-prem git, letové skúšky na polygóne a armádna prebierka.
* **[FC-03: Onboarding & Prístupy (Freelancer vs. TPP)](diagrams/fc03-onboarding-access.html)** – Povinný zmluvný prevod majetkových autorských práv (IP assignment) a zónová matica.
* **[FC-04: Nákupný proces P2P (Procure-to-Pay)](diagrams/fc04-p2p-procurement.html)** – Schvaľovacie limity L1–L4, PO systém, 3-Way Match a pravidlo 4 očí.
* **[FC-07 & FC-06: Due Diligence partnerov & Platba agentovi](diagrams/fc07-due-diligence.html)** – UBO previerka, protikorupčné doložky (ABAC) a bezhotovostné platby agentom.
* **[FC-09: Sankcie, Licencie MH SR & Export Control](diagrams/fc09-sanctions-export-control.html)** – Licenčné konanie MH SR, originál EUC a colná expedícia.
* **[FC-08 & FC-14: Incident Response & SIEM Eskalácia](diagrams/fc08-fc14-incident-response.html)** – Triáž P1–P4 do 15 minút, forenzika a zákonné hlásenie NBÚ do 72 hodín.
* **[FC-15: BCP & Disaster Recovery krízový štáb](diagrams/fc15-bcp-dr.html)** – Havarijný plán, priority obnovy systémov (IdP → Komunikácia → Platby → ERP).
* **[FC-10, FC-11 & FC-12: Integrita, Whistleblowing & Konflikt záujmov](diagrams/fc10-fc12-ethics-governance.html)** – Zákonná ochrana oznamovateľov (zák. 54/2019 Z. z.), register darov a riešenie COI.

### 3. Sekvencie & AI Governance
* **[FC-13: Schvaľovacie limity L1–L4 & Podpisový poriadok](diagrams/fc13-approval-limits.html)** – Sekvencia schvaľovania finančných záväzkov a 4-oči v banke.
* **[FC-16: AI Agent Gated Flow & Dual Control Replay](diagrams/fc16-ai-agent-decision.html)** – Autonómne rozhodovanie AI agentov, mandatórny Human Gate pri rizikových akciách a nemenný audit log pre 100% deterministický replay.

---

## ⚖️ Legislatívny rámec
* Zákon č. 392/2011 Z. z. o obchodovaní s vojenským materiálom
* Zákon č. 215/2004 Z. z. o ochrane utajovaných skutočností
* Nariadenie (EÚ) 2021/821 (Dual-Use exportná kontrola)
* Zákon č. 54/2019 Z. z. o ochrane oznamovateľov protispoločenskej činnosti
* Zákon č. 69/2018 Z. z. o kybernetickej bezpečnosti (NIS2) & EU AI Act

---

© 2026 IOTA Defence a.s. Všetky práva vyhradené. Klasifikácia: Interné – Dôverné.
