---
title: "Eliminare una proprietà specifica di un documento"
second_title: "Documento"
linktitle: "Elimina"
type: docs
url: /it/document-properties/delete/
aliases: [  /it/remove-a-particular-document-property/ ]
keywords: "Aspose.Cells, eliminare proprietà documento, API metadati Excel, REST, SDK cloud, esempio cURL"
description: "Elimina una proprietà specifica di un documento da un foglio di calcolo Excel utilizzando l'API REST Aspose.Cells Cloud v3.0. Include esempi cURL e SDK per C#, Java, Python e altri linguaggi."
weight: 50
---

Questa REST API elimina una proprietà di documento da un foglio di calcolo.

## API REST

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}
```

### Parametri della richiesta

| Nome parametro | Tipo   | Posizione | Obbligatorio | Descrizione                                      |
| -------------- | ------ | --------- | ------------ | ------------------------------------------------ |
| name           | string | path      | Sì           | Il nome del foglio di calcolo Excel.             |
| propertyName   | string | path      | Sì           | Il nome della proprietà di documento da eliminare. |
| folder         | string | query     | No           | Il percorso della cartella in cui è salvato il foglio di calcolo. |
| storageName    | string | query     | No           | Il nome del servizio di archiviazione.           |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Properties/DeleteDocumentProperty) definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties/author" \
     -X DELETE \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Risposte di errore

| Stato HTTP | Descrizione                                                          | Esempio JSON                                                   |
| ---------- | -------------------------------------------------------------------- | -------------------------------------------------------------- |
| 400        | Richiesta non valida – parametri obbligatori mancanti o valori non validi. | `{"Code":400,"Message":"Parametro obbligatorio 'name' mancante."}` |
| 401        | Non autorizzato – token JWT non valido o assente.                   | `{"Code":401,"Message":"Token di accesso non valido."}`        |
| 404        | Non trovato – il foglio di calcolo o la proprietà specificata non esistono. | `{"Code":404,"Message":"Proprietà documento non trovata."}`    |
| 500        | Errore interno del server – si è verificata una condizione imprevista. | `{"Code":500,"Message":"Si è verificato un errore imprevisto."}` |

## Famiglia di SDK cloud

L'utilizzo di un SDK rappresenta il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK cloud di Aspose.Cells.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDocumentProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDocumentProperty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDocumentProperty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDocumentProperty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteDocumentProperty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDocumentProperty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDocumentProperty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDocumentProperty.go" >}}

{{< /tab >}}

{{< /tabs >}}