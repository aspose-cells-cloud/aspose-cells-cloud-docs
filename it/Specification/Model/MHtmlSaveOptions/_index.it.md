---
title: MHTMLSaveOpzione
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/specification/model/mhtmlsaveoptions/
description: "Aspose.Cells Specifica del modello cloud: MHTmlSaveOptions. Gestisci facilmente Excel e altri fogli di calcolo con funzionalità come apertura, generazione, modifica, divisione, unione, confronto e conversione"
weight: 50
---
## **mHtmlSaveOptions**

 Rappresenta le opzioni di salvataggio del file .mhtml.

| Nome della proprietà| Tipo di proprietà| Nullabile| Sola lettura| Valore di default| Descrizione|
|:- |:- |:- |:- |:- |:- |
| Directory dei file allegati| Corda| VERO| Falso|| La directory in cui verranno salvati i file allegati. Solo per il salvataggio nel flusso html.|
| Prefisso URLFilesallegato| Corda| VERO| Falso||Specificare il prefisso URL dei file allegati come l'immagine nel file html. Solo per il salvataggio nel flusso html.|
| Codifica| Corda| VERO| Falso|| Se non impostato, utilizza Encoding.UTF8 come tipo di codifica predefinito.|
| Esporta solo foglio di lavoro attivo| Booleano| VERO| Falso|| Indica se esportare l'intera cartella di lavoro in un file html.|
| ExportChartImageFormat| Corda| VERO| Falso|| Ottieni o imposta il formato dell'immagine della carta prima dell'esportazione|
| Esporta immagini come base64| Booleano| VERO| Falso|| Specifica se le immagini vengono salvate in formato Base64 su HTML, MHTML o EPUB.|
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