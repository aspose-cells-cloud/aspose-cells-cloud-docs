---
title: "Ottieni i dati delle celle in base a un intervallo denominato"
second_title: "Documenti"
linktype: "Valori"
type: docs
url: /it/ranges/get/values/
aliases: [  /it/get-cells-data-based-on-named-range/ ]
keywords: "Aspose.Cells, Cloud, API REST, Excel, intervallo denominato, valori delle celle, foglio di lavoro"
description: "Recupera i valori delle celle da un intervallo denominato in un foglio di lavoro Excel utilizzando l'API REST di Aspose.Cells Cloud. Il servizio è disponibile tramite numerosi SDK (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go) e funziona su una vasta gamma di piattaforme di sviluppo."
weight: 20
ArticleTitle: "Ottieni i dati delle celle in base a un intervallo denominato – Aspose.Cells Cloud API"
---

**Prerequisiti**

- Un token di accesso JWT valido con l'ambito appropriato.  
- Il workbook deve essere caricato nello storage di Aspose Cloud (o in una cartella specificata).  
- Assicurati di fornire il nome dello storage di destinazione se utilizzi uno storage non predefinito.

Questa API REST restituisce un elenco di celle all'interno di un intervallo identificato da un intervallo denominato o da indici riga-colonna.

Questa operazione consente agli sviluppatori di recuperare programmaticamente i valori delle celle appartenenti a un intervallo denominato specifico in un foglio di lavoro Excel. Fornendo l'identificatore `namedRange` oppure gli indici espliciti di riga e colonna, l'API restituisce un elenco dettagliato delle celle, inclusi il relativo indirizzo, riga, colonna, valore, tipo di dati e informazioni sul formato. La risposta può essere utilizzata per alimentare applicazioni basate sui dati, generare report o eseguire ulteriori calcoli lato server. Il servizio Aspose.Cells Cloud supporta numerose lingue di programmazione tramite i relativi SDK, garantendo un'integrazione fluida indipendentemente dalla piattaforma di sviluppo. L'utilizzo di HTTPS garantisce la trasmissione sicura dei dati, e l'API rispetta i principi REST restituendo codici di stato HTTP standard per le condizioni di successo ed errore.

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/value
```

### **Parametri della richiesta**

| Nome parametro | Tipo    | Posizione | Descrizione                                                                                  |
| -------------- | ------- | --------- | -------------------------------------------------------------------------------------------- |
| name           | string  | path      | Nome del file workbook.                                                                      |
| sheetName      | string  | path      | Nome del foglio di lavoro all'interno del workbook.                                          |
| namedRange     | string  | query     | Intervallo denominato da recuperare, ad esempio `A1:B2` o `range_name1`.                     |
| firstRow       | integer | query     | Indice in base zero della prima riga dell'intervallo (utilizzato quando `namedRange` non è fornito). |
| firstColumn    | integer | query     | Indice in base zero della prima colonna dell'intervallo (utilizzato quando `namedRange` non è fornito). |
| rowCount       | integer | query     | Numero di righe da includere nell'intervallo.                                                |
| columnCount    | integer | query     | Numero di colonne da includere nell'intervallo.                                              |
| folder         | string  | query     | Cartella contenente il workbook.                                                             |
| storageName    | string  | query     | Nome dello storage cloud in cui risiede il workbook.                                         |

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Ranges/GetWorksheetCellsRangeValue) definisce un'interfaccia di programmazione pubblicamente accessibile e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per chiamare facilmente i servizi web di Aspose.Cells. L'esempio seguente illustra come richiedere i valori delle celle da un intervallo denominato.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

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

```json
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

**Nota sulla sicurezza:** Utilizza sempre HTTPS quando chiami l'API. Il servizio non supporta HTTP in chiaro; l'uso di HTTPS garantisce che la richiesta sia crittografata e rispetti le best practice in materia di sicurezza.

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                               |
|--------|-----------------------------|-----------------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante.                          |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione.         |
| 500    | Errore interno del server   | Errore imprevisto sul server.                             |

**Esempio di risposta di errore (400 Bad Request)**

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "Il parametro 'namedRange' è mancante o non valido."
}
```

> **Suggerimento:** L'API utilizza indici in base zero per `firstRow` e `firstColumn`. Ad esempio, la prima riga del foglio di lavoro corrisponde a `0`.

## Famiglia di SDK Cloud

L'utilizzo di un SDK rappresenta il modo più efficiente per accelerare lo sviluppo. Un SDK astrae i dettagli di basso livello, consentendo di concentrarsi sulla logica di business. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

Gli esempi di codice seguenti illustrano come chiamare i servizi web di Aspose.Cells utilizzando diversi SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellsRangeValue.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellsRangeValue.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellsRangeValue.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellsRangeValue.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellsRangeValue.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellsRangeValue.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellsRangeValue.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCellsRangeValue.go" >}}

{{< /tab >}}

{{< /tabs >}}