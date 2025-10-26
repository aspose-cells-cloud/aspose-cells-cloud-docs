---
title: Opzione Converti cartella di lavoro
second_title: Documen
linktitle: Opzione Converti cartella di lavoro
type: docs
url: /it/convert-workbook-options/
keywords: ConvertWorkbookOptions
description: Aspose.Cells Cloud REST API supporta l'importazione di file Excel in diversi formati. L'SDK supporta diversi linguaggi di sviluppo, tra cui Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e Swift.
weight: 79
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdown, Opzioni di conversione della cartella di lavoro
---
# Proprietà ConvertWorkbookOptions

Nome | Tipo | Descrizione | Note
------------ | ------------- | ------------- | -------------
**Fonte dati** | **Oggetto** Fonte del file di dati: CloudFileSystem, RequestFiles, HttpUri. |
**[FileInfo](/cells/file-info/)** | **Oggetto** | Descrizione delle informazioni sul file. Include nome del file, dimensione del file e contenuto del file (stringa base64). |
**[Impostazione pagina](/cells/page-setup/)** | **Oggetto** | Proprietà di impostazione della pagina. |
**Opzioni di salvataggio** | **Oggetto** | Opzioni di salvataggio: DbfSaveOptions, DifSaveOptions, DocxSaveOptions, HtmlSaveOptions, XlsSaveOptions, XlsxSaveOptions, XpsSaveOptions, PngSaveOptions, JpgSaveOptions, GifSaveOptions, EmfSaveOptions, BmpSaveOptions, MdSaveOptions, NumbersSaveOptions, WmfSaveOptions, SvgSaveOptions, TxtSaveOptions, TifSaveOptions, XlsbSaveOptions |
**ConvertiFormato** | **corda** | Formato del file: csv, xls, html, mhtml, ods, pdf, xml, txt, tiff, xlsb, xlsm, xlsx, xltm, xltx, xps, png, jpg, gif, emf, bmp, md, Numbers, wmf, svg e così via. |
**CheckExcelRestriction** | **booleano** | Ottiene e imposta il tipo di testo con adattamento automatico. |

## **Proprietà fileSource**

| Nome della proprietà| Tipo di proprietà| Nullabile| Sola lettura| Valore predefinito| Descrizione|
|:- |:- |:- |:- |:- |:- |
|Tipo di origine file|Corda|VERO| falso||Una proprietà denominata FileSourceType di tipo FileSourceType a cui è possibile accedere e che può essere modificata. (CloudFileSystem/RequestFiles/HttpUri)|
|Percorso file|Corda|VERO| falso||Percorso della posizione del file.|

## **Proprietà DbfSaveOptions**

| Nome della proprietà| Tipo di proprietà| Nullabile| Sola lettura| Valore predefinito| Descrizione|
|:- |:- |:- |:- |:- |:- |
|Esporta come stringa|Booleano|VERO| falso|||
|SalvaFormato|Corda|VERO| falso|||
|CartellaFileCassata|Corda|VERO| falso|||
|Cancella dati|Booleano|VERO| falso|||
|Crea directory|Booleano|VERO| falso|||
|Abilita compressione HTTP|Booleano|VERO| falso|||
|AggiornaCacheGrafico|Booleano|VERO| falso|||
|OrdinaNomi|Booleano|VERO| falso|||
|ValidateMergedAreas|Booleano|VERO| falso|||
|MergeAreas|Booleano|VERO| falso|||
|OrdinaNomiEsterni|Booleano|VERO| falso|||
|CheckExcelRestriction|Booleano|VERO| falso|||
|AggiornaSmartArt|Booleano|VERO| falso|||
|EncryptDocumentProperties|Booleano|VERO| falso|||

## **Proprietà DifSaveOptions**

