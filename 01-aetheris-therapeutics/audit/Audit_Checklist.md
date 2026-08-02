# 📑 ISO/IEC 27001:2022 & NIST CSF v1.1 — Audit Checklist
## Lista di Controllo e Questionnaire d'Ispezione per il Fieldwork

**Standard di Riferimento:** ISO/IEC 27001:2022 (Clausole 4–10 & Annex A) & NIST CSF v1.1  
**Organizzazione:** Aetheris Therapeutics S.p.A.  
**Rif. Documento:** AUD-CHK-2026-04  
**Versione:** 1.0  
**Stato:** Approvato  
**Classificazione:** Uso Interno Team d'Audit  
**Data dell'Audit:** 10 – 14 Agosto 2026  

---

## 1. Istruzioni Operative per l'Auditor (ISO 19011:2018)

Questa checklist guida l'ispezione sul campo presso **Aetheris Therapeutics S.p.A.**. Per ogni punto di controllo, l'Auditor deve:
1. Porre la **Domanda Guida** all'intervistato.
2. Richiedere la visione dell'**Evidenza Documentale o Tecnica** (Campionamento).
3. Verificare la conformità e registrare l'Esito: **PASS** (Conforme), **NC Major** (Non-Conformità Maggiore), **NC Minor** (Non-Conformità Minore) o **OFI** (Opportunità di Miglioramento).

---

## 2. Checklist Clausole Obbligatorie ISO 27001:2022 (SGSI)

### Clausola 4: Contesto dell'Organizzazione
| Ref. Norma | Requisito / Domanda di Verifica | Evidenza da Richiedere / Campione | Esito | Riferimento Rilievo |
| :--- | :--- | :--- | :---: | :--- |
| **Cl. 4.1 / 4.2** | Sono stati identificati i fattori interni/esterni e i requisiti delle parti interessate (GDPR, EMA)? | Documento "Analisi Contesto & Parti Interessate v1.0". | **PASS** | — |
| **Cl. 4.3** | È stato definito e documentato lo Campo di Applicazione (Scope) dello SGSI? | Documento di Definizione dello Scope SGSI. | **PASS** | — |

---

### Clausola 5: Leadership e Impegno
| Ref. Norma | Requisito / Domanda di Verifica | Evidenza da Richiedere / Campione | Esito | Riferimento Rilievo |
| :--- | :--- | :--- | :---: | :--- |
| **Cl. 5.1 / 5.2** | Esiste una Politica per la Sicurezza firmata dall'Alta Direzione e comunicata? | Politica SGSI pubblicata in Intranet. | **NC Minor** | NC-MIN-02 |
| **Cl. 5.3** | Sono stati formalizzati i ruoli e le responsabilità SGSI (CISO / ISMS Owner)? | Organigramma e Mansionari delle risorse IT/Security. | **NC Minor** | NC-MIN-02 |

---

### Clausola 6: Pianificazione
| Ref. Norma | Requisito / Domanda di Verifica | Evidenza da Richiedere / Campione | Esito | Riferimento Rilievo |
| :--- | :--- | :--- | :---: | :--- |
| **Cl. 6.1.2** | Viene eseguita una valutazione dei rischi conforme a una metodologia formalizzata? | Risk Assessment Report e Metodologia ISO 27005. | **PASS** | — |
| **Cl. 6.1.3** | È stato formalizzato un Risk Treatment Plan (RTP) approvato dalla Direzione? | Piano di Trattamento dei Rischi approvato. | **NC Major** | NC-MAJ-01 / RTP |

---

### Clausola 7: Supporto e Risorse
| Ref. Norma | Requisito / Domanda di Verifica | Evidenza da Richiedere / Campione | Esito | Riferimento Rilievo |
| :--- | :--- | :--- | :---: | :--- |
| **Cl. 7.2 / 7.3** | Vengono svolte sessioni di formazione e awareness sulla sicurezza per i dipendenti? | Registro presenze corsi, report Phishing Simulation. | **NC Minor** | NC-MIN-03 / OFI-02 |
| **Cl. 7.5** | Le informazioni documentate del SGSI sono controllate, revisionate e protette? | Procedura di Controllo Documentale ex Cl. 7.5. | **PASS** | — |

---

### Clausola 8: Attività Operative
| Ref. Norma | Requisito / Domanda di Verifica | Evidenza da Richiedere / Campione | Esito | Riferimento Rilievo |
| :--- | :--- | :--- | :---: | :--- |
| **Cl. 8.1** | I processi pianificati per il trattamento del rischio vengono attuati regolarmente? | Ticket di remediation, registri di manutenzione. | **NC Major** | NC-MAJ-02 |

---

