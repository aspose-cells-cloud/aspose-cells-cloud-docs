---
title: "Ottenere i nomi da un workbook Excel"
second_title: "Documento"
linktitle: "Nomi"
type: docs
url: /get-names-from-an-excel-file/
aliases:
  [
    /get-names-count-from-excel-workbooks/,
    /workbook/names/,
    /workbook/get/names/,
  ]
keywords: "Aspose.Cells, Cloud, Excel, Workbook, Nomi, REST API, SDK"
description: "Recupera tutti i nomi definiti da un workbook Excel utilizzando l'API REST di Aspose.Cells Cloud. Include indicazioni sull'autenticazione, un esempio cURL, lo schema di risposta, la gestione degli errori e esempi di SDK."
weight: 120
ArticleTitle: "Ottenere i nomi da un workbook Excel – Aspose.Cells Cloud API"
---

Questa API REST recupera i nomi definiti da un workbook Excel.

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione tramite token JWT</a>.

## API GetWorkbookNames

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/names
```

I parametri della richiesta sono:

| Nome parametro | Tipo   | Posizione | Descrizione                             |
| -------------- | ------ | --------- | --------------------------------------- |
| name           | string | path      | Nome del file del workbook.             |
| folder         | string | query     | Cartella contenente il workbook.        |
| storageName    | string | query     | Nome dello storage da utilizzare.       |

La richiesta deve includere le seguenti intestazioni HTTP:

| Intestazione  | Tipo   | Descrizione                                   |
|---------------|--------|-----------------------------------------------|
| Authorization | string | Token bearer JWT (obbligatorio)               |
| Accept        | string | `application/json`                            |
| Content-Type  | string | `application/json` (per richieste con corpo) |

**Autenticazione** – L'API richiede un token bearer OAuth2/JWT. Ottenere un token da `https://api.aspose.cloud/connect/token` utilizzando il proprio client‑id e client‑secret, quindi includere l'intestazione `Authorization: Bearer <jwt token>` in ogni richiesta.

La [specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkbookNames) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere ai servizi web di Aspose.Cells. L'esempio seguente mostra come chiamare l'API Aspose.Cells Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/names" \
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
  "Names": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "Count": 0,
    "NameList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        }
      }
    ]
  }
}
```

_Campi della risposta_

- **Status** _(string)_ – Messaggio di stato dell'operazione.
- **Names.link** _(object)_ – Informazioni sull'hyperlink della raccolta.
- **Names.Count** _(integer)_ – Numero totale di nomi definiti restituiti.
- **Names.NameList** _(array)_ – Elenco di oggetti nome; ogni oggetto contiene un oggetto **link** con i dettagli di navigazione.

**Gestione degli errori** – Il servizio può restituire i seguenti codici di stato HTTP:

| Codice | Significato            | Azione consigliata                                           |
| ------ | ---------------------- | ------------------------------------------------------------ |
| 401    | Non autorizzato        | Verificare che sia stato fornito un token JWT valido.        |
| 404    | Non trovato            | Verificare che il nome del workbook, la cartella e lo storage siano corretti. |
| 500    | Errore interno del server | Riprovare più tardi o contattare il supporto Aspose se il problema persiste. |

{{< /tab >}}

{{< /tabs >}}

## Famiglia di SDK Cloud

Utilizzare un SDK è il modo più rapido per sviluppare. Un SDK gestisce i dettagli di basso livello, consentendovi di concentrarvi sul vostro progetto. Consultate il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbookNames.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbookNames.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbookNames.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbookNames.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbookNames.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbookNames.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbookNames.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbookNames.go" >}}

{{< /tab >}}

{{< /tabs >}}
---