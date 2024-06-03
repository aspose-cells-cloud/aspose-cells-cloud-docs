---
title: PdfSaveOpzione
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/specification/model/pdfsaveoptions/
description: "Aspose.Cells Specifica del modello cloud: PdfSaveOptions. Gestisci facilmente Excel e altri fogli di calcolo con funzionalità come apertura, generazione, modifica, divisione, unione, confronto e conversione"
kwords: Excel, Office, Foglio di calcolo, Cloud REST API, PdfSaveOptions
weight: 50
---
## **pdfSalvaOpzioni**

 Rappresenta le opzioni di salvataggio del file pdf.

| Nome della proprietà| Tipo di proprietà| Nullabile| Sola lettura| Valore di default| Descrizione|
|:- |:- |:- |:- |:- |:- |
| VisualizzaTitoloDoc| Booleano| VERO| Falso|| Indica se la barra del titolo della finestra deve visualizzare il titolo del documento.|
| ExportDocumentStructure| Booleano| VERO| Falso|| Indica se esportare la struttura del documento.|
| EmfRenderSetting| Corda| VERO| Falso|| Impostazione per il rendering del metafile Emf.|
| EsportazioneProprietàPersonalizzate| Corda| VERO| Falso|| Specifica il modo in cui CustomDocumentPropertyCollection viene esportato nel file PDF.|
| Tipo di ottimizzazione| Corda| VERO| Falso|| Ottiene e imposta il tipo di ottimizzazione PDF.|
| Produttore| Corda| VERO| Falso|| Ottiene e imposta il produttore del documento PDF generato.|
| PdfCompressione| Corda| VERO| Falso|| Indicare l'algoritmo di compressione.|
| Codifica dei caratteri| Corda| VERO| Falso|| Ottiene o imposta la codifica dei caratteri incorporati in pdf.|
| Filigrana|Classe:RenderingWatermark| VERO| Falso|| Ottiene o imposta la filigrana sull'output.|
| CalcolaFormula| Booleano| VERO| Falso|| Indica se calcolare le formule prima di salvare il file PDF. Il valore predefinito è false.|
| Controlla la compatibilità dei caratteri| Booleano| VERO| Falso|| Indica se verificare la compatibilità dei caratteri per ogni carattere nel testo. Il valore predefinito è vero. Disabilitare questa proprietà può fornire prestazioni migliori. Ma quando il carattere predefinito o specificato del testo/carattere non può essere utilizzato per eseguirne il rendering, nel pdf generato potrebbero essere presenti caratteri illeggibili (come il blocco). Per tale situazione l'utente dovrebbe mantenere questa proprietà su true in modo che sia possibile cercare e utilizzare caratteri alternativi per visualizzare il testo;|
| Conformità| Corda| VERO| Falso|| La cartella di lavoro viene convertita in PDF secondo PdfCompliance in questa proprietà.|
| Carattere predefinito| Corda| VERO| Falso||Quando i caratteri in Excel sono Unicode e non sono impostati con il carattere corretto nello stile cella, potrebbero apparire come blocchi in pdf, immagine. Imposta il DefaultFont come MingLiu o MS Gothic per mostrare questi caratteri. Se questa proprietà non è impostata, Aspose.Cells utilizzerà il carattere predefinito del sistema per mostrare questi caratteri Unicode.|
| Una pagina per foglio| Booleano| VERO| Falso|| Se OnePagePerSheet è true , tutto il contenuto di un foglio verrà visualizzato in una sola pagina come risultato. Il formato carta di pagesetup non sarà valido e le altre impostazioni di pagesetup continueranno ad avere effetto.|
| PrintingPageType| Corda| VERO| Falso|| Indica quali pagine non verranno stampate.|
| Opzioni di sicurezza| Classe: PdfSecurityOptions| VERO| Falso|| Imposta queste opzioni quando è necessaria la sicurezza nel risultato xls2pdf.|
| PPI desiderato| Numero intero| VERO| Falso||Imposta il PPI (pixel per pollice) desiderato per le immagini di ricampionamento e la qualità jpeg. Tutte le immagini verranno convertite in JPEG con l'impostazione di qualità specificata e le immagini che sono maggiori del PPI (pixel per pollice) specificato verranno ricampionate. Pixel per pollice desiderati. 220 di alta qualità. 150 qualità dello schermo. 96 qualità della posta elettronica.|
| jpegQualità| Numero intero| VERO| Falso|| Imposta il PPI (pixel per pollice) desiderato per le immagini di ricampionamento e la qualità jpeg. Tutte le immagini verranno convertite in JPEG con l'impostazione di qualità specificata e le immagini che sono maggiori del PPI (pixel per pollice) specificato verranno ricampionate. 0 - 100% JPEG qualità.|
| Tipoimmagine| Corda| VERO| Falso|| Rappresenta il tipo di immagine durante la conversione del grafico e della forma.|
| Salva formato| Corda| VERO| Falso|||
| Cartella file memorizzata nella cache| Corda| VERO| Falso|||
| Cancella i dati| Booleano| VERO| Falso|||
| CreaDirectory| Booleano| VERO| Falso|||
| Abilita compressione HTTP| Booleano| VERO| Falso|||
| AggiornaChartCache| Booleano| VERO| Falso|||
| OrdinaNomi| Booleano| VERO| Falso|||
| ValidateMergedAreas| Booleano| VERO| Falso|||

**Nome del genitore** : [SalvaOpzioni](/specification/model/saveoptions)