### Clausola 9 & 10: Valutazione delle Prestazioni e Miglioramento
| Ref. Norma | Requisito / Domanda di Verifica | Evidenza da Richiedere / Campione | Esito | Riferimento Rilievo |
| :--- | :--- | :--- | :---: | :--- |
| **Cl. 9.2** | Vengono condotti Internal Audit periodici del SGSI secondo ISO 19011? | Piano e Report di Internal Audit precedente. | **NC Major** | NC-MAJ-05 |
| **Cl. 9.3 / 10.1**| L'Alta Direzione riesamina lo SGSI (Management Review) e si gestiscono le CAPA? | Verbale del Riesame della Direzione e Registro CAPA. | **NC Minor** | NC-MIN-02 |

---

## 3. Checklist Controlli Selezionati ISO 27001 Annex A & NIST CSF v1.1

### Controlli Tecnologici e Access Control (Annex A.8 / NIST PR & DE)
| Ref. ISO Annex A | Ref. NIST CSF | Domanda di Verifica / Campo d'Ispezione | Evidenza Tecnica Campionata | Esito | Ref. Rilievo |
| :--- | :--- | :--- | :--- | :---: | :--- |
| **A.5.15 / A.8.5** | **PR.AC-1 / PR.AC-6** | L'accesso remoto via VPN richiede l'Autenticazione a Più Fattori (MFA)? | Configurazione Palo Alto VPN GlobalProtect / Azure Conditional Access. | **NC Major** | NC-MAJ-01 |
| **A.8.2 / A.8.18** | **PR.AC-4 / PR.PT-3** | Gli account con privilegi amministrativi elevati sono nominali e protetti da PAM? | Dump account Active Directory (`Domain Admins`) e Active Directory Users. | **NC Major** | NC-MAJ-02 |
| **A.8.16 / A.8.15** | **DE.AE-1 / DE.CM-1** | I log di rete, firewall e server sono centralizzati e analizzati in tempo reale (SIEM/SOC)? | Console di gestione log e architettura di correlazione eventi. | **NC Major** | NC-MAJ-05 |
| **A.8.7 / A.8.8** | **DE.CM-4 / PR.DS-5** | È presente una soluzione EDR/Antivirus centralizzata gestita su tutti gli endpoint? | Dashboard Console Antivirus / Defender for Endpoint. | **OFI** | OFI-01 |
| **A.8.12** | **PR.DS-5** | Sono attive regole di Data Loss Prevention (DLP) per bloccare l'esfiltrazione di dati R&D? | Policy M365 Purview / Ruleset DLP su gateway e-mail. | **OFI** | OFI-03 |

---

### Controlli Organizzativi, Privacy & Incident Response (Annex A.5 & A.6 / NIST ID, RS, RC)
| Ref. ISO Annex A | Ref. NIST CSF | Domanda di Verifica / Campo d'Ispezione | Evidenza Tecnica Campionata | Esito | Ref. Rilievo |
| :--- | :--- | :--- | :--- | :---: | :--- |
| **A.5.24 / A.5.26** | **RS.RP-1 / RS.CO-1** | Esiste un Incident Response Plan (IRP) formalizzato per la gestione dei data breach? | Procedura IRP e matrice di escalation/notifica Garante Privacy. | **NC Major** | NC-MAJ-03 |
| **A.5.31 / A.5.34** | **ID.GV-3 / ID.AM-5** | È presente il Registro dei Trattamenti ex Art. 30 GDPR per i dati clinici dei pazienti? | Registro Trattamenti Dati Personali (Art. 30 GDPR). | **NC Major** | NC-MAJ-04 |
| **A.5.9 / A.5.10** | **ID.AM-1 / ID.AM-2** | Esiste un inventario automatizzato degli asset IT hardware e software? | File Excel / Database IT Asset Inventory. | **NC Minor** | NC-MIN-01 |
| **A.5.19 / A.5.21** | **ID.SC-1 / ID.SC-3** | I contratti con i fornitori IT terzi includono clausole e Security Annex sulla sicurezza? | Campione contratti fornitori SaaS/IT e SLA. | **NC Minor** | NC-MIN-04 |
| **A.8.13 / A.8.14** | **RC.RP-1 / PR.IP-4** | Vengono eseguiti backup periodici cifrati con test di ripristino/DR documentati? | Job di backup Azure Immutable Blob e Report ultimo test DR. | **PASS** | — |
| **A.7.1 / A.7.2** | **PR.IP-5** | L'accesso ai laboratori R&D è protetto da varchi biometrici/badge e videosorveglianza? | Ispezione visiva varchi e Registro log accessi fisici. | **PASS** | — |

---

## 4. Controllo Documentale e Approvazione (ISO 27001:2022 Clausola 7.5)

| Ruolo | Nome e Cognome | Stato | Data |
| :--- | :--- | :--- | :--- |
| **Redatto da (Lead Auditor)** | Emanuele Tarchi | Completato | 10 Agosto 2026 |
| **Revisionato da (IT Director)** | IT Director ad interim | Revisionato | 11 Agosto 2026 |
| **Approvato da (Alta Direzione)** | Chief Executive Officer (CEO) | Approvato | 12 Agosto 2026 |