| Nome della proprietà| Tipo di proprietà| Nullabile| Sola lettura| Valore predefinito| Descrizione|
|:- |:- |:- |:- |:- |:- |
|SalvaFormato|Corda|VERO| falso|||
|CartellaFileCassata|Corda|VERO| falso|||
|Cancella dati|Booleano|VERO| falso|||
|Crea directory|Booleano|VERO| falso|||
|Abilita compressione HTTP|Booleano|VERO| falso|||
|AggiornaCacheGrafico|Booleano|VERO| falso|||
|OrdinaNomi|Booleano|VERO| falso|||
|ValidateMergedAreas|Booleano|VERO| falso|||
|MergeAreas|Booleano|VERO| falso|||
|OrdinaNomiEsterni|Booleano|VERO| falso|||
|CheckExcelRestriction|Booleano|VERO| falso|||
|AggiornaSmartArt|Booleano|VERO| falso|||
|EncryptDocumentProperties|Booleano|VERO| falso|||

## **Proprietà DocxSaveOptions**

| Nome della proprietà| Tipo di proprietà| Nullabile| Sola lettura| Valore predefinito| Descrizione|
|:- |:- |:- |:- |:- |:- |
|Carattere predefinito|Corda|VERO| falso|||
|Controlla il carattere predefinito della cartella di lavoro|Booleano|VERO| falso|||
|Verifica compatibilità font|Booleano|VERO| falso|||
|IsFontSubstitutionCharGranularity|Booleano|VERO| falso|||
|Una pagina per foglio|Booleano|VERO| falso|||
|Tutte le colonne in una pagina per foglio|Booleano|VERO| falso|||
|IgnoraErrore|Booleano|VERO| falso|||
|OutputBlankPageWhenNothingToPrint|Booleano|VERO| falso|||
|Indice delle pagine|Intero|VERO| falso|||
|Numero di pagine|Intero|VERO| falso|||
|Tipo di pagina di stampa|Corda|VERO| falso|||
|Tipo di griglia|Corda|VERO| falso|||
|TestoCrossType|Corda|VERO| falso|||
|Lingua di modifica predefinita|Corda|VERO| falso|||
|EmfRenderSetting|Corda|VERO| falso|||
|MergeAreas|Booleano|VERO| falso|||
|OrdinaNomiEsterni|Booleano|VERO| falso|||
|AggiornaSmartArt|Booleano|VERO| falso|||
|SalvaFormato|Corda|VERO| falso|||
|CartellaFileCassata|Corda|VERO| falso|||
|Cancella dati|Booleano|VERO| falso|||
|Crea directory|Booleano|VERO| falso|||
|Abilita compressione HTTP|Booleano|VERO| falso|||
|AggiornaCacheGrafico|Booleano|VERO| falso|||
|OrdinaNomi|Booleano|VERO| falso|||
|ValidateMergedAreas|Booleano|VERO| falso|||
|CheckExcelRestriction|Booleano|VERO| falso|||
|EncryptDocumentProperties|Booleano|VERO| falso|||

## **Proprietà HtmlSaveOptions**

