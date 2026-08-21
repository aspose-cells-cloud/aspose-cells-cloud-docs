---
---
title: "Guida per sviluppatori di Aspose.Cells Cloud 3.0"
ArticleTitle: "Guida per sviluppatori di Aspose.Cells Cloud 3.0 REST API – Creazione, conversione e formattazione di cartelle di lavoro Excel"
second_title: "Documento"
type: docs
url: /developer-guide-3.0/
aliases: [/developer-guide/v3.0/,/developer-guide-v3.0/]
keywords: "Aspose.Cells Cloud, API REST per Excel, conversione di cartelle di lavoro, API per grafici, importazione dati, esportazione, PDF, CSV, JSON, guida per sviluppatori"
description: "Scopri come utilizzare le API REST di Aspose.Cells Cloud 3.0 per la creazione, la conversione, la formattazione, la gestione di grafici, tabelle e molto altro ancora relative alle cartelle di lavoro Excel. Include esempi di codice e suggerimenti sulle best practice."
weight: 150
---

## Utilizzo delle API REST di Aspose.Cells Cloud

La **Guida per sviluppatori di Aspose.Cells Cloud 3.0** fornisce una panoramica concisa e ricercabile delle operazioni più comuni delle API REST relative alle cartelle di lavoro e ai fogli di lavoro Excel. È rivolta agli sviluppatori che devono creare, modificare, convertire e manipolare file Excel in modo programmatico. Utilizza le sezioni riportate di seguito per individuare l’operazione desiderata; ogni collegamento rimanda a una pagina dettagliata contenente la sintassi della richiesta, i parametri e gli esempi. Questa pagina centrale raccoglie il riferimento alle **API REST di Aspose.Cells Cloud**, rendendo più semplice individuare gli endpoint relativi alle cartelle di lavoro, la gestione dei grafici, le funzioni di importazione ed esportazione dei dati.

**Prerequisiti:** Prima di utilizzare le API, assicurati di avere un account Aspose Cloud valido, una chiave e un segreto API, nonché gli SDK appropriati installati per il tuo ambiente di sviluppo.

