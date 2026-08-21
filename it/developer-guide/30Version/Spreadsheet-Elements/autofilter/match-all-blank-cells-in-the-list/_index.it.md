---
title: "Rileva tutte le celle vuote in un foglio di lavoro Excel"
ArticleTitle: "Rileva tutte le celle vuote in un foglio di lavoro Excel – Guida API Aspose.Cells Cloud"
second_title: "Documento"
linktitle: "Rileva tutte le celle vuote"
type: docs
url: /autofilter/match-all-blank/
aliases: [/match-all-blank-cells-in-the-list/]
keywords: "Aspose.Cells, celle vuote, AutoFilter, API REST, Excel"
description: "Scopri come utilizzare l'API REST Aspose.Cells Cloud per filtrare e rilevare tutte le celle vuote in un foglio di lavoro Excel. Include endpoint, parametri, fasi di autenticazione, esempio cURL e frammenti di codice SDK per C#, Java, Python e altro."
weight: 100
---

Questa API REST rileva tutte le **celle vuote** nell'elenco di filtraggio in un foglio di lavoro Excel.

**Prerequisiti:** Prima di chiamare questo endpoint, assicurati di avere un token di accesso JWT valido, che il file di lavoro sia caricato nello storage di Aspose Cloud e che conosci la cartella di storage (se applicabile). Fornisci i parametri `folder` e `storageName` qualora il file non si trovi nella root predefinita.

## API PostWorksheetMatchBlanks

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/matchBlanks
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.


### Parametri della richiesta

| Nome parametro | Tipo    | Posizione | Descrizione                                                           |
|----------------|---------|-----------|-----------------------------------------------------------------------|
| name           | string  | path      | Nome del file di lavoro.                                              |
| sheetName      | string  | path      | Nome del foglio di lavoro contenente il filtro.                       |
| fieldIndex     | integer | query     | Indice in base zero della colonna a cui viene applicato il filtro.    |
| folder         | string  | query     | Percorso della cartella nello storage in cui si trova il file di lavoro. |
| storageName    | string  | query     | Nome dello storage di Aspose Cloud.                                    |

### **Risposta**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Codici di stato HTTP**

| Codice | Significato                  | Descrizione                                                   |
|--------|------------------------------|---------------------------------------------------------------|
| 200    | OK                           | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida         | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato              | Token JWT non valido o mancante.                               |
| 413    | Payload troppo grande        | Il file caricato supera il limite di dimensione.              |
| 500    | Errore interno del server    | Errore imprevisto del server.                                 |
## Come utilizzare l'API PostWorksheetMatchBlanks con gli SDK

### Specifica dell'API PostWorksheetMatchBlanks

La [specifica OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PostWorksheetMatchBlanks) definisce un'interfaccia di programmazione pubblicamente accessibile e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere ai servizi web di Aspose.Cells. L'esempio seguente mostra come chiamare l'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}
```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/matchBlanks?fieldIndex=0" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK nasconde i dettagli a basso livello e ti consente di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMatchBlanks.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMatchBlanks.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMatchBlanks.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMatchBlanks.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMatchBlanks.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMatchBlanks.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMatchBlanks.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMatchBlanks.go" >}}
{{< /tab >}}

{{< /tabs >}}