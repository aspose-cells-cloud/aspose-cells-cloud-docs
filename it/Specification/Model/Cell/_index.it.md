---
title: Cel
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/specification/model/cell/
description: "Aspose.Cells Specifica modello Cloud: Cell. Gestisci facilmente Excel e altri fogli di calcolo con funzionalità come apertura, generazione, modifica, divisione, unione, confronto e conversione"
kwords: Excel, Office, Foglio di calcolo, Cloud REST API, Cellulare
weight: 50
---
## **cellula**

 Incapsula l'oggetto che rappresenta una singola cella della cartella di lavoro.

| Nome della proprietà| Tipo di proprietà| Nullabile| Sola lettura| Valore di default| Descrizione|
|:- |:- |:- |:- |:- |:- |
| Nome| Corda| VERO| Falso|| Ottiene il nome della cella.|
| Riga| Numero intero| VERO| Falso|| Ottiene il numero di riga (in base zero) della cella.|
| Colonna| Numero intero| VERO| Falso|| Ottiene il numero di colonna (in base zero) della cella.|
| Valore| Corda| VERO| Falso|| Ottiene il valore contenuto in questa cella.|
| Tipo| Corda| VERO| Falso|| Rappresenta il tipo di valore della cella.|
| Formula| Corda| VERO| Falso||Ottiene o imposta una formula di .|
| ÈFormula| Booleano| VERO| Falso|| Rappresenta se la cella specificata contiene una formula.|
| È unito| Booleano| VERO| Falso|| Controlla se una cella fa parte di un intervallo unito o meno.|
| IsArrayHeader| Booleano| VERO| Falso|| Indica che la formula della cella è una formula di matrice ed è la prima cella della matrice.|
| IsInArray| Booleano| VERO| Falso|| Indica se la formula della cella è una formula di matrice.|
| IsErrorValue| Booleano| VERO| Falso|| Controlla se il valore di questa cella è un errore.|
| IsInTable| Booleano| VERO| Falso|| Indica se questa cella fa parte della formula della tabella.|
| IsStyleSet| Booleano| VERO| Falso|| Indica se lo stile della cella è impostato. Se restituisce false, significa che questa cella ha un formato di cella predefinito.|
| HtmlString| Corda| VERO| Falso|| Ottiene e imposta la stringa html che contiene dati e alcuni formati in questa cella.|
| Stile| Classe:LinkElement| VERO| Falso|||
| Foglio di lavoro| Corda| VERO| Falso|| Ottiene il foglio di lavoro padre.|
| collegamento| Classe: collegamento| VERO| Falso|||

**Nome del genitore** : [Elemento di collegamento](/specification/model/linkelement)

