# 🛡️ Aetheris Therapeutics S.p.A. — Enterprise Cybersecurity Gap Analysis & ISO 27001 Readiness

![NIST CSF v1.1](https://img.shields.io/badge/Framework-NIST%20CSF%20v1.1-blue)
![ISO/IEC 27001:2022](https://img.shields.io/badge/Standard-ISO%2FIEC%2027001%3A2022-green)
![Status](https://img.shields.io/badge/Audit%20Status-Evaluated-success)

Questo progetto contiene l'analisi completa di **Cybersecurity Gap Analysis** e **Readiness Audit** condotta per **Aetheris Therapeutics S.p.A.**, basata sui framework **NIST Cybersecurity Framework (CSF) v1.1** e **ISO/IEC 27001:2022**.

---

## 📌 Panoramica del Caso Studio

L'analisi valuta la postura di sicurezza e la maturità della gestione del rischio di **Aetheris Therapeutics S.p.A.**, un'organizzazione biofarmaceutica di medie dimensioni (~250 dipendenti) che gestisce proprietà intellettuale critica (brevetti, formule molecolari), dati sanitari sensibili dei pazienti (PII/GDPR) e un'architettura ibrida (On-Premise + Cloud Azure/O365).

La valutazione esamina in modo sistematico i controlli organizzativi, procedurali e tecnologici:
1. **NIST CSF v1.1:** Mappatura della resilienza operativa sui 5 domini core (*Identify, Protect, Detect, Respond, Recover*).
2. **ISO/IEC 27001:2022:** Verifiche ispettive sulle **Clausole Obbligatorie (4–10)** e formulazione della **Statement of Applicability (SoA)** valutata sui **93 controlli dell'Annex A**.

---

## 🗂️ Struttura dei Deliverables

### 📄 Executive Audit Reports & PDF Ufficiali (`docs/`)
* 📂 [NIST CSF v1.1 Gap Analysis Consolidata (PDF)](docs/Aetheris_Therapeutics_NIST_CSF_Gap_Analysis_Consolidated.pdf)  
  *Report consolidato di 10 pagine con la valutazione completa dei 5 domini NIST, esiti (PASS/FAIL/NA) e motivazioni d'audit.*
* 📂 [Case Study & Fieldwork Evidences (PDF)](docs/Aetheris_Therapeutics_Case_Study_and_Interviews.pdf)  
  *Profilo di Aetheris Therapeutics S.p.A. e sintesi analitica delle interviste condotte con IT, Security, Legal e HR.*
* 📂 [ISO/IEC 27001:2022 — Mandatory Clauses Audit Report (PDF)](docs/Aetheris_Therapeutics_ISO27001_Mandatory_Clauses_Audit.pdf)  
  *Valutazione d'audit formale sui 30 requisiti normativi obbligatori delle Clausole 4–10 con rilievi ed evidenze d'audit.*
* 📂 [ISO/IEC 27001:2022 — Statement of Applicability (SoA) Evaluated (PDF)](docs/Aetheris_Therapeutics_ISO27001_Annex_A_SoA_Evaluated.pdf)  
  *Dichiarazione di Applicabilità (SoA) compilata e valutata sui 93 controlli dell'Annex A con giustificazioni tecniche.*

### 📝 Documentazione di Dettaglio e Sorgenti (`markdown/`)
Per la consultazione rapida e nativa all'interno di GitHub:
* 📄 [00 — Case Study & Interviews](markdown/00_Case_Study_and_Interviews.md) *(Profilo aziendale, interviste ed evidenze)*
* 📄 [01 — Identify (ID)](markdown/01_Identify.md) *(Asset Management, Risk Assessment, Governance)*
* 📄 [02 — Protect (PR)](markdown/02_Protect.md) *(Access Control, Data Security, Patching, Training)*
* 📄 [03 — Detect (DE)](markdown/03_Detect.md) *(Anomaly Detection, Continuous Monitoring, SIEM)*
* 📄 [04 — Respond (RS)](markdown/04_Respond.md) *(Incident Response, Digital Forensics, Escalation)*
* 📄 [05 — Recover (RC)](markdown/05_Recover.md) *(Disaster Recovery, Resilienza Operativa, PR/Crisis)*
* 🎯 [Executive Roadmap](markdown/Executive_Roadmap.md) *(Piano Triennale di Remediation Strategica e Programma CISO)*

---

## 🎯 Principali Rilievi emersi dall'Audit

* **Punti di Forza Operativi:** Segmentazione di rete efficace tramite VLAN e Firewall Palo Alto Next-Gen; presenza di procedure di Disaster Recovery e backup regolari; ottima sorveglianza fisica dei centri di ricerca.
* **Gap Critici da Sanare:** Assenza di autenticazione a due fattori (MFA) sulla VPN; gestione condivisa degli account amministrativi (manca una soluzione PAM); assenza di SIEM ed EDR centralizzato per la detection 24/7; mancanza di una politica formale di Data Governance/Classificazione dei dati e non-conformità GDPR.

---

## ⚖️ Disclaimer e Note Legali

* **Finalità:** Questo caso studio è stato sviluppato esclusivamente per scopi di portfolio professionale personale.
* **Contesto Fittizio:** Tutte le entità aziendali (es. *Aetheris Therapeutics S.p.A.*), i nomi di persone e i riferimenti tecnologici sono interamente fittizi.
