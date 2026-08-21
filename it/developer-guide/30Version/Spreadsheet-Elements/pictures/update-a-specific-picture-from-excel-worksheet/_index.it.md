---
title: "Aggiorna immagine in un file Excel"
second_title: "Documento"
linktitle: "Aggiorna"
type: docs
url: /it/pictures/update/
aliases: [  /it/update-a-specific-picture-from-excel-workshee/ ]
keywords: "Aspose.Cells Cloud, Excel, Aggiorna immagine, REST API, SDK"
description: "Scopri come aggiornare un'immagine in un foglio di lavoro Excel utilizzando l'API REST di Aspose.Cells Cloud. Include dettagli sulla richiesta, un esempio cURL e frammenti di codice SDK per diversi linguaggi."
ArticleTitle: "Aggiorna immagine in un file Excel utilizzando l'API REST di Aspose.Cells Cloud"
weight: 70
---

Questa API REST aggiorna un'immagine, identificata dal suo indice, in un foglio di lavoro Excel.

**Prerequisiti:** È necessario possedere un token JWT valido di Aspose Cloud, il file Excel target archiviato nell'archivio Aspose Cloud e utilizzare la versione API 3.0 o successiva.

## API PostWorksheetPicture

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### **Parametri della richiesta**

| Nome parametro | Tipo    | Posizione | Descrizione                                                  |
| -------------- | ------- | -------- | ------------------------------------------------------------ |
| name           | string  | path     | Nome del documento Excel.                                    |
| sheetName      | string  | path     | Nome del foglio di lavoro contenente l'immagine.             |
| pictureIndex   | integer | path     | Indice in base zero dell'immagine da aggiornare.             |
| picture        | object  | body     | Oggetto JSON che descrive le proprietà dell'immagine da aggiornare. |
| folder         | string  | query    | Cartella in cui è archiviato il documento.                   |
| storageName    | string  | query    | Nome del servizio di archiviazione.                          |

**Nota:** L'indice dell'immagine è in base zero. I formati di immagine supportati includono JPEG, PNG, BMP e GIF. La dimensione massima dell'immagine è di 10 MB.

### Risposte di errore

| Codice HTTP | Descrizione                                            |
| ----------- | ------------------------------------------------------ |
| 401         | Non autorizzato – token mancante o non valido.         |
| 404         | Non trovato – il file, il foglio di lavoro o l'indice dell'immagine specificati non esistono. |
| 400         | Richiesta non valida – sintassi della richiesta non corretta o parametri non validi. |
| 500         | Errore interno del server – si è verificata una condizione imprevista. |

La <a href="https://apireference.aspose.cloud/cells/#/Pictures/PostWorksheetPicture" rel="noopener noreferrer">Specifiche OpenAPI</a> definiscono un'interfaccia di programmazione pubblicamente accessibile e permettono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare una chiamata all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures/1" \
-X POST \
-d "{ \"UpperLeftRow\": 10, \"Top\": 0, \"UpperLeftColumn\": 1, \"Left\": 0, \"LowerRightRow\": 0, \"Bottom\": 0, \"LowerRightColumn\": 3, \"ImageFormat\": \"jpg\", \"SourceFullName\": \"download.jpg\"}" \
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

Utilizzare un SDK è il modo più rapido per sviluppare. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}

*Vedi anche:* Aggiungi immagine, Elimina immagine, Ottieni immagine, Pulisci immagini – altre operazioni relative alle immagini nell'API Aspose.Cells Cloud.