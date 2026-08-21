---
title: "Aggiungi una firma digitale a un libro Excel"
ArticleTitle: "Aggiungi una firma digitale a un libro Excel – Aspose.Cells Cloud API"
second_title: "Documento"
linktype: "firma digitale"
type: docs
url: /excel-digital-signature/
aliases:
  - /protect/digital-signature/
  - /workbook/digital-signature/
keywords: "Aspose.Cells Cloud, firma digitale, libro Excel, API REST, .pfx, JWT, API per firme"
description: "Scopri come aggiungere una firma digitale a un libro Excel utilizzando l'API REST di Aspose.Cells Cloud (versione 4.0). Include endpoint, parametri, autenticazione, schema di risposta, gestione degli errori ed esempi di SDK per diversi linguaggi."
weight: 35
---


**Prerequisiti:**  
Prima di chiamare questo endpoint, assicurati di disporre di:

- Un token di accesso JWT valido ottenuto tramite l'autenticazione di Aspose Cloud.  
- Il libro di destinazione caricato nello storage di Aspose Cloud.  
- Un file di firma digitale in formato `.pfx` o `.p12` e la relativa password.

Questa API REST aggiunge una **firma digitale** a un libro Excel.

## API PostDigitalSignature

```http
POST https://api.aspose.cloud/v4.0/cells/{name}/digitalsignature
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome del parametro        | Tipo   | Posizione               | Descrizione                                           |
| ------------------------- | ------ | ----------------------- | ----------------------------------------------------- |
| **name**                  | string | `<code>path</code>`     | Nome del libro.                                       |
| **digitalsignaturefile**  | string | `<code>query</code>`    | Percorso del file di firma digitale (`.pfx` o `.p12`).|
| **password**              | string | `<code>query</code>`    | Password del libro, se protetto.                      |
| **folder**                | string | `<code>query</code>`    | Cartella in cui è memorizzato il libro.               |
| **storageName**           | string | `<code>query</code>`    | Nome del servizio di storage da utilizzare.           |

*Nota: Se il nome del file contiene caratteri speciali, effettua l'URL encoding prima di aggiungerlo alla stringa di query.*

### Gestione degli errori

| Stato HTTP | Significato                                              |
| ---------- | -------------------------------------------------------- |
| 200        | Firma applicata con successo.                            |
| 400        | Richiesta non valida – parametri mancanti o non validi. |
| 401        | Non autorizzato – token OAuth non valido o scaduto.     |
| 403        | Accesso negato – autorizzazioni insufficienti.          |
| 500        | Errore interno del server – errore imprevisto.          |

### Risposte di errore con codice HTTP

| Stato HTTP | Codice              | Descrizione                                                 |
| ---------- | ------------------- | ----------------------------------------------------------- |
| 400        | BadRequest          | Parametri mancanti o non validi.                            |
| 401        | Unauthorized        | Token di accesso non valido o mancante.                     |
| 404        | NotFound            | Libro specificato non trovato nella cartella/storage indicata. |
| 500        | InternalServerError | Errore imprevisto del server.                               |


## Come utilizzare l'API PostDigitalSignature con gli SDK

### Specifica dell'API PostDigitalSignature

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Protection/PostDigitalSignature) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per chiamare i servizi web di Aspose.Cells. L'esempio riportato di seguito mostra una richiesta all'API:

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/digitalsignature?digitalsignaturefile=signature.pfx&password=LaTuaPassword" \
  -X POST \
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

**Schema della risposta**  
L'API restituisce un oggetto JSON con i seguenti campi:

| Campo          | Tipo   | Descrizione                                              |
| -------------- | ------ | -------------------------------------------------------- |
| `Code`         | int    | Codice di stato simile a HTTP che indica il risultato.  |
| `Status`       | string | Testo breve che descrive l'esito (ad esempio, `OK`).     |
| `SignatureId`  | string | Identificativo della firma digitale applicata (opzionale).|
| `Message`      | string | Informazioni aggiuntive o dettagli sull'errore (opzionale).|

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK semplifica l'integrazione e riduce il codice ripetitivo. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostDigitalSignature.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostDigitalSignature.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostDigitalSignature.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostDigitalSignature.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82a2de2e4189bc27ae92abf73c36b4df0" "Example_PostDigitalSignature.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostDigitalSignature.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostDigitalSignature.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostDigitalSignature.go" >}}

{{< /tab >}}

{{< /tabs >}}