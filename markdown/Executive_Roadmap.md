# National Institute of Standards and Technology (NIST) Cybersecurity Framework (CSF) v1.1
## Executive Roadmap & Piano Triennale di Remediation
**Organizzazione Target:** Aetheris Therapeutics S.p.A.  
**Tipo di Documento:** Strategia di Sicurezza Aziendale & Programma CISO  
**Classificazione:** Riservato / Portfolio Professionale  

---

## 🎯 Visione Strategica & Obiettivi

A seguito della Gap Analysis condotta sull'infrastruttura di **Aetheris Therapeutics S.p.A.** basata sul NIST CSF v1.1, è emersa una percentuale di conformità globale dell'**8.5%**. 

La priorità strategica per il prossimo triennio è trasformare la postura di sicurezza aziendale da **reattiva ("antincendio")** a **proattiva, resiliente e conforme** ai principali standard internazionali (ISO/IEC 27001, GDPR).

### Obiettivi Target a 3 Anni:
1. **Protezione della Proprietà Intellettuale:** Messa in sicurezza delle formule di ricerca e dei dati dei laboratori clinici.
2. **Resilienza Operativa:** Azzeramento del rischio di blocco operativo totale causato da attacchi Ransomware.
3. **Governance & Compliance:** Formalizzazione delle policy, delle matrici di responsabilità e piena conformità GDPR.

---

## 🗓️ Tabella di Marcia Triennale (Phased Implementation Plan)

```text
FASE 1: ANNO 1 (Mesi 01-12) ──► FONDAMENTA & MITIGAZIONE RISCHI CRITICI
FASE 2: ANNO 2 (Mesi 13-24) ──► ARCHITETTURA PROATTIVA & MONITORAGGIO CONTINUO
FASE 3: ANNO 3 (Mesi 25-36) ──► OTTIMIZZAZIONE, RESILIENZA & CERTIFICAZIONE ISO 27001
```

### 🔴 FASE 1: Anno 1 (Mesi 01-12) - Fondamenta & Mitigazione Rischi Critici
*Focus: Messa in sicurezza immediata degli accessi, governance di base e protezione contro le minacce ad alto impatto (Ransomware/Data Leakage).*

| Ambito | Iniziativa Strategica | Dettaglio Operativo & Deliverables | Priorità |
| :--- | :--- | :--- | :---: |
| **Governance** | Nomina CISO / Cyber Security Manager | Formalizzazione della funzione di sicurezza con reporting diretto al Board. | `CRITICA` |
| **Governance** | Information Security Policy (ISP) | Redazione e approvazione della policy generale e delle linee guida di sicurezza. | `ALTA` |
| **IAM** | Rollout MFA Multi-Fattore | Obbligo MFA su VPN, Office 365 e piattaforma SaaS *BioNexus Cloud*. | `CRITICA` |
| **IAM** | Adozione Soluzione PAM | Eliminazione password condivise Domain Admin e tracciamento accessi privilegiati. | `ALTA` |
| **Data Protection** | Controllo USB & DLP di base | Blocco delle porte USB non autorizzate tramite GPO e attivazione Microsoft DLP. | `ALTA` |
| **Data Protection** | Backup Immutabili (WORM) | Aggiornare i repository di backup con isolamento logico/Air-Gap anti-ransomware. | `CRITICA` |
| **Response** | Redazione Incident Response Plan (IRP) | Formalizzazione del piano d'emergenza, matrici RACIR e playbook per Ransomware/Phishing. | `ALTA` |

---

### 🟡 FASE 2: Anno 2 (Mesi 13-24) - Architettura Proattiva & SOC 24/7
*Focus: Visibilità completa della telemetria, gestione sistematica delle vulnerabilità e monitoraggio continuo.*

