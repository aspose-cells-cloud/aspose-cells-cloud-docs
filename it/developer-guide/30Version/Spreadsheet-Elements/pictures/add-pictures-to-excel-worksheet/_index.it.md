---
title: "Aggiungi un'immagine in un file Excel"
second_title: "Documento"
linktitle: "Aggiungi"
type: docs
url: /it/pictures/add/
aliases: [  /it/add-pictures-to-excel-worksheet/ ]
keywords: "Aspose.Cells, Excel, aggiungi immagine, API REST"
description: "Usa l'API REST di Aspose.Cells Cloud per aggiungere un'immagine a un foglio di lavoro Excel. Gli SDK per Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby e Swift semplificano l'integrazione multipiattaforma."
weight: 20
ArticleTitle: "Aggiungi un'immagine a un foglio di lavoro Excel – Aspose.Cells Cloud API"
---

Questa API REST aggiunge una nuova immagine a un foglio di lavoro Excel.  
**Prerequisiti:** È necessario disporre di un token di autenticazione valido di Aspose Cloud, di un foglio di lavoro esistente archiviato in un'archiviazione supportata e delle opportune autorizzazioni per modificare il foglio di lavoro.

## API PutWorksheetAddPicture

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro   | Tipo    | Posizione | Descrizione                                                                                  |
| ---------------- | ------- | -------- | -------------------------------------------------------------------------------------------- |
| name             | string  | path     | Nome del foglio di lavoro.                                                                   |
| sheetName        | string  | path     | Nome del foglio di lavoro.                                                                   |
| picture          | object  | body     | Oggetto immagine (dati binari).                                                              |
| upperLeftRow     | integer | query    | Indice iniziale a zero della riga superiore sinistra in cui posizionare l'immagine.          |
| upperLeftColumn  | integer | query    | Indice iniziale a zero della colonna superiore sinistra in cui posizionare l'immagine.       |
| lowerRightRow    | integer | query    | Indice iniziale a zero della riga inferiore destra dell'area dell'immagine.                  |
| lowerRightColumn | integer | query    | Indice iniziale a zero della colonna inferiore destra dell'area dell'immagine.               |
| picturePath      | string  | query    | Percorso del file immagine; se omesso, i dati dell'immagine devono essere forniti nel corpo della richiesta. |
| folder           | string  | query    | Cartella contenente il foglio di lavoro.                                                     |
| storageName      | string  | query    | Nome del servizio di archiviazione.                                                          |

**Nota sul corpo della richiesta:** Quando `picturePath` è omesso, inviare i dati binari dell'immagine nel corpo della richiesta utilizzando `multipart/form-data`.

### Codici di stato HTTP

| Codice | Significato                 | Descrizione                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad es. tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante.                |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server   | Errore imprevisto sul server.                   |

**Esempio di schema di risposta 200**

```json
{
  "Code": 200,
  "Status": "OK",
  "PictureUrl": "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/1"
}
```

**Nota:** La dimensione massima dell'immagine è di 10 MB; i file più grandi verranno rifiutati con una risposta `400 Bad Request`.

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Pictures/PutWorksheetAddPicture) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.com/v1.1/cells/Sample_Test_Book.xls/worksheets/Sheet6/pictures?picturePath=aspose-cloud.png" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Famiglia di SDK Cloud

L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetAddPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetAddPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetAddPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetAddPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82deb4189bc27ae92abf73c36b4df0" "Example_PutWorksheetAddPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetAddPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetAddPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetAddPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Nota:** I formati di immagine supportati includono PNG, JPEG, BMP e GIF. La dimensione massima dell'immagine è di 10 MB; i file più grandi verranno rifiutati con una risposta `400 Bad Request`.