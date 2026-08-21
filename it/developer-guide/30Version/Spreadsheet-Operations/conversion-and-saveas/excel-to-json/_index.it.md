---
title: "Excel in JSON"
second_title: "Documenti"
linktype: "Excel in JSON"
type: docs
url: /convert-excel-file-to-json-file/
keywords: "Aspose.Cells, Excel in JSON, API cloud, conversione foglio di calcolo, API REST"
description: "Scopri come convertire fogli di calcolo Excel in file JSON tramite l'API REST di Aspose.Cells Cloud. Include esempio cURL, frammenti SDK (C#, Java, Python), parametri richiesti, autenticazione e formato della risposta."
weight: 100
ArticleTitle: "Converti Excel in JSON usando l'API REST di Aspose.Cells Cloud – Guida rapida"
---

## API REST

Questa API REST converte un file di foglio di calcolo in un file in formato JSON.

```http
POST https://api.aspose.cloud/v3.0/cells/convert/json
```

### Sicurezza e autenticazione

Le API REST di Aspose.Cells Cloud sono sicure e richiedono [autenticazione basata su token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Richiesta

**Parametri di query**

| Nome del parametro      | Tipo   | Descrizione                                                                 |
| ----------------------- | ------ | --------------------------------------------------------------------------- |
| `password`              | string | Password necessaria per aprire il file Excel (opzionale).                  |
| `storageName`           | string | Nome dello storage in cui si trova il file (opzionale).                    |
| `checkExcelRestriction` | bool   | Applica restrizioni specifiche di Excel alla modifica delle celle (opzionale). |

**Parametro nel corpo della richiesta**

| Nome del parametro | Tipo | Descrizione                                                                                              |
| ------------------ | ---- | -------------------------------------------------------------------------------------------------------- |
| `datafile`         | file | Il file Excel da caricare. Deve essere inviato come prima parte di una richiesta `multipart/form-data`. |

#### Esempio di chiamata cURL

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/json" \
     -H "Authorization: Bearer $ACCESS_TOKEN" \
     -H "accept: application/json" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@myWorkbook.xlsx"
```

### Risposta

Il servizio restituisce un oggetto **FileInfo**. I campi principali sono descritti di seguito:

| Campo         | Tipo    | Descrizione                                                                     |
| ------------- | ------- | ------------------------------------------------------------------------------- |
| `Filename`    | string  | Nome del file JSON generato (ad esempio, `myWorkbook.json`).                    |
| `FileSize`    | integer | Dimensione del file generato in byte.                                           |
| `FileContent` | string  | Contenuto del file JSON codificato in Base64. Decodificarlo per ottenere il JSON effettivo. |

**Esempio di risposta**

```json
{
  "Filename": "myWorkbook.json",
  "FileSize": 8423,
  "FileContent": "eyJmb3JtYXR0ZWRfZGF0YSI6IH ... (stringa in base64) ..."
}
```

#### Gestione degli errori

Se la richiesta ha esito negativo, l'API restituisce un oggetto di errore con la seguente struttura:

| Campo     | Tipo   | Descrizione                                    |
| --------- | ------ | ---------------------------------------------- |
| `Code`    | string | Identificatore dell'errore leggibile da macchina. |
| `Message` | string | Descrizione leggibile dell'errore.             |

Codici di stato HTTP comuni:

- **400** – Richiesta non valida (ad esempio, file mancante o parametri non validi).
- **401** – Non autorizzato (token di accesso non valido o mancante).
- **500** – Errore interno del server.

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                                              |
|--------|-----------------------------|--------------------------------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante.                                         |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione.                        |
| 500    | Errore interno del server   | Errore imprevisto del server.                                            |

## Come usare l'API PostConvertWorkbookToJson con gli SDK

### Specifica dell'API PostConvertWorkbookToJson

La <a href="https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToJson" rel="noopener noreferrer" title="Specifiche OpenAPI di Aspose.Cells – Converti cartella di lavoro in JSON">Specifiche OpenAPI</a> definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando **cURL** per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/json" \
     -H "Authorization: Bearer $ACCESS_TOKEN" \
     -H "accept: application/json" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@myWorkbook.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "myWorkbook.json",
  "FileSize": 8423,
  "FileContent": "eyJmb3JtYXR0ZWRfZGF0YSI6IH... (stringa in base64)"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK rappresenta il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer" title="SDK di Aspose.Cells Cloud su GitHub">repository GitHub</a> per l'elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToJson.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToJson.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToJson.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToJson.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToJson.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToJson.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToJson.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToJson.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Altre API che implementano funzionalità simili

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Salva un file Excel come file HTML con impostazioni aggiuntive e memorizza il risultato nello storage specificato.
- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Converte un file Excel in un file HTML con impostazioni aggiuntive e restituisce il risultato nella risposta.
- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Recupera un file Excel; può essere utilizzato con parametri di query per ottenere il file in formato HTML.