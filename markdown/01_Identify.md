# National Institute of Standards and Technology (NIST) Cybersecurity Framework (CSF) v1.1 - Gap Analysis
## Funzione Core: IDENTIFY (ID) - Identificazione
**Organizzazione Target:** Aetheris Therapeutics S.p.A.  
**Tipo di Documento:** Gap Analysis e Valutazione della Postura di Sicurezza  
**Classificazione:** Interno / Portfolio Professionale  

---

## 📊 Sintesi dei Risultati (Funzione Identify)

| Sottocategoria | Controlli Totali | PASS | FAIL | N/A | % di Conformità |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Asset Management (ID.AM)** | 5 | 1 | 4 | 0 | 20% |
| **Business Environment (ID.BE)** | 5 | 1 | 3 | 1 | 25% |
| **Governance (ID.GV)** | 4 | 0 | 4 | 0 | 0% |
| **Risk Assessment (ID.RA)** | 6 | 0 | 6 | 0 | 0% |
| **Risk Management Strategy (ID.RM)** | 3 | 0 | 2 | 1 | 0% |
| **TOTALE** | **23** | **2** | **19** | **2** | **8,7%** |

---

## 🔍 Valutazione Dettagliata dei Controlli

### 1. Gestione degli Asset (ID.AM)

| Codice | Obiettivo di Controllo / Domanda | Esito | Motivazione Tecnica ed Evidenza d'Audit |
| :--- | :--- | :---: | :--- |
| **ID.AM-1** | I dispositivi fisici e i sistemi all'interno dell'organizzazione sono censiti? | `FAIL` | Il tracciamento hardware si basa su un foglio Excel statico contenente solo i numeri di serie e i dettagli di garanzia dei laptop. Non esiste un CMDB automatizzato né una revisione formale del ciclo di vita degli asset fisici. |
| **ID.AM-2** | Le piattaforme software e le applicazioni dell'organizzazione sono censite? | `FAIL` | Manca un inventario software centralizzato o il tracciamento delle applicazioni SaaS (es. Office 365, BioNexus Cloud). Completa assenza di controlli sullo Shadow IT. |
| **ID.AM-3** | I flussi di dati e le comunicazioni organizzative sono mappati? | `PASS` | Il team di ingegneria di rete mantiene diagrammi di rete chiari, dettagliati e aggiornati, inclusi iTopology cloud ibridi (Microsoft Azure). |
| **ID.AM-4** | I sistemi informativi esterni sono catalogati? | `FAIL` | Le applicazioni SaaS di terze parti (BioNexus Cloud, Office 365) non sono catalogate formalmente in un registro di sicurezza. I contratti sono gestiti esclusivamente da Procurement/Finance senza revisione IT/Security. |
| **ID.AM-5** | Le risorse sono prioritarie in base alla classificazione e alla criticità? | `FAIL` | Non esiste un quadro di governance dei dati né uno schema di classificazione delle informazioni. Di conseguenza, gli asset IT e i server non possono essere classificati in base alla sensibilità o all'impatto sul business. |

---

### 2. Contesto di Business (ID.BE)

| Codice | Obiettivo di Controllo / Domanda | Esito | Motivazione Tecnica ed Evidenza d'Audit |
| :--- | :--- | :---: | :--- |
| **ID.BE-1** | Il ruolo dell'organizzazione nella catena di fornitura è identificato e documentato? | `FAIL` | Non esiste un processo di Third-Party Risk Management (TPRM). I fornitori e i provider SaaS non sono categorizzati o valutati in base al rischio della supply chain cyber. |
| **ID.BE-2** | La posizione dell'organizzazione nelle infrastrutture critiche è identificata? | `N/A` | Aetheris Therapeutics opera nella ricerca biofarmaceutica privata e non è formalmente designata come Infrastruttura Critica Nazionale o Operatore di Servizi Essenziali. |
| **ID.BE-3** | Le priorità, la missione e gli obiettivi dell'organizzazione sono comunicati? | `PASS` | Il CEO Dr. Arthur Vance ha definito e comunicato una chiara strategia di crescita commerciale focalizzata sull'espansione del mercato e sulla ricerca proprietaria. |
| **ID.BE-4** | Le funzioni critiche e le dipendenze sono stabilite? | `FAIL` | Sebbene l'IT esegua backup operativi, non esiste una mappatura formale guidata dal business che colleghi le dipendenze tecnologiche alle funzioni aziendali critiche (es. dipendenza dal SaaS di laboratorio). |
| **ID.BE-5** | I requisiti di resilienza e le verifiche SLA/SOC sono definiti? | `FAIL` | Non è stata condotta alcuna Analisi d'Impatto sul Business (BIA) formale. Non vengono effettuate attività di due diligence o revisioni di report SOC per i provider SaaS terzi. |

---

### 3. Governance (ID.GV)

