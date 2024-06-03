---
title: DataBa
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/specification/model/databar/
description: "Aspose.Cells Specifica del modello cloud: DataBar. Gestisci facilmente Excel e altri fogli di calcolo con funzionalità come apertura, generazione, modifica, divisione, unione, confronto e conversione"
kwords: Excel, Office, Foglio di calcolo, Cloud REST API, DataBar
weight: 50
---
## **dataBar**

 Descrivere la regola di formattazione condizionale DataBar. Questa regola di formattazione condizionale visualizza una barra dati graduata nell'intervallo di celle.

| Nome della proprietà| Tipo di proprietà| Nullabile| Sola lettura| Valore di default| Descrizione|
|:- |:- |:- |:- |:- |:- |
| Colore asse| Classe: colore| VERO| Falso|| Ottiene il colore dell'asse per le celle con formattazione condizionale come barre dei dati.|
| Posizione dell'asse| Corda| VERO| Falso|| Ottiene o imposta la posizione dell'asse delle barre dei dati specificata da una regola di formattazione condizionale.|
| BarBorder| Classe:DataBarBorder| VERO| Falso|| Ottiene un oggetto che specifica il bordo di una barra dei dati.|
| BarFillType| Corda| VERO| Falso|| Ottiene o imposta il modo in cui una barra dati viene riempita di colore.|
| Colore| Classe: colore| VERO| Falso|| Ottieni o imposta il colore di questa DataBar.|
| Direzione| Corda| VERO| Falso||Ottiene o imposta la direzione in cui viene visualizzata la barra dei dati.|
| MaxCfvo| Classe: ConditionalFormattingValue| VERO| Falso|| Ottieni o imposta l'oggetto valore massimo di questo DataBar. Impossibile impostare null o CFValueObject con il tipo FormatConditionValueType.Min.|
| Lunghezza massima| Numero intero| VERO| Falso|| Rappresenta la lunghezza massima della barra dati.|
| MinCfvo| Classe: ConditionalFormattingValue| VERO| Falso|| Ottieni o imposta l'oggetto valore minimo di questo DataBar. Impossibile impostare null o CFValueObject con il tipo FormatConditionValueType.Max.|
| Lunghezza minima| Numero intero| VERO| Falso|| Rappresenta la lunghezza minima della barra dati.|
| NegativeBarFormat| Classe: NegativeBarFormat| VERO| Falso|| Ottiene l'oggetto NegativeBarFormat associato a una regola di formattazione condizionale della barra dati.|
| Mostra valore| Booleano| VERO| Falso|| Ottieni o imposta il flag che indica se mostrare i valori delle celle su cui è applicata questa barra dati. Il valore predefinito è vero.|

