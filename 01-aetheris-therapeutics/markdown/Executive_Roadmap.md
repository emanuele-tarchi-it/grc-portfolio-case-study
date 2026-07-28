# Aetheris Therapeutics S.p.A. — Executive Remediation Roadmap

## 🎯 Visione Strategica e Programma CISO (Piano Triennale)

La seguente Roadmap delinea gli interventi prioritari raccomandati per sanare i gap emersi dalla valutazione integrata **NIST CSF v1.1** e **ISO/IEC 27001:2022**, trasformando l'attuale operatività reattiva in un **Sistema di Gestione della Sicurezza dell'Informazione (SGSI)** maturo e certificabile.

---

### 🚨 FASE 1: Quick Wins & Contenimento del Rischio Critico (Mesi 0 - 6)
* **Identity & Access Governance:**
  * Implementazione dell'autenticazione a più fattori (**MFA**) su tutti i punti d'accesso remoti (VPN, Azure Cloud, Office 365).
  * Eliminazione degli account amministrativi condivisi e introduzione di soluzioni di **Privileged Access Management (PAM)**.
* **Data Protection & Compliance:**
  * Redazione della **Information Security Policy (ISP)** formale e del **Registro dei Trattamenti (GDPR)**.
  * Definizione della policy aziendale di classificazione delle informazioni.
* **Incident Preparedness:**
  * Formalizzazione del primo **Incident Response Plan (IRP)** con matrice RACI di escalation verso la direzione.

---

### 🛡️ FASE 2: Consolidamento Architetturale & Monitoring (Mesi 6 - 18)
* **SOC & Continuous Detection:**
  * Deployment di una soluzione centralizzata **EDR / XDR** su tutti i client e server aziendali.
  * Attivazione di un servizio **SIEM** (es. Microsoft Sentinel) integrato con copertura SOC 24/7 (gestito in MSSP).
* **Vulnerability Management:**
  * Formalizzazione della procedura di Vulnerability Management con scansioni schedulate via Qualys e SLA di patching obbligatorie.
* **AirGap & Backup Immutabili:**
  * Implementazione dell'isolamento logico e dell'immutabilità dei dati dei backup di Disaster Recovery contro minacce ransomware.

---

### 🏛️ FASE 3: Governance Avanzata & Certificazione ISO 27001 (Mesi 18 - 36)
* **Third-Party Risk Management (TPRM):**
  * Istituzione di un processo di due diligence di sicurezza per fornitori terzi e partner SaaS.
* **Security Awareness Program:**
  * Avvio di campagne periodiche di simulazione phishing e corsi di formazione obbligatori per tutto il personale.
* **Certificazione ISO/IEC 27001:2022:**
  * Esecuzione di audit interni formali, Management Review della direzione e svolgimento dell'Audit di Certificazione con Ente Terzo accreditato.
