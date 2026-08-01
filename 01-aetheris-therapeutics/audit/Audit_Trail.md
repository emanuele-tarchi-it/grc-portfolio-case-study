# 🛡️ Audit Trail — Aetheris Therapeutics S.p.A.
## ISO/IEC 27001:2022 & NIST CSF v1.1

Documento che traccia tutte le attività svolte durante l’audit: interviste, evidenze raccolte, verifiche tecniche, documenti analizzati e correlazioni con i rilievi finali.

---

## 1. Informazioni Generali

**Organizzazione:** Aetheris Therapeutics S.p.A.  
**Settore:** Biotecnologico / Farmaceutico  
**Audit Team:**  
- Lead Auditor: Emanuele Tarchi  
- Supporto: IT Manager, Cybersecurity Analyst  

**Periodo dell’Audit:**  
- Preparazione: 1 settimana  
- Fieldwork: 2 settimane  
- Reporting: 1 settimana  

---

## 2. Stakeholder Coinvolti

| Ruolo | Nome | Dipartimento | Modalità Intervista | Data |
|------|------|--------------|----------------------|------|
| IT Director & Systems Administrator | — | IT Operations | Intervista tecnica | Giorno 1 |
| Cybersecurity Analyst | — | Security | Intervista tecnica | Giorno 2 |
| Legal, Compliance & HR Manager | — | Governance & HR | Intervista funzionale | Giorno 3 |
| R&D Lab Manager | — | Ricerca | Walkthrough laboratori | Giorno 4 |

*(I nomi non sono riportati per motivi di privacy.)*

---

## 3. Evidenze Raccolte

### 3.1 Interviste (Fieldwork)

Le interviste sono documentate nel file:

- **`/evidences/Interviews_Case_Study.pdf`**

Estratti significativi:

> “Gestiamo i laptop tramite un foglio Excel aggiornato manualmente. Non abbiamo un CMDB…”  
> “Non esiste un documento scritto di Incident Response…”  
> “Manca un registro ufficiale dei trattamenti dei dati…”

Queste evidenze sono state utilizzate per assegnare i FAIL nelle categorie ID, PR, DE, RS.

---

### 3.2 Documenti Analizzati

| Documento | Fonte | Esito |
|----------|--------|-------|
| Policy IT generica | IT Department | Incompleta |
| Diagrammi di rete | IT Network Team | Conformi |
| Configurazioni firewall Palo Alto | IT Network Team | Conformi |
| Registro trattamenti dati | Legal/HR | Assente |
| Procedure Incident Response | Security | Assenti |
| Contratti fornitori SaaS | Finance/Legal | Mancano requisiti cyber |

---

### 3.3 Evidenze Tecniche

| Evidenza | Descrizione | Rilievo associato |
|----------|-------------|-------------------|
| Inventario asset in Excel | Inventario non automatizzato | ID.AM-1 (FAIL) |
| Nessun software inventory | Shadow IT non controllato | ID.AM-2 (FAIL) |
| VPN senza MFA | Accesso remoto non sicuro | PR.AC-3 (FAIL) |
| Account Admin condivisi | Assenza PAM | PR.AC-4 (FAIL) |
| Nessun SIEM | Log non correlati | DE.AE-3 (FAIL) |
| Nessun IRP | Incident Response assente | RS.RP-1 (FAIL) |
| Nessun DLP | Data leak non controllati | PR.DS-4 (FAIL) |

---

## 4. Verifiche Tecniche Effettuate

### 4.1 Walkthrough infrastrutturale
- Verifica segmentazione VLAN  
- Verifica configurazioni firewall Palo Alto  
- Verifica criteri password AD  
- Verifica configurazione VPN  
- Verifica backup e DR test  
- Verifica gestione dispositivi endpoint  

### 4.2 Controlli ISO 27001 Annex A

Valutazione completa dei 93 controlli nel documento:

- **`/soa/SoA_Annex_A_Evaluated.pdf`**

Risultato:  
**89 controlli NON CONFORMI**  
**4 controlli CONFORMI**

---

## 5. Correlazione Evidenze → Rilievi

| Evidenza | Rilievo | Categoria |
|----------|---------|-----------|
| Inventario asset manuale | ID.AM-1 | OFI |
| Nessun software inventory | ID.AM-2 | NC |
| VPN senza MFA | PR.AC-3 | NC |
| Account Admin condivisi | PR.AC-4 | NC |
| Nessun SIEM | DE.AE-3 | NC |
| Nessun IRP | RS.RP-1 | NC |
| Nessun DLP | PR.DS-4 | NC |
| Nessun registro trattamenti | ID.GV-3 | NC |

---

## 6. Archivio Evidenze

Tutte le evidenze sono archiviate nella cartella:

```
/evidences
    Interviews_Case_Study.pdf
    Screenshots/
    Logs/
    Configurations/
```

---

## 7. Conclusioni del Trail

L’Audit Trail dimostra che:

- Le evidenze raccolte sono complete e coerenti.  
- I rilievi NIST e ISO sono basati su fatti verificabili.  
- Le interviste sono state condotte con stakeholder chiave.  
- Le verifiche tecniche confermano le non conformità.  
- Il reporting finale (NC/OFI Matrix, Risk Register, Roadmap) può essere costruito in modo affidabile.

---

## 8. Approvazione

Il presente Audit Trail è approvato da:

- Lead Auditor  
- IT Manager  
- Direzione aziendale (se nominata)

---