| Nome della proprietà| Tipo di proprietà| Nullabile| Sola lettura| Valore predefinito| Descrizione|
|:- |:- |:- |:- |:- |:- |
|Esporta intestazioni di pagina|Booleano|VERO| falso|||
|Esporta piè di pagina|Booleano|VERO| falso|||
|Esporta intestazioni riga colonna|Booleano|VERO| falso|||
|Mostra tutti i fogli|Booleano|VERO| falso|||
|Opzioni immagine|Classe|VERO| falso|||
|Salva come singolo file|Booleano|VERO| falso|||
|EsportaFoglioDiLavoroNascosto|Booleano|VERO| falso|||
|Esportare le linee della griglia|Booleano|VERO| falso|||
|PresentazionePreferenza|Booleano|VERO| falso|||
|PrefissoCellCss|Corda|VERO| falso|||
|TableCssId|Corda|VERO| falso|||
|IsFullPathLink|Booleano|VERO| falso|||
|Esporta foglio di lavoro CSS separatamente|Booleano|VERO| falso|||
|ExportSimilarBorderStyle|Booleano|VERO| falso|||
|MergeEmptyTdForcely|Booleano|VERO| falso|||
|ExportCellCoordinate|Booleano|VERO| falso|||
|Esportazione ExtraTitoli|Booleano|VERO| falso|||
|Esporta intestazioni|Booleano|VERO| falso|||
|ExportFormula|Booleano|VERO| falso|||
|Aggiungi testo suggerimento|Booleano|VERO| falso|||
|ExportBogusRowData|Booleano|VERO| falso|||
|Escludi stili non utilizzati|Booleano|VERO| falso|||
|ExportDocumentProperties|Booleano|VERO| falso|||
|ExportWorksheetProperties|Booleano|VERO| falso|||
|EsportaProprietàCartellaDiLavoro|Booleano|VERO| falso|||
|EsportaFrameScriptsAndProperties|Booleano|VERO| falso|||
|Directory dei file allegati|Corda|VERO| falso|||
|Prefisso URL file allegati|Corda|VERO| falso|||
|Codifica|Corda|VERO| falso|||
|Esporta solo foglio di lavoro attivo|Booleano|VERO| falso|||
|EsportaGraficoImmagineFormato|Corda|VERO| falso|||
|Esporta immagini come Base64|Booleano|VERO| falso|||
|HiddenColDisplayType|Corda|VERO| falso|||
|HiddenRowDisplayType|Corda|VERO| falso|||
|Tipo stringa incrociata HTML|Corda|VERO| falso|||
|IsExpImageToTempDir|Booleano|VERO| falso|||
|Titolo della pagina|Corda|VERO| falso|||
|ParseHtmlTagInCell|Booleano|VERO| falso|||
|AttributoNomeCella|Corda|VERO| falso|||
|SalvaFormato|Corda|VERO| falso|||
|CartellaFileCassata|Corda|VERO| falso|||
|Cancella dati|Booleano|VERO| falso|||
|Crea directory|Booleano|VERO| falso|||
|Abilita compressione HTTP|Booleano|VERO| falso|||
|AggiornaCacheGrafico|Booleano|VERO| falso|||
|OrdinaNomi|Booleano|VERO| falso|||
|ValidateMergedAreas|Booleano|VERO| falso|||
|MergeAreas|Booleano|VERO| falso|||
|OrdinaNomiEsterni|Booleano|VERO| falso|||
|CheckExcelRestriction|Booleano|VERO| falso|||
|AggiornaSmartArt|Booleano|VERO| falso|||
|EncryptDocumentProperties|Booleano|VERO| falso|||

## **Proprietà ImageSaveOptions**

| Nome della proprietà| Tipo di proprietà| Nullabile| Sola lettura| Valore predefinito| Descrizione|
|:- |:- |:- |:- |:- |:- |
|Tipo di immagine del grafico|Corda|VERO| falso|||
|NomeImmagineEmbededInSvg|Corda|VERO| falso|||
|Risoluzione orizzontale|Intero|VERO| falso|||
|Formato immagine|Corda|VERO| falso|||
|IsCellAutoFit|Booleano|VERO| falso|||
|Una pagina per foglio|Booleano|VERO| falso|||
|SoloArea|Booleano|VERO| falso|||
|StampaPagina|Corda|VERO| falso|||
|Stampa con dialogo di stato|Booleano|VERO| falso|||
|Qualità|Intero|VERO| falso|||
|Compressione Tiff|Corda|VERO| falso|||
|Risoluzione verticale|Intero|VERO| falso|||
|SalvaFormato|Corda|VERO| falso|||
|CartellaFileCassata|Corda|VERO| falso|||
|Cancella dati|Booleano|VERO| falso|||
|Crea directory|Booleano|VERO| falso|||
|Abilita compressione HTTP|Booleano|VERO| falso|||
|AggiornaCacheGrafico|Booleano|VERO| falso|||
|OrdinaNomi|Booleano|VERO| falso|||
|ValidateMergedAreas|Booleano|VERO| falso|||
|MergeAreas|Booleano|VERO| falso|||
|OrdinaNomiEsterni|Booleano|VERO| falso|||
|CheckExcelRestriction|Booleano|VERO| falso|||
|AggiornaSmartArt|Booleano|VERO| falso|||
|EncryptDocumentProperties|Booleano|VERO| falso|||