| Codice | Obiettivo di Controllo / Domanda | Esito | Motivazione Tecnica ed Evidenza d'Audit |
| :--- | :--- | :---: | :--- |
| **ID.GV-1** | È stabilita una politica di sicurezza delle informazioni aziendale? | `FAIL` | Esiste solo una policy IT operativa generica. Non esiste una Information Security Policy (ISP) formale approvata dalla direzione esecutiva. |
| **ID.GV-2** | I ruoli e le responsabilità della sicurezza delle informazioni sono coordinati? | `FAIL` | I compiti di cybersecurity sono delegati informalmente al team IT generale. I ruoli di sicurezza mancano di definizione formale, autorità o linee di reporting dedicate alla dirigenza. |
| **ID.GV-3** | I requisiti legali e normativi (es. GDPR) sono compresi e gestiti? | `FAIL` | La mancanza di registri di trattamento dei dati, policy di protezione dei dati o mappatura della conformità GDPR espone l'organizzazione a gravi responsabilità legali e normative. |
| **ID.GV-4** | I processi di governance affrontano il rischio informatico? | `FAIL` | Il Consiglio di Amministrazione e il CEO non hanno visibilità formale sui rischi informatici e tecnologici. La gestione del rischio interna è limitata strettamente ai rischi finanziari tradizionali. |

---

### 4. Valutazione del Rischio (ID.RA)

| Codice | Obiettivo di Controllo / Domanda | Esito | Motivazione Tecnica ed Evidenza d'Audit |
| :--- | :--- | :---: | :--- |
| **ID.RA-1** | Le scansioni delle vulnerabilità vengono eseguite regolarmente? | `FAIL` | Lo scanner Qualys è stato acquistato ma viene utilizzato esclusivamente su base estemporanea (ad-hoc). Le scansioni non sono programmate e mancano di reportistica formale, metriche o flussi di lavoro di remediation/patching prioritari. |
| **ID.RA-2** | L'intelligence sulle minacce viene ricevuta da feed/fonti? | `FAIL` | Nessuna iscrizione a feed di Threat Intelligence o comunità di condivisione delle informazioni (es. ISAC/CERT). L'analista di sicurezza opera in modalità puramente reattiva. |
| **ID.RA-3** | Le minacce interne ed esterne sono identificate e documentate? | `FAIL` | Non esiste un processo di modellazione delle minacce (threat modeling) per identificare o documentare gli attori ostili che prendono di mira le formule biofarmaceutiche proprietarie e la proprietà intellettuale della ricerca. |
| **ID.RA-4** | I potenziali impatti sul business e le probabilità sono identificati? | `FAIL` | L'assenza di valorizzazione degli asset e di una BIA rende impossibile quantificare gli impatti finanziari, operativi o reputazionali di potenziali incidenti informatici. |
| **ID.RA-5** | Minacce, vulnerabilità e impatti vengono utilizzati per determinare il rischio? | `FAIL` | Non è implementata alcuna metodologia di valutazione del rischio (es. ISO 27005) per calcolare i punteggi di rischio basati sulla probabilità della minaccia e sull'impatto sugli asset. |
| **ID.RA-6** | Le risposte al rischio sono identificate e prioritizzate? | `FAIL` | In assenza di un framework di rischio formale, gli investimenti in sicurezza e le azioni di remediation non possono essere prioritizzati in base al reale impatto sul business. |

---

### 5. Strategia di Gestione del Rischio (ID.RM)

| Codice | Obiettivo di Controllo / Domanda | Esito | Motivazione Tecnica ed Evidenza d'Audit |
| :--- | :--- | :---: | :--- |
| **ID.RM-1** | Un processo di gestione del rischio è approvato dall'alta dirigenza? | `FAIL` | Il top management non ha mai approvato un processo di gestione del rischio informatico poiché non esiste attualmente un framework strutturato a livello organizzativo. |
| **ID.RM-2** | La tolleranza al rischio organizzativa è definita tramite la propensione al rischio (Risk Appetite)? | `FAIL` | Non è stata redatta o approvata dal CdA alcuna Dichiarazione di Propensione al Rischio Informatico per stabilire le soglie di perdita accettabili. |
| **ID.RM-3** | La tolleranza al rischio si basa sui vincoli dell'infrastruttura? | `N/A` | I vincoli di tolleranza al rischio delle infrastrutture critiche non si applicano direttamente alle attuali operazioni commerciali interne. |

---

## 💡 Principali Priorità di Remediation per `IDENTIFY`

1. **Governance e Leadership:** Assumere un Cyber Security Manager / CISO dedicato e pubblicare una Information Security Policy formale approvata dalla direzione esecutiva.
2. **Inventario Asset e Software:** Sostituire il tracciamento Excel statico con una soluzione CMDB automatizzata che cataloghi hardware, software e abbonamenti SaaS critici (*BioNexus Cloud*).
3. **Gestione del Rischio Terze Parti (TPRM):** Implementare un flusso di valutazione dei fornitori per esaminare le baseline di sicurezza dei SaaS prima dell'approvvigionamento.
4. **Governance dei Dati:** Condurre un'attività di data discovery e stabilire una politica di classificazione dei dati per proteggere la proprietà intellettuale della ricerca proprietaria.
