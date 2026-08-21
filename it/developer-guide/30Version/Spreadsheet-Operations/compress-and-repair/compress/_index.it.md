---
title: "Comprimere dati in un file Excel"
ArticleTitle: "Comprimere dati in un file Excel – Aspose.Cells Cloud API"
second_title: "Documento"
linktype: "Comprimere file Excel"
type: docs
url: /it/compress-excel-files/
aliases: [  /it/compress/ ]
keywords: "comprimere file Excel, Aspose Cells Cloud, compressione Excel, compressione fogli elettronici, API REST, compressione file"
description: "Comprimi file Excel (XLS, XLSX, XLSM, XLSB, ODS) utilizzando l'API REST di Aspose.Cells Cloud. Imposta il livello di compressione, gestisci più file e integra tramite SDK."
weight: 39
---

## L'API PostCompress dei servizi web Aspose.Cells Cloud

**Prerequisiti:**  
- È richiesto un token JWT valido per l'autenticazione.  
- I formati di file supportati sono XLS, XLSX, XLSM, XLSB e ODS.  
- La dimensione massima consentita per file è di 500 MB per richiesta (soggetta ai limiti del servizio).

Questa API REST comprime i dati in un file Excel.

- Comprimi XLS, XLSX, XLSM, XLSB, ODS  
- Comprimi rapidamente più file di fogli elettronici Excel  
- Scegli il livello di compressione  
- Supporta più file  

### Endpoint dell'API Web

```http
POST https://api.aspose.cloud/v3.0/cells/compress
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro | Tipo    | Percorso/Query string/Corpo HTTP | Descrizione                                     |
|----------------|---------|----------------------------------|-------------------------------------------------|
| file           | file    | formData                         | File da caricare                                |
| CompressLevel  | integer | query                            | Livello di compressione (0‑100); valori più alti indicano una compressione più intensa |

### Parametro del corpo della richiesta

| Nome parametro | Tipo | Descrizione                                    |
| -------------- | ---- | ---------------------------------------------- |
| data           | file | Contenuto binario del file del workbook da comprimere. |

### **Risposta**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[nome file unito]",
    "Filesize" : [dimensione file],
    "FileContent" : "[Base64String]"
}
```

*Nota:* `FileContent` contiene il workbook compresso codificato in stringa Base64. La lunghezza della stringa corrisponde alla dimensione del file compresso; puoi decodificarla utilizzando strumenti standard Base64 per recuperare il file Excel in formato binario.

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                            |
|--------|-----------------------------|--------------------------------------------------------|
| 200  | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400  | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401  | Non autorizzato             | Token JWT non valido o mancante. |
| 413  | Payload troppo grande       | Il file caricato supera il limite di dimensione. |
| 500  | Errore interno del server   | Errore imprevisto nel server. |

## Come utilizzare l'API PostCompress con gli SDK

### Specifica dell'API PostCompress

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostCompress) definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
# Utilizzare HTTPS per una connessione sicura
curl -v "https://api.aspose.cloud/v3.0/cells/compress?CompressLevel=88" \
-X POST \
-H "Content-Type: multipart/form-data" \
-H "Accept: application/json" \
-H "Authorization: Bearer <token jwt>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'
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

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK rappresenta il modo più rapido per accelerare lo sviluppo. Un SDK astrae i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCompress.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCompress.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCompress.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCompress.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCompress.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCompress.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCompress.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCompress.go" >}}

{{< /tab >}}

{{< /tabs >}}