# RootCauseAnalysis


🔹 Struttura del sistema

Il file HTML contiene tutto in uno: questionario, form per compilare i report, lista dei report, Pareto Chart e Risk Matrix.

🔸 1) Costruisci il questionario (Admin)

Vai nella sezione “1) Costruisci il questionario (Admin)”.

Puoi aggiungere:

Input testo → per descrizioni o note libere.

Select → menu a tendina con opzioni definite.

Checkbox → più opzioni selezionabili.

Campo causa (tag) → serve per inserire le cause (usato nella Root Cause Analysis).

Ogni domanda viene salvata in localStorage, così rimane anche dopo il refresh della pagina.

Puoi salvare o eliminare il template.

🔸 2) Compila un incident report

Dopo aver creato il template, clicca su “Avvia report”.

Si apre un modulo con le domande che hai definito.

In fondo c’è la sezione Probabilità (Likelihood) e Impatto (Impact) → valori da 1 a 5.

Quando clicchi “Invia report”:

Il sistema salva le risposte in localStorage.

Calcola il Risk Score = Probabilità × Impatto.

🔸 3) Report inviati

Vedi la tabella con tutti i report già inseriti.

Per ogni report: data, risposte, Risk Score.

Puoi cancellare singoli report o tutti.

Puoi esportare tutto in CSV (Excel/LibreOffice).

🔸 4) Root Cause Analysis (RCA)

Ogni volta che inserisci un campo causa (tag) nei report, questi valori vengono contati.

Il sistema crea un Pareto Chart con:

Barre = frequenza di ogni causa.

Linea = percentuale cumulativa.

Così capisci quali cause incidono di più sugli incidenti.

🔸 5) Risk Matrix

È una matrice 5×5 (Probabilità × Impatto).

Ogni cella mostra quanti report hanno quel livello di rischio.

Le celle cambiano colore in base alla gravità:

Chiaro = pochi eventi

Arancio = medi

Rosso = alti

🔹 Salvataggio dati

Tutto viene salvato in localStorage del browser.
Se vuoi multi-utente o condivisione su rete, bisogna collegarlo a un backend (es. Flask, Firebase, Azure, Node).