### Indice
- [Operazioni sui file](#file-operations)
- [Home (Formattazione celle e gestione righe/columne)](#home-cell-formatting--rowcolumn-management)
- [Inserisci (Grafici, tabelle e oggetti OLE)](#insert-charts-tables--ole-objects)
- [Layout pagina (Interruzioni di pagina e impostazioni)](#page-layout-page-breaks--setup)
- [Formule (Calcolo e nomi)](#formulas-calculate--names)
- [Dati (Raggruppamento, filtri e importazione)](#data-outline-filter--import)
- [Revisione (Commenti e protezione)](#review-comments--protection)
- [Visualizzazione (Finestre e controlli di zoom)](#view-window--zoom-controls)

### Riepilogo rapido delle API

| Gruppo API | Endpoint di esempio | Azione principale |
|-----------|----------------|----------------|
| **Crea cartella di lavoro** | `POST /cells/workbook` | Crea una nuova cartella di lavoro Excel vuota |
| **Converti cartella di lavoro** | `PUT /cells/workbook/convert` | Converte un file Excel in PDF, CSV, JSON, ecc. |
| **Aggiungi grafico** | `POST /cells/worksheets/{sheetName}/charts` | Inserisce un nuovo grafico in un foglio di lavoro |
| **Gestisci tabelle** | `PUT /cells/worksheets/{sheetName}/tables/{tableName}` | Aggiorna o elimina un oggetto elenco (tabella) |
| **Importa dati** | `POST /cells/worksheets/{sheetName}/import` | Importa CSV, JSON, immagini o array in un foglio di lavoro |
| **Calcola formule** | `POST /cells/workbook/calculate` | Ricalcola tutte le formule in una cartella di lavoro |
| **Applica filtri** | `POST /cells/worksheets/{sheetName}/filters` | Aggiunge o rimuove criteri di filtro automatico |
| **Proteggi cartella di lavoro** | `POST /cells/workbook/protect` | Applica la protezione tramite password a una cartella di lavoro |

Queste operazioni ad alta frequenza coprono la funzionalità principale dell’**API REST di Aspose.Cells Cloud per Excel** e conducono direttamente alle pagine di documentazione dettagliate.

Puoi scaricare una versione PDF del riepilogo rapido delle API per il riferimento offline.

{{< tabs tabTotal="8" tabID="1" tabName1="File" tabName2="Home" tabName3="Insert" tabName4="Page Layout" tabName5="Formulas" tabName6="Data" tabName7="Review" tabName8="View" >}}
{{< tab tabNum="1" >}}
<div class="row">
    <div class="col-md-6">
        <p>Cartella di lavoro: Nuova, Converti, Salva con nome</p>
        <ul>
            <li><a href="/cells/create-an-empty-excel-workbook/" title="Crea una cartella di lavoro Excel vuota tramite API" rel="noopener">Crea una cartella di lavoro Excel vuota.</a></li>
            <li><a href="/cells/create-excel-workbook-from-a-template-file/" title="Crea una cartella di lavoro da un file modello" rel="noopener">Crea una cartella di lavoro Excel da un file modello.</a></li>
            <li><a href="/cells/create-excel-workbook-from-a-smartmarker-template/" title="Crea una cartella di lavoro da un modello SmartMarker" rel="noopener">Crea una cartella di lavoro Excel da un modello SmartMarker.</a></li>
            <li><a href="/cells/convert/" title="Converti una cartella di lavoro Excel in un altro formato" rel="noopener">Converti una cartella di lavoro Excel in diversi formati file.</a></li>
            <li><a href="/cells/saveas-other-formats/" title="Salva una cartella di lavoro Excel in un altro formato" rel="noopener">Salva una cartella di lavoro Excel in diversi formati file.</a></li>
        </ul>
        <p>Cerca, Sostituisci</p>
        <ul>
            <li><a href="/cells/search/" title="Cerca testo nei file Excel" rel="noopener">Cerca testo nei file Excel.</a></li>
            <li><a href="/cells/replace/" title="Sostituisci valori nei file Excel" rel="noopener">Sostituisci valori precedenti con nuovi valori nei file Excel.</a></li>
        </ul>
        <p>Comprimi</p>
        <ul>
            <li><a href="/cells/compress/" title="Comprimi file Excel" rel="noopener">Comprimi file Excel.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Cartella di lavoro: Unisci, Dividi</p>
        <ul>
            <li><a href="/cells/merge/" title="Unisci più cartelle di lavoro Excel" rel="noopener">Unisci cartelle di lavoro Excel.</a></li>
            <li><a href="/cells/split/" title="Dividi una cartella di lavoro Excel in file separati" rel="noopener">Dividi cartelle di lavoro Excel.</a></li>
        </ul>
        <p>Acque marce</p>
        <ul>
            <li><a href="/cells/add-background-in-workbook/" title="Aggiungi un'immagine di sfondo a una cartella di lavoro" rel="noopener">Aggiungi uno sfondo a una cartella di lavoro.</a></li>
            <li><a href="/cells/delete-background-in-workbook/" title="Elimina un'immagine di sfondo di una cartella di lavoro" rel="noopener">Elimina lo sfondo da una cartella di lavoro.</a></li>
            <li><a href="/cells/set-background-or-watermark-for-excel-worksheet/" title="Imposta uno sfondo o un'acqua mark su un foglio di lavoro" rel="noopener">Imposta sfondo o acqua mark su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/delete-background-or-watermark-of-excel-worksheet/" title="Elimina lo sfondo o l'acqua mark di un foglio di lavoro" rel="noopener">Elimina sfondo o acqua mark da un foglio di lavoro Excel.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="2" >}}
<div class="row">
    <div class="col-md-6">
        <p>Caratteri, stili, formattazione condizionale e valori delle celle</p>
        <ul>
            <li><a href="/cells/get-cell-style-from-a-worksheet/" title="Recupera uno stile cella da un foglio di lavoro" rel="noopener">Ottieni lo stile cella da un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/update-multiple-cells-style/" title="Aggiorna gli stili di più celle" rel="noopener">Aggiorna lo stile di più celle su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/change-cell-style-in-excel-worksheet/" title="Modifica lo stile di una singola cella" rel="noopener">Aggiorna lo stile cella su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/apply-rich-text-formatting-to-a-cell/" title="Applica formattazione RTF a una cella" rel="noopener">Imposta la formattazione RTF per una cella su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/clear-contents-and-styles-of-cells-in-excel-worksheet/" title="Cancella contenuti e stili delle celle" rel="noopener">Cancella contenuti e stili delle celle su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/working-with-conditional-formatting/" title="Gestisci le regole di formattazione condizionale" rel="noopener">Aggiungi, elimina e aggiorna la formattazione condizionale su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/set-value-of-a-cell-in-a-worksheet/" title="Imposta il valore di una cella" rel="noopener">Imposta il valore di una cella su un foglio di lavoro Excel.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Riga/Colonna: Inserisci, Elimina, Copia, Nascondi e Adatta automaticamente</p>
        <ul>
            <li><a href="/cells/add-an-empty-row-in-a-worksheet/" title="Inserisci una riga vuota in un foglio di lavoro" rel="noopener">Aggiungi una riga vuota su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/delete-row-from-a-worksheet/" title="Elimina una riga da un foglio di lavoro" rel="noopener">Elimina una riga da un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/copy-rows-in-excel-worksheet/" title="Copia righe all'interno di un foglio di lavoro" rel="noopener">Copia righe su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/hide-rows-in-excel-worksheet/" title="Nascondi righe in un foglio di lavoro" rel="noopener">Nascondi righe su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/auto-fit-rows-in-excel-workbooks/" title="Adatta automaticamente le righe in una cartella di lavoro" rel="noopener">Adatta automaticamente le righe su una cartella di lavoro Excel.</a></li>
            <li><a href="/cells/columns/add/" title="Inserisci una colonna vuota in un foglio di lavoro" rel="noopener">Aggiungi una colonna vuota su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/columns/delete/" title="Elimina una colonna da un foglio di lavoro" rel="noopener">Elimina una colonna da un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/columns/copy/" title="Copia colonne all'interno di un foglio di lavoro" rel="noopener">Copia colonne su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/columns/hide/" title="Nascondi colonne in un foglio di lavoro" rel="noopener">Nascondi colonne su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/columns/autofit/" title="Adatta automaticamente le colonne in una cartella di lavoro" rel="noopener">Adatta automaticamente le colonne su una cartella di lavoro Excel.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="3" >}}
<div class="row">
    <div class="col-md-6">
        <p>Grafico</p>
        <ul>
            <li><a href="/cells/add-a-chart-in-a-worksheet/" title="Aggiungi un grafico a un foglio di lavoro" rel="noopener">Aggiungi un grafico su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/delete-a-chart-from-a-worksheet/" title="Elimina un grafico da un foglio di lavoro" rel="noopener">Elimina un grafico su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/delete-all-charts-from-a-worksheet/" title="Elimina tutti i grafici da un foglio di lavoro" rel="noopener">Elimina tutti i grafici su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/convert-chart-to-image/" title="Converti un grafico in un file immagine" rel="noopener">Converti un grafico in un'immagine.</a></li>
            <li><a href="/cells/hide-chart-legend-in-a-worksheet/" title="Nascondi la legenda di un grafico" rel="noopener">Nascondi la legenda del grafico su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/update-chart-title-in-excel-worksheet/" title="Aggiorna il titolo di un grafico" rel="noopener">Aggiorna il titolo del grafico su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/delete-chart-title-in-a-worksheet/" title="Elimina il titolo di un grafico" rel="noopener">Elimina il titolo del grafico in un foglio di lavoro.</a></li>
        </ul>
        <p>Tabella</p>
        <ul>
            <li><a href="/cells/add-a-list-object-or-table-inside-the-worksheet/" title="Aggiungi una tabella (oggetto elenco) a un foglio di lavoro" rel="noopener">Aggiungi un oggetto elenco su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/update-a-list-object-or-table-inside-the-worksheet/" title="Aggiorna una tabella in un foglio di lavoro" rel="noopener">Aggiorna un oggetto elenco su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/convert-list-object-or-table-to-range/" title="Converti una tabella in un intervallo" rel="noopener">Converti un oggetto elenco in un intervallo.</a></li>
            <li><a href="/cells/sort-table-data/" title="Ordina i dati all'interno di una tabella" rel="noopener">Ordina i dati della tabella.</a></li>
        </ul>
        <p>Oggetto OLE</p>
        <ul>
            <li><a href="/cells/add-oleobject-to-excel-worksheet/" title="Aggiungi un oggetto OLE a un foglio di lavoro" rel="noopener">Aggiungi un oggetto OLE su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/update-a-specific-oleobject-from-excel-worksheet/" title="Aggiorna un oggetto OLE specifico" rel="noopener">Aggiorna un oggetto OLE specifico su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/convert-oleobject-to-image/" title="Converti un oggetto OLE in un'immagine" rel="noopener">Converti un oggetto OLE in immagine.</a></li>
            <li><a href="/cells/delete-all-oleobjects-from-excel-worksheet/" title="Elimina tutti gli oggetti OLE da un foglio di lavoro" rel="noopener">Elimina tutti gli oggetti OLE su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/delete-a-specific-oleobject-from-excel-worksheet/" title="Elimina un oggetto OLE specifico" rel="noopener">Elimina un oggetto OLE specifico su un foglio di lavoro Excel.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Forma</p>
        <ul>
            <li><a href="/cells/add-a-shape-inside-the-worksheet/" title="Aggiungi una forma a un foglio di lavoro" rel="noopener">Aggiungi una forma su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/delete-all-shapes-inside-the-worksheet/" title="Elimina tutte le forme da un foglio di lavoro" rel="noopener">Elimina tutte le forme su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/delete-a-shape-by-index-inside-the-worksheet/" title="Elimina una forma per indice" rel="noopener">Elimina una forma per indice su un foglio di lavoro Excel.</a></li>
        </ul>
        <p>Tabella pivot</p>
        <ul>
            <li><a href="/cells/add-a-pivot-table-in-a-worksheet/" title="Aggiungi una tabella pivot a un foglio di lavoro" rel="noopener">Aggiungi una tabella pivot su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/delete-worksheet-pivot-tables/" title="Elimina tutte le tabelle pivot da un foglio di lavoro" rel="noopener">Elimina tutte le tabelle pivot su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/delete-worksheet-pivot-table-by-index/" title="Elimina una tabella pivot per indice" rel="noopener">Elimina una tabella pivot per indice su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/update-cell-style-for-pivot-table/" title="Aggiorna lo stile cella in una tabella pivot" rel="noopener">Aggiorna lo stile cella di una tabella pivot su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/update-style-for-pivot-table/" title="Aggiorna lo stile complessivo di una tabella pivot" rel="noopener">Aggiorna lo stile di una tabella pivot su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/working-with-pivot-filters/" title="Lavora con i filtri della tabella pivot" rel="noopener">Lavora con i filtri della tabella pivot su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/hide-pivot-field-item/" title="Nascondi un elemento di campo della tabella pivot" rel="noopener">Nascondi elementi di campo della tabella pivot su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/move-pivot-table/" title="Sposta una tabella pivot all'interno di un foglio di lavoro" rel="noopener">Sposta una tabella pivot su un foglio di lavoro Excel.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="4" >}}
<div class="row">
    <div class="col-md-6">
        <p>Interruzione di pagina</p>
        <ul>
            <li><a href="/cells/insert-horizontal-page-break-inside-worksheet/" title="Inserisci un'interruzione di pagina orizzontale" rel="noopener">Inserisci un'interruzione di pagina orizzontale su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/insert-vertical-page-break-inside-worksheet/" title="Inserisci un'interruzione di pagina verticale" rel="noopener">Inserisci un'interruzione di pagina verticale su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/delete-horizontal-page-break-inside-worksheet/" title="Elimina un'interruzione di pagina orizzontale" rel="noopener">Elimina un'interruzione di pagina orizzontale su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/delete-vertical-page-break-inside-worksheet/" title="Elimina un'interruzione di pagina verticale" rel="noopener">Elimina un'interruzione di pagina verticale su un foglio di lavoro Excel.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Impostazioni pagina</p>
        <ul>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="5" >}}
<div class="row">
    <div class="col-md-6">
        <p>Calcola</p>
        <ul>
            <li><a href="/cells/calculate-all-formulas-in-a-workbook/" title="Calcola tutte le formule in una cartella di lavoro" rel="noopener">Calcola tutte le formule su una cartella di lavoro Excel.</a></li>
            <li><a href="/cells/calculate-cells-formula/" title="Calcola la formula di una cella specifica" rel="noopener">Calcola le formule delle celle su una cartella di lavoro Excel.</a></li>
            <li><a href="/cells/calculate-formula-in-a-worksheet/" title="Calcola una formula in un foglio di lavoro" rel="noopener">Calcola una formula su un foglio di lavoro Excel.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Nome</p>
        <ul>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="6" >}}
<div class="row">
    <div class="col-md-6">
        <p>Raggruppamento</p>
        <ul>
            <li><a href="/cells/group-rows-in-excel-worksheet/" title="Raggruppa righe in un foglio di lavoro" rel="noopener">Raggruppa righe su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/ungroup-rows-in-excel-worksheet/" title="Separa righe in un foglio di lavoro" rel="noopener">Separa righe su un foglio di lavoro Excel.</a></li>
        </ul>
        <p>Filtro</p>
        <ul>
            <li><a href="/cells/add-a-filter-for-a-filter-column/" title="Aggiungi un filtro a una colonna" rel="noopener">Aggiungi un filtro per una colonna su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/delete-a-filter-for-a-filter-column/" title="Elimina un filtro colonna" rel="noopener">Elimina un filtro per una colonna su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/remove-a-date-filter/" title="Rimuovi un filtro data" rel="noopener">Rimuovi un filtro data su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/add-an-icon-filter/" title="Aggiungi un filtro per icone" rel="noopener">Aggiungi un filtro per icone su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/add-date-filter-in-a-worksheet/" title="Aggiungi un filtro data" rel="noopener">Aggiungi un filtro data su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/filter-data-by-using-an-autofilter/" title="Filtra dati usando il filtro automatico" rel="noopener">Filtra dati usando il filtro automatico su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/filter-the-top-10-items-in-the-list/" title="Filtra i primi 10 elementi" rel="noopener">Filtra i primi 10 elementi dell'elenco su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/match-all-blank-cells-in-the-list/" title="Individua tutte le celle vuote" rel="noopener">Individua tutte le celle vuote nell'elenco su un foglio di lavoro Excel.</a></li>
        </ul>
        <p>Ordina</p>
        <ul>
            <li><a href="/cells/sort-worksheet-data/" title="Ordina i dati del foglio di lavoro" rel="noopener">Ordina i dati su un foglio di lavoro Excel.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Importa dati</p>
        <ul>
            <li><a href="/cells/import/" title="Importa dati nei file Excel" rel="noopener">Importa dati nei file Excel.</a></li>
            <li><a href="/cells/import-CSV-data-into-worksheet/" title="Importa dati CSV in un foglio di lavoro" rel="noopener">Importa dati CSV in un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/import/picture/" title="Importa un'immagine in un foglio di lavoro" rel="noopener">Importa un'immagine in un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/import/double-array/" title="Importa un array di numeri in virgola mobile a doppia precisione in un foglio di lavoro" rel="noopener">Importa un array di numeri in virgola mobile a doppia precisione in un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/import/integer-array/" title="Importa un array di interi in un foglio di lavoro" rel="noopener">Importa un array di interi in un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/import/string-array/" title="Importa un array di stringhe in un foglio di lavoro" rel="noopener">Importa un array di stringhe in un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/import/with-using-storage/" title="Importa dati utilizzando lo storage" rel="noopener">Importa dati in un foglio di lavoro Excel utilizzando lo storage.</a></li>
            <li><a href="/cells/import/without-using-storage/" title="Importa dati senza utilizzare lo storage" rel="noopener">Importa dati in un foglio di lavoro Excel senza utilizzare lo storage.</a></li>
        </ul>
        <p>Assemblaggio</p>
        <ul>
            <li><a href="/cells/assembly/" title="Assembla dati nei file Excel" rel="noopener">Assembla dati nei file Excel.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="7" >}}
