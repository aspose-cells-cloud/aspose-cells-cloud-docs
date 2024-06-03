---
title: Descrizione della tabella analizzata
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/specification/model/analyzedtabledescription/
description: "Aspose.Cells Specifica del modello cloud: AnalizzatoTableDescription. Gestisci facilmente Excel e altri fogli di calcolo con funzionalità come apertura, generazione, modifica, divisione, unione, confronto e conversione"
kwords: Excel, Office, Foglio di calcolo, Cloud REST API, Descrizione tabella analizzata
weight: 50
---
## **DescrizioneTabella analizzata**

 Rappresenta la descrizione della tabella analizzata.

| Nome della proprietà| Tipo di proprietà| Nullabile| Sola lettura| Valore di default| Descrizione|
|:- |:- |:- |:- |:- |:- |
| Nome| Corda| VERO| Falso|| Rappresenta il nome della tabella.|
| NomeFoglio| Corda| VERO| Falso|| Rappresenta il nome del foglio di lavoro in cui si trova la tabella.|
| Colonne| Contenitore| VERO| Falso|| Rappresenta la descrizione analizzata sulle colonne della tabella.|
| DataColonne| Contenitore| VERO| Falso|| Rappresenta l'elenco delle colonne della data.|
| NumeroColonne| Contenitore| VERO| Falso|| Rappresenta l'elenco delle colonne numeriche.|
| Colonne di testo| Contenitore| VERO| Falso|| Rappresenta l'elenco delle colonne di stringhe.|
| Colonne d'eccezione| Contenitore| VERO| Falso|| Rappresenta l'elenco delle colonne delle eccezioni.|
| HasTableHeaderRow| Booleano| VERO| Falso|| Indica che nella tabella è presente un'intestazione di tabella.|
| HasTableTotalRow| Booleano| VERO| Falso|| Rappresenta la presenza di una riga totale nella tabella.|
| StartDataColumnIndex| Numero intero| VERO| Falso|| Rappresenta l'indice della colonna come colonna dei dati iniziali.|
| EndDataColumnIndex| Numero intero| VERO| Falso|| Rappresenta l'indice della colonna come colonna di dati finale.|
| StartDataRowIndex| Numero intero| VERO| Falso|| Rappresenta l'indice della riga come riga di dati iniziale.|
| EndDataRowIndex| Numero intero| VERO| Falso|| Rappresenta l'indice della riga come riga di dati finale.|
|Miniatura| Corda| VERO| Falso|| Rappresenta la miniatura della tabella. Base64String|
| ScopriGrafici| Contenitore| VERO| Falso|| Rappresenta una raccolta di grafici, ovvero una raccolta di grafici creata in base all'analisi dei dati di una tabella.|
| Scopri tabelle pivot| Contenitore| VERO| Falso|| Rappresenta una raccolta di tabelle pivot, ovvero una raccolta di tabelle pivot create in base all'analisi dei dati di una tabella.|

