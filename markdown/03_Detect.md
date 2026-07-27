# National Institute of Standards and Technology (NIST) Cybersecurity Framework (CSF) v1.1 - Gap Analysis
## Funzione Core: DETECT (DE) - Rilevamento
**Organizzazione Target:** Aetheris Therapeutics S.p.A.  
**Tipo di Documento:** Gap Analysis e Valutazione della Postura di Sicurezza  
**Classificazione:** Interno / Portfolio Professionale  

---

## 📊 Sintesi dei Risultati (Funzione Detect)

| Sottocategoria | Controlli Totali | PASS | FAIL | N/A | % di Conformità |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Anomalies and Events (DE.AE)** | 5 | 0 | 5 | 0 | 0% |
| **Security Continuous Monitoring (DE.CM)** | 8 | 1 | 7 | 0 | 12,5% |
| **Detection Processes (DE.DP)** | 5 | 0 | 5 | 0 | 0% |
| **TOTALE** | **18** | **1** | **17** | **0** | **5,6%** |

---

## 🔍 Valutazione Dettagliata dei Controlli

### 1. Anomalie ed Eventi (DE.AE)

| Codice | Obiettivo di Controllo / Domanda | Esito | Motivazione Tecnica ed Evidenza d'Audit |
| :--- | :--- | :---: | :--- |
| **DE.AE-1** | Una baseline del traffico di rete e delle operazioni sui dati è stabilita e mantenuta? | `FAIL` | Non esiste una profilazione del comportamento di rete basale o dei flussi dati. L'azienda non dispone di strumenti di rilevamento delle anomalie comportamentali. |
| **DE.AE-2** | Gli eventi rilevati vengono analizzati per comprendere la natura dell'attacco? | `FAIL` | Mancano strumenti di correlazione dei log. L'unico analista di sicurezza analizza manualmente ed estemporaneamente solo gli avvisi locali dell'antivirus Defender. |
| **DE.AE-3** | I dati degli eventi di sicurezza vengono aggregati e correlati da più fonti? | `FAIL` | Assenza totale di un sistema SIEM (Security Information and Event Management) per centralizzare i log di Azure, Office 365, firewall Palo Alto e sistemi on-premise. |
| **DE.AE-4** | L'impatto degli eventi di sicurezza viene determinato? | `FAIL` | Manca una matrice di classificazione dell'impatto degli incidenti. Gli eventi non vengono categorizzati in base alla gravità o alla criticità degli asset coinvolti. |
| **DE.AE-5** | Le soglie di allerta per le anomalie sono stabilite e affinate nel tempo? | `FAIL` | Le soglie di allerta sono quelle predefinite di fabbrica degli apparati singoli; non è stato effettuato alcun tuning personalizzato per ridurre i falsi positivi/negativi. |

---

### 2. Monitoraggio Continuo della Sicurezza (DE.CM)

