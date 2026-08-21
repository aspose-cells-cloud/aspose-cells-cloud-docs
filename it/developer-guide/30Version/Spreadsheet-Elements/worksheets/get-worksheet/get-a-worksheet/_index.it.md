---
title: "Esporta un foglio di calcolo con l'API Aspose.Cells Cloud – Formati, esempi cURL e SDK"
second_title: "Documento"
linktitle: "Esportazione foglio di calcolo"
type: docs
url: /it/worksheets/get-worksheet/
keywords: "Aspose.Cells Cloud Get Worksheet, esportazione foglio di calcolo, API Excel, REST, CSV, PDF, PNG, JPEG, GIF, BMP, TIFF, EMF, XPS, OTS, XLS, XLSX, XLSB, XLSM, ODS, FODS, Numbers, API cloud"
description: "Scopri come esportare un singolo foglio di calcolo da un file Excel utilizzando l'API REST Aspose.Cells Cloud. Include endpoint, parametri, un esempio cURL corretto, dettagli sull'autenticazione, gestione degli errori e frammenti di codice SDK per C#, Java, Python e altro ancora."
weight: 10
ArticleTitle: "Esporta un foglio di calcolo con l'API Aspose.Cells Cloud – Formati, esempi cURL e SDK"
---

Questa API REST consente di **esportare un foglio di calcolo** da un file Excel in molti formati diversi.

**Riepilogo** – Utilizza l'endpoint **Get Worksheet** per scaricare un singolo foglio di calcolo da un libro nel formato desiderato.

Puoi esportare nei seguenti formati:

| Formato | Estensione | Tipo MIME                                                       |
| ------- | ---------- | --------------------------------------------------------------- |
| XLS     | .xls       | application/vnd.ms-excel                                        |
| XLSX    | .xlsx      | application/vnd.openxmlformats-officedocument.spreadsheetml.sheet |
| XLSB    | .xlsb      | application/vnd.ms-excel.sheet.binary.macroEnabled.12           |
| CSV     | .csv       | text/csv                                                        |
| TSV     | .tsv       | text/tab-separated-values                                       |
| XLSM    | .xlsm      | application/vnd.ms-excel.sheet.macroEnabled.12                  |
| ODS     | .ods       | application/vnd.oasis.opendocument.spreadsheet                  |
| TXT     | .txt       | text/plain                                                      |
| PDF     | .pdf       | application/pdf                                                 |
| OTS     | .ots       | application/vnd.oasis.opendocument.spreadsheet-template         |
| XPS     | .xps       | application/vnd.ms-xpsdocument                                  |
| DIF     | .dif       | application/x-dif                                               |
| PNG     | .png       | image/png                                                       |
| JPEG    | .jpeg      | image/jpeg                                                      |
| GIF     | .gif       | image/gif                                                       |
| BMP     | .bmp       | image/bmp                                                       |
| WMF     | .wmf       | image/wmf                                                       |
| TIFF    | .tiff      | image/tiff                                                      |
| EMF     | .emf       | image/emf                                                       |
| NUMBERS | .numbers   | application/vnd.apple.numbers                                   |
| FODS    | .fods      | application/vnd.oasis.opendocument.spreadsheet-flat-xml         |

## Sicurezza e autenticazione
Le API Aspose.Cells Cloud sono sicure e richiedono [autenticazione basata su token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### **Parametri della richiesta**

| Nome parametro           | Tipo    | Posizione | Descrizione                                                           |
| ------------------------ | ------- | --------- | --------------------------------------------------------------------- |
| **name**                 | string  | path      | **Obbligatorio.** Nome del file Excel.                                |
| **sheetName**            | string  | path      | **Obbligatorio.** Nome del foglio di calcolo da esportare.           |
| **format**               | string  | query     | Formato di destinazione per il foglio di calcolo esportato (es. `pdf`, `png`). |
| **verticalResolution**   | integer | query     | Risoluzione DPI per i formati che lo supportano (es. PNG, JPEG).      |
| **horizontalResolution** | integer | query     | Risoluzione DPI per i formati che lo supportano.                      |
| **area**                 | string  | query     | Intervallo di celle da esportare (es. `A1:D10`).                      |
| **pageIndex**            | integer | query     | Indice della pagina da esportare quando il foglio di calcolo è paginato. |
| **folder**               | string  | query     | Percorso della cartella nello storage in cui si trova il file sorgente. |
| **storageName**          | string  | query     | Nome dello storage Aspose Cloud.                                      |

La <a href="https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet" target="_blank" rel="noopener noreferrer">Specifiche OpenAPI</a> definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di effettuare direttamente interazioni REST da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come chiamare l'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1?format=gif" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```http
HTTP/1.1 200 OK
Content-Type: image/gif
Content-Disposition: attachment; filename="Sheet1.gif"

<dati binari>
```

{{< /tab >}}

{{< /tabs >}}

## Gestione degli errori

L'API restituisce i codici di stato HTTP standard. Le risposte comuni includono:

| Codice di stato | Significato                                                     | Esempio di corpo JSON                          |
| --------------- | --------------------------------------------------------------- | ---------------------------------------------- |
| **200**         | Successo – il flusso del foglio di calcolo viene restituito.   | `{ "stream": "..." }`                          |
| **400**         | Richiesta non valida – parametri mancanti o non validi.        | `{ "error": "Parametro format non valido." }` |
| **401**         | Non autorizzato – token JWT non valido o mancante.             | `{ "error": "Autenticazione non riuscita." }` |
| **404**         | Non trovato – il file o il foglio di calcolo specificato non esiste. | `{ "error": "Foglio di calcolo non trovato." }` |
| **500**         | Errore interno del server – condizione imprevista sul server.  | `{ "error": "Errore imprevisto." }`           |

Gestisci queste risposte nel tuo codice client per fornire feedback appropriati agli utenti.

## Famiglia di SDK cloud

Utilizzare un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}