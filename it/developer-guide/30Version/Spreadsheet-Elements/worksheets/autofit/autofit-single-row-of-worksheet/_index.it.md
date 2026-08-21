---
title: "Adattamento automatico di una riga in un foglio di calcolo Excel"
second_title: "Documento"
linktitle: "Riga"
type: docs
url: /it/worksheets/autofit/row/
aliases: [/autofit-single-row-of-worksheet/]
description: "Scopri come utilizzare l'API REST di Aspose.Cells Cloud per eseguire l'adattamento automatico di una riga in un foglio di calcolo Excel. Include endpoint, parametri, autenticazione, gestione degli errori, richiesta cURL ed esempi di SDK."
keywords: "adattamento automatico riga, Aspose.Cells Cloud, API Excel, REST, foglio di calcolo, SDK, foglio elettronico, API cloud"
weight: 30
ArticleTitle: "Adattamento automatico riga in un foglio di calcolo Excel tramite Aspose.Cells Cloud API"
---

Questa API REST **esegue l'adattamento automatico di una riga** in un foglio di calcolo Excel.

## Sicurezza e autenticazione
Le API REST di Aspose.Cells Cloud sono sicure e richiedono l'[autenticazione tramite token JWT](https://docs.aspose.cloud/total/it/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitrow
```

### **Parametri della richiesta**

| Nome parametro    | Tipo    | Posizione | Descrizione                                                                                                                                                                                               |
| ----------------- | ------- | --------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name              | string  | path      | Nome del file Excel.                                                                                                                                                                                      |
| sheetName         | string  | path      | Nome del foglio di calcolo.                                                                                                                                                                               |
| rowIndex          | integer | query     | Indice in base zero della riga da adattare automaticamente.                                                                                                                                                |
| firstColumn       | integer | query     | Indice della prima colonna inclusa nell'operazione.                                                                                                                                                       |
| lastColumn        | integer | query     | Indice dell'ultima colonna inclusa nell'operazione.                                                                                                                                                       |
| autoFitterOptions | object  | body      | Oggetto che controlla il comportamento di adattamento automatico (ad esempio, se considerare le celle unite, l'a capo automatico, ecc.). Vedere [AutoFitterOptions](/it/cells/auto-fitter-options){:rel="noopener" title="Controlla il comportamento di adattamento automatico"}. |
| folder            | string  | query     | Cartella in cui è memorizzato il file.                                                                                                                                                                    |
| storageName       | string  | query     | Nome dello storage.                                                                                                                                                                                       |

**Esempio di corpo JSON `autoFitterOptions`**

```json
{
  "IsMergedCells": true,
  "IsWrapped": false,
  "AutoFitMergedCells": true,
  "AutoFitWrappedCells": false
}
```

### Definizioni delle entità

| Entità              | Descrizione                                                                                  |
| ------------------- | ------------------------------------------------------------------------------------------- |
| `rowIndex`          | Indice in base zero della riga di destinazione.                                              |
| `firstColumn`       | Colonna iniziale per l'operazione di adattamento automatico.                                 |
| `lastColumn`        | Colonna finale per l'operazione di adattamento automatico.                                   |
| `autoFitterOptions` | Impostazioni opzionali che influenzano il modo in cui viene eseguito l'adattamento automatico della riga (celle unite, a capo automatico, ecc.). |

La [Specifiche OpenAPI](/it/cells/#/Worksheets/PostAutofitWorksheetRow) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di eseguire interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come chiamare l'API tramite cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitrow?rowIndex=2&firstColumn=1&lastColumn=10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

| Campo  | Descrizione                                |
| ------ | ------------------------------------------ |
| Code   | `200` – richiesta riuscita.                |
| Status | `"OK"` – la riga è stata adattata automaticamente con successo. |

{{< /tab >}}

{{< /tabs >}}

## Gestione degli errori

L'API restituisce i codici di stato HTTP standard. Le risposte di errore comuni per questo endpoint sono:

| Codice HTTP | Esempio di payload                                        | Significato                                                                                  |
| ----------- | --------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| 400         | `{ "Code": 400, "Message": "Indice riga fuori intervallo." }`   | L'`rowIndex` fornito non esiste nel foglio di calcolo.                                        |
| 401         | `{ "Code": 401, "Message": "Token non valido o scaduto." }` | Autenticazione non riuscita – verificare il token JWT e assicurarsi che la richiesta avvenga tramite HTTPS. |
| 404         | `{ "Code": 404, "Message": "File non trovato." }`           | Il file Excel o il foglio di calcolo specificato non può essere individuato.                 |
| 500         | `{ "Code": 500, "Message": "Errore interno del server." }`  | Si è verificato un problema imprevisto lato server.                                          |

## Famiglia di SDK cloud

L'utilizzo di un SDK rappresenta il metodo più rapido per lo sviluppo. Un SDK astrae i dettagli di basso livello, consentendo di concentrarsi sulla logica di business. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud){:rel="noopener noreferrer"} per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetRow.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetRow.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetRow.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetRow.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2c4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetRow.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetRow.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetRow.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetRow.go" >}}
{{< /tab >}}

{{< /tabs >}}

**Vedi anche:** [Adattamento automatico colonna](/it/worksheets/autofit/column/), [Adattamento automatico righe](/it/worksheets/autofit/rows/), [AutoFitterOptions](/it/cells/auto-fitter-options).