| Codice | Obiettivo di Controllo / Domanda | Esito | Motivazione Tecnica ed Evidenza d'Audit |
| :--- | :--- | :---: | :--- |
| **DE.CM-1** | La rete aziendale è monitorata per rilevare potenziali eventi di sicurezza? | `FAIL` | Assenza di sensori IDS/IPS centralizzati o di analisi del traffico di rete in tempo reale su scala aziendale. |
| **DE.CM-2** | L'ambiente fisico è monitorato per rilevare potenziali eventi di sicurezza? | `PASS` | Presidio con telecamere TVCC 24/7 e controllo degli accessi fisici ai laboratori di ricerca con registrazione continuativa degli ingressi. |
| **DE.CM-3** | Le attività del personale e degli utenti sono monitorate per rilevare anomalie? | `FAIL` | Non viene effettuato alcun monitoraggio delle attività degli utenti (UEBA) né tracciamento dell'uso improprio di credenziali o accessi anomali fuori orario. |
| **DE.CM-4** | Il codice e i servizi di terze parti (SaaS) vengono monitorati per anomalie? | `FAIL` | Nessun monitoraggio della piattaforma SaaS di laboratorio (*BioNexus Cloud*) o delle integrazioni API con l'ambiente Microsoft 365. |
| **DE.CM-5** | Il codice malevolo (malware) viene rilevato in tempo reale sugli endpoint? | `FAIL` | La protezione degli endpoint si affida alla versione base di Microsoft Defender senza agenti EDR/XDR centralizzati con capacità di isolamento automatico dell'host. |
| **DE.CM-6** | I supporti esterni e i dispositivi mobili vengono monitorati per rilevare anomalie? | `FAIL` | Nessun tracciamento o controllo sugli eventi di inserimento di supporti di memoria USB o connessione di dispositivi non autorizzati. |
| **DE.CM-7** | Le scansioni di vulnerabilità e il monitoraggio continuo vengono integrati? | `FAIL` | Le scansioni Qualys vengono eseguite ad-hoc e i relativi risultati non sono integrati con alcun flusso di monitoraggio continuo o SIEM. |
| **DE.CM-8** | Il monitoraggio della sicurezza è attivo H24 7/7 (SOC 24/7)? | `FAIL` | Non esiste un Security Operations Center (SOC) né interno né erogato tramite provider gestito (MSSP). Il monitoraggio durante il weekend e gli orari notturni è assente. |

---

### 3. Processi di Rilevamento (DE.DP)

| Codice | Obiettivo di Controllo / Domanda | Esito | Motivazione Tecnica ed Evidenza d'Audit |
| :--- | :--- | :---: | :--- |
| **DE.DP-1** | Ruoli e responsabilità per il rilevamento delle minacce sono chiaramente definiti? | `FAIL` | Le attività di monitoraggio e detection non sono formalmente assegnate; ricadono in modo generico e non strutturato sul singolo analista IT. |
| **DE.DP-2** | Le attività di rilevamento soddisfano tutti i requisiti normativi e legali? | `FAIL` | L'assenza di tracciamento e conservazione centralizzata dei log di audit rende impossibile soddisfare i requisiti di accountability e tracciabilità previsti dal GDPR. |
| **DE.DP-3** | I processi di rilevamento vengono testati regolarmente per verificarne l'efficacia? | `FAIL` | Non vengono eseguite simulazioni di attacco (Red Team, Purple Team o test di intrusione) per verificare la capacità di rilevamento delle difese. |
| **DE.DP-4** | Le informazioni sugli eventi rilevati vengono comunicate ai ruoli opportuni? | `FAIL` | Manca un flusso di escalation definito. In caso di anomalia, non vi è una procedura automatica di notifica verso il responsabile IT o la dirigenza. |
| **DE.DP-5** | I processi di rilevamento vengono continuamente migliorati? | `FAIL` | Non è previsto alcun processo di revisione periodica delle logiche di detection o aggiornamento delle firme/regole basato sulle nuove minacce emergenti. |

---

## 💡 Principali Priorità di Remediation per `DETECT`

1. **Adozione di una Soluzione SIEM (MSSP / In-House):** Ingestionare centralmente i log di Azure, Office 365, firewall Palo Alto e Active Directory in un SIEM per la correlazione degli eventi in tempo reale.
2. **Implementazione di Agenti EDR/XDR:** Sostituire l'antivirus tradizionale sugli endpoint con agenti EDR per garantire la visibilità della telemetria sugli host e il blocco automatico dei processi malevoli.
3. **Attivazione di un Servizio SOC 24/7:** Affidarsi a un Managed Security Service Provider (MSSP) per garantire il monitoraggio e il triage degli allarmi di sicurezza H24 7 giorni su 7.
4. **Definizione di Regole e Baseline di Allerta:** Configurare regole di rilevamento specifiche per comportamenti anomali su file di ricerca sensibili e tentativi di accesso da posizioni geografiche insolite.
