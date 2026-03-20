# Vendibilit-Estesa

# 📊 Vendibilità Estesa – Activities Summary

## 📋 Activities Overview

| #  | Attività | Responsabile | Scadenza | Stato | Note |
|----|----------|--------------|----------|--------|------|
| 1  | Rimozione quota parte | Team | Completato | ✅ Done | Primo fix |
| 2A | Stato Building (positivo) | Antonio / Luca | Fine Marzo | ⏳ In corso | Richiede analisi |
| 2B | Stato Building (negativo - KO tecnico) | Team | Fine Aprile | ⏳ Pending | Serve stringa di identificazione |
| 3  | Modifica calcolo distanza (civico → ROE) | Team | Soon | ⏳ | Update geospaziale |
| 4  | Collegamento RPFS → civico vendibile | Team | TBD | ⏳ | Analisi geospaziale |
| 5  | Spostamento distanza su PTE | Team | Unclear | ⏳ | Quasi pronto |
| 6  | Saturazione | Unknown | TBD | ❓ | Non completamente chiaro |
| 7  | Modifica recupero POP | Team | TBD | ⏳ | Da progettazione o padre |
| 8  | Estesa Facile | Team | Post Giugno | ⏸️ Posticipato | Bassa priorità |
| 9  | Controllo coppia POP-Comune | Nico / Luca | ASAP | 🟡 | Quick win |
| 10 | Controllo coordinate (AEB + CED) | Nico | Soon | 🔴 Complesso | Richiede Spark + analisi |

---

## ⚠️ Critical Technical Issues

- 📈 Aumento degli step dovuto ai filtri → impatto diretto sulle performance  
- 🐢 Esecuzione tramite Hive + UZI → molto lenta (fino a ~1 ora)  
- 🔁 Presenza di duplicati in PNI → necessaria gestione  
- 🔄 Cambio codice indirizzo → milioni di civici risultano "nuovi"  
- 🔀 Workflow non più lineare → difficile da mantenere  

---

## 🧠 Key Insights

- ✅ Possibile utilizzo di una **blacklist** come soluzione temporanea  
- ⚙️ Alcuni processi possono essere eseguiti manualmente (Zeppelin / TML)  
- 📚 Necessità forte di **documentazione completa del processo**  
- ⏸️ Task bloccati da più di un mese → bisogno di prioritizzazione  

---

## 🔥 Recommended Action Plan

### 🚀 Step 1 (Quick Win)
- ✔️ Controllo POP-Comune  

### ⚠️ Step 2
- Analisi iniziale: **Controllo coordinate (AEB + CED)**  

### 📌 Step 3
- Definire:
  - 🧾 Lista task bloccati  
  - 📊 Priorità  

### 🔄 Parallel Track
- 📚 Avviare documentazione del processo  

---

## 🛠️ Notes

- Priorità attuale: migliorare performance e stabilità  
- Evitare aumento complessità senza refactoring  
- Spingere verso pipeline più lineare e mantenibile  


# 🌐 Vendibilità Estesa – Data Pipeline & Processing

## 🧭 High-Level Flow

    ┌────────────┐
    │ STRADARIO  │
    └─────┬──────┘
          │
          ▼
    ┌────────────┐
    │ CIVICI     │
    └─────┬──────┘
          │
  ┌───────┴────────┐
  ▼                ▼