| Ambito | Iniziativa Strategica | Dettaglio Operativo & Deliverables | Priorità |
| :--- | :--- | :--- | :---: |
| **Detection** | Implementazione EDR/XDR | Sostituzione dell'antivirus tradizionale con agenti EDR centralizzati sugli endpoint. | `ALTA` |
| **Detection** | Adozione SIEM + Servizio SOC 24/7 | Ingestionamento log (Azure, Palo Alto, O365, AD) e monitoraggio tramite MSSP H24. | `ALTA` |
| **Vulnerability** | Vulnerability & Patch Management | Programma di scansione Qualys mensile e ciclo di patching vincolante (SLA 14gg per vulnerabilità *High/Critical*). | `MEDIA` |
| **Asset Mgmt** | CMDB & Software Inventory | Implementazione CMDB automatizzato e tracciamento dello Shadow IT / SaaS. | `MEDIA` |
| **Awareness** | Programma di Formazione Continua | Campagne di Security Awareness obbligatorie e simulazioni periodiche di Phishing. | `MEDIA` |
| **TPRM** | Vendor Risk Management Program | Procedura d'analisi dei rischi di sicurezza per i fornitori e contratti SaaS terzi. | `MEDIA` |

---

### 🟢 FASE 3: Anno 3 (Mesi 25-36) - Resilienza, Compliance & Certificazioni
*Focus: Consolidamento della postura di sicurezza, esercitazioni avanzate e adeguamento agli standard internazionali.*

| Ambito | Iniziativa Strategica | Dettaglio Operativo & Deliverables | Priorità |
| :--- | :--- | :---: | :---: |
| **Compliance** | ISO/IEC 27001 Readiness & Audit | Allineamento dell'ISMS e conduzione di audit per l'ottenimento della certificazione ISO 27001. | `MEDIA` |
| **Compliance** | GDPR Compliance & DPIA | Valutazione formale d'impatto sulla protezione dei dati per le piattaforme di ricerca e cliniche. | `MEDIA` |
| **Testing** | Red Team / Penetration Testing | Esecuzione di esercitazioni di attacco simulato (Red Team) e test d'intrusione annuali. | `MEDIA` |
| **Resilience** | Tabletop Exercises & BCP/DR | Simulationi di crisi aziendale con il Board e ripristino Bare-Metal programmato. | `MEDIA` |

---

## 💰 Stima Indicativa degli Investimenti (CapEx / OpEx)

| Categoria d'Investimento | Anno 1 | Anno 2 | Anno 3 |
| :--- | :---: | :---: | :---: |
| **Governance, Licensing & PAM/MFA** | € 45.000 | € 20.000 | € 20.000 |
| **Infrastruttura Backup Immutabili & DLP** | € 35.000 | € 10.000 | € 10.000 |
| **Servizi SOC 24/7 / EDR / SIEM (MSSP)** | € 30.000 | € 60.000 | € 60.000 |
| **Audit, Certificazioni ISO 27001 & PenTest** | € 15.000 | € 25.000 | € 30.000 |
| **Formazione & Awareness** | € 10.000 | € 10.000 | € 10.000 |
| **TOTALE ANNUALE STIMATO** | **€ 135.000** | **€ 125.000** | **€ 130.000** |

---

## 📈 Indicatori Chiave di Prestazione (KPI) per il Monitoraggio

Per tracciare i progressi dell'Executive Roadmap, il CISO riferirà trimestralmente al Board tramite i seguenti KPI:
* **MFA Adoption Rate:** Target = 100% degli utenti attivi entro il Mese 3.
* **Mean Time to Detect (MTTD):** Riduzione del tempo medio di rilevamento da "Sconosciuto" a **< 15 minuti** (tramite SOC 24/7).
* **Mean Time to Respond (MTTR):** Riduzione del tempo medio di risposta/isolamento da "Sconosciuto" a **< 60 minuti**.
* **Patch Compliance:** 95%+ delle vulnerabilità *High/Critical* risolte entro 14 giorni dalla rilevazione.
* **Phishing Click Rate:** Riduzione della percentuale di dipendenti vulnerabili al phishing a **< 5%**.

* **MFA Adoption Rate:** Target = 100% degli utenti attivi entro il Mese 3.
* **Mean Time to Detect (MTTD):** Riduzione del tempo medio di rilevamento da "Sconosciuto" a **< 15 minuti** (tramite SOC 24/7).
* **Mean Time to Respond (MTTR):** Riduzione del tempo medio di risposta/isolamento da "Sconosciuto" a **< 60 minuti**.
* **Patch Compliance:** 95%+ delle vulnerabilità *High/Critical* risolte entro 14 giorni dalla rilevazione.
* **Phishing Click Rate:** Riduzione della percentuale di dipendenti vulnerabili al phishing a **< 5%**.
