---
title: "Ottenere una Proprietà Specifica del Documento"
second_title: "Documento"
linktitle: "Ottieni"
type: docs
url: /document-properties/get/
aliases: [/get-a-particular-document-property/]
keywords: "Aspose.Cells, API Cloud, Ottieni Proprietà Documento, Metadata Excel, REST GET, Esempi SDK"
description: "Recupera una proprietà nominata del documento (ad esempio, Autore, Titolo) da un file Excel utilizzando l'API REST Cloud di Aspose.Cells. Include un esempio cURL, frammenti di codice SDK e schema di risposta."
weight: 20
---

Questa REST API legge una proprietà del documento per nome.

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}
```

### Parametri della Richiesta

| Nome Parametro | Tipo   | Posizione | Descrizione                                           |
| -------------- | ------ | --------- | ----------------------------------------------------- |
| name           | string | path      | Il nome del file Excel.                              |
| propertyName   | string | path      | Il nome della proprietà del documento da recuperare. |
| folder         | string | query     | La cartella contenente il file (opzionale).          |
| storageName    | string | query     | Il nome dello storage (opzionale).                   |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Properties/GetDocumentProperty) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando **cURL** per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties/author" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "DocumentProperty": {
    "Name": "Author",
    "Value": "",
    "BuiltIn": "True",
    "link": {
      "Href": "/test.xlsx/documentproperties/Author",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Dettagli della Risposta

L'oggetto JSON restituito dall'API contiene i seguenti campi:

| Campo                           | Tipo    | Descrizione                                                      |
| ------------------------------- | ------- | ---------------------------------------------------------------- |
| **DocumentProperty.Name**       | string  | Il nome della proprietà (ad esempio, `Author`).                  |
| **DocumentProperty.Value**      | string  | Il valore della proprietà. Può essere vuoto se non impostato.    |
| **DocumentProperty.BuiltIn**    | boolean | Indica se la proprietà è una proprietà integrata di Excel.       |
| **DocumentProperty.link.Href**  | string  | URL relativo alla risorsa della proprietà.                       |
| **DocumentProperty.link.Rel**   | string  | Tipo di relazione, di solito `self`.                             |
| **DocumentProperty.link.Title** | string  | Titolo leggibile (può essere `null`).                            |
| **DocumentProperty.link.Type**  | string  | Tipo MIME della risorsa collegata (può essere `null`).           |
| **Code**                        | integer | Codice di stato HTTP restituito dal servizio.                    |
| **Status**                      | string  | Descrizione testuale dello stato (ad esempio, `OK`).             |

### Risposte di Errore

| Stato HTTP | Codice                 | Descrizione                                           |
| ---------- | ---------------------- | ----------------------------------------------------- |
| 400        | `InvalidParameter`     | Uno o più parametri della richiesta non sono validi.  |
| 401        | `AuthenticationFailed` | Token JWT mancante o non valido.                      |
| 404        | `PropertyNotFound`     | La proprietà del documento specificata non esiste.    |
| 500        | `InternalError`        | Si è verificato un errore imprevisto sul server.      |

Un corpo di errore tipico ha il seguente aspetto:

```json
{
  "Code": 404,
  "Status": "Property not found"
}
```

## Famiglia di SDK Cloud

L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, permettendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetDocumentProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetDocumentProperty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetDocumentProperty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetDocumentProperty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetDocumentProperty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetDocumentProperty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetDocumentProperty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetDocumentProperty.go" >}}

{{< /tab >}}

{{< /tabs >}}

### Terminologia

| Termine               | Definizione                                                                                  |
| --------------------- | -------------------------------------------------------------------------------------------- |
| **Proprietà Documento** | Un pezzo di metadata associato a un file Excel (ad esempio, Autore, Titolo, Creato).         |
| **Metadata**          | Termine generico per dati che descrivono altri dati; in questo contesto si riferisce alle proprietà del documento. |
| **Proprietà Personalizzata** | Una proprietà definita dall'utente non inclusa nell'insieme integrato.                      |

### Domande Frequenti

**Domanda:** _Come posso recuperare la proprietà Autore di un file Excel archiviato in Aspose Cloud?_  
**Risposta:** Invia una richiesta GET a `https://api.aspose.cloud/v3.0/cells/{fileName}/documentproperties/author` con un token Bearer valido. La risposta JSON include `DocumentProperty.Name = "Author"` e il relativo `Value`.

**Domanda:** _Quale errore viene restituito se la proprietà richiesta non esiste?_  
**Risposta:** L'API restituisce HTTP 404 con un corpo JSON contenente `Code: 404` e `Status: "Property not found"`.

**Domanda:** _Devo specificare `storageName` quando il file si trova nello storage predefinito?_  
**Risposta:** No. Il parametro di query `storageName` è opzionale; omettilo per utilizzare lo storage predefinito configurato per il tuo account.

---