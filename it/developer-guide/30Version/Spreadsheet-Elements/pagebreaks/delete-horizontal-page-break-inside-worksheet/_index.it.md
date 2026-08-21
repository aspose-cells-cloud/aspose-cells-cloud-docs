---
title: "Elimina interruzione di pagina orizzontale"
ArticleTitle: "Aspose.Cells Cloud – Elimina interruzione di pagina orizzontale (REST API)"
second_title: "Documento"
linktitle: "Elimina interruzione di pagina orizzontale"
type: docs
url: /page-breaks/delete-horizontal-page-break/
aliases: [/delete-horizontal-page-break-inside-worksheet/]
keywords: "Aspose.Cells Cloud, Elimina interruzione di pagina orizzontale, foglio Excel, REST API, SDK"
description: "Elimina un’interruzione di pagina orizzontale da un foglio Excel utilizzando l’API REST di Aspose.Cells Cloud. SDK disponibili per C#, Java, PHP, Ruby, Node.js, Python, Perl, Go."
weight: 50
---

Questa API REST elimina un’**interruzione di pagina orizzontale**.

**Prerequisiti**: Per chiamare questo endpoint devi possedere un token di accesso JWT valido di Aspose Cloud. Ottienilo seguendo la [Guida all’autenticazione](https://docs.aspose.cloud/cells/authentication/).

## API DeleteHorizontalPageBreak

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks/{index}
```

*Tutte le chiamate API devono essere effettuate tramite **HTTPS**.*

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l’<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro | Tipo    | Posizione | Descrizione                                                         |
|----------------|---------|-----------|---------------------------------------------------------------------|
| `name`         | stringa | path      | Nome del file Excel (cartella di lavoro).                          |
| `sheetName`    | stringa | path      | Nome del foglio di lavoro contenente l’interruzione di pagina.     |
| `index`        | intero  | path      | Indice in base zero dell’interruzione di pagina orizzontale da eliminare. |
| `folder`       | stringa | query     | Percorso facoltativo della cartella nello storage dove si trova il file. |
| `storageName`  | stringa | query     | Nome facoltativo del servizio di storage.                          |

### Risposte di errore

| Codice HTTP | Descrizione                                                           |
|-------------|-----------------------------------------------------------------------|
| 401         | Non autorizzato – token mancante o non valido.                       |
| 404         | Non trovato – il file, il foglio di lavoro o l’indice dell’interruzione di pagina specificati non esistono. |
| 400         | Richiesta non valida – sintassi della richiesta errata o parametri non validi. |
| 500         | Errore interno del server – si è verificata una condizione imprevista. |

**Vedi anche:**  
- [Aggiungi interruzione di pagina orizzontale](/page-breaks/add-horizontal-page-break/)  
- [Ottieni interruzioni di pagina orizzontali](/page-breaks/get-horizontal-page-breaks/)  
- [Elimina interruzione di pagina verticale](/page-breaks/delete-vertical-page-break/)

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/PageBreaks/DeleteHorizontalPageBreak) definiscono un’interfaccia di programmazione pubblicamente accessibile e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando **cURL** per accedere facilmente ai servizi web di Aspose.Cells. L’esempio seguente mostra come effettuare la chiamata con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/horizontalpagebreaks/0" \
  -X DELETE \
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

**Schema della risposta**

| Campo   | Tipo    | Descrizione                                     |
|---------|---------|-------------------------------------------------|
| Code    | intero  | Codice di stato HTTP (es., 200).                |
| Status  | stringa | Messaggio di stato testuale (es., "OK").        |
| Message | stringa | Informazioni aggiuntive facoltative per casi di errore. |

{{< /tab >}}

{{< /tabs >}}

## Famiglia di SDK per il cloud

Utilizzare un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli a basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteHorizontalPageBreak.cs" >}}
*Se l’esempio non si carica, visualizzalo sul [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/8a5b324fdf3e574dbd747c1a1e24b05d).*

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteHorizontalPageBreak.java" >}}
*Se l’esempio non si carica, visualizzalo sul [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/c59aa5c02f735466a5e34751cee73f5f).*

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteHorizontalPageBreak.php" >}}
*Se l’esempio non si carica, visualizzalo sul [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/84283c8ba766ed815f47e6dfb0891152).*

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteHorizontalPageBreak.rb" >}}
*Se l’esempio non si carica, visualizzalo sul [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/36ed8b8727561b92692939513d365fca).*

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteHorizontalPageBreak.ts" >}}
*Se l’esempio non si carica, visualizzalo sul [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/e82de2e4189bc27ae92abf73c36b4df0).*

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteHorizontalPageBreak.py" >}}
*Se l’esempio non si carica, visualizzalo sul [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/61e922de11e6e7144db88adcad6501c1).*

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteHorizontalPageBreak.pl" >}}
*Se l’esempio non si carica, visualizzalo sul [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/f82a3a00251e34ff8766116282c8c9ca).*

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteHorizontalPageBreak.go" >}}
*Se l’esempio non si carica, visualizzalo sul [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/2b824d4e13644368d12682856aa49185).*

{{< /tab >}}

{{< /tabs >}}