## **Proprietà JsonSaveOptions**

| Nome della proprietà| Tipo di proprietà| Nullabile| Sola lettura| Valore predefinito| Descrizione|
|:- |:- |:- |:- |:- |:- |
|Area di esportazione|Classe|VERO| falso|||
|HaIntestazioneRiga|Booleano|VERO| falso|||
|Esporta come stringa|Booleano|VERO| falso|||
|Rientro|Corda|VERO| falso|||
|SalvaFormato|Corda|VERO| falso|||
|CartellaFileCassata|Corda|VERO| falso|||
|Cancella dati|Booleano|VERO| falso|||
|Crea directory|Booleano|VERO| falso|||
|Abilita compressione HTTP|Booleano|VERO| falso|||
|AggiornaCacheGrafico|Booleano|VERO| falso|||
|OrdinaNomi|Booleano|VERO| falso|||
|ValidateMergedAreas|Booleano|VERO| falso|||
|MergeAreas|Booleano|VERO| falso|||
|OrdinaNomiEsterni|Booleano|VERO| falso|||
|CheckExcelRestriction|Booleano|VERO| falso|||
|AggiornaSmartArt|Booleano|VERO| falso|||
|EncryptDocumentProperties|Booleano|VERO| falso|||

## **Proprietà MarkdownSaveOptions**

| Nome della proprietà| Tipo di proprietà| Nullabile| Sola lettura| Valore predefinito| Descrizione|
|:- |:- |:- |:- |:- |:- |
|Codifica|Corda|VERO| falso|||
|FormatStrategy|Corda|VERO| falso|||
|Separatore di linea|Corda|VERO| falso|||
|SalvaFormato|Corda|VERO| falso|||
|CartellaFileCassata|Corda|VERO| falso|||
|Cancella dati|Booleano|VERO| falso|||
|Crea directory|Booleano|VERO| falso|||
|Abilita compressione HTTP|Booleano|VERO| falso|||
|AggiornaCacheGrafico|Booleano|VERO| falso|||
|OrdinaNomi|Booleano|VERO| falso|||
|ValidateMergedAreas|Booleano|VERO| falso|||
|MergeAreas|Booleano|VERO| falso|||
|OrdinaNomiEsterni|Booleano|VERO| falso|||
|CheckExcelRestriction|Booleano|VERO| falso|||
|AggiornaSmartArt|Booleano|VERO| falso|||
|EncryptDocumentProperties|Booleano|VERO| falso|||

## **Proprietà OoxmlSaveOptions**

| Nome della proprietà| Tipo di proprietà| Nullabile| Sola lettura| Valore predefinito| Descrizione|
|:- |:- |:- |:- |:- |:- |
|ExportCellName|Booleano|VERO| falso|||
|AggiornaZoom|Booleano|VERO| falso|||
|AbilitaZip64|Booleano|VERO| falso|||
|EmbedOoxmlAsOleObject|Booleano|VERO| falso|||
|Tipo di compressione|Corda|VERO| falso|||
|SalvaFormato|Corda|VERO| falso|||
|CartellaFileCassata|Corda|VERO| falso|||
|Cancella dati|Booleano|VERO| falso|||
|Crea directory|Booleano|VERO| falso|||
|Abilita compressione HTTP|Booleano|VERO| falso|||
|AggiornaCacheGrafico|Booleano|VERO| falso|||
|OrdinaNomi|Booleano|VERO| falso|||
|ValidateMergedAreas|Booleano|VERO| falso|||
|MergeAreas|Booleano|VERO| falso|||
|OrdinaNomiEsterni|Booleano|VERO| falso|||
|CheckExcelRestriction|Booleano|VERO| falso|||
|AggiornaSmartArt|Booleano|VERO| falso|||
|EncryptDocumentProperties|Booleano|VERO| falso|||

