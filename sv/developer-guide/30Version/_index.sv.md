---
title: "Aspose.Cells Cloud 3.0 Utvecklarguide"
ArticleTitle: "Aspose.Cells Cloud 3.0 REST API Utvecklarguide – Skapa, konvertera och formatera Excel-arbetsböcker"
second_title: "Dokument"
type: docs
url: /developer-guide-3.0/
aliases: [/developer-guide/v3.0/, /developer-guide-v3.0/]
keywords: "Aspose.Cells Cloud, Excel REST API, konvertering av arbetsbok, diagram-API, dataimport, export, PDF, CSV, JSON, utvecklarguide"
description: "Lär dig hur du använder Aspose.Cells Cloud 3.0 REST API:er för att skapa, konvertera, formatera, arbeta med diagram, tabeller och mer i Excel. Innehåller kodexempel och bästa praxis-tips."
weight: 150
---

## Arbeta med Aspose.Cells Cloud REST API:er

**Aspose.Cells Cloud 3.0 Utvecklarguide** ger en koncis, sökbar översikt över de mest använda REST API-åtgärderna för Excel-arbetsböcker och -ark. Den är riktad till utvecklare som behöver skapa, redigera, konvertera och manipulera Excel-filer programmatiskt. Använd avsnitten nedan för att hitta den åtgärd du behöver; varje länk leder till en detaljerad sida med begärsyntax, parametrar och exempel. Denna hubbsida sammanställer referensen till **Aspose.Cells Cloud REST API**, vilket gör det lättare att hitta arbetsboksspecifika slutpunkter, hantering av diagram, dataimport- och exportfunktioner.

**Förutsättningar:** Innan du använder API:erna, se till att du har ett giltigt Aspose Cloud-konto, en API-nyckel och hemlighet, samt de lämpliga SDK:er som är installerade för din utvecklingsmiljö.

### Innehållsförteckning

