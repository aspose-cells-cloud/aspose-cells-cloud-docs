---
title: "Converti foglio di lavoro in PDF, PNG, CSV e altro – Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "Converti foglio di lavoro"
type: docs
url: /worksheets/conversion/
aliases:
  - /convert-worksheet-to-image/
  - /worksheets/to-image/
keywords: "Aspose.Cells, conversione foglio di lavoro, API REST, cURL, SDK, PDF, PNG, CSV"
description: "Scopri come convertire un singolo foglio di lavoro da un libro Excel in PDF, PNG, CSV e più di 15 altri formati utilizzando l'API REST Aspose.Cells Cloud. Include esempi in cURL, frammenti di codice SDK e un riferimento completo ai parametri."
weight: 130
ArticleTitle: "Converti foglio di lavoro in PDF, PNG, CSV e altro – Aspose.Cells Cloud API"
---

**API per la conversione del foglio di lavoro** – L'endpoint `GET /cells/{name}/worksheets/{sheetName}` converte un singolo foglio di lavoro (una scheda all'interno di un libro Excel) in un altro tipo di file.

> **Prerequisito:** Prima di chiamare questo endpoint, devi disporre di un token JWT valido e del libro memorizzato in una posizione di archiviazione Aspose Cloud supportata.

Formati supportati per l'**importazione** (il foglio di lavoro può essere letto da):

- XLS, XLSX, XLSB, CSV, TSV, XLSM, ODS, TXT

Formati supportati per l'**esportazione esclusiva** (il foglio di lavoro può essere salvato come):

- PDF, OTS, XPS, DIF, PNG, JPEG, BMP, SVG, TIFF, EMF, NUMBERS, FODS

## API REST

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetWithFormat) descrive l'interfaccia pubblicamente accessibile.

### **Parametri della richiesta**

| Parametro                | Tipo    | Obbligatorio | Valore predefinito | Valori consentiti                                                   | Descrizione                                     |
| ------------------------ | ------- | ------------ | ------------------ | ------------------------------------------------------------------- | ----------------------------------------------- |
| **format**               | string  | Sì           | –                  | pdf, png, jpeg, bmp, svg, tiff, emf, csv, txt, … (vedi elenco supportato) | Format di output finale.                        |
| **verticalResolution**   | integer | No           | 96                 | 72‑600                                                              | Risoluzione verticale in DPI per output immagine. |
| **horizontalResolution** | integer | No           | 96                 | 72‑600                                                              | Risoluzione orizzontale in DPI per output immagine. |
| **password**             | string  | No           | –                  | –                                                                   | Password per aprire un libro protetto.          |
| **folder**               | string  | No           | –                  | –                                                                   | Cartella cloud in cui è memorizzato il libro di origine. |
| **storage**              | string  | No           | –                  | –                                                                   | Nome dell'archiviazione (es. “Default”).        |

### Risposta

| Codice di stato | Descrizione                                                          | Tipo restituito            |
| --------------- | -------------------------------------------------------------------- | -------------------------- |
| **200**         | Conversione riuscita; viene restituito il flusso binario del file convertito. | `application/octet-stream` |
| **400**         | Richiesta non valida – parametri mancanti o non validi.             | Oggetto di errore JSON     |
| **401**         | Non autorizzato – token JWT non valido o mancante.                  | Oggetto di errore JSON     |
| **404**         | Non trovato – il libro o il foglio di lavoro non esistono.          | Oggetto di errore JSON     |
| **500**         | Errore interno del server – errore imprevisto.                      | Oggetto di errore JSON     |

#### Esempio di richiesta (cURL)

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1?format=png&verticalResolution=96&horizontalResolution=96" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

#### Esempio di risposta

```
Immagine convertita (flusso binario)
```

## Famiglia di SDK su cloud

Utilizzare un SDK è il modo più rapido per sviluppare. Un SDK gestisce i dettagli a basso livello, permettendoti di concentrarti sul tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

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
---