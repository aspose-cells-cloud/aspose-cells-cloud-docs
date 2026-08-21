---
title: "Excel in TIFF"
second_title: "Documenti"
linketitle: "Excel in TIFF"
type: docs
url: /convert-excel-file-to-tiff-file/
aliases: [/convert-excel-file-to-tiff-in-cloud/, /convert/excel-to-tiff/]
keywords: "Aspose.Cells Cloud, conversione Excel in TIFF, API REST, cURL, SDK, .NET, Java, Python, esportazione immagini"
description: "Scopri come convertire file Excel in immagini TIFF di alta qualità utilizzando l'API Aspose.Cells Cloud. Comandi cURL dettagliati, esempi di SDK (C#, Java, Python, ...), fasi di autenticazione e gestione degli errori."
weight: 90
---

Gli endpoint **Convert**, **SaveAs** ed **Export** di Aspose.Cells Cloud ti permettono di trasformare un file Excel in un'immagine TIFF.  
Puoi richiamare questi endpoint direttamente con **cURL** oppure tramite uno degli SDK supportati.

## API REST

| **API**                | **Metodo** | **Scopo**                                                                                     | **Link Swagger**                                                                            |
| ---------------------- | ---------- | --------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `/cells/convert`       | PUT        | Converte un file Excel fornito nel corpo della richiesta nel formato specificato (TIFF).      | [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) |
| `/cells/{name}`        | GET        | Esporta il file Excel indicato in un altro formato (TIFF) e restituisce il risultato nella risposta. | [GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)               |
| `/cells/{name}/saveAs` | POST       | Salva il file Excel nel formato scelto (TIFF) e memorizza il risultato nell'archivio cloud.   | [PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)   |

Questi endpoint sono pubblicamente accessibili e possono essere chiamati direttamente da un browser web o da qualsiasi client HTTP.

### Esempi con cURL

{{< tabs tabTotal="3" tabID="11" tabName11="convert" tabName12="saveas" tabName13="export">}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/convert?format=tiff" \
     -X PUT \
     -d '{"File":{"Name":"book1.xlsx","Data":"<contenuto-base64>"},"SaveFormat":"tiff"}' \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="12" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx/saveas?newfilename=book1.tiff" \
     -X POST \
     -d '{"SaveFormat":"tiff","ImageFormat":"tiff"}' \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="13" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=tiff" \
     -X GET \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< /tabs >}}

> **Nota:**
>
> - Il corpo della richiesta per **Convert** deve contenere il file (o un riferimento a un file memorizzato) e il `SaveFormat` desiderato.
> - La richiesta di **Export** non richiede un corpo di richiesta; il formato viene fornito tramite la stringa di query (`format=tiff`).

## Gestione degli errori

| **Codice di stato** | **Significato**       | **Causa tipica**                            |
| ------------------- | --------------------- | ------------------------------------------- |
| 200                 | Operazione riuscita   | L'immagine TIFF viene restituita (stream binario). |
| 400                 | Richiesta non valida  | Parametri mancanti o malformati.            |
| 401                 | Non autorizzato       | Token JWT non valido o mancante.            |
| 404                 | Non trovato           | Il file Excel specificato non esiste.       |
| 500                 | Errore interno del server | Condizioni impreviste lato server.          |

Quando si verifica un errore, l'API restituisce un payload JSON contenente i campi `Code`, `Message` e, opzionalmente, `Description`.

## Famiglia di SDK cloud

L'utilizzo di un SDK rappresenta il modo più rapido per sviluppare. Un SDK gestisce i dettagli a basso livello, permettendoti di concentrarti sul tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbookToTiff.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbookToTiff.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbookToTiff.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbookToTiff.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbookToTiff.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbookToTiff.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbookToTiff.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbookToTiff.go" >}}

{{< /tab >}}

{{< /tabs >}}