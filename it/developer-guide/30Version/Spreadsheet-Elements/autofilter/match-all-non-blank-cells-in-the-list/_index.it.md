---
title: "Confronta tutte le celle non vuote in un foglio di lavoro Excel"
second_title: "Documento"
linktitle: "Confronta tutte le celle non vuote"
type: docs
url: /it/autofilter/match-all-non-blank/
aliases: [  /it/match-all-non-blank-cells-in-the-list/ ]
keywords: "Aspose.Cells Cloud, confronta celle non vuote, AutoFilter, API Excel"
description: "Scopri come utilizzare l'API REST di Aspose.Cells Cloud per confrontare tutte le celle non vuote in un elenco AutoFilter su un foglio di lavoro Excel. Include endpoint, parametri, autenticazione, schema di risposta, codici di errore ed esempi di SDK."
ArticleTitle: "Confronta tutte le celle non vuote in un foglio di lavoro Excel utilizzando l'API Aspose.Cells Cloud"
weight: 100
---

**Panoramica**  
L'operazione *Confronta tutte le celle non vuote* applica un filtro automatico (AutoFilter) a un foglio di lavoro e restituisce solo le righe in cui la colonna specificata contiene dati, ignorando le celle vuote. Questo è utile per pulire set di dati, generare report o preparare i dati per ulteriori analisi.

**Prerequisiti**  
- Un token JWT valido per l'autenticazione con Aspose.Cells Cloud.  
- Il libro deve essere caricato nell'archivio Aspose Cloud.  
- È necessario il nome del file, il nome del foglio di lavoro e l'indice zero-based (`fieldIndex`) della colonna da filtrare.

Questa API REST confronta tutte le celle non vuote nell'elenco AutoFilter su un foglio di lavoro Excel.

## API PostWorksheetMatchNonBlanks

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/matchNonBlanks
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro | Tipo    | Posizione | Descrizione                                                    |
| -------------- | ------- | -------- | -------------------------------------------------------------- |
| name           | string  | path     | Nome del file Excel.                                           |
| sheetName      | string  | path     | Nome del foglio di lavoro contenente l'AutoFilter.             |
| fieldIndex     | integer | query    | Indice zero-based della colonna a cui viene applicato il filtro. |
| folder         | string  | query    | _(Opzionale)_ Percorso della cartella in cui è memorizzato il file. |
| storageName    | string  | query    | _(Opzionale)_ Nome del servizio di archiviazione da utilizzare. |

### **Risposta**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante. |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server   | Errore imprevisto del server. |

*Esempio di risposta di errore (400)*  

```json
{
  "Code": 400,
  "Message": "Parametro non valido: fieldIndex deve essere un intero non negativo."
}
```

## Come utilizzare l'API PostWorksheetMatchNonBlanks con gli SDK

### Specifica dell'API PostWorksheetMatchNonBlanks

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PostWorksheetMatchNonBlanks) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare direttamente interazioni REST da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/matchNonBlanks?fieldIndex=0" \
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

### Utilizzo degli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMatchNonBlanks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMatchNonBlanks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMatchNonBlanks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMatchNonBlanks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMatchNonBlanks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMatchNonBlanks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMatchNonBlanks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMatchNonBlanks.go" >}}

{{< /tab >}}

{{< /tabs >}}