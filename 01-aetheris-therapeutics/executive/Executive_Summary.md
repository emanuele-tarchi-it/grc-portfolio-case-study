# 🛡️ Executive Summary — Cybersecurity Gap Analysis & ISO 27001 Readiness
## Report Strategico per l'Alta Direzione — Aetheris Therapeutics S.p.A.

**Standard di Riferimento:** ISO/IEC 27001:2022 & NIST Cybersecurity Framework v1.1  
**Organizzazione:** Aetheris Therapeutics S.p.A.  
**Rif. Documento:** EXEC-SUM-2026-01  
**Versione:** 1.0  
**Stato:** Approvato  
**Classificazione:** Riservato / Riservato al Board  
**Data di Efficacia:** Agosto 2026  

---

## 1. Context & Business Challenge

**Aetheris Therapeutics S.p.A.** è un'azienda biotecnologica operante nella ricerca, sviluppo e commercializzazione di soluzioni farmaceutiche avanzate. Gli asset più critici dell'organizzazione sono rappresentati da:
* **Proprietà Intellettuale (IP):** Formule chimico-molecolari e brevetti R&D.
* **Dati Sanitari & Clinici (PII):** Dati personali e genetici dei pazienti coinvolti nelle sperimentazioni cliniche (soggetti a tutela GDPR e normativa sanitaria).
* **Continuità Operativa R&D:** Sistemi di laboratorio e infrastruttura ibrida Cloud (Azure/Microsoft 365).

In vista dell'espansione del mercato e dei requisiti di conformità richiesti da partner e organi regolatori, l'Alta Direzione ha commissionato un'attività indipendente di **Cybersecurity Gap Analysis e ISO/IEC 27001 Readiness Audit**, volta a valutare la postura di sicurezza aziendale e definire la roadmap per il raggiungimento della certificazione ISO 27001:2022.

---

## 2. Sintesi della Postura di Sicurezza Attuale (Key Findings)

L'audit condotto nel mese di **Agosto 2026** ha evidenziato una **postura di sicurezza reattiva e orientata principalmente alla sola gestione infrastrutturale IT**, a fronte di una marcata carenza negli aspetti strutturali di **Governance, Risk & Compliance (GRC)**.

### Matrice di Sintesi dei Rilievi (ISO 19011)
* 🚨 **5 Non-Conformità Maggiori (NC Major):** Lacune bloccanti ai fini della certificazione ISO 27001 e fonte di rischio d'impresa elevato.
* ⚠️ **4 Non-Conformità Minori (NC Minor):** Inadempienze procedurali e parziali nell'attuazione dei controlli dell'Annex A.
* 💡 **3 Opportunità di Miglioramento (OFI):** Raccomandazioni tecniche per elevare la maturità tecnologica e la resilienza operativa.
* ✅ **4 Controlli Conformi (PASS):** Controlli tecnici di segmentazione di rete, backup cifrati e sicurezza fisica adeguati.

### I 5 Rischi Critici Identificati
1. **Accessi Remoti Non Sicuri (VPN senza MFA):** Elevata esposizione a rilevamento credenziali e attacchi brute-force.
2. **Utenze Amministrative Condivise (No PAM):** Mancanza di tracciabilità delle azioni eseguite con privilegi `Domain Admin`.
3. **Mancanza del Registro Trattamenti GDPR (Art. 30):** Rischio di pesanti sanzioni dal Garante Privacy e data breach su dati sanitari sensibili.
4. **Assenza di SIEM e SOC h24:** Incapacità di rilevare tempestivamente intrusioni o la presenza di ransomware in rete (Dwell Time elevato).
5. **Assenza di Incident Response Plan (IRP):** Mancanza di procedure formalizzate di gestione delle emergenze e notifica delle violazioni.

## 3. Profilo di Maturità NIST CSF v1.1

La valutazione effettuata sui 5 domini core del **NIST Cybersecurity Framework v1.1** mostra un livello di maturità complessivo pari a **Tier 1 (Informal/Reactive)**, ben al di sotto del Target aziendale di **Tier 3 (Repeatable/Defined)**:

| Dominio Core NIST | Livello Attuale | Target Aziendale | Valutazione e Stato |
| :--- | :---: | :---: | :--- |
| **Identify (ID)** | **1.4 / 5.0** | 3.5 / 5.0 | Reattivo — Inventario asset manuale su Excel |
| **Protect (PR)** | **2.1 / 5.0** | 4.0 / 5.0 | Incompleto — Assenza MFA su VPN e PAM per Admin |
| **Detect (DE)** | **1.2 / 5.0** | 3.5 / 5.0 | Critico — Assenza di SIEM e monitoraggio h24 |
| **Respond (RS)** | **1.0 / 5.0** | 3.5 / 5.0 | Assente — Mancanza di un Incident Response Plan |
| **Recover (RC)** | **3.0 / 5.0** | 4.0 / 5.0 | Buono — Backup cifrati e immutabili attivi |

---

## 4. Strategia di Trattamento e Proposta d'Investimento

Per colmare le lacune riscontrate, portare l'organizzazione a un livello di Rischio Residuale **Accettabile** e preparare Aetheris Therapeutics alla certificazione **ISO/IEC 27001:2022**, è stato definito un **Risk Treatment Plan (RTP)** coordinato della durata di 12 mesi.

### Risorse e Financial Impact
* **Budget Remediation Anno 1 (Capex + Opex):** **€ 70.000**
  * *Capex (Investimenti tecnologici PAM/Setup):* € 15.000
  * *Opex (Licenze Cloud MFA, SIEM Sentinel, SOC h24 MSSP, ITAM):* € 42.000 / anno
  * *Consulenza Governance (IRP, GDPR, Policy SGSI):* € 13.000

---

## 5. Decisione Richiesta al Board dell'Alta Direzione

L'Alta Direzione è chiamata ad approvare formalmente:
1. Il **Piano di Trattamento dei Rischi (`RSK-RTP-2026-03`)** e l'allocazione del budget straordinario di **€ 70.000**.
2. La nomina formale dell'**ISMS Owner / CISO** per la supervisione della Roadmap SGSI.
3. L'avvio dell'esecuzione prioritaria della **Fase 1 (Primi 90 giorni)** per l'abbattimento immediato delle 5 Non-Conformità Maggiori.

---

## 6. Controllo Documentale e Approvazione (ISO 27001:2022 Clausola 7.5)

| Ruolo | Nome e Cognome | Stato | Data |
| :--- | :--- | :--- | :--- |
| **Redatto da (Lead Auditor)** | Emanuele Tarchi | Completato | Agosto 2026 |
| **Revisionato da (IT Director)** | IT Director ad interim | Revisionato | Agosto 2026 |
| **Approvato da (Alta Direzione)** | Chief Executive Officer (CEO) | Approvato | Agosto 2026 |
