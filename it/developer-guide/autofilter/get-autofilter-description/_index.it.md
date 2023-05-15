---
title: Ottieni un filtro automatico in un foglio di lavoro Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Ottieni il filtro automatico
type: docs
url: /it/autofilter/get/
aliases: [/get-autofilter-description/]
keywords: Gets auto filter description from an Excel worksheet
description: Il supporto Aspose.Cells Cloud API ottiene la descrizione del filtro automatico da un foglio di lavoro Excel. L'SDK supporta i tipi di linguaggi di sviluppo. Includono Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e swift
weight: 50
---
Questo REST API indica ottenere la descrizione `auto filter` in un foglio di lavoro Excel.
 
## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter
 
```
 I parametri della richiesta sono:
 
| Nome parametro| Tipo| Percorso/Stringa di query/HTTPBody|Descrizione|
|:- |:- |:- |:- |
| nome| corda| sentiero||
| foglioNome| corda| sentiero||
| cartella| corda| domanda||
| storageName| corda| domanda| nome di archiviazione.|
 
 IL[Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/GetWorksheetAutoFilter) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.
 
È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi Web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate a Cloud API con cURL.
 


{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl  "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

 {
  "Status": "string",
  "AutoFilter": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "FilterColumns": [
      {
        "FieldIndex": 0,
        "FilterType": "string",
        "MultipleFilters": {
          "MatchBlank": true,
          "MultipleFilterList": [
            {}
          ]
        },
        "ColorFilter": {
          "FilterByFillColor": "string",
          "Pattern": "string",
          "Color": {
            "Color": {
              "A": 0,
              "R": 0,
              "G": 0,
              "B": 0
            },
            "ColorIndex": 0,
            "IsShapeColor": true,
            "ThemeColor": {
              "ColorType": "string",
              "Tint": 0
            },
            "Type": "string"
          },
          "ForegroundColorColor": {
            "Color": {
              "A": 0,
              "R": 0,
              "G": 0,
              "B": 0
            },
            "ColorIndex": 0,
            "IsShapeColor": true,
            "ThemeColor": {
              "ColorType": "string",
              "Tint": 0
            },
            "Type": "string"
          },
          "BackgroundColor": {
            "Color": {
              "A": 0,
              "R": 0,
              "G": 0,
              "B": 0
            },
            "ColorIndex": 0,
            "IsShapeColor": true,
            "ThemeColor": {
              "ColorType": "string",
              "Tint": 0
            },
            "Type": "string"
          }
        },
        "CustomFilters": [
          {
            "FilterOperatorType": "string"
          }
        ],
        "DynamicFilter": {
          "DynamicFilterType": "string"
        },
        "IconFilter": {
          "IconId": 0,
          "IconSetType": "string"
        },
        "Top10Filter": {
          "Criteria": "string",
          "IsPercent": true,
          "IsTop": true,
          "Items": 0
        },
        "Visibledropdown": "string"
      }
    ],
    "Range": "string",
    "Sorter": {
      "CaseSensitive": true,
      "HasHeaders": true,
      "KeyList": [
        {
          "Key": 0,
          "SortOrder": "string",
          "CustomList": "string"
        }
      ],
      "SortLeftToRight": true
    }
  }
}
```

{{< /tab >}}

{{< /tabs >}}


## Famiglia di SDK cloud

 L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Si prega di controllare il[Deposito GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:


{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-Worksheet-GetWorksheetAutoFilter-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-filters-GetAutoFilterDescriptionExample-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-AutoFilter-GetWorksheetAutoFilter-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-AutoFilter-get_worksheet_auto_filter-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-GetWorksheetAutoFilter-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "75ea6b5d2f6d82f9c2f9279fb37ebbdf" "Examples-Android-filters-AddDateWorksheetExample-1.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-GetWorksheetAutoFilter-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "4258eab6a50d4856861377a108d0c7dd" >}}

{{< /tab >}}

{{< /tabs >}}
