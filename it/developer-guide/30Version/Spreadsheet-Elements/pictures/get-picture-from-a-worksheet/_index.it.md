---
title: "Recupera tutte le immagini in un foglio di lavoro Excel"
second_title: "Documento"
linktitle: "Ottieni tutte"
type: docs
url: /it/pictures/get-all/
aliases: [/it/get-picture-from-a-worksheet/]
keywords: "Aspose.Cells Cloud, foglio di lavoro Excel, API immagini, recupera tutte le immagini, REST API, SDK"
description: "Recupera tutti gli oggetti immagine da un foglio di lavoro Excel tramite l'API REST Aspose.Cells Cloud."
ArticleTitle: "Recupera tutte le immagini in un foglio di lavoro Excel - Aspose.Cells Cloud API"
weight: 10
---

Questa REST API recupera tutte le informazioni sulle immagini da un foglio di lavoro Excel.

**Prerequisiti**  
Prima di chiamare questo endpoint, assicurati di disporre di:

- Un token di accesso JWT valido di Aspose Cloud.  
- Il file Excel di destinazione caricato nello storage selezionato.  
- Il nome dello storage corretto (se si utilizza uno storage personalizzato).  
- Il nome del foglio di lavoro contenente le immagini.

## API GetWorksheetPictures

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

**Nota:** Utilizza HTTPS (TLS 1.2 o versione successiva) durante la chiamata all’API e includi un token JWT valido nell’header `Authorization`.

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l’<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### **Parametri della richiesta**

| Nome parametro | Tipo   | Posizione | Descrizione                                           |
| -------------- | ------ | --------- | ----------------------------------------------------- |
| name           | string | path      | Il nome del file Excel.                               |
| sheetName      | string | path      | Il nome del foglio di lavoro contenente le immagini. |
| folder         | string | query     | Il percorso della cartella in cui è archiviato il file. |
| storageName    | string | query     | Il nome del servizio di archiviazione.                |

### Risposte di errore

| Codice HTTP | Descrizione                                                               |
| ----------- | ------------------------------------------------------------------------- |
| 401         | Non autorizzato – token mancante o non valido.                            |
| 404         | Non trovato – il file, il foglio di lavoro o l'indice di interruzione di pagina specificato non esiste. |
| 400         | Richiesta non valida – sintassi della richiesta errata o parametri non validi. |
| 500         | Errore interno del server – si è verificata una condizione imprevista.   |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Pictures/GetWorksheetPictures) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Pictures": {
    "PictureList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/1",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/2",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      }
    ],
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet2/pictures",
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

**Risposta di successo** – Una chiamata riuscita restituisce HTTP 200 con un payload JSON contenente un oggetto `Pictures` che elenca il link di risorsa di ciascuna immagine.

## Famiglia di SDK Cloud

Utilizzare un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli a basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

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

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetPictureWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetPictureWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetPictureWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetPictureWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetPictureWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}

Puoi scaricare gli SDK direttamente dai rispettivi gestori di pacchetti (ad esempio, NuGet per .NET, Maven Central per Java, Composer per PHP, npm per Node.js, PyPI per Python, CPAN per Perl e Go modules per Go).  

*Vedi anche:* Aggiungi un’immagine, Elimina un’immagine, Aggiorna le proprietà dell’immagine.