<div class="row">
    <div class="col-md-6">
        <p>Commenti</p>
        <ul>
            <li><a href="/cells/add-a-comment-to-a-cell-in-a-worksheet/" title="Aggiungi un commento a una cella" rel="noopener">Aggiungi un commento a una cella su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/update-a-comment-in-excel-workbook/" title="Aggiorna un commento cella" rel="noopener">Aggiorna un commento su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/delete-all-comments-in-a-worksheet/" title="Elimina tutti i commenti in un foglio di lavoro" rel="noopener">Elimina tutti i commenti su un foglio di lavoro Excel.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Modifiche</p>
        <ul>
            <li><a href="/cells/protect-excel-workbooks/" title="Proteggi una cartella di lavoro Excel" rel="noopener">Proteggi una cartella di lavoro Excel.</a></li>
            <li><a href="/cells/unprotect-excel-workbooks/" title="Rimuovi la protezione da una cartella di lavoro Excel" rel="noopener">Rimuovi la protezione da una cartella di lavoro Excel.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="8" >}}
<div class="row">
    <div class="col-md-6">
        <p>Finestre</p>
        <ul>
            <li><a href="/cells/freeze-panes-in-excel-worksheet/" title="Blocca riquadri in un foglio di lavoro" rel="noopener">Blocca riquadri su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/unfreeze-panes-in-excel-worksheet/" title="Sblocca riquadri in un foglio di lavoro" rel="noopener">Sblocca riquadri su un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/hide-excel-worksheets/" title="Nascondi un foglio di lavoro" rel="noopener">Nascondi un foglio di lavoro Excel.</a></li>
            <li><a href="/cells/unhide-excel-worksheets/" title="Mostra un foglio di lavoro nascosto" rel="noopener">Mostra un foglio di lavoro Excel precedentemente nascosto.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Zoom</p>
        <ul>
            <li><a href="/cells/set-zoom-in-excel-worksheet/" title="Imposta lo zoom del foglio di lavoro" rel="noopener">Imposta lo zoom su un foglio di lavoro Excel.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}

{{< /tabs >}}
---