# Sintesi automatica di cartelle cliniche con Huggingface

## Contesto aziendale
Un'azienda ospedaliera, che gestisce migliaia di cartelle cliniche digitali, desidera migliorare l’efficienza del proprio staff medico. I medici spesso devono analizzare numerosi ricoveri, anamnesi e referti, operazione che richiede molto tempo. Per ottimizzare questa attività, l’azienda vuole implementare un sistema automatizzato che generi un riassunto delle informazioni rilevanti per ogni paziente.

## Obiettivi del progetto
Lo studente dovrà sviluppare uno script Python che:
1. **Legga un file JSON contenente le cartelle cliniche**.
2. **Utilizzi i modelli di Huggingface per generare una sintesi automatica** delle informazioni principali, come diagnosi, anamnesi, prognosi e risultati degli esami.
3. **Produca un file di output contenente le sintesi generate per ogni paziente**.

---

## Specifiche tecniche

### Input
- **File JSON di input**: Contiene 10 cartelle cliniche simulate, dove ogni paziente ha una lista di ricoveri con informazioni quali diagnosi, anamnesi, prognosi, date di ricovero e dimissione, medicinali somministrati e referti. Il file è disponibile a questo link: [https://raw.githubusercontent.com/Profession-AI/progetti-deeplearning/refs/heads/main/Sintesi%20automatica%20di%20cartelle%20cliniche%20di%20un%E2%80%99azienda%20ospedaliera/hospital_records.json](https://raw.githubusercontent.com/Profession-AI/progetti-deeplearning/refs/heads/main/Sintesi%20automatica%20di%20cartelle%20cliniche%20di%20un%E2%80%99azienda%20ospedaliera/hospital_records.json)

### Output
- **File di output**: Riassume per ciascun paziente le informazioni cliniche essenziali in un paragrafo leggibile.

---

## Requisiti tecnici

1. **Librerie necessarie**:
   - `transformers` (Huggingface)
   - `json`
   - `torch` (se richiesto dal modello Huggingface scelto)
   
2. **Modello NLP**:
   - Utilizzare un modello pre-addestrato di Huggingface per la generazione di riassunti. Ad esempio: 
     - `facebook/bart-large-cnn`
     - `t5-small`

3. **Flusso del progetto**:
   - Caricamento del file JSON con le cartelle cliniche.
   - Iterazione sulle cartelle cliniche per generare un testo concatenato che comprenda le informazioni più importanti (ad esempio: diagnosi, anamnesi, prognosi e referti).
   - Utilizzo del modello Huggingface per generare il riassunto.
   - Scrittura del file JSON di output.


## Benefici aziendali
- **Riduzione del carico di lavoro dei medici**: Il sistema fornisce sintesi rapide e precise delle cartelle cliniche, permettendo ai medici di prendere decisioni più velocemente.
- **Efficienza operativa**: La standardizzazione dei riassunti aiuta a mantenere una comunicazione chiara e consistente tra i vari reparti.
- **Automazione**: Sostituisce processi manuali lunghi e soggetti a errori.

