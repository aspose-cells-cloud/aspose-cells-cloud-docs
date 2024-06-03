---
title: OpzioneSalvaimmagine
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/specification/model/imagesaveoptions/
description: "Aspose.Cells Specifica del modello cloud: ImageSaveOptions. Gestisci facilmente Excel e altri fogli di calcolo con funzionalità come apertura, generazione, modifica, divisione, unione, confronto e conversione"
kwords: Excel, Office, Foglio di calcolo, Cloud REST API, ImageSaveOptions
weight: 50
---
## **imageSaveOptions**

 Rappresenta le opzioni di salvataggio del file immagine.

| Nome della proprietà| Tipo di proprietà| Nullabile| Sola lettura| Valore di default| Descrizione|
|:- |:- |:- |:- |:- |:- |
| ChartImageType| Corda| VERO| Falso|| Indicare il tipo di immagine del grafico durante la conversione.|
| Nomeimmagine incorporataInSvg| Corda| VERO| Falso|| Indicare il nome del file dell'immagine incorporata in formato SVG. Dovrebbe essere il percorso completo con una directory come "c:\\xpsEmbeded"|
| Risoluzione orizzontale| Numero intero| VERO| Falso|| Ottiene o imposta la risoluzione orizzontale per le immagini generate, in punti per pollice. Applica il metodo di generazione delle immagini ad eccezione delle immagini in formato Emf. Il valore predefinito è 96.|
| Formatoimmagine| Corda| VERO| Falso|| Ottiene o imposta il formato delle immagini generate. Non applicare il metodo che restituisce un oggetto Bitmap. Il valore predefinito è ImageFormat.Bmp. Non applicare il metodo che restituisce un oggetto Bitmap.|
| IsCellAutoFit| Booleano| VERO| Falso|| Indica se la larghezza e l'altezza delle celle vengono adattate automaticamente al valore della cella. Il valore predefinito è falso.|
| Una pagina per foglio| Booleano| VERO| Falso||Se OnePagePerSheet è true , tutto il contenuto di un foglio verrà visualizzato in una sola pagina come risultato. Il formato carta di pagesetup non sarà valido e le altre impostazioni di pagesetup continueranno ad avere effetto.|
| OnlyArea| Booleano| VERO| Falso|| Se questa proprietà è true , verrà generata solo l'Area e nessuna scala avrà effetto.|
| Pagina di stampa| Corda| VERO| Falso|| Indica quali pagine non verranno stampate.|
| Finestra di dialogo StampaConStato| Booleano| VERO| Falso|| Se PrintWithStatusDialog = true , verrà visualizzata una finestra di dialogo che mostra lo stato corrente della stampa. altrimenti non verrà visualizzata alcuna finestra di dialogo.|
| Qualità| Numero intero| VERO| Falso|| Ottiene o imposta un valore che determina la qualità delle immagini generate da applicare solo quando si salvano le pagine nel formato Jpeg. Ha effetto solo quando si salva su JPEG. Il valore deve essere compreso tra 0 e 100. Il valore predefinito è 100.|
| TiffCompressione| Corda| VERO| Falso|| Ottiene o imposta il tipo di compressione da applicare solo quando si salvano le pagine nel formato Tiff. Ha effetto solo quando si salva su TIFF. Il valore predefinito è Lzw.|
| Risoluzione verticale| Numero intero| VERO| Falso||Ottiene o imposta la risoluzione verticale per le immagini generate, in punti per pollice. Applica il metodo di generazione dell'immagine ad eccezione dell'immagine in formato Emf. Il valore predefinito è 96.|
| Salva formato| Corda| VERO| Falso|||
| Cartella file memorizzata nella cache| Corda| VERO| Falso|||
| Cancella i dati| Booleano| VERO| Falso|||
| CreaDirectory| Booleano| VERO| Falso|||
| Abilita compressione HTTP| Booleano| VERO| Falso|||
| AggiornaChartCache| Booleano| VERO| Falso|||
| OrdinaNomi| Booleano| VERO| Falso|||
| ValidateMergedAreas| Booleano| VERO| Falso|||

**Nome del genitore** : [SalvaOpzioni](/specification/model/saveoptions)