## **Proprietà PclSaveOptions**

| Nome della proprietà| Tipo di proprietà| Nullabile| Sola lettura| Valore predefinito| Descrizione|
|:- |:- |:- |:- |:- |:- |
|fontFullName|Corda|VERO| falso|||
|fontPclName|Corda|VERO| falso|||
|SalvaFormato|Corda|VERO| falso|||
|CartellaFileCassata|Corda|VERO| falso|||
|Cancella dati|Booleano|VERO| falso|||
|Crea directory|Booleano|VERO| falso|||
|Abilita compressione HTTP|Booleano|VERO| falso|||
|AggiornaCacheGrafico|Booleano|VERO| falso|||
|OrdinaNomi|Booleano|VERO| falso|||
|ValidateMergedAreas|Booleano|VERO| falso|||
|MergeAreas|Booleano|VERO| falso|||
|OrdinaNomiEsterni|Booleano|VERO| falso|||
|CheckExcelRestriction|Booleano|VERO| falso|||
|AggiornaSmartArt|Booleano|VERO| falso|||
|EncryptDocumentProperties|Booleano|VERO| falso|||

## **Proprietà PdfSaveOptions**

| Nome della proprietà| Tipo di proprietà| Nullabile| Sola lettura| Valore predefinito| Descrizione|
|:- |:- |:- |:- |:- |:- |
|Visualizza titolo documento|Booleano|VERO| falso|||
|ExportDocumentStructure|Booleano|VERO| falso|||
|EmfRenderSetting|Corda|VERO| falso|||
|Esportazione proprietà personalizzate|Corda|VERO| falso|||
|Tipo di ottimizzazione|Corda|VERO| falso|||
|Produttore|Corda|VERO| falso|||
|Compressione PDF|Corda|VERO| falso|||
|Codifica dei caratteri|Corda|VERO| falso|||
|Filigrana|Classe|VERO| falso|||
|CalcolaFormula|Booleano|VERO| falso|||
|Verifica compatibilità font|Booleano|VERO| falso|||
|Conformità|Corda|VERO| falso|||
|Carattere predefinito|Corda|VERO| falso|||
|Una pagina per foglio|Booleano|VERO| falso|||
|Tipo di pagina di stampa|Corda|VERO| falso|||
|Opzioni di sicurezza|Classe|VERO| falso|||
|PPI desiderato|Intero|VERO| falso|||
|jpegQuality|Intero|VERO| falso|||
|Tipo di immagine|Corda|VERO| falso|||
|SalvaFormato|Corda|VERO| falso|||
|CartellaFileCassata|Corda|VERO| falso|||
|Cancella dati|Booleano|VERO| falso|||
|Crea directory|Booleano|VERO| falso|||
|Abilita compressione HTTP|Booleano|VERO| falso|||
|AggiornaCacheGrafico|Booleano|VERO| falso|||
|OrdinaNomi|Booleano|VERO| falso|||
|ValidateMergedAreas|Booleano|VERO| falso|||
|MergeAreas|Booleano|VERO| falso|||
|OrdinaNomiEsterni|Booleano|VERO| falso|||
|CheckExcelRestriction|Booleano|VERO| falso|||
|AggiornaSmartArt|Booleano|VERO| falso|||
|EncryptDocumentProperties|Booleano|VERO| falso|||

## **Proprietà PptxSaveOptions**

