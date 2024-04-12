---
title: PaginatedSaveOption
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/specification/model/paginatedsaveoptions/
description: "Aspose.Cells Specifica del modello cloud: PaginatedSaveOptions. Gestisci facilmente Excel e altri fogli di calcolo con funzionalità come apertura, generazione, modifica, divisione, unione, confronto e conversione"
weight: 50
---
## **paginatedSaveOptions**

 Rappresenta le opzioni per l'impaginazione.

| Nome della proprietà| Tipo di proprietà| Nullabile| Sola lettura| Valore di default| Descrizione|
|:- |:- |:- |:- |:- |:- |
| Carattere predefinito| Corda| VERO| Falso||Quando i caratteri in Excel sono Unicode e non sono impostati con il carattere corretto nello stile cella, potrebbero apparire come blocchi in pdf, immagine. Imposta il carattere predefinito come MingLiu o MS Gothic per mostrare questi caratteri. Se questa proprietà non è impostata, Aspose.Cells utilizzerà il carattere predefinito del sistema per mostrare questi caratteri Unicode.|
| ControllareWorkbookDefaultFont| Booleano| VERO| Falso|| Quando i caratteri in Excel sono Unicode e non sono impostati con il carattere corretto nello stile cella, potrebbero apparire come blocco in pdf,immagine. Impostalo su true per provare a utilizzare il carattere predefinito della cartella di lavoro per mostrare prima questi caratteri.|
| Controlla la compatibilità dei caratteri| Booleano| VERO| Falso|| Indica se verificare la compatibilità dei caratteri per ogni carattere del testo.|
| IsFontSubstitutionCharGranularity| Booleano| VERO| Falso|| Indica se sostituire il carattere del carattere solo quando il carattere della cella non è compatibile con esso.|
| Una pagina per foglio| Booleano| VERO| Falso|| Se OnePagePerSheet è true , tutto il contenuto di un foglio verrà visualizzato in una sola pagina come risultato. Il formato carta di pagesetup non sarà valido e le altre impostazioni di pagesetup avranno comunque effetto.|
| Tutte le colonne in una pagina per foglio| Booleano| VERO| Falso||Se AllColumnsInOnePagePerSheet è true , tutto il contenuto delle colonne di un foglio verrà visualizzato in una sola pagina come risultato. La larghezza del formato carta di pagesetup verrà ignorata e le altre impostazioni di pagesetup avranno comunque effetto.|
| Ignora errore| Booleano| VERO| Falso|| Indica se è necessario nascondere l'errore durante il rendering. L'errore può essere un errore nella forma, nell'immagine, nel rendering del grafico, ecc.|
| OutputPaginaVuotaQuandoNienteDaStampare| Booleano| VERO| Falso|| Indica se stampare una pagina vuota quando non c'è nulla da stampare.|
| IndicePagina| Numero intero| VERO| Falso|| Ottiene o imposta l'indice in base 0 della prima pagina da salvare.|
| Conteggio pagine| Numero intero| VERO| Falso|| Ottiene o imposta il numero di pagine da salvare.|
| PrintingPageType| Corda| VERO| Falso|| Indica quali pagine non verranno stampate.|
| Tipo di griglia| Corda| VERO| Falso|| Ottiene o imposta il tipo di linea della griglia.|
| TextCrossType| Corda| VERO| Falso|| Ottiene o imposta la visualizzazione del tipo di testo quando la larghezza del testo è maggiore della larghezza della cella.|
| Lingua di modifica predefinita| Corda| VERO| Falso|| Ottiene o imposta la lingua di modifica predefinita.|
| EmfRenderSetting| Corda| VERO| Falso|||
| Unisci aree| Booleano| VERO| Falso|||
|Ordina nomi esterni| Booleano| VERO| Falso|||
| AggiornaSmartArt| Booleano| VERO| Falso|||
| Salva formato| Corda| VERO| Falso|||
| Cartella file memorizzata nella cache| Corda| VERO| Falso|||
| Cancella i dati| Booleano| VERO| Falso|||
| CreaDirectory| Booleano| VERO| Falso|||
| Abilita compressione HTTP| Booleano| VERO| Falso|||
| AggiornaChartCache| Booleano| VERO| Falso|||
|OrdinaNomi| Booleano| VERO| Falso|||
| ValidateMergedAreas| Booleano| VERO| Falso|||

**Nome del genitore** : (OpzioniSalva)[opzionisalva]**Nome dei bambini** : 
	-  [DocxSaveOptions](docxsaveoptions) 
	-  [PptxSaveOptions](pptxsaveoptions) 
	-  [XpsSaveOptions](xpssaveoptions) 
