# National Institute of Standards and Technology (NIST) Cybersecurity Framework (CSF) v1.1 - Gap Analysis
## Funzione Core: RESPOND (RS) - Risposta
**Organizzazione Target:** Aetheris Therapeutics S.p.A.  
**Tipo di Documento:** Gap Analysis e Valutazione della Postura di Sicurezza  
**Classificazione:** Interno / Portfolio Professionale  

---

## 📊 Sintesi dei Risultati (Funzione Respond)

| Sottocategoria | Controlli Totali | PASS | FAIL | N/A | % di Conformità |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Response Planning (RS.RP)** | 1 | 0 | 1 | 0 | 0% |
| **Communications (RS.CO)** | 5 | 0 | 5 | 0 | 0% |
| **Analysis (RS.AN)** | 5 | 0 | 5 | 0 | 0% |
| **Mitigation (RS.MI)** | 3 | 0 | 3 | 0 | 0% |
| **Improvements (RS.IM)** | 2 | 0 | 2 | 0 | 0% |
| **TOTALE** | **16** | **0** | **16** | **0** | **0%** |

---

## 🔍 Valutazione Dettagliata dei Controlli

### 1. Pianificazione della Risposta (RS.RP)

| Codice | Obiettivo di Controllo / Domanda | Esito | Motivazione Tecnica ed Evidenza d'Audit |
| :--- | :--- | :---: | :--- |
| **RS.RP-1** | Il piano di risposta agli incidenti (IRP) è eseguito durante o dopo un incidente? | `FAIL` | Assenza totale di un Incident Response Plan (IRP) formalizzato. La gestione degli eventi critici avviene in modo estemporaneo ("antincendio") ad opera dell'unico analista IT. |

---

### 2. Comunicazioni (RS.CO)

| Codice | Obiettivo di Controllo / Domanda | Esito | Motivazione Tecnica ed Evidenza d'Audit |
| :--- | :--- | :---: | :--- |
| **RS.CO-1** | Il personale conosce il proprio ruolo e l'ordine di notifica durante un incidente? | `FAIL` | Mancano matrici di escalation (RACIR) o alberi di chiamata definiti per la notifica tempestiva degli incidenti all'IT Manager, al CEO o al Board. |
| **RS.CO-2** | Gli incidenti vengono segnalati in conformità ai requisiti legali/normativi? | `FAIL` | L'assenza di procedure di Incident Response impedisce il rispetto delle tempistiche di notifica del data breach previste dal GDPR (es. notifica al Garante entro 72 ore). |
| **RS.CO-3** | Le informazioni sugli incidenti vengono condivise con gli stakeholder interni ed esterni? | `FAIL` | Manca una procedura stabilita per la condivisione protetta delle informazioni sugli incidenti con i dipendenti, la direzione o i clienti. |
| **RS.CO-4** | Il coordinamento con i soggetti esterni (es. Law Enforcement, CERT) è stabilito? | `FAIL` | Nessun contatto preventivo o canale di coordinamento formalizzato con la Polizia Postale, CSIRT Nazionale o esperti legali/forensi esterni. |
| **RS.CO-5** | La condivisione volontaria delle informazioni sulle minacce è praticata? | `FAIL` | L'organizzazione non partecipa a gruppi di condivisione delle minacce del settore biofarmaceutico o della difesa informatica. |

---

### 3. Analisi (RS.AN)

| Codice | Obiettivo di Controllo / Domanda | Esito | Motivazione Tecnica ed Evidenza d'Audit |
| :--- | :--- | :---: | :--- |
| **RS.AN-1** | La notifica dei sistemi di rilevamento viene verificata ed esaminata? | `FAIL` | Gli alert non vengono sottoposti a triage strutturato (Livello 1/2/3). Gli avvisi locali di Defender vengono spesso ignorati o gestiti senza analisi approfondita. |
| **RS.AN-2** | L'impatto dell'incidente viene compreso e documentato? | `FAIL` | Non esiste una procedura di repertazione o quantificazione dei danni operativi, finanziari e reputazionali causati da un incidente di sicurezza. |
| **RS.AN-3** | L'analisi forense digitale viene eseguita per determinare le cause della violazione? | `FAIL` | Assenza di strumenti forensi (DFIR), competenze interne o contratti di retention con società terze specializzate per l'analisi dei vettori di attacco. |
| **RS.AN-4** | Gli incidenti vengono categorizzati in base alle risposte d'emergenza? | `FAIL` | Manca un sistema di prioritizzazione degli incidenti basato sulla gravità della minaccia o sul valore dei dati/sistemi coinvolti. |
| **RS.AN-5** | I processi per identificare le vulnerabilità sfruttate nell'attacco sono attivi? | `FAIL` | Nessuna correlazione sistematica tra le vulnerabilità note rilevate da Qualys e gli incidenti di sicurezza riscontrati sui sistemi. |

---

### 4. Mitigazione (RS.MI)

| Codice | Obiettivo di Controllo / Domanda | Esito | Motivazione Tecnica ed Evidenza d'Audit |
| :--- | :--- | :---: | :--- |
| **RS.MI-1** | Gli incidenti vengono contenuti per prevenire l'ulteriore propagazione? | `FAIL` | Assenza di agenti EDR/XDR in grado di isolare automaticamente la macchina infetta dalla rete o di applicare la quarantena logica immediata. |
| **RS.MI-2** | Le vulnerabilità o le minacce identificate vengono attenuate? | `FAIL` | Le azioni di remediation vengono applicate in modo ad-hoc senza verifiche post-intervento per confermare l'effettiva eradicazione della minaccia. |
| **RS.MI-3** | Le vulnerabilità residue vengono identificate e gestite? | `FAIL` | Non viene svolta alcuna valutazione dei rischi residui dopo la chiusura di un incidente informatico. |

---

### 5. Miglioramenti (RS.IM)

| Codice | Obiettivo di Controllo / Domanda | Esito | Motivazione Tecnica ed Evidenza d'Audit |
| :--- | :--- | :---: | :--- |
| **RS.IM-1** | I piani di risposta vengono aggiornati sulla base delle lezioni apprese? | `FAIL` | Manca una fase formale di "Lessons Learned" al termine degli incidenti per identificare le lacune e aggiornare le difese aziendali. |
| **RS.IM-2** | Le strategie di risposta sono aggiornate in base alle nuove minacce rilevate? | `FAIL` | Non sono previste revisioni periodiche o aggiornamenti adattivi delle procedure di difesa/risposta. |

---

## 💡 Principali Priorità di Remediation per `RESPOND`

1. **Creazione dell'Enterprise Incident Response Plan (IRP):** Redigere e formalizzare un piano aziendale di risposta agli incidenti che includa matrici di escalation (RACIR) e ruoli operativi definiti.
2. **Sviluppo dei Playbook di Attacco (5 Scenari Principali):** Creare procedure operative di dettaglio (playbook) per la gestione automatizzata/guidata dei 5 attacchi più comuni:
   * Ransomware e Cifratura Dati
   * Phishing & Compromissione Credenziali (BEC)
   * Infezione Malware / Compromissione Endpoint
   * Data Leakage / Esfiltrazione Proprietà Intellettuale
   * Attacco DDoS / Interruzione Servizi Cloud
3. **Servizio DFIR in Retainer (Digital Forensics & Incident Response):** Stipulare un contratto di pronto intervento con una società specializzata per l'analisi forense e la gestione delle crisi cyber complesse.
4. **Procedura di Notifica Data Breach (GDPR):** Definire il flusso procedurale per la notifica tempestiva alle autorità competenti (Garante Privacy) ed agli interessati entro i termini di legge.
