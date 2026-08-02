# 🛡️ Aetheris Therapeutics S.p.A. — Enterprise Cybersecurity Gap Analysis & ISO 27001 Readiness

![NIST CSF v1.1](https://img.shields.io/badge/Framework-NIST%20CSF%20v1.1-blue)
![ISO/IEC 27001:2022](https://img.shields.io/badge/Standard-ISO%2FIEC%2027001%3A2022-green)
![ISO/IEC 27005:2022](https://img.shields.io/badge/Risk-ISO%2FIEC%2027005-orange)
![ISO 19011:2018](https://img.shields.io/badge/Audit-ISO%2019011-purple)
![Status](https://img.shields.io/badge/Audit%20Status-Completed-success)
![License](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey)

Questo repository raccoglie il pacchetto completo di **Cybersecurity Gap Analysis, Assessment di Rischio e Readiness Audit ISO/IEC 27001:2022** sviluppato per **Aetheris Therapeutics S.p.A.**, azienda biotecnologica impegnata nella ricerca e sviluppo farmaceutico.

Il progetto integra metodologicamente i framework **ISO/IEC 27001:2022**, **ISO/IEC 27005:2022**, **ISO 19011:2018** e **NIST Cybersecurity Framework (CSF) v1.1**.

---

## 📌 Panoramica del Caso Studio

L'analisi valuta la postura di sicurezza e la maturità GRC di **Aetheris Therapeutics S.p.A.** (~250 dipendenti), la cui operatività si fonda sulla gestione di asset ad alto valore critico:
* **Proprietà Intellettuale (IP):** Formule chimico-molecolari, brevetti R&D.
* **Dati Sanitari & PII:** Dati clinici e genetici dei pazienti (soggetti a tutela GDPR Art. 30 e normativa sanitaria).
* **Infrastruttura Ibrida:** Sistemi di laboratorio On-Premise e tenant Cloud Microsoft Azure / Office 365.

L'attività d'audit ha mappato la resilienza dell'infrastruttura sui 5 domini del **NIST CSF v1.1** (*Identify, Protect, Detect, Respond, Recover*), esaminato i **93 controlli dell'Annex A di ISO 27001:2022** e definito il **Risk Treatment Plan (RTP)** con relativo impatto finanziario per l'Alta Direzione.

---

## 🗂️ Struttura della Repository

Il repository è strutturato in tre macro-aree funzionali per riflettere tutte le fasi operative di un vero ingaggio GRC ed Enterprise Audit:

### 📋 1. Fasi d'Audit & Working Papers (`/audit`)
* 📂 **`audit/Audit_Plan.md`**: Piano d'Audit formale secondo ISO 19011:2018, perimetro dello SGSI, ruoli, responsabilità e calendario interviste.
* 📂 **`audit/Audit_Checklist.md`**: Lista di controllo, questionnaire d'ispezione sul campo e campionamenti tecnici.
* 📂 **`audit/Audit_Trail.md`**: Registro delle attività di fieldwork, trascrizione delle interviste chiave ed esame documentale.
* 📂 **`audit/NC_OFI_Matrix.md`**: Matrice Ufficiale dei Rilievi (5 NC Major, 4 NC Minor, 3 OFI, 4 PASS) con analisi Causa Radice e Azioni Correttive (CAPA).
* 📂 **`audit/Audit_Summary.md`**: Rapporto Finale di Sintesi dell'Auditor (ISO 19011 Cl. 6.5) con valutazione e giurisprudenza d'audit.

### 🎲 2. Risk Management Framework (`/risk`)
* 📂 **`risk/Risk_Methodology.md`**: Metodologia di valutazione del rischio conforme a ISO 27005:2022 e ISO 27001 Cl. 6.1.2.
* 📂 **`risk/Risk_Scoring_Model.md`**: Modello matematico di scoring ($P \times I$), Matrice 5x5 e soglie di Risk Appetite.
* 📂 **`risk/Risk_Register.md`**: Registro formale dei Rischi specifici (Inerenti vs Residuali) collegati agli asset critici di Aetheris S.p.A.
* 📂 **`risk/Risk_Treatment_Plan_RTP.md`**: Piano di Trattamento del Rischio con allocazione budget (€ 70k), scadenze e criteri di re-audit.

### 📊 3. Executive Reporting & Board Governance (`/executive`)
* 📂 **`executive/Executive_Summary.md`**: Report strategico per il Board e C-Level con analisi CMMI e giustificazione finanziaria dell'investimento.
* 📂 **`executive/Maturity_Dashboard.md`**: Dashboard di maturità sui domini NIST CSF (Visual Radar Analysis nativa) e conformità controlli ISO 27001 Annex A.
* 📂 **`executive/Strategic_Roadmap_3-6-12.md`**: Roadmap strategica e operativa a 3, 6 e 12 mesi per il raggiungimento della certificazione.
* 📂 **`executive/Board_Presentation.md`**: Board Executive Deck per la presentazione al Consiglio di Amministrazione e delibera d'investimento.

### 📄 4. Documentazione Integrativa (`/docs`)
* 📂 **`docs/Aetheris_Therapeutics_ISO27001_Annex_A_SoA_Evaluated.pdf`**: Statement of Applicability (SoA) valutata sui 93 controlli dell'Annex A.

---

## 🎯 Key Findings & Risultati dell'Audit

* **Punti di Forza:** Segmentazione di rete isolata per i laboratori R&D tramite Next-Gen Firewall Palo Alto; procedure di backup notturno immutabile e cifrato su Azure; ottimo controllo degli accessi fisici ai laboratori (badge e videosorveglianza).
* **Non-Conformità Maggiori Riscontrate:**
  1. Accesso VPN remoto senza autenticazione a più fattori (MFA).
  2. Presenza di account `Domain Admin` condivisi senza soluzioni PAM.
  3. Assenza del Registro dei Trattamenti dei Dati Personali (Art. 30 GDPR).
  4. Assenza di una piattaforma SIEM e di un monitoraggio SOC h24.
  5. Mancanza di un Incident Response Plan (IRP) formalizzato e testato.

---

## 💼 Valore di Business e Piano d'Investimento

Il **Risk Treatment Plan** approvato prevede un investimento totale nel primo anno pari a **€ 70.000** (Capex: € 15.000 / Opex: € 42.000/anno / Consulenza Governance: € 13.000) per l'azzeramento dei rischi critici e la preparazione dell'organizzazione all'Audit di Certificazione ISO/IEC 27001:2022 entro 12 mesi.

---

## ⚖️ Disclaimer e Note Legali

* **Finalità:** Questo progetto costituisce un caso di studio reale sviluppato per finalità di portfolio professionale in ambito Governance, Risk & Compliance (GRC) e Cybersecurity Auditing.
* **Riservatezza & Fittitietà:** L'entità aziendale *Aetheris Therapeutics S.p.A.*, gli scenari specifici e i dati nominativi non direttamente riconducibili all'autore sono utilizzati a titolo esemplificativo per la rappresentazione dei processi GRC.

---

**Lead Auditor & GRC Specialist:** Emanuele Tarchi  
*ISO/IEC 27001 Lead Auditor Trainee*
