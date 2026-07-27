# National Institute of Standards and Technology (NIST) Cybersecurity Framework (CSF) v1.1 - Gap Analysis
## Funzione Core: PROTECT (PR) - Protezione
**Organizzazione Target:** Aetheris Therapeutics S.p.A.  
**Tipo di Documento:** Gap Analysis e Valutazione della Postura di Sicurezza  
**Classificazione:** Interno / Portfolio Professionale  

---

## 📊 Sintesi dei Risultati (Funzione Protect)

| Sottocategoria | Controlli Totali | PASS | FAIL | N/A | % di Conformità |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Identity Management & Access Control (PR.AC)** | 7 | 1 | 6 | 0 | 14,3% |
| **Awareness and Training (PR.AT)** | 5 | 0 | 5 | 0 | 0% |
| **Data Security (PR.DS)** | 8 | 1 | 7 | 0 | 12,5% |
| **Info Protection Processes & Procedures (PR.IP)** | 12 | 2 | 10 | 0 | 16,7% |
| **Maintenance (PR.MA)** | 2 | 0 | 2 | 0 | 0% |
| **Protective Technology (PR.PT)** | 5 | 1 | 4 | 0 | 20% |
| **TOTALE** | **39** | **5** | **34** | **0** | **12,8%** |

---

## 🔍 Valutazione Dettagliata dei Controlli

### 1. Gestione delle Identità, Autenticazione e Controllo Accessi (PR.AC)

| Codice | Obiettivo di Controllo / Domanda | Esito | Motivazione Tecnica ed Evidenza d'Audit |
| :--- | :--- | :---: | :--- |
| **PR.AC-1** | Gli identità e le credenziali sono gestite per gli utenti e i dispositivi autorizzati? | `FAIL` | Sebbene Active Directory sia in uso, la creazione e la disattivazione degli utenti non seguono un processo formale di Joiner-Mover-Leaver (JML). Mancano revisioni periodiche degli accessi. |
| **PR.AC-2** | L'accesso fisico alle risorse aziendali è gestito e protetto? | `PASS` | Presidio con telecamere TVCC 24/7, controllo accessi tramite badge biometrici/elettronici nei laboratori di ricerca e rigoroso vetting del personale. |
| **PR.AC-3** | L'accesso remoto è gestito e protetto? | `FAIL` | È presente una connessione VPN per il lavoro remoto, ma **non è implementata l'Autenticazione a Due Fattori (MFA)**. L'accesso si basa unicamente su username e password. |
| **PR.AC-4** | I permessi di accesso e le autorizzazioni sono gestiti in base al minimo privilegio? | `FAIL` | Gli accessi vengono concessi "su richiesta" senza verificare il principio del minimo privilegio (*least privilege*) o la separazione dei compiti (*separation of duties*). |
| **PR.AC-5** | L'integrità della rete è salvaguardata tramite separazione e segmentazione? | `FAIL` | Sebbene la rete interna presenti VLAN, non vi è una micro-segmentazione rigorosa tra la rete di ricerca/laboratorio e la rete uffici/SaaS cloud. |
| **PR.AC-6** | Le identità sono verificate tramite sistemi di autenticazione robusti (es. MFA)? | `FAIL` | L'MFA è totalmente assente su VPN, posta elettronica Office 365 e sulla piattaforma SaaS di laboratorio (*BioNexus Cloud*). |
| **PR.AC-7** | Gli utenti con privilegi elevati (Admin) sono gestiti e monitorati? | `FAIL` | Assenza di soluzioni PAM (Privileged Access Management). La password dell'account "Domain Admin" è condivisa in chiaro tra più tecnici IT senior. |

---

### 2. Formazione e Consapevolezza (PR.AT)

| Codice | Obiettivo di Controllo / Domanda | Esito | Motivazione Tecnica ed Evidenza d'Audit |
| :--- | :--- | :---: | :--- |
| **PR.AT-1** | Tutti gli utenti ricevono una formazione di base sulla sicurezza informatica? | `FAIL` | Esiste solo un modulo web introduttivo generico durante il processo di onboarding. Manca una formazione obbligatoria e ricorrente con cadenza almeno annuale. |
| **PR.AT-2** | Gli utenti con privilegi elevati comprendono i propri ruoli e responsabilità? | `FAIL` | Nessun corso di formazione specifico per gli amministratori di sistema o per il personale IT con credenziali privilegiate. |
| **PR.AT-3** | I terzi e i fornitori comprendono le loro responsabilità di sicurezza? | `FAIL` | Nessun requisito di formazione o clausola di consapevolezza della sicurezza è inserita nei contratti con i fornitori terzi. |
| **PR.AT-4** | Il personale di sicurezza comprende ruoli e responsabilità? | `FAIL` | L'unico analista di sicurezza opera in modalità reattiva senza formazione continua o certificazioni aggiornate sui processi d'incident response. |
| **PR.AT-5** | La dirigenza e il CdA comprendono i propri doveri di sicurezza delle informazioni? | `FAIL` | Manca qualsiasi attività di awareness o executive briefing rivolta al Board di Aetheris Therapeutics sui rischi cyber e di governance. |