- [Filåtgärder](#file-operations)
- [Hem (Cellformatering & rad/kolumnhantering)](#home-cell-formatting--rowcolumn-management)
- [Infoga (Diagram, tabeller & OLE-objekt)](#insert-charts-tables--ole-objects)
- [Sidlayout (Sidbrytningar & inställningar)](#page-layout-page-breaks--setup)
- [Formler (Beräkna & namn)](#formulas-calculate--names)
- [Data (Grodning, filter & import)](#data-outline-filter--import)
- [Granska (Kommentarer & skydd)](#review-comments--protection)
- [Visa (Fönster & zoomstyrning)](#view-window--zoom-controls)

### Snabb API-sammanfattning

| API-grupp                | Exempel på slutpunkt                                   | Primär åtgärd                                                |
| ------------------------ | ------------------------------------------------------ | ------------------------------------------------------------ |
| **Skapa arbetsbok**      | `POST /cells/workbook`                                 | Skapa en ny tom Excel-arbetsbok                              |
| **Konvertera arbetsbok** | `PUT /cells/workbook/convert`                          | Konvertera en Excel-fil till PDF, CSV, JSON etc.             |
| **Lägg till diagram**    | `POST /cells/worksheets/{sheetName}/charts`            | Infoga ett nytt diagram i ett kalkylark                      |
| **Hantera tabeller**     | `PUT /cells/worksheets/{sheetName}/tables/{tableName}` | Uppdatera eller ta bort ett listobjekt (tabell)              |
| **Importera data**       | `POST /cells/worksheets/{sheetName}/import`            | Importera CSV, JSON, bilder eller arrayer till ett kalkylark |
| **Beräkna formler**      | `POST /cells/workbook/calculate`                       | Omberäkna alla formler i en arbetsbok                        |
| **Tillämpa filter**      | `POST /cells/worksheets/{sheetName}/filters`           | Lägg till eller ta bort AutoFilter-kriterier                 |
| **Säkerställ arbetsbok** | `POST /cells/workbook/protect`                         | Tillämpa lösenordsskydd på en arbetsbok                      |

Dessa högt frekvent använda åtgärder täcker kärnfunktionerna i **Aspose.Cells Cloud Excel REST API** och länkar direkt till detaljerad dokumentation.

Du kan ladda ner en PDF-version av tabellen Snabb API-sammanfattning för offlineanvändning.

{{< tabs tabTotal="8" tabID="1" tabName1="Fil" tabName2="Hem" tabName3="Infoga" tabName4="Sidlayout" tabName5="Formler" tabName6="Data" tabName7="Granska" tabName8="Visa" >}}
{{< tab tabNum="1" >}}

<div class="row">
    <div class="col-md-6">
        <p>Arbetsbok: Ny, konvertera, Spara som</p>
        <ul>
            <li><a href="/cells/create-an-empty-excel-workbook/" title="Skapa en tom Excel-arbetsbok via API" rel="noopener">Skapa en tom Excel-arbetsbok.</a></li>
            <li><a href="/cells/create-excel-workbook-from-a-template-file/" title="Skapa en arbetsbok från en mallfil" rel="noopener">Skapa en Excel-arbetsbok från en mallfil.</a></li>
            <li><a href="/cells/create-excel-workbook-from-a-smartmarker-template/" title="Skapa en arbetsbok från en SmartMarker-mall" rel="noopener">Skapa en Excel-arbetsbok från en SmartMarker-mall.</a></li>
            <li><a href="/cells/convert/" title="Konvertera en Excel-arbetsbok till ett annat format" rel="noopener">Konvertera en Excel-arbetsbok till olika filformat.</a></li>
            <li><a href="/cells/saveas-other-formats/" title="Spara en Excel-arbetsbok i ett annat format" rel="noopener">Spara en Excel-arbetsbok i olika filformat.</a></li>
        </ul>
        <p>Sök, Ersätt</p>
        <ul>
            <li><a href="/cells/search/" title="Sök text i Excel-filer" rel="noopener">Sök text i Excel-filer.</a></li>
            <li><a href="/cells/replace/" title="Ersätt värden i Excel-filer" rel="noopener">Ersätt gamla värden med nya i Excel-filer.</a></li>
        </ul>
        <p>Komprimera</p>
        <ul>
            <li><a href="/cells/compress/" title="Komprimera Excel-filer" rel="noopener">Komprimera Excel-filer.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Arbetsbok: Sammanfoga, dela</p>
        <ul>
            <li><a href="/cells/merge/" title="Sammanfoga flera Excel-arbetsböcker" rel="noopener">Sammanfoga Excel-arbetsböcker.</a></li>
            <li><a href="/cells/split/" title="Dela en Excel-arbetsbok i separata filer" rel="noopener">Dela Excel-arbetsböcker.</a></li>
        </ul>
        <p>Vattenstämplar</p>
        <ul>
            <li><a href="/cells/add-background-in-workbook/" title="Lägg till en bakgrundsbild i en arbetsbok" rel="noopener">Lägg till bakgrund i en arbetsbok.</a></li>
            <li><a href="/cells/delete-background-in-workbook/" title="Ta bort en arbetsboks bakgrundsbild" rel="noopener">Ta bort bakgrund från en arbetsbok.</a></li>
            <li><a href="/cells/set-background-or-watermark-for-excel-worksheet/" title="Ställ in bakgrund eller vattenstämpel på ett kalkylark" rel="noopener">Ställ in bakgrund eller vattenstämpel på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/delete-background-or-watermark-of-excel-worksheet/" title="Ta bort ett kalkylarks bakgrund eller vattenstämpel" rel="noopener">Ta bort bakgrund eller vattenstämpel från ett Excel-kalkylark.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="2" >}}
<div class="row">
    <div class="col-md-6">
        <p>Cellteckensnitt, stilar, villkorlig formatering och värden</p>
        <ul>
            <li><a href="/cells/get-cell-style-from-a-worksheet/" title="Hämta en cellstil från ett kalkylark" rel="noopener">Hämta cellstil från ett Excel-kalkylark.</a></li>
            <li><a href="/cells/update-multiple-cells-style/" title="Uppdatera stilar för flera celler" rel="noopener">Uppdatera flera cellers stil på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/change-cell-style-in-excel-worksheet/" title="Ändra en cells stil" rel="noopener">Uppdatera cellstil på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/apply-rich-text-formatting-to-a-cell/" title="Tillämpa riktextformatering på en cell" rel="noopener">Ställ in riktextformatering för en cell på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/clear-contents-and-styles-of-cells-in-excel-worksheet/" title="Rensa cellinnehåll och stilar" rel="noopener">Rensa innehåll och stilar för celler på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/working-with-conditional-formatting/" title="Hantera villkorsformateringsregler" rel="noopener">Lägg till, ta bort och uppdatera villkorlig formatering på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/set-value-of-a-cell-in-a-worksheet/" title="Ställ in en cells värde" rel="noopener">Ställ in värdet på en cell på ett Excel-kalkylark.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Rad/kolumn: Infoga, ta bort, kopiera, dölja och autoanpassa</p>
        <ul>
            <li><a href="/cells/add-an-empty-row-in-a-worksheet/" title="Infoga en tom rad i ett kalkylark" rel="noopener">Lägg till en tom rad på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/delete-row-from-a-worksheet/" title="Ta bort en rad från ett kalkylark" rel="noopener">Ta bort en rad från ett Excel-kalkylark.</a></li>
            <li><a href="/cells/copy-rows-in-excel-worksheet/" title="Kopiera rader inom ett kalkylark" rel="noopener">Kopiera rader på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/hide-rows-in-excel-worksheet/" title="Dölja rader i ett kalkylark" rel="noopener">Dölj rader på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/auto-fit-rows-in-excel-workbooks/" title="Autoanpassa rader i en arbetsbok" rel="noopener">Autoanpassa rader på en Excel-arbetsbok.</a></li>
            <li><a href="/cells/columns/add/" title="Infoga en tom kolumn i ett kalkylark" rel="noopener">Lägg till en tom kolumn på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/columns/delete/" title="Ta bort en kolumn från ett kalkylark" rel="noopener">Ta bort en kolumn från ett Excel-kalkylark.</a></li>
            <li><a href="/cells/columns/copy/" title="Kopiera kolumner inom ett kalkylark" rel="noopener">Kopiera kolumner på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/columns/hide/" title="Dölja kolumner i ett kalkylark" rel="noopener">Dölj kolumner på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/columns/autofit/" title="Autoanpassa kolumner i en arbetsbok" rel="noopener">Autoanpassa kolumner på en Excel-arbetsbok.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="3" >}}
<div class="row">
    <div class="col-md-6">
        <p>Diagram</p>
        <ul>
            <li><a href="/cells/add-a-chart-in-a-worksheet/" title="Lägg till ett diagram i ett kalkylark" rel="noopener">Lägg till ett diagram på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/delete-a-chart-from-a-worksheet/" title="Ta bort ett diagram från ett kalkylark" rel="noopener">Ta bort ett diagram på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/delete-all-charts-from-a-worksheet/" title="Ta bort alla diagram från ett kalkylark" rel="noopener">Ta bort alla diagram på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/convert-chart-to-image/" title="Konvertera ett diagram till en bildfil" rel="noopener">Konvertera ett diagram till en bild.</a></li>
            <li><a href="/cells/hide-chart-legend-in-a-worksheet/" title="Dölj ett diagram-legend" rel="noopener">Dölj diagramlegend på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/update-chart-title-in-excel-worksheet/" title="Uppdatera ett diagramtitel" rel="noopener">Uppdatera diagramtitel på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/delete-chart-title-in-a-worksheet/" title="Ta bort ett diagramtitel" rel="noopener">Ta bort diagramtitel i ett kalkylark.</a></li>
        </ul>
        <p>Tabell</p>
        <ul>
            <li><a href="/cells/add-a-list-object-or-table-inside-the-worksheet/" title="Lägg till en tabell (listobjekt) i ett kalkylark" rel="noopener">Lägg till ett listobjekt på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/update-a-list-object-or-table-inside-the-worksheet/" title="Uppdatera en tabell i ett kalkylark" rel="noopener">Uppdatera ett listobjekt på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/convert-list-object-or-table-to-range/" title="Konvertera en tabell till ett intervall" rel="noopener">Konvertera ett listobjekt till ett intervall.</a></li>
            <li><a href="/cells/sort-table-data/" title="Sortera data inom en tabell" rel="noopener">Sortera tabelldata.</a></li>
        </ul>
        <p>OLE-objekt</p>
        <ul>
            <li><a href="/cells/add-oleobject-to-excel-worksheet/" title="Lägg till ett OLE-objekt i ett kalkylark" rel="noopener">Lägg till OLE-objekt på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/update-a-specific-oleobject-from-excel-worksheet/" title="Uppdatera ett specifikt OLE-objekt" rel="noopener">Uppdatera ett specifikt OLE-objekt på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/convert-oleobject-to-image/" title="Konvertera ett OLE-objekt till en bild" rel="noopener">Konvertera OLE-objekt till bild.</a></li>
            <li><a href="/cells/delete-all-oleobjects-from-excel-worksheet/" title="Ta bort alla OLE-objekt från ett kalkylark" rel="noopener">Ta bort alla OLE-objekt på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/delete-a-specific-oleobject-from-excel-worksheet/" title="Ta bort ett specifikt OLE-objekt" rel="noopener">Ta bort ett specifikt OLE-objekt på ett Excel-kalkylark.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Form</p>
        <ul>
            <li><a href="/cells/add-a-shape-inside-the-worksheet/" title="Lägg till en form i ett kalkylark" rel="noopener">Lägg till en form på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/delete-all-shapes-inside-the-worksheet/" title="Ta bort alla former från ett kalkylark" rel="noopener">Ta bort alla former på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/delete-a-shape-by-index-inside-the-worksheet/" title="Ta bort en form efter dess index" rel="noopener">Ta bort en form efter index på ett Excel-kalkylark.</a></li>
        </ul>
        <p>Pivotdiagram</p>
        <ul>
            <li><a href="/cells/add-a-pivot-table-in-a-worksheet/" title="Lägg till ett pivotdiagram i ett kalkylark" rel="noopener">Lägg till ett pivotdiagram på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/delete-worksheet-pivot-tables/" title="Ta bort alla pivotdiagram från ett kalkylark" rel="noopener">Ta bort alla pivotdiagram på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/delete-worksheet-pivot-table-by-index/" title="Ta bort ett pivotdiagram efter dess index" rel="noopener">Ta bort ett pivotdiagram efter index på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/update-cell-style-for-pivot-table/" title="Uppdatera cellstil i ett pivotdiagram" rel="noopener">Uppdatera cellstil i ett pivotdiagram på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/update-style-for-pivot-table/" title="Uppdatera hela pivotdiagrammets stil" rel="noopener">Uppdatera stil i ett pivotdiagram på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/working-with-pivot-filters/" title="Arbeta med pivotfilter" rel="noopener">Arbeta med pivotfilter på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/hide-pivot-field-item/" title="Dölj ett pivotfältobjekt" rel="noopener">Dölj pivotfältobjekt på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/move-pivot-table/" title="Flytta ett pivotdiagram inom ett kalkylark" rel="noopener">Flytta ett pivotdiagram på ett Excel-kalkylark.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="4" >}}
<div class="row">
    <div class="col-md-6">
        <p>Sidbrytning</p>
        <ul>
            <li><a href="/cells/insert-horizontal-page-break-inside-worksheet/" title="Infoga en horisontell sidbrytning" rel="noopener">Infoga en horisontell sidbrytning på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/insert-vertical-page-break-inside-worksheet/" title="Infoga en vertikal sidbrytning" rel="noopener">Infoga en vertikal sidbrytning på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/delete-horizontal-page-break-inside-worksheet/" title="Ta bort en horisontell sidbrytning" rel="noopener">Ta bort en horisontell sidbrytning på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/delete-vertical-page-break-inside-worksheet/" title="Ta bort en vertikal sidbrytning" rel="noopener">Ta bort en vertikal sidbrytning på ett Excel-kalkylark.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p> Sidinställning</p>
        <ul>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="5" >}}
<div class="row">
    <div class="col-md-6">
        <p>Beräkna</p>
        <ul>
            <li><a href="/cells/calculate-all-formulas-in-a-workbook/" title="Beräkna alla formler i en arbetsbok" rel="noopener">Beräkna alla formler på en Excel-arbetsbok.</a></li>
            <li><a href="/cells/calculate-cells-formula/" title="Beräkna en specifik cells formel" rel="noopener">Beräkna cellformler på en Excel-arbetsbok.</a></li>
            <li><a href="/cells/calculate-formula-in-a-worksheet/" title="Beräkna en formel i ett kalkylark" rel="noopener">Beräkna en formel på ett Excel-kalkylark.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Namn</p>
        <ul>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="6" >}}
<div class="row">
    <div class="col-md-6">
        <p>Grodning</p>
        <ul>
            <li><a href="/cells/group-rows-in-excel-worksheet/" title="Gruppera rader i ett kalkylark" rel="noopener">Gruppera rader på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/ungroup-rows-in-excel-worksheet/" title="Avgruppera rader i ett kalkylark" rel="noopener">Avgruppera rader på ett Excel-kalkylark.</a></li>
        </ul>
        <p>Filter</p>
        <ul>
            <li><a href="/cells/add-a-filter-for-a-filter-column/" title="Lägg till ett filter till en kolumn" rel="noopener">Lägg till ett filter för en kolumn på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/delete-a-filter-for-a-filter-column/" title="Ta bort ett kolumnfilter" rel="noopener">Ta bort ett filter för en kolumn på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/remove-a-date-filter/" title="Ta bort ett datumfilter" rel="noopener">Ta bort ett datumfilter på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/add-an-icon-filter/" title="Lägg till ett ikonfilter" rel="noopener">Lägg till ett ikonfilter på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/add-date-filter-in-a-worksheet/" title="Lägg till ett datumfilter" rel="noopener">Lägg till ett datumfilter i ett Excel-kalkylark.</a></li>
            <li><a href="/cells/filter-data-by-using-an-autofilter/" title="Filtrera data med AutoFilter" rel="noopener">Filtrera data med AutoFilter på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/filter-the-top-10-items-in-the-list/" title="Filtrera de 10 bästa objekten" rel="noopener">Filtrera de 10 bästa objekten i listan på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/match-all-blank-cells-in-the-list/" title="Matcha alla tomma celler" rel="noopener">Matcha alla tomma celler i listan på ett Excel-kalkylark.</a></li>
        </ul>
        <p>Sortera</p>
        <ul>
            <li><a href="/cells/sort-worksheet-data/" title="Sortera kalkylarkdata" rel="noopener">Sortera data på ett Excel-kalkylark.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Importera data</p>
        <ul>
            <li><a href="/cells/import/" title="Importera data till Excel-filer" rel="noopener">Importera data till Excel-filer.</a></li>
            <li><a href="/cells/import-CSV-data-into-worksheet/" title="Importera CSV-data till ett kalkylark" rel="noopener">Importera CSV-data till ett Excel-kalkylark.</a></li>
            <li><a href="/cells/import/picture/" title="Importera en bild till ett kalkylark" rel="noopener">Importera en bild till ett Excel-kalkylark.</a></li>
            <li><a href="/cells/import/double-array/" title="Importera en dubbelarray till ett kalkylark" rel="noopener">Importera en dubbelarray till ett Excel-kalkylark.</a></li>
            <li><a href="/cells/import/integer-array/" title="Importera en heltalsarray till ett kalkylark" rel="noopener">Importera en heltalsarray till ett Excel-kalkylark.</a></li>
            <li><a href="/cells/import/string-array/" title="Importera en strängarray till ett kalkylark" rel="noopener">Importera en strängarray till ett Excel-kalkylark.</a></li>
            <li><a href="/cells/import/with-using-storage/" title="Importera data med lagring" rel="noopener">Importera data till ett Excel-kalkylark med lagring.</a></li>
            <li><a href="/cells/import/without-using-storage/" title="Importera data utan att använda lagring" rel="noopener">Importera data till ett Excel-kalkylark utan att använda lagring.</a></li>
        </ul>
        <p>Sammanställning</p>
        <ul>
            <li><a href="/cells/assembly/" title="Sammanställ data i Excel-filer" rel="noopener">Sammanställ data i Excel-filer.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="7" >}}