| Nome della proprietà| Tipo di proprietà| Nullabile| Sola lettura| Valore predefinito| Descrizione|
|:- |:- |:- |:- |:- |:- |
|IgnoraRigheNascoste|Booleano|VERO| falso|||
|Regola dimensione carattere per tipo riga|Corda|VERO| falso|||
|ExportViewType|Corda|VERO| falso|||
|Carattere predefinito|Corda|VERO| falso|||
|Controlla il carattere predefinito della cartella di lavoro|Booleano|VERO| falso|||
|Verifica compatibilità font|Booleano|VERO| falso|||
|IsFontSubstitutionCharGranularity|Booleano|VERO| falso|||
|Una pagina per foglio|Booleano|VERO| falso|||
|Tutte le colonne in una pagina per foglio|Booleano|VERO| falso|||
|IgnoraErrore|Booleano|VERO| falso|||
|OutputBlankPageWhenNothingToPrint|Booleano|VERO| falso|||
|Indice delle pagine|Intero|VERO| falso|||
|Numero di pagine|Intero|VERO| falso|||
|Tipo di pagina di stampa|Corda|VERO| falso|||
|Tipo di griglia|Corda|VERO| falso|||
|TestoCrossType|Corda|VERO| falso|||
|Lingua di modifica predefinita|Corda|VERO| falso|||
|EmfRenderSetting|Corda|VERO| falso|||
|MergeAreas|Booleano|VERO| falso|||
|OrdinaNomiEsterni|Booleano|VERO| falso|||
|AggiornaSmartArt|Booleano|VERO| falso|||
|SalvaFormato|Corda|VERO| falso|||
|CartellaFileCassata|Corda|VERO| falso|||
|Cancella dati|Booleano|VERO| falso|||
|Crea directory|Booleano|VERO| falso|||
|Abilita compressione HTTP|Booleano|VERO| falso|||
|AggiornaCacheGrafico|Booleano|VERO| falso|||
|OrdinaNomi|Booleano|VERO| falso|||
|ValidateMergedAreas|Booleano|VERO| falso|||
|CheckExcelRestriction|Booleano|VERO| falso|||
|EncryptDocumentProperties|Booleano|VERO| falso|||

## **Proprietà SqlScriptSaveOptions**

| Nome della proprietà| Tipo di proprietà| Nullabile| Sola lettura| Valore predefinito| Descrizione|
|:- |:- |:- |:- |:- |:- |
|ControllaSeLaTabellaEsiste|Booleano|VERO| falso|||
|Mappa tipo colonna|Corda|VERO| falso|||
|Controlla tutti i dati per il tipo di colonna|Booleano|VERO| falso|||
|AggiungiRigaVuotaTraRighe|Booleano|VERO| falso|||
|Separatore|Corda|VERO| falso|||
|Tipo di operatore|Corda|VERO| falso|||
|Chiave primaria|Intero|VERO| falso|||
|Crea tabella|Booleano|VERO| falso|||
|Nome ID|Corda|VERO| falso|||
|ID di inizio|Intero|VERO| falso|||
|NomeTabella|Corda|VERO| falso|||
|Esporta come stringa|Booleano|VERO| falso|||
|Area di esportazione|Classe|VERO| falso|||
|HaIntestazioneRiga|Booleano|VERO| falso|||
|SalvaFormato|Corda|VERO| falso|||
|CartellaFileCassata|Corda|VERO| falso|||
|Cancella dati|Booleano|VERO| falso|||
|Crea directory|Booleano|VERO| falso|||
|Abilita compressione HTTP|Booleano|VERO| falso|||
|AggiornaCacheGrafico|Booleano|VERO| falso|||
|OrdinaNomi|Booleano|VERO| falso|||
|ValidateMergedAreas|Booleano|VERO| falso|||
|MergeAreas|Booleano|VERO| falso|||
|OrdinaNomiEsterni|Booleano|VERO| falso|||
|CheckExcelRestriction|Booleano|VERO| falso|||
|AggiornaSmartArt|Booleano|VERO| falso|||
|EncryptDocumentProperties|Booleano|VERO| falso|||

