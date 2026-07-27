# National Institute of Standards and Technology (NIST) Cybersecurity Framework (CSF) v1.1 - Gap Analysis
## Funzione Core: RECOVER (RC) - Ripristino
**Organizzazione Target:** Aetheris Therapeutics S.p.A.  
**Tipo di Documento:** Gap Analysis e Valutazione della Postura di Sicurezza  
**Classificazione:** Interno / Portfolio Professionale  

---

## 📊 Sintesi dei Risultati (Funzione Recover)

| Sottocategoria | Controlli Totali | PASS | FAIL | N/A | % di Conformità |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Recovery Planning (RC.RP)** | 1 | 0 | 1 | 0 | 0% |
| **Improvements (RC.IM)** | 2 | 0 | 2 | 0 | 0% |
| **Communications (RC.CO)** | 3 | 0 | 3 | 0 | 0% |
| **TOTALE** | **6** | **0** | **6** | **0** | **0%** |

---

## 🔍 Valutazione Dettagliata dei Controlli

### 1. Pianificazione del Ripristino (RC.RP)

| Codice | Obiettivo di Controllo / Domanda | Esito | Motivazione Tecnica ed Evidenza d'Audit |
| :--- | :--- | :---: | :--- |
| **RC.RP-1** | Il piano di ripristino (Recovery Plan) è eseguito durante o dopo un incidente? | `FAIL` | Sebbene l'IT esegua backup e test di ripristino operativi sui dati, manca un piano formale di Cyber Recovery integrato con l'Incident Response Plan per gestire attacchi complessi (es. ransomware esteso). |

---

### 2. Miglioramenti (RC.IM)

| Codice | Obiettivo di Controllo / Domanda | Esito | Motivazione Tecnica ed Evidenza d'Audit |
| :--- | :--- | :---: | :--- |
| **RC.IM-1** | I piani di ripristino vengono aggiornati incorporando le lezioni apprese? | `FAIL` | Non esiste un processo formale di revisione post-incident o di aggiornamento delle procedure di disaster recovery basato su scenari di attacco reali. |
| **RC.IM-2** | Le strategie di ripristino vengono aggiornate per riflettere le modifiche all'architettura? | `FAIL` | Le strategie di ripristino non sono state aggiornate a seguito dell'introduzione dei servizi cloud (Azure) e della piattaforma SaaS di laboratorio (*BioNexus Cloud*). |

---

### 3. Comunicazioni (RC.CO)

| Codice | Obiettivo di Controllo / Domanda | Esito | Motivazione Tecnica ed Evidenza d'Audit |
| :--- | :--- | :---: | :--- |
| **RC.CO-1** | Le attività di ripristino sono coordinate con gli stakeholder interni ed esterni? | `FAIL` | Manca una matrice di comunicazione definita per aggiornare la direzione, i dipendenti o i partner durante la fase di ripristino dei sistemi critici. |
| **RC.CO-2** | La gestione della reputazione e le PR aziendali sono coordinate durante il ripristino? | `FAIL` | Nessun piano di PR o gestione della crisi reputazionale è predisposto per mitigare il danno d'immagine a seguito di un'interruzione prolungata dei servizi o di un data breach. |
| **RC.CO-3** | Le comunicazioni sulle attività di ripristino soddisfano i requisiti di trasparenza? | `FAIL` | Mancano linee guida per la comunicazione trasparente e conforme ai requisiti legali ed etici nei confronti di clienti, autorità e organismi di regolamentazione. |

---

## 💡 Principali Priorità di Remediation per `RECOVER`

1. **Adozione di Backup Immutabili e Air-Gapped:** Aggiornare l'architettura dei backup implementando repository immutabili (WORM) e isolamento logico/fisico (Air-Gap) per garantire la ripristinabilità dei dati in caso di attacco ransomware.
2. **Integrazione BCP/DR e Cyber Resilience:** Formalizzare un piano di Disaster Recovery e Business Continuity aggiornato, calibrato sui tempi di ripristino target (RTO/RPO) definiti dal business per la ricerca biofarmaceutica.
3. **Piano di Comunicazione di Crisi & PR:** Sviluppare playbook di comunicazione esecutiva e gestione delle PR per coordinare la gestione della reputazione con gli stakeholder e le autorità durante la fase di ripristino.
4. **Esercitazioni e Simulation Tabletop:** Svolgere simulazioni periodiche di ripristino completo da zero (Bare-Metal Recovery) e test di crisi aziendale coinvolgendo la dirigenza.
