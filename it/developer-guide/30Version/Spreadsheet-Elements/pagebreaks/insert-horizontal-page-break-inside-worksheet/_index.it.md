---
title: "Aggiungi interruzione di pagina orizzontale"
second_title: "Documento"
linktitle: "Aggiungi interruzione di pagina orizzontale"
type: docs
url: /it/page-breaks/add-horizontal-page-break/
aliases: [  /it/insert-horizontal-page-break-inside-worksheet/ ]
keywords: "interruzione di pagina orizzontale, Aspose.Cells Cloud, Excel API, REST, SDK, foglio di calcolo, cURL"
description: "Scopri come aggiungere un'interruzione di pagina orizzontale a un foglio di calcolo Excel utilizzando l'API REST di Aspose.Cells Cloud. Include i dettagli della richiesta, un esempio cURL e frammenti di codice SDK per diversi linguaggi di programmazione."
weight: 30
ArticleTitle: "Aggiungi interruzione di pagina orizzontale – Aspose.Cells Cloud API"
---

L'API **Aggiungi interruzione di pagina orizzontale** inserisce un'interruzione di pagina orizzontale in un foglio di calcolo Excel.

**Prerequisiti e autenticazione**  
Per tutte le chiamate all'API Aspose.Cells Cloud è necessario un token JWT valido. Ottieni il token tramite il flusso OAuth 2.0 descritto nella guida all'autenticazione e includilo nell'intestazione della richiesta come `Authorization: Bearer <jwt token>`. Il libro di lavoro di destinazione deve trovarsi in una posizione di archiviazione accessibile all'API (archiviazione predefinita o un `storageName` personalizzato da te specificato).

## API PutHorizontalPageBreak

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro | Tipo    | Posizione | Descrizione                                                                 |
| -------------- | ------- | --------- | --------------------------------------------------------------------------- |
| name           | string  | path      | Nome del file Excel.                                                        |
| sheetName      | string  | path      | Nome del foglio di calcolo in cui verrà aggiunta l'interruzione.           |
| cellname       | string  | query     | Riferimento alla cella (es. **A1**) che contrassegna l'inizio dell'interruzione. |
| row            | integer | query     | Indice di riga in base zero per l'interruzione di pagina.                   |
| column         | integer | query     | Indice di colonna in base zero per l'interruzione di pagina.                |
| startColumn    | integer | query     | Colonna iniziale dell'intervallo quando si inserisce un'interruzione.       |
| endColumn      | integer | query     | Colonna finale dell'intervallo quando si inserisce un'interruzione.         |
| folder         | string  | query     | Percorso della cartella contenente il file Excel.                           |
| storageName    | string  | query     | Nome dell'archiviazione Aspose Cloud.                                       |

La <a href="https://apireference.aspose.cloud/cells/#/PageBreaks/PutHorizontalPageBreak" target="_blank" rel="noopener noreferrer">Specifiche OpenAPI</a> definiscono un'interfaccia accessibile pubblicamente che consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando **cURL** per accedere facilmente ai servizi web Aspose.Cells. Il seguente esempio mostra come chiamare l'API con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
# Utilizza HTTPS per garantire una comunicazione crittografata
curl -v "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/horizontalpagebreaks?row=18" \
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

Esempio di risposta di errore quando il token JWT è mancante o non valido:

```json
{
  "Code": 401,
  "Status": "Unauthorized",
  "Message": "Token JWT non valido o mancante."
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                                    |
|--------|-----------------------------|----------------------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (es. tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante.                               |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione.               |
| 500    | Errore interno del server   | Errore imprevisto nel server.                                  |

Per ulteriori dettagli sulle operazioni correlate, consulta le pagine API per **[Ottieni interruzioni di pagina orizzontali](../get-horizontal-page-breaks/)** e **[Elimina interruzione di pagina orizzontale](../delete-horizontal-page-break/)**.

## Famiglia di SDK per il cloud

Utilizzare un SDK rappresenta il modo più rapido per sviluppare. Un SDK astrae i dettagli di basso livello, permettendoti di concentrarti sul tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutHorizontalPageBreak.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutHorizontalPageBreak.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutHorizontalPageBreak.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutHorizontalPageBreak.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutHorizontalPageBreak.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutHorizontalPageBreak.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutHorizontalPageBreak.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutHorizontalPageBreak.go" >}}
{{< /tab >}}

{{< /tabs >}}