## **Proprietà SvgSaveOptions**

| Nome della proprietà| Tipo di proprietà| Nullabile| Sola lettura| Valore predefinito| Descrizione|
|:- |:- |:- |:- |:- |:- |
|IndiceFoglio|Intero|VERO| falso|||
|Tipo di immagine del grafico|Corda|VERO| falso|||
|NomeImmagineEmbededInSvg|Corda|VERO| falso|||
|Risoluzione orizzontale|Intero|VERO| falso|||
|Formato immagine|Corda|VERO| falso|||
|IsCellAutoFit|Booleano|VERO| falso|||
|Una pagina per foglio|Booleano|VERO| falso|||
|SoloArea|Booleano|VERO| falso|||
|StampaPagina|Corda|VERO| falso|||
|Stampa con dialogo di stato|Booleano|VERO| falso|||
|Qualità|Intero|VERO| falso|||
|Compressione Tiff|Corda|VERO| falso|||
|Risoluzione verticale|Intero|VERO| falso|||
|SalvaFormato|Corda|VERO| falso|||
|CartellaFileCassata|Corda|VERO| falso|||
|Cancella dati|Booleano|VERO| falso|||
|Crea directory|Booleano|VERO| falso|||
|Abilita compressione HTTP|Booleano|VERO| falso|||
|AggiornaCacheGrafico|Booleano|VERO| falso|||
|OrdinaNomi|Booleano|VERO| falso|||
|ValidateMergedAreas|Booleano|VERO| falso|||
|MergeAreas|Booleano|VERO| falso|||
|OrdinaNomiEsterni|Booleano|VERO| falso|||
|CheckExcelRestriction|Booleano|VERO| falso|||
|AggiornaSmartArt|Booleano|VERO| falso|||
|EncryptDocumentProperties|Booleano|VERO| falso|||

## **Proprietà TxtSaveOptions**

| Nome della proprietà| Tipo di proprietà| Nullabile| Sola lettura| Valore predefinito| Descrizione|
|:- |:- |:- |:- |:- |:- |
|Tipo di citazione|Corda|VERO| falso|||
|Separatore|Corda|VERO| falso|||
|SeparatoreStringa|Corda|VERO| falso|||
|Sempre citato|Booleano|VERO| falso|||
|SalvaFormato|Corda|VERO| falso|||
|CartellaFileCassata|Corda|VERO| falso|||
|Cancella dati|Booleano|VERO| falso|||
|Crea directory|Booleano|VERO| falso|||
|Abilita compressione HTTP|Booleano|VERO| falso|||
|AggiornaCacheGrafico|Booleano|VERO| falso|||
|OrdinaNomi|Booleano|VERO| falso|||
|ValidateMergedAreas|Booleano|VERO| falso|||
|MergeAreas|Booleano|VERO| falso|||
|OrdinaNomiEsterni|Booleano|VERO| falso|||
|CheckExcelRestriction|Booleano|VERO| falso|||
|AggiornaSmartArt|Booleano|VERO| falso|||
|EncryptDocumentProperties|Booleano|VERO| falso|||

## **Proprietà XlsSaveOptions&XlsbSaveOptions**

| Nome della proprietà| Tipo di proprietà| Nullabile| Sola lettura| Valore predefinito| Descrizione|
|:- |:- |:- |:- |:- |:- |
|MatchColor|Booleano|VERO| falso|||
|Compatibilità Wps|Booleano|VERO| falso|||
|SalvaFormato|Corda|VERO| falso|||
|CartellaFileCassata|Corda|VERO| falso|||
|Cancella dati|Booleano|VERO| falso|||
|Crea directory|Booleano|VERO| falso|||
|Abilita compressione HTTP|Booleano|VERO| falso|||
|AggiornaCacheGrafico|Booleano|VERO| falso|||
|OrdinaNomi|Booleano|VERO| falso|||
|ValidateMergedAreas|Booleano|VERO| falso|||
|MergeAreas|Booleano|VERO| falso|||
|OrdinaNomiEsterni|Booleano|VERO| falso|||
|CheckExcelRestriction|Booleano|VERO| falso|||
|AggiornaSmartArt|Booleano|VERO| falso|||
|EncryptDocumentProperties|Booleano|VERO| falso|||