<div class="row">
    <div class="col-md-6">
        <p>Kommentarer</p>
        <ul>
            <li><a href="/cells/add-a-comment-to-a-cell-in-a-worksheet/" title="Lägg till en kommentar till en cell" rel="noopener">Lägg till en kommentar till en cell på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/update-a-comment-in-excel-workbook/" title="Uppdatera en cellkommentar" rel="noopener">Uppdatera en kommentar på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/delete-all-comments-in-a-worksheet/" title="Ta bort alla kommentarer i ett kalkylark" rel="noopener">Ta bort alla kommentarer på ett Excel-kalkylark.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Ändringar</p>
        <ul>
            <li><a href="/cells/protect-excel-workbooks/" title="Säkerställ en Excel-arbetsbok" rel="noopener">Säkerställ en Excel-arbetsbok.</a></li>
            <li><a href="/cells/unprotect-excel-workbooks/" title="Av säkerställ en Excel-arbetsbok" rel="noopener">Av säkerställ en Excel-arbetsbok.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="8" >}}
<div class="row">
    <div class="col-md-6">
        <p>Fönster</p>
        <ul>
            <li><a href="/cells/freeze-panes-in-excel-worksheet/" title="Frys rutor i ett kalkylark" rel="noopener">Frys rutor på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/unfreeze-panes-in-excel-worksheet/" title="Släpp frysning av rutor i ett kalkylark" rel="noopener">Släpp frysning av rutor på ett Excel-kalkylark.</a></li>
            <li><a href="/cells/hide-excel-worksheets/" title="Dölj ett kalkylark" rel="noopener">Dölj ett Excel-kalkylark.</a></li>
            <li><a href="/cells/unhide-excel-worksheets/" title="Visa ett dolt kalkylark" rel="noopener">Visa ett dolt Excel-kalkylark.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Zoom</p>
        <ul>
            <li><a href="/cells/set-zoom-in-excel-worksheet/" title="Ställ in kalkylarkzoomnivå" rel="noopener">Ställ in zoom på ett Excel-kalkylark.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}

## {{< /tabs >}}
