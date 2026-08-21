---
title: "Rimuovi protezione dal workbook Excel – Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "Rimuovi protezione dal file Excel"
type: docs
url: /it/excel-file-unprotect/
aliases:
  - /unprotect-excel-workbooks/
  - /workbook/unprotect/
keywords: "Aspose Cells, API per rimuovere protezione Excel, rimuovi protezione workbook, API REST, foglio di calcolo cloud"
description: "Scopri come rimuovere la protezione da un workbook Excel utilizzando l'API REST di Aspose.Cells Cloud. Include la sintassi della richiesta, i parametri, un esempio cURL e codice SDK in diversi linguaggi."
weight: 60
ArticleTitle: "Rimuovi protezione dal workbook Excel – Aspose.Cells Cloud API"
---

Utilizza questa API REST per rimuovere la protezione da un workbook Excel.

## API DeleteUnProtectWorkbook

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/protection
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri del percorso

| Parametro | Tipo   | Descrizione                                              | Obbligatorio |
| --------- | ------ | -------------------------------------------------------- | ------------ |
| **name**  | string | Nome del file workbook (inclusa l'estensione).           | Sì           |

### Parametri di query

| Nome parametro | Tipo   | Descrizione                                                  |
| -------------- | ------ | ------------------------------------------------------------ |
| folder         | string | Percorso della cartella contenente il workbook originale.   |
| storageName    | string | Nome del servizio di archiviazione in cui risiede il workbook. |

### Parametri del corpo della richiesta

| Nome parametro | Tipo                      | Descrizione                                               |
| -------------- | ------------------------- | --------------------------------------------------------- |
| protection     | WorkbookProtectionRequest | Oggetto che specifica le impostazioni di protezione da rimuovere. |

#### WorkbookProtectionRequest

| Nome parametro | Tipo   | Descrizione                                                                                           |
| -------------- | ------ | ----------------------------------------------------------------------------------------------------- |
| ProtectionType | string | Tipo di protezione da rimuovere (`ALL`, `CONTENTS`, `NONE`, `OBJECTS`, `SCENARIOS`, `STRUCTURE`, `WINDOWS`). |
| Password       | string | Password richiesta per rimuovere la protezione (opzionale).                                          |

#### Esempio cURL

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/protection?folder=MyFolder&storageName=MyStorage" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -d '{ "ProtectionType": "ALL", "Password": "aspose"}'
```

#### Risposta (successo)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Risposte di errore HTTP

| Stato HTTP | Codice                | Descrizione                                                 |
| ---------- | --------------------- | ----------------------------------------------------------- |
| 400        | BadRequest            | Parametri mancanti o non validi.                            |
| 401        | Unauthorized          | Token di accesso non valido o mancante.                     |
| 404        | NotFound              | Workbook specificato non trovato nella cartella/archiviazione fornita. |
| 500        | InternalServerError   | Errore imprevisto del server.                               |

## Come utilizzare l'API DeleteUnProtectWorkbook con gli SDK

### Specifica dell'API DeleteUnProtectWorkbook

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Protection/DeleteUnProtectWorkbook) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

### Utilizzo degli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK semplifica l'integrazione e riduce il codice ripetitivo. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteUnProtectWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteUnProtectWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteUnProtectWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteUnProtectWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteUnProtectWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteUnProtectWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteUnProtectWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteUnProtectWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
---