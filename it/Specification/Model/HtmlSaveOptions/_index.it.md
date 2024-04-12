---
title: HtmlSaveOpzione
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/specification/model/htmlsaveoptions/
description: "Aspose.Cells Specifica del modello cloud: HtmlSaveOptions. Gestisci facilmente Excel e altri fogli di calcolo con funzionalità come apertura, generazione, modifica, divisione, unione, confronto e conversione"
weight: 50
---
## **htmlSaveOptions**

 Rappresenta le opzioni di salvataggio del file .html.

| Nome della proprietà| Tipo di proprietà| Nullabile| Sola lettura| Valore di default| Descrizione|
|:- |:- |:- |:- |:- |:- |
| Esporta intestazioni di pagina| Booleano| VERO| Falso|||
| Esporta piè di pagina| Booleano| VERO| Falso|||
| EsportaIntestazioniRigaColonna| Booleano| VERO| Falso|||
| Mostra tutti i fogli| Booleano| VERO| Falso|||
| Opzioni immagine| Classe:ImageOrPrintOptions| VERO| Falso|||
| Salva come file singolo| Booleano| VERO| Falso|| Indica se salvare l'html come file singolo. Il valore predefinito è falso.|
| Esporta foglio di lavoro nascosto| Booleano| VERO| Falso|| Indica se salvare l'html come file singolo. Il valore predefinito è falso.|
| EsportaGridLines| Booleano| VERO| Falso||Indica se esportare la griglia. Il valore predefinito è false.|
| Preferenza presentazione| Booleano| VERO| Falso|| Indica se il file html o mht è la preferenza di presentazione. Il valore predefinito è false. Se desideri ottenere una presentazione più bella, imposta il valore su true.|
| CellCssPrefisso| Corda| VERO| Falso|| Ottiene e imposta il prefisso del nome CSS, il valore predefinito è "".|
| TableCssId| Corda| VERO| Falso|| Ottiene e imposta il prefisso del tipo nome css come tr,col,td e così via, sono contenuti nell'elemento table che ha l'attributo specifico TableCssId. Il valore predefinito è "".|
| IsFullPathLink| Booleano| VERO| Falso|| Indica se si utilizza il collegamento al percorso completo in sheet00x.htm, filelist.xml e tabstrip.htm. Il valore predefinito è falso.|
| Esporta foglio di lavoro CSS separatamente| Booleano| VERO| Falso|| Indica se esportare il foglio di lavoro CSS separatamente. Il valore predefinito è false.|
| Esporta stile bordo simile| Booleano| VERO| Falso|||
| UnisciVuotoTdForzamente| Booleano| VERO| Falso||Indica se unire forzatamente l'elemento TD vuoto durante l'esportazione del file in html. La dimensione del file html verrà ridotta in modo significativo dopo aver impostato il valore su true. Il valore predefinito è falso. Se desideri importare il file html in Excel o esportare linee di griglia perfette quando salvi il file in html, mantieni il valore predefinito.|
| EsportaCoordinataCella| Booleano| VERO| Falso|| Indica se esportare le coordinate Excel delle celle non vuote durante il salvataggio del file in html. Il valore predefinito è falso. Se desideri importare l'HTML di output in Excel, mantieni il valore predefinito.|
| Esporta intestazioni extra| Booleano| VERO| Falso|| Indica se esportare intestazioni aggiuntive quando la lunghezza del testo è maggiore della colonna massima di visualizzazione. Il valore predefinito è falso. Se desideri importare il file html in Excel, mantieni il valore predefinito.|
| Esporta intestazioni| Booleano| VERO| Falso||Indica se esportare le intestazioni durante il salvataggio del file in html. Il valore predefinito è false. Se desideri importare il file html in Excel, mantieni il valore predefinito.|
| EsportaFormula| Booleano| VERO| Falso|| Indica se esportare la formula durante il salvataggio del file in html. Il valore predefinito è vero. Se desideri importare l'HTML di output in Excel, mantieni il valore predefinito|
| Aggiungi testo tooltip| Booleano| VERO| Falso|| Indica se aggiungere testo di descrizione comando quando i dati non possono essere visualizzati completamente.|
| EsportaBogusRowData| Booleano| VERO| Falso|| Indica se si stanno esportando dati fasulli della riga inferiore. Il valore predefinito è true. Se desideri importare il file html o mht in Excel, mantieni il valore predefinito.|
| Escludi stili non utilizzati| Booleano| VERO| Falso|| Indica se escludere gli stili non utilizzati. Il valore predefinito è false. Se desideri importare il file html o mht in Excel, mantieni il valore predefinito.|
| EsportaProprietàDocumento| Booleano| VERO| Falso||Indica se esportare le proprietà del documento. Il valore predefinito è true. Se desideri importare il file html o mht in Excel, mantieni il valore predefinito.|
| EsportaProprietàfogliodilavoro| Booleano| VERO| Falso|| Indica se esportare le proprietà del foglio di lavoro. Il valore predefinito è true. Se desideri importare il file html o mht in Excel, mantieni il valore predefinito.|
| ExportWorkbookProperties| Booleano| VERO| Falso|| Indica se esportare le proprietà della cartella di lavoro. Il valore predefinito è true. Se desideri importare il file html o mht in Excel, mantieni il valore predefinito.|
| ExportFrameScriptsAndProperties| Booleano| VERO| Falso|| Indica se esportare script di frame e proprietà del documento. Il valore predefinito è true. Se desideri importare il file html o mht in Excel, mantieni il valore predefinito.|
| Directory dei file allegati| Corda| VERO| Falso|| La directory in cui verranno salvati i file allegati. Solo per il salvataggio nel flusso html.|
| Prefisso URLFilesallegato| Corda| VERO| Falso||Specificare il prefisso URL dei file allegati come l'immagine nel file html. Solo per il salvataggio nel flusso html.|
| Codifica| Corda| VERO| Falso|||
| Esporta solo foglio di lavoro attivo| Booleano| VERO| Falso|| Indica se esportare l'intera cartella di lavoro in un file html.|
| ExportChartImageFormat| Corda| VERO| Falso|| Ottieni o imposta il formato dell'immagine della carta prima dell'esportazione|
| Esporta immagini come base64| Booleano| VERO| Falso|||
| HiddenColDisplayType| Corda| VERO| Falso|| Colonna nascosta (la larghezza di questa colonna è 0) in Excel, prima di salvarla in formato html, se HtmlHiddenColDisplayType è "Rimuovi", la colonna nascosta non verrebbe emessa, se il valore è "Nascosto", la colonna verrebbe emessa, ma era nascosto, il valore predefinito è "Nascosto"|
| HiddenRowDisplayType| Corda| VERO| Falso||Riga nascosta (l'altezza di questa riga è 0) in Excel, prima di salvarla in formato html, se HtmlHiddenRowDisplayType è "Rimuovi", la riga nascosta non verrebbe emessa, se il valore è "Nascosto", la riga verrebbe emessa, ma era nascosto, il valore predefinito è "Nascosto"|
| HtmlCrossStringType| Corda| VERO| Falso|| Indica se una stringa incrociata verrà visualizzata allo stesso modo di MS Excel quando si salva un file Excel in formato html. Per impostazione predefinita, il valore è Default, quindi, per le stringhe tra celle, c'è poca differenza tra i file html creati da Aspose.Cells e MS Excel. Ma le prestazioni per la creazione di file html di grandi dimensioni, impostando il valore su Cross sarebbero molte volte più veloci rispetto a impostandolo su Predefinito o Fit2Cell.|
| IsExpImageToTempDir| Booleano| VERO| Falso|| Indica se esportare i file di immagine nella directory temporanea. Solo per il salvataggio nel flusso html.|
| Titolo della pagina| Corda| VERO| Falso||Il titolo della pagina html. Solo per il salvataggio nel flusso html.|
| ParseHtmlTagInCell| Booleano| VERO| Falso|| Analizza il tag html nella cella, ad esempio, come valore della cella o come tag html, il valore predefinito è true|
| Salva formato| Corda| VERO| Falso|||
| Cartella file memorizzata nella cache| Corda| VERO| Falso|||
| Cancella i dati| Booleano| VERO| Falso|||
| CreaDirectory| Booleano| VERO| Falso|||
| Abilita compressione HTTP| Booleano| VERO| Falso|||
| AggiornaChartCache| Booleano| VERO| Falso|||
|OrdinaNomi| Booleano| VERO| Falso|||
| ValidateMergedAreas| Booleano| VERO| Falso|||

**Nome del genitore** : (OpzioniSalva)[opzionisalva]