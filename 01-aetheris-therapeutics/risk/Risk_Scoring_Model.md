# 🧮 Risk Scoring Model & Valuation Methodology — ISO/IEC 27005:2022
## Modello di Calcolo del Rischio, Matrice 5x5 e Criteri di Accettabilità

**Standard di Riferimento:** ISO/IEC 27005:2022 & ISO/IEC 27001:2022 (Clausola 6.1.2)  
**Organizzazione:** Aetheris Therapeutics S.p.A.  
**Rif. Documento:** RSK-SCM-2026-02  
**Versione:** 1.0  
**Stato:** Approvato  
**Classificazione:** Uso Interno GRC & Risk Team  
**Data di Efficacia:** Agosto 2026  

---

## 1. Algoritmo di Calcolo e Formula del Rischio

Il modello di scoring adotta un approccio semi-quantitativo conforme alla norma **ISO/IEC 27005:2022**. Il livello di rischio viene calcolato attraverso la seguente formulazione matematica:

$$Rischio = Probabilità (P) \times Impatto (I)$$

* **Rischio Inerente ($R_I$):** Il livello di rischio espresso prima dell'applicazione o in assenza dei controlli di sicurezza compensativi.
* **Fattore Mitigante del Controllo ($C_M$):** La percentuale di efficacia dei controlli di sicurezza applicati o pianificati (da $0\%$ a $80\%$).
* **Rischio Residuale ($R_R$):** Il livello di rischio rimanente dopo l'attuazione delle misure di mitigazione previste dal Risk Treatment Plan (RTP):

$$R_R = R_I \times (1 - C_M)$$

---

## 2. Definizione delle Scale di Valutazione (Scoring Scale)

### 2.1 Scala della Probabilità / Minaccia (Likelihood - P)

| Valore (P) | LIVELLO | Frequenza Stimata | Descrizione Operativa |
| :---: | :--- | :--- | :--- |
| **1** | **Molto Bassa** | Meno di 1 volta ogni 5 anni | Evento raro, richiede condizioni eccezionali e capacità avanzate dell'attaccante. |
| **2** | **Bassa** | 1 volta ogni 1 – 5 anni | Evento poco frequente ma possibile in presenza di vulnerabilità note non mitigate. |
| **3** | **Media** | 1 volta all'anno | Evento probabile nel corso dell'operatività ordinaria; minacce comuni presenti. |
| **4** | **Alta** | Più volte all'anno | Evento altamente probabile; tentativi di scansione/exploit quotidiani. |
| **5** | **Molto Alta** | Continuo / Quotidiano | Evento quasi certo o già in corso; assenza completa di barriere difensive. |

---

### 2.2 Scala dell'Impatto di Business (Impact - I)

| Valore (I) | LIVELLO | Impatto Finanziario / Legale | Impatto Operativo / Reputazionale |
| :---: | :--- | :--- | :--- |
| **1** | **Insignificante** | $< € 5.000$ | Nessun blocco operativo; nessun danno alla reputazione o sanzione. |
| **2** | **Minore** | $€ 5.000 - € 25.000$ | Interruzione marginale ($< 4$ ore); impatto limitato gestibile localmente. |
| **3** | **Moderato** | $€ 25.000 - € 100.000$ | Blocco parziale R&D ($< 24$ ore); sanzioni amministrative minori o danno locale. |
| **4** | **Grave** | $€ 100.000 - € 500.000$ | Blocco operativo esteso ($24 - 72$ ore); violazione GDPR Art. 33/34 con notifiche. |
| **5** | **Critico** | $> € 500.000$ | Compromissione brevetti R&D, blocco produttivo $> 3$ giorni; danno d'immagine grave. |

---

## 3. Matrice di Valutazione del Rischio 5x5 (Risk Matrix)

Combinando la Probabilità ($P$) e l'Impatto ($I$), si ottiene il Punteggio di Rischio (Score da 1 a 25) con la seguente classificazione di severità:

| Probabilità (P) \ Impatto (I) | Insignificante (1) | Minore (2) | Moderato (3) | Grave (4) | Critico (5) |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Molto Alta (5)** | 🟡 5 (Medio) | 🟧 10 (Alto) | 🟥 15 (Critico) | 🟥 20 (Critico) | 🟥 25 (Critico) |
| **Alta (4)** | 🟢 4 (Basso) | 🟡 8 (Medio) | 🟧 12 (Alto) | 🟥 16 (Critico) | 🟥 20 (Critico) |
| **Media (3)** | 🟢 3 (Basso) | 🟢 6 (Basso) | 🟡 9 (Medio) | 🟧 12 (Alto) | 🟥 15 (Critico) |
| **Bassa (2)** | 🟢 2 (Basso) | 🟢 4 (Basso) | 🟢 6 (Basso) | 🟡 8 (Medio) | 🟧 10 (Alto) |
| **Molto Bassa (1)** | 🟢 1 (Basso) | 🟢 2 (Basso) | 🟢 3 (Basso) | 🟢 4 (Basso) | 🟡 5 (Medio) |

---

## 4. Soglie di Tolleranza e Criteri di Trattamento (Risk Appetite)

La direzione di **Aetheris Therapeutics S.p.A.** ha formalizzato la soglia di tolleranza al rischio (*Risk Appetite*) ponendo il **limite massimo accettabile a Score 6 (Verde / Basso)**.

| Livello di Rischio | Score | Azione di Trattamento Richiesta (ISO 27001 Cl. 6.1.3) | SLA Remediation |
| :--- | :---: | :--- | :--- |
| 🟥 **CRITICO** | **15 – 25** | **Mitigazione Immediata:** Intervento d'emergenza obbligatorio. Notifica immediata al Board. | **Entro 30 giorni** |
| 🟧 **ALTO** | **10 – 14** | **Trattamento Prioritario:** Allocazione budget nel Risk Treatment Plan (RTP). | **Entro 90 giorni** |
| 🟡 **MEDIO** | **5 – 9** | **Gestione Pianificata:** Attuazione controlli procedurali o tecnici entro il piano annuale. | **Entro 180 giorni** |
| 🟢 **BASSO** | **1 – 4** | **Accettazione del Rischio:** Rischio all'interno del Risk Appetite. Monitoraggio periodico. | **Riesame Annuale** |

---

## 5. Controllo Documentale e Approvazione (ISO 27001:2022 Clausola 7.5)

| Ruolo | Nome e Cognome | Stato | Data |
| :--- | :--- | :--- | :--- |
| **Redatto da (Lead Auditor)** | Emanuele Tarchi | Completato | Agosto 2026 |
| **Revisionato da (IT Director)** | IT Director ad interim | Revisionato | Agosto 2026 |
| **Approvato da (Alta Direzione)** | Chief Executive Officer (CEO) | Approvato | Agosto 2026 |