## **Proprietà XmlSaveOptions**

| Nome della proprietà| Tipo di proprietà| Nullabile| Sola lettura| Valore predefinito| Descrizione|
|:- |:- |:- |:- |:- |:- |
|Indici dei fogli|Vettore|VERO| falso|||
|Area di esportazione|Classe|VERO| falso|||
|HaIntestazioneRiga|Booleano|VERO| falso|||
|NomeMappaXml|Corda|VERO| falso|||
|NomeFoglioComeNomeElemento|Booleano|VERO| falso|||
|Dati come attributo|Booleano|VERO| falso|||
|SalvaFormato|Corda|VERO| falso|||
|CartellaFileCassata|Corda|VERO| falso|||
|Cancella dati|Booleano|VERO| falso|||
|Crea directory|Booleano|VERO| falso|||
|Abilita compressione HTTP|Booleano|VERO| falso|||
|AggiornaCacheGrafico|Booleano|VERO| falso|||
|OrdinaNomi|Booleano|VERO| falso|||
|ValidateMergedAreas|Booleano|VERO| falso|||
|MergeAreas|Booleano|VERO| falso|||
|OrdinaNomiEsterni|Booleano|VERO| falso|||
|CheckExcelRestriction|Booleano|VERO| falso|||
|AggiornaSmartArt|Booleano|VERO| falso|||
|EncryptDocumentProperties|Booleano|VERO| falso|||

## **Proprietà XpsSaveOptions**

| Nome della proprietà| Tipo di proprietà| Nullabile| Sola lettura| Valore predefinito| Descrizione|
|:- |:- |:- |:- |:- |:- |
|Carattere predefinito|Corda|VERO| falso|||
|Controlla il carattere predefinito della cartella di lavoro|Booleano|VERO| falso|||
|Verifica compatibilità font|Booleano|VERO| falso|||
|IsFontSubstitutionCharGranularity|Booleano|VERO| falso|||
|Una pagina per foglio|Booleano|VERO| falso|||
|Tutte le colonne in una pagina per foglio|Booleano|VERO| falso|||
|IgnoraErrore|Booleano|VERO| falso|||
|OutputBlankPageWhenNothingToPrint|Booleano|VERO| falso|||
|Indice delle pagine|Intero|VERO| falso|||
|Numero di pagine|Intero|VERO| falso|||
|Tipo di pagina di stampa|Corda|VERO| falso|||
|Tipo di griglia|Corda|VERO| falso|||
|TestoCrossType|Corda|VERO| falso|||
|Lingua di modifica predefinita|Corda|VERO| falso|||
|EmfRenderSetting|Corda|VERO| falso|||
|MergeAreas|Booleano|VERO| falso|||
|OrdinaNomiEsterni|Booleano|VERO| falso|||
|AggiornaSmartArt|Booleano|VERO| falso|||
|SalvaFormato|Corda|VERO| falso|||
|CartellaFileCassata|Corda|VERO| falso|||
|Cancella dati|Booleano|VERO| falso|||
|Crea directory|Booleano|VERO| falso|||
|Abilita compressione HTTP|Booleano|VERO| falso|||
|AggiornaCacheGrafico|Booleano|VERO| falso|||
|OrdinaNomi|Booleano|VERO| falso|||
|ValidateMergedAreas|Booleano|VERO| falso|||
|CheckExcelRestriction|Booleano|VERO| falso|||
|EncryptDocumentProperties|Booleano|VERO| falso|||
