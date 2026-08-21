---
title: "Aspose.Cells Cloud API – Ottieni immagine da foglio di calcolo"
second_title: "Documento"
linktitle: "Ottieni"
type: docs
url: /it/pictures/get/
aliases: [  /it/convert-picture-to-image/ ]
keywords: "Aspose.Cells, Ottieni immagine, API, Excel, Cloud, REST"
description: "Recupera una specifica immagine da un foglio di calcolo Excel utilizzando l'API REST di Aspose.Cells Cloud. Include endpoint, parametri, fasi di autenticazione, codici di risposta ed esempi di codice."
weight: 10
ArticleTitle: "Aspose.Cells Cloud API – Ottieni immagine da foglio di calcolo"
---

Questa REST API recupera un’immagine tramite il suo indice in base zero da un foglio di calcolo Excel.

## API REST

Per chiamare questo endpoint è necessario includere un token di accesso JWT valido nell'header **Authorization**. I token vengono ottenuti tramite il flusso di autenticazione di Aspose.Cells Cloud e richiedono gli ambiti appropriati per l'accesso ai file. Per ulteriori dettagli sull'acquisizione di un token, consulta la guida globale **Autenticazione**.

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}
```

### Parametri della richiesta

| Nome parametro | Tipo    | Posizione | Descrizione                                                                                                         |
| -------------- | ------- | --------- | ------------------------------------------------------------------------------------------------------------------- |
| name           | string  | path      | Nome del documento Excel.                                                                                           |
| sheetName      | string  | path      | Nome del foglio di calcolo.                                                                                         |
| pictureIndex   | integer | path      | Indice in base zero dell'immagine.                                                                                  |
| format         | string  | query     | Formato di esportazione desiderato (ad esempio, png, jpg, bmp, gif, tiff). Se omesso, l'immagine viene restituita nel formato originale. |
| folder         | string  | query     | Cartella contenente il documento.                                                                                   |
| storageName    | string  | query     | Nome della posizione di archiviazione.                                                                              |

### Risposte di errore

| Codice HTTP | Descrizione                                                           |
| ----------- | --------------------------------------------------------------------- |
| 401         | Non autorizzato – token mancante o non valido.                        |
| 404         | Non trovato – il file, il foglio di calcolo o l'indice di interruzione di pagina specificati non esistono. |
| 400         | Richiesta non valida – sintassi della richiesta non corretta o parametri non validi. |
| 500         | Errore interno del server – si è verificata una condizione imprevista. |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Pictures/GetWorksheetPicture) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di eseguire interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come chiamare l'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures/1?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```bash
# Dati dell'immagine binaria (PNG) restituiti nel corpo della risposta.
# Esempio: frammento in base64
iVBORw0KGgoAAAANSUhEUgAA...
```

{{< /tab >}}

{{< /tabs >}}

## Famiglia di SDK Cloud

Utilizzare un SDK è il modo più rapido per sviluppare. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sul tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetPictureWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetPictureWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetPictureWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "ExampleGetWorksheetPictureWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "ExampleGetWorksheetPictureWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ExampleGetWorksheetPictureWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "ExampleGetWorksheetPictureWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "ExampleGetWorksheetPictureWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}
---