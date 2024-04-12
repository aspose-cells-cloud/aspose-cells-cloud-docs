---
title: SqlScriptSaveOption
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/specification/model/sqlscriptsaveoptions/
description: "Aspose.Cells Specifica del modello cloud: SqlScriptSaveOptions. Gestisci facilmente Excel e altri fogli di calcolo con funzionalità come apertura, generazione, modifica, divisione, unione, confronto e conversione"
weight: 50
---
## **sqlScriptSaveOptions**

Rappresenta le opzioni di salvataggio del file .sql.

| Nome della proprietà| Tipo di proprietà| Nullabile| Sola lettura| Valore di default| Descrizione|
|:- |:- |:- |:- |:- |:- |
| ControllaSeTabellaEsiste| Booleano| VERO| Falso|| Controlla se il nome della tabella esiste prima di crearlo|
| ColumnTypeMap| Corda| VERO| Falso|| Ottiene e imposta la mappa del tipo di colonna per database diversi.|
| CheckAllDataForColumnType| Booleano| VERO| Falso|| Controlla tutti i dati per trovare il tipo di dati delle colonne.|
| Aggiungi riga vuota tra le righe| Booleano| VERO| Falso|| Inserisci una riga vuota tra ciascun dato.|
| Separatore| Corda| VERO| Falso|| Ottiene e imposta il separatore di caratteri dello script SQL.|
| OperatorType| Corda| VERO| Falso|| Ottiene e imposta il tipo di operatore di sql.|
| Chiave primaria| Numero intero| VERO| Falso|| Rappresenta quale colonna è la chiave primaria della tabella dati.|
| Crea tabella| Booleano| VERO| Falso|| Indica se esportare SQL della creazione della tabella.|
| IDNome| Corda| VERO| Falso|| Ottiene e imposta il nome della colonna ID.|
| StartId| Numero intero| VERO| Falso|| Ottiene e imposta l'ID iniziale.|
| NomeTabella| Corda| VERO| Falso|| Ottiene e imposta il nome della tabella.|
|EsportaAsString| Booleano| VERO| Falso|| Indica se esportare tutti i dati come valore stringa.|
| Area di esportazione| Classe:CellArea| VERO| Falso|| Ottiene o imposta l'intervallo di esportazione.|
| HasHeaderRow| Booleano| VERO| Falso|| Indica se l'intervallo contiene una riga di intestazione.|
| Salva formato| Corda| VERO| Falso|||
| Cartella file memorizzata nella cache| Corda| VERO| Falso|||
| Cancella i dati| Booleano| VERO| Falso|||
| CreaDirectory| Booleano| VERO| Falso|||
| Abilita compressione HTTP| Booleano| VERO| Falso|||
| AggiornaChartCache| Booleano| VERO| Falso|||
|OrdinaNomi| Booleano| VERO| Falso|||
| ValidateMergedAreas| Booleano| VERO| Falso|||

**Nome del genitore** : (OpzioniSalva)[opzionisalva]