---

### 3. Sicurezza dei Dati (PR.DS)

| Codice | Obiettivo di Controllo / Domanda | Esito | Motivazione Tecnica ed Evidenza d'Audit |
| :--- | :--- | :---: | :--- |
| **PR.DS-1** | I dati a riposo (*Data at Rest*) sono protetti? | `FAIL` | La cifratura del disco (es. BitLocker) non è imposta in modo centralizzato tramite policy su tutti i laptop aziendali. |
| **PR.DS-2** | I dati in transito (*Data in Transit*) sono protetti? | `PASS` | Le comunicazioni verso Azure e i servizi SaaS utilizzano protocolli crittografati standard (HTTPS / TLS 1.2+). |
| **PR.DS-3** | Le risorse e i supporti di memorizzazione sono gestiti formalmente? | `FAIL` | Non esistono restrizioni sull'uso di chiavette USB o hard disk esterni, esponendo l'azienda al rischio di esfiltrazione di proprietà intellettuale. |
| **PR.DS-4** | La capacità della rete e dei sistemi è gestita per garantire la disponibilità? | `FAIL` | Non sono definiti bilanciamenti di carico o monitoraggi formali della capacità di banda per far fronte ad attacchi di tipo Denial of Service (DoS). |
| **PR.DS-5** | È implementata una soluzione di Data Loss Prevention (DLP)? | `FAIL` | Completa assenza di strumenti DLP a livello endpoint, mail o cloud per prevenire la fuga di formule proprietarie o dati clinici. |
| **PR.DS-6** | L'integrità dei dati e dei software è verificata tramite controlli? | `FAIL` | Non vengono utilizzate tecniche di hashing o firma digitale per verificare l'integrità dei file di ricerca o del codice interno. |
| **PR.DS-7** | Gli ambienti di sviluppo e test sono separati da quello di produzione? | `FAIL` | Mancanza di una netta separazione logica e procedurale tra i sistemi di laboratorio in cui si sviluppano le formule e i sistemi di produzione. |
| **PR.DS-8** | La riservatezza dei dati è protetta tramite etichettatura e classificazione? | `FAIL` | Assenza di strumenti di etichettatura automatica o manuale dei file sensibili (es. Microsoft Azure Information Protection - AIP). |

---

### 4. Processi e Procedure di Protezione delle Informazioni (PR.IP)

| Codice | Obiettivo di Controllo / Domanda | Esito | Motivazione Tecnica ed Evidenza d'Audit |
| :--- | :--- | :---: | :--- |
| **PR.IP-1** | Una baseline di configurazione dei sistemi è creata e mantenuta? | `FAIL` | Non esistono immagini di sistema con hardening di sicurezza (es. benchmark CIS) applicate in modo standardizzato su server e PC. |
| **PR.IP-2** | Il ciclo di vita dello sviluppo software (SDLC) include la sicurezza? | `FAIL` | Le applicazioni o gli script interni sviluppati per la ricerca non seguono linee guida di Secure Coding o controlli di sicurezza nel codice. |
| **PR.IP-3** | La gestione dei cambiamenti (*Change Management*) è formalizzata? | `FAIL` | Le modifiche all'infrastruttura IT avvengono senza un comitato di approvazione (CAB) o una valutazione preventiva dell'impatto di sicurezza. |
| **PR.IP-4** | I backup dei dati sono eseguiti, protetti e testati regolarmente? | `PASS` | Il team IT effettua backup periodici dei dati e conduce test pratici di ripristino con esito positivo. |
| **PR.IP-5** | I backup sono protetti da attacchi informatici (es. Ransomware)? | `FAIL` | I backup non dispongono di isolamento logico/AirGap o immutabilità. In caso di compromissione del Domain Admin, anche i backup rischiano la cifratura. |
| **PR.IP-6** | La sicurezza fisica degli impianti è regolamentata da procedure? | `PASS` | Procedura di accesso ai laboratori ben documentata con registrazione degli ingressi e monitoraggio continuativo. |
| **PR.IP-7** | I piani di risposta e ripristino sono migliorati continuamente? | `FAIL` | Nessuna revisione post-incidente o aggiornamento procedurale formalizzato, vista la mancanza di un Incident Response Plan. |
| **PR.IP-8** | L'efficacia delle strategie di protezione è verificata tramite audit? | `FAIL` | Non è previsto un programma di audit interno o esterno periodico specifico sulla cybersecurity. |
| **PR.IP-9** | I piani di Incident Response e Business Continuity sono testati? | `FAIL` | Sebbene l'IT testi il ripristino dati, non vengono condotte esercitazioni simulate di risposta agli incidenti (Tabletop Exercises). |
| **PR.IP-10** | I piani di risposta includono un piano di comunicazione e gestione della crisi? | `FAIL` | Assenza di un piano di comunicazione PR o di gestione della reputazione in caso di data breach o blocco operativo. |
| **PR.IP-11** | La protezione dei dati soddisfa le normative sulla privacy (es. GDPR)? | `FAIL` | Manca la conduzione di valutazioni d'impatto sulla protezione dei dati (DPIA) per i trattamenti di dati clinici o di ricerca. |
| **PR.IP-12** | La gestione delle vulnerabilità e delle patch segue un programma stabilito? | `FAIL` | Qualys viene usato ad-hoc. Manca una patch policy con tempistiche vincolanti per la risoluzione delle vulnerabilità di livello *High* o *Critical*. |

