---
title: "Decrittografa un Workbook di Excel"
second_title: "Documento"
linktitle: "Decrittografa un file Excel"
type: docs
url: /it/excel-file-decrypt/
aliases: [  /it/decrypt-excel-workbooks/ , /it/workbook/decrypt/ ]
keywords: "Aspose.Cells, decrittografia Excel, REST API, SDK cloud"
description: "Scopri come decrittografare un workbook di Excel utilizzando l'API REST di Aspose.Cells Cloud. Include i parametri obbligatori, un esempio cURL, esempi di codice SDK e dettagli sulla gestione degli errori."
ArticleTitle: "Come decrittografare un workbook di Excel usando l'API di Aspose.Cells Cloud"
weight: 50
---

**Prerequisiti**

- Un token di accesso JWT valido.
- Il workbook deve essere caricato nello storage di Aspose Cloud e il suo percorso deve essere specificato nel parametro di query `folder`.

## API DeleteDecryptWorkbook

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/encryption
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### Parametri di Query

| Nome Parametro | Tipo   | Descrizione                                             |
| -------------- | ------ | ------------------------------------------------------- |
| folder         | string | Percorso della cartella del workbook originale.         |
| storageName    | string | Nome dello storage in cui risiede il workbook.          |

### Parametro del Corpo della Richiesta

| Nome Parametro | Tipo                      | Descrizione                                         |
| -------------- | ------------------------- | --------------------------------------------------- |
| encryption     | WorkbookEncryptionRequest | Impostazioni di crittografia necessarie per la decrittografia. |

### WorkbookEncryptionRequest

| Nome Parametro | Tipo    | Descrizione                                                                                                  |
| -------------- | ------- | ------------------------------------------------------------------------------------------------------------ |
| EncryptionType | string  | Algoritmo di crittografia (`XOR`, `Compatible`, `EnhancedCryptographicProviderV1`, `StrongCryptographicProvider`). |
| KeyLength      | integer | Lunghezza della chiave di crittografia in bit.                                                               |
| Password       | string  | Password utilizzata per la decrittografia.                                                                   |

### Risposta

```json
{
  "Status":"OK",
  "Code":200
}
```

**Esempi di Risposte di Errore**

```json
{
  "Code": "400",
  "Message": "Parametri di richiesta non validi."
}
```

```json
{
  "Code": "401",
  "Message": "Autenticazione non riuscita. Token JWT non valido o mancante."
}
```

```json
{
  "Code": "413",
  "Message": "Payload troppo grande. Il file caricato supera la dimensione consentita."
}
```

```json
{
  "Code": "500",
  "Message": "Errore interno del server. Riprovare più tardi."
}
```

**Codici di Stato HTTP**

| Codice | Significato                    | Descrizione                                           |
|--------|--------------------------------|-------------------------------------------------------|
| 200    | OK                             | Filtro applicato con successo; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta Non Valida           | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non Autorizzato                | Token JWT non valido o mancante. |
| 413    | Payload Troppo Grande          | Il file caricato supera il limite di dimensione. |
| 500    | Errore Interno del Server      | Errore imprevisto del server. |

## Come utilizzare l'API DeleteDecryptWorkbook con gli SDK

### Specifica dell'API DeleteDecryptWorkbook

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/DeleteDecryptWorkbook) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare **cURL** per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come chiamare l'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/encryption" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{ "EncryptionType": "XOR", "KeyLength": 1280, "Password": "aspose"}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

### Utilizzare gli SDK di Aspose.Cells Cloud

Utilizzare un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDecryptWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDecryptWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDecryptWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDecryptWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteDecryptWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDecryptWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDecryptWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDecryptWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
---