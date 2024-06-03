---
title: OoxmlSaveOpzione
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/specification/model/ooxmlsaveoptions/
description: "Aspose.Cells Specifica del modello cloud: OoxmlSaveOptions. Gestisci facilmente Excel e altri fogli di calcolo con funzionalità come apertura, generazione, modifica, divisione, unione, confronto e conversione"
kwords: Excel, Office, Foglio di calcolo, Cloud REST API, OoxmlSaveOptions
weight: 50
---
## **ooxmlSaveOptions**

 Rappresenta le opzioni di salvataggio del file ooxml.

| Nome della proprietà| Tipo di proprietà| Nullabile| Sola lettura| Valore di default| Descrizione|
|:- |:- |:- |:- |:- |:- |
| EsportaNomeCella| Booleano| VERO| Falso|| Indica se esportare il nome della cella nel file Excel2007 .xlsx (.xlsm, .xltx, .xltm). Se è possibile accedere al file di output da SQL Server DTS, questo valore deve essere true. L'impostazione del valore su false aumenterà notevolmente le prestazioni e ridurrà le dimensioni del file durante la creazione di file di grandi dimensioni. Il valore predefinito è falso.|
| AggiornaZoom| Booleano| VERO| Falso|| Indica se aggiornare il fattore di ridimensionamento prima di salvare il file se le proprietà PageSetup.FitToPagesWide e PageSetup.FitToPagesTall controllano il modo in cui viene ridimensionato il foglio di lavoro.|
| AbilitaZip64| Booleano| VERO| Falso||Utilizza sempre le estensioni ZIP64 quando scrivi archivi zip, anche quando non sono necessarie.|
| IncorporaOoxmlAsOleObject| Booleano| VERO| Falso|| Indica se incorporare file Ooxml di OleObject come oggetto ole.|
| Tipo di compressione| Corda| VERO| Falso|| Ottiene e imposta il tipo di compressione per il file ooxml.|
| Salva formato| Corda| VERO| Falso|||
| Cartella file memorizzata nella cache| Corda| VERO| Falso|||
| Cancella i dati| Booleano| VERO| Falso|||
| CreaDirectory| Booleano| VERO| Falso|||
| Abilita compressione HTTP| Booleano| VERO| Falso|||
| AggiornaChartCache| Booleano| VERO| Falso|||
| OrdinaNomi| Booleano| VERO| Falso|||
| ValidateMergedAreas| Booleano| VERO| Falso|||

**Nome del genitore** : [SalvaOpzioni](/specification/model/saveoptions)