---

### 5. Manutenzione (PR.MA)

| Codice | Obiettivo di Controllo / Domanda | Esito | Motivazione Tecnica ed Evidenza d'Audit |
| :--- | :--- | :---: | :--- |
| **PR.MA-1** | La manutenzione dei sistemi è eseguita e tracciata con strumenti autorizzati? | `FAIL` | Le attività di manutenzione dei sistemi IT avvengono senza un registro formale o un tracciamento puntuale degli interventi effettuati. |
| **PR.MA-2** | La manutenzione remota è approvata e controllata con autenticazione forte? | `FAIL` | Gli interventi di supporto remoto da parte di terzi avvengono tramite strumenti estemporanei senza MFA o sessioni registrate. |

---

### 6. Tecnologia Protettiva (PR.PT)

| Codice | Obiettivo di Controllo / Domanda | Esito | Motivazione Tecnica ed Evidenza d'Audit |
| :--- | :--- | :---: | :--- |
| **PR.PT-1** | I log di audit sono determinati, registrati e protetti da alterazioni? | `FAIL` | I log sono abilitati sui singoli apparati ma non vengono inviati a un repository centralizzato protetto da modifiche. |
| **PR.PT-2** | I supporti rimovibili (USB) sono limitati in base alle esigenze di business? | `FAIL` | Le porte USB sono completamente sbloccate su tutte le workstation senza alcuna restrizione tramite Group Policy (GPO). |
| **PR.PT-3** | Il principio del minimo privilegio è applicato alle funzioni di rete? | `PASS` | I firewall Palo Alto applicano regole di filtraggio e segmentazione basate sulle porte e sui servizi strettamente necessari. |
| **PR.PT-4** | Le reti di comunicazione sono protette da strumenti di sicurezza? | `FAIL` | Assenza di strumenti avanzati di protezione della rete cloud/ibrida e mancanza di ispezione crittografica SSL/TLS sui flussi uscenti. |
| **PR.PT-5** | Meccanismi di protezione sono implementati per prevenire codice malevolo? | `FAIL` | La protezione degli endpoint si affida unicamente alla versione base di Microsoft Defender senza gestione centralizzata avanzata o EDR. |

---

## 💡 Principali Priorità di Remediation per `PROTECT`

1. **Rollout dell'Autenticazione a Due Fattori (MFA/2FA):** Implementare immediatamente l'MFA su VPN, Microsoft 365 e sulla piattaforma SaaS di laboratorio (*BioNexus Cloud*).
2. **Gestione degli Accessi Privilegiati (PAM):** Eliminare la condivisione delle password di amministratore, adottare l'accesso basato sui ruoli (RBAC) e distribuire una soluzione PAM.
3. **Data Loss Prevention (DLP) e Blocco USB:** Disabilitare l'uso non autorizzato di supporti di memoria USB ed erogare strumenti Microsoft DLP e classificazione Azure AIP per le formule di ricerca.
4. **Vulnerability & Patch Management Program:** Strutturare un programma periodico e vincolante di patching basato sui report delle scansioni Qualys.
5. **Formazione sulla Sicurezza:** Avviare un programma di formazione annuale obbligatorio sulla sicurezza per tutti i dipendenti, integrato da simulazioni di phishing.
