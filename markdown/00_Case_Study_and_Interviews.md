# Case Study: Aetheris Therapeutics S.p.A.
## Contesto Aziendale e Sintesi delle Interviste di Audit

### 🏢 Profilo Aziendale e Contesto Operativo
* **Ragione Sociale:** Aetheris Therapeutics S.p.A.
* **Settore:** Biofarmaceutico e Ricerca Medica Avanzata
* **Strategia di Business:** Rapida espansione di mercato e focalizzazione sul brevetto di formule di ricerca proprietarie e terapie cliniche ad alto valore strategico.
* **Architettura IT/OT:** Ambiente ibrido composto da cloud Microsoft Azure, servizi SaaS (Office 365, piattaforma di laboratorio *BioNexus Cloud*), laboratori di ricerca locali e infrastruttura client/server on-premise.

---

### 🎤 Evidenze Emerse dai Colloqui con i Dipartimenti (Audit Findings)

#### 1. Dipartimento Cyber Security & Governance
* **Composizione del Team:** 
  * 1x Analista di Sicurezza (profilo generalista, gestione degli incidenti in modalità puramente reattiva "antincendio", riporta all'IT Manager).
  * 1x Sistemista di Rete (gestione ed esercizio dei firewall, riporta al Network Team Leader).
  * 1x Consulente di Sicurezza Esterno (nuovo ruolo incaricato di valutare la postura di sicurezza e definire il programma di remediation).
* **Governance e Policy:** Il CEO (*Dr. Arthur Vance*) ha definito una visione commerciale molto chiara, ma i ruoli e le responsabilità per la cybersecurity non sono formalizzati e vengono delegati in blocco al team IT. È presente un'unica policy IT generica; mancano una *Information Security Policy* (ISP) strutturata e policy sulla classificazione dei dati.

#### 2. Dipartimento Gestione del Rischio e Terze Parti (TPRM)
* **Risk Management:** Il team di Risk Management interno si occupa esclusivamente di rischi di natura finanziaria. Non esiste alcun processo formale di valutazione o gestione del rischio tecnologico o cyber.
* **Third-Party Risk Management (TPRM):** Assenza totale di gestione del rischio della supply chain. I contratti con fornitori terzi (inclusa la piattaforma SaaS critica *BioNexus Cloud*) vengono esaminati unicamente da Procurement e Finance sotto il profilo commerciale, senza alcun coinvolgimento dell'IT o verifiche sui requisiti di sicurezza.

#### 3. Gestione delle Identità e degli Accessi (IAM)
* **Autenticazione:** Utilizzo di Microsoft Active Directory per utenti e gruppi. Sono richieste password complesse, ma **non è implementata l'Autenticazione a Due Fattori (MFA)** per l'accesso VPN remoto o ai servizi cloud.
* **Account Privilegiati:** Assenza di soluzioni di Privileged Access Management (PAM). La password dell'account "Domain Admin" è condivisa stabilmente tra più membri senior del team IT.
* **Gestione Permessi:** Gli accessi alle risorse aziendali vengono concessi meramente "su richiesta", senza applicare il principio del minimo privilegio (*least privilege*) e in assenza di revisioni periodiche dei diritti di accesso.

#### 4. Sicurezza di Rete e Sicurezza Fisica
* **Rete:** La rete è segmentata tramite VLAN e protetta da firewall Palo Alto Next-Gen configurati, aggiornati e sottoposti ad audit annuale dal team di rete. I diagrammi di rete sono aggiornati e includono l'ambiente cloud Azure.
* **Sicurezza Fisica:** Eccellente postura di sicurezza fisica. Presidio con telecamere TVCC 24/7, monitoraggio continuo dei laboratori di ricerca e approfondito processo di vetting/background check per tutti i dipendenti.

#### 5. Gestione degli Asset, Protezione Dati e Vulnerabilità
* **Gestione Asset:** L'inventario hardware si basa su un foglio Excel statico contenente seriali e garanzie dei soli laptop. Mancano un CMDB automatizzato e un inventario dei software installati o dei servizi SaaS in uso.
* **Data Security & DLP:** Tutti i dati risiedono in Azure e O365. Non sono implementate soluzioni di *Data Loss Prevention* (DLP) né restrizioni sull'uso di chiavette USB/supporti rimovibili.
* **Vulnerability Management:** È stato acquistato lo scanner Qualys, ma viene utilizzato dall'IT solo su base estemporanea ("ad-hoc"). Non esiste un programma formale di patching, con un elevato numero di vulnerabilità *High* e *Severe* non risolte.

#### 6. Rilevamento, Risposta agli Incidenti e Continuità Operativa
* **Detection & SIEM:** Assenza di soluzioni SIEM, EDR/XDR centralizzate o monitoraggio SOC 24/7. Il rilevamento delle minacce è affidato unicamente agli avvisi locali dell'antivirus (Microsoft Defender) sui singoli endpoint.
* **Incident Response:** Mancanza di un piano formale di Incident Response (IRP), di matrici di escalation o di capacità di analisi forense digitale.
* **Business Continuity (BCP/DR):** Il team IT esegue regolarmente backup, dispone di piani BCP documentati e conduce test periodici di Disaster Recovery sui salvataggi dati. *(Criticità: i backup non dispongono di isolamento logico/AirGap o immutabilità contro attacchi ransomware)*.
* **Formazione:** Ai neoassunti viene erogato solo un modulo web introduttivo generico (induction). Mancano sessioni di aggiornamento periodico e simulazioni di phishing.
