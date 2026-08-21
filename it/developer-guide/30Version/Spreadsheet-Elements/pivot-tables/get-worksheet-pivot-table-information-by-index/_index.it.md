---
title: "Ottenere una tabella pivot in un foglio Excel"
second_title: "Document"
linktype: Get
type: docs
url: /it/pivot-tables/get/
aliases: [  /it/get-worksheet-pivot-table-information-by-index/ ]
keywords: "Aspose.Cells, tabella pivot, Excel, REST API, ottenere tabella pivot del foglio"
description: "Recuperare una tabella pivot da un foglio Excel tramite l'API REST di Aspose.Cells Cloud. Include sintassi della richiesta, parametri, autenticazione, schema della risposta, gestione degli errori ed esempi di SDK."
weight: 10
ArticleTitle: "Ottenere una tabella pivot in un foglio Excel"
---

Questa REST API recupera le informazioni sulla **tabella pivot** di un foglio tramite il suo indice.

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione tramite token JWT</a>.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivottableIndex}
```

### Parametri della richiesta

| Nome parametro      | Tipo    | Posizione | Descrizione                                              |
| ------------------- | ------- | -------- | -------------------------------------------------------- |
| **name**            | string  | path     | Nome del file Excel.                                     |
| **sheetName**       | string  | path     | Nome del foglio che contiene la tabella pivot.          |
| **pivottableIndex** | integer | path     | Indice in base zero della tabella pivot nel foglio.     |
| **folder**          | string  | query    | Cartella in cui è memorizzato il documento.             |
| **storageName**     | string  | query    | Nome dello storage Aspose Cloud.                        |

Puoi utilizzare lo strumento a riga di comando **cURL** per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come chiamare l'API con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "PivotFilters": [
    {
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
              "MultipleFilterList": [{}]
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
            "VisibleDropdown": "string"
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
      },
      "EvaluationOrder": 0,
      "FieldIndex": 0,
      "FilterType": "string",
      "MeasureFldIndex": 0,
      "MemberPropertyFieldIndex": 0,
      "Name": "string",
      "Value1": "string",
      "Value2": "string"
    }
  ]
}
```

**Schema della risposta**

| Campo          | Tipo    | Descrizione                                      |
|----------------|---------|--------------------------------------------------|
| Status         | string  | Testo dello stato dell’operazione (es. “OK”).   |
| PivotFilters   | array   | Raccolta di definizioni dei filtri pivot.       |
| └─ AutoFilter  | object  | Dettagli del filtro automatico applicato alla tabella pivot. |
|    └─ link     | object  | Informazioni sull’hyperlink del filtro.         |
|    └─ FilterColumns | array | Impostazioni individuali del filtro per colonna. |
|    └─ Range    | string  | Intervallo di celle a cui si applica il filtro. |
|    └─ Sorter   | object  | Configurazione dell’ordinamento per i dati filtrati. |
| (ulteriori campi nidificati seguono la stessa struttura mostrata nel JSON di esempio) |

{{< /tab >}}

{{< /tabs >}}

### Gestione degli errori

L’API segue i codici di stato HTTP standard. Le risposte tipiche includono:

| Codice stato | Significato                                                          | Esempio JSON (errore)                             |
| ----------- | -------------------------------------------------------------------- | ------------------------------------------------- |
| 200         | Successo – la tabella pivot viene restituita                         | —                                                 |
| 401         | Non autorizzato – token non valido o mancante                       | `{"code":401,"message":"Token di accesso non valido."}`  |
| 404         | Non trovato – il file, il foglio o l'indice della tabella pivot non esistono | `{"code":404,"message":"Tabella pivot non trovata."}` |
| 500         | Errore del server – condizione imprevista                           | `{"code":500,"message":"Errore interno del server."}` |

**Note:** L’API supporta file Excel fino a 150 MB e funziona con i formati Excel 2007‑2021. Assicurati che il nome del foglio sia distinto tra maiuscole e minuscole.

## Famiglia di SDK cloud

Utilizzare un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, permettendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Android" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-GetWorksheetPivotTableByIndex-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-GetWorksheetPivotInfoByIndex-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetWorksheetPivotTablesInformationByIndex.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-GetWorksheetPivotTableByIndex-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Examples-Android-pivottables-GetPivotTableIndexWorksheet-get-pivottable-index-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-GetWorksheetPivotTableByIndex-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3ff21d138764aa6b6fd51fbaab8cdb95" >}}

{{< /tab >}}

{{< /tabs >}}