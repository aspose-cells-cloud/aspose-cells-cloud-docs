---
title: Ottieni i dati delle celle in base all'intervallo denominato
second_title: Aspose.Cells Cloud Documen
linktitle: Valore
type: docs
url: /it/ranges/get/values/
aliases: [/get-cells-data-based-on-named-range/]
keywords: Get cells data based on named range on an Excel worksheet
description: Aspose.Cells Cloud REST API supporta l'ottenimento dei dati delle celle in base all'intervallo denominato in un foglio di lavoro Excel. L'SDK supporta i tipi di linguaggi di sviluppo. Includono Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e swift
weight: 20
---
 Questo REST API indica Ottieni elenco celle in un intervallo per nome intervallo o indici colonna riga

 
## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/value
 
```
 I parametri della richiesta sono:
 
| Nome parametro| Tipo| Percorso/Stringa di query/HTTPBody|Descrizione|
|:- |:- |:- |:- |
| nome| corda| sentiero| nome della cartella di lavoro|
| foglioNome| corda| sentiero| nome del foglio di lavoro|
| namerange| corda| domanda| nome dell'intervallo, ad esempio: "A1:B2" o "nome_intervallo1"|
| prima riga| numero intero| domanda| la prima riga dell'intervallo|
| firstColumn| numero intero| domanda| la prima colonna dell'intervallo|
| rowCount| numero intero| domanda| il conteggio delle righe nell'intervallo|
| colonnaCount| numero intero| domanda| il conteggio delle colonne nell'intervallo|
| cartella| corda| domanda| Cartella della cartella di lavoro.|
| storageName| corda| domanda| nome di archiviazione.|
 
 IL[Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Ranges/GetWorksheetCellsRangeValue) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.
 
È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi Web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate a Cloud API con cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/value?namerange=data" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
```bash
{

  "CellsList": [

    {

      "Name": "B10",

      "Row": 9,

      "Column": 1,

      "Value": null,

      "Type": "IsNull",

      "Formula": null,

      "IsFormula": false,

      "IsMerged": false,

      "IsArrayHeader": false,

      "IsInArray": false,

      "IsErrorValue": false,

      "IsInTable": false,

      "IsStyleSet": false,

      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",

      "Style": {

        "link": {

          "Href": "/style",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      "Worksheet": null,

      "link": null

    },

    {

      "Name": "C10",

      "Row": 9,

      "Column": 2,

      "Value": null,

      "Type": "IsNull",

      "Formula": null,

      "IsFormula": false,

      "IsMerged": false,

      "IsArrayHeader": false,

      "IsInArray": false,

      "IsErrorValue": false,

      "IsInTable": false,

      "IsStyleSet": false,

      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",

      "Style": {

        "link": {

          "Href": "/style",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      "Worksheet": null,

      "link": null

    },

    {

      "Name": "D10",

      "Row": 9,

      "Column": 3,

      "Value": null,

      "Type": "IsNull",

      "Formula": null,

      "IsFormula": false,

      "IsMerged": false,

      "IsArrayHeader": false,

      "IsInArray": false,

      "IsErrorValue": false,

      "IsInTable": false,

      "IsStyleSet": false,

      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",

      "Style": {

        "link": {

          "Href": "/style",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      "Worksheet": null,

      "link": null

    },

    {

      "Name": "E10",

      "Row": 9,

      "Column": 4,

      "Value": null,

      "Type": "IsNull",

      "Formula": null,

      "IsFormula": false,

      "IsMerged": false,

      "IsArrayHeader": false,

      "IsInArray": false,

      "IsErrorValue": false,

      "IsInTable": false,

      "IsStyleSet": false,

      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",

      "Style": {

        "link": {

          "Href": "/style",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      "Worksheet": null,

      "link": null

    },

    {

      "Name": "F10",

      "Row": 9,

      "Column": 5,

      "Value": null,

      "Type": "IsNull",

      "Formula": null,

      "IsFormula": false,

      "IsMerged": false,

      "IsArrayHeader": false,

      "IsInArray": false,

      "IsErrorValue": false,

      "IsInTable": false,

      "IsStyleSet": false,

      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",

      "Style": {

        "link": {

          "Href": "/style",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      "Worksheet": null,

      "link": null

    },

    {

      "Name": "G10",

      "Row": 9,

      "Column": 6,

      "Value": null,

      "Type": "IsNull",

      "Formula": null,

      "IsFormula": false,

      "IsMerged": false,

      "IsArrayHeader": false,

      "IsInArray": false,

      "IsErrorValue": false,

      "IsInTable": false,

      "IsStyleSet": false,

      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",

      "Style": {

        "link": {

          "Href": "/style",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      "Worksheet": null,

      "link": null

    },

    {

      "Name": "H10",

      "Row": 9,

      "Column": 7,

      "Value": "a8",

      "Type": "IsString",

      "Formula": null,

      "IsFormula": false,

      "IsMerged": false,

      "IsArrayHeader": false,

      "IsInArray": false,

      "IsErrorValue": false,

      "IsInTable": false,

      "IsStyleSet": false,

      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">a8</Font>",

      "Style": {

        "link": {

          "Href": "/style",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      "Worksheet": null,

      "link": null

    }

  ],

  "Code": 200,

  "Status": "OK"

}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Famiglia di SDK cloud
 
 L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Si prega di controllare il[Deposito GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.
 
I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:
 
 