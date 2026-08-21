---
title: "Applicare la formattazione del testo ricco a una cella"
type: docs
url: /apply-rich-text-formatting-to-a-cell/
weight: 40
keywords: "Aspose.Cells, Excel, testo ricco, formattazione celle, REST API, Aspose.Cells Cloud"
description: "Scopri come applicare la formattazione del testo ricco a una specifica cella Excel utilizzando l'API REST di Aspose.Cells Cloud. Include la sintassi della richiesta, i dettagli dei parametri, un esempio cURL e frammenti di codice SDK."
ArticleTitle: "Applicare la formattazione del testo ricco a una cella utilizzando l'API Aspose.Cells Cloud"
---

Questa REST API applica la **formattazione del testo ricco** a una cella in un file Excel.

**Prerequisiti:** È necessario disporre di un token JWT valido e il file Excel di destinazione deve già esistere nella cartella di archiviazione specificata prima di invocare questa operazione.

**Contesto:** La formattazione del testo ricco consente di applicare stili di carattere multipli all'interno di una singola cella, abilitando una presentazione dei dati più espressiva nei fogli di lavoro Excel.

## API PostCellCharacters

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/characters
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro | Tipo   | Posizione                     | Descrizione                                                                 |
|----------------|--------|-------------------------------|-----------------------------------------------------------------------------|
| name           | string | path                          | Il nome del file Excel (ad esempio, `Book1.xlsx`).                         |
| sheetName      | string | path                          | Il foglio di lavoro contenente la cella di destinazione.                   |
| cellName       | string | path                          | L'indirizzo della cella da formattare (ad esempio, `A1`).                  |
| options        | object | body                          | Oggetto JSON che definisce le impostazioni di formattazione del testo ricco per la cella. |
| folder         | string | query                         | La cartella nell'archivio in cui si trova il file Excel.                   |
| storageName    | string | query                         | Il nome del servizio di archiviazione (se viene utilizzato un archivio personalizzato). |

### **Risposta**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                                  |
|--------|-----------------------------|--------------------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante.                             |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione.            |
| 500    | Errore interno del server   | Errore imprevisto del server.                                |

## Come utilizzare l'API PostCellCharacters con gli SDK

### Specifica dell'API PostCellCharacters

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostCellCharacters) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come chiamare l'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/A1/characters" \
-X POST \
-d "{ \"FontSetting\": [ { \"Font\": { \"IsBold\": \"true\", \"Size\": \"24\" }, \"Length\": \"5\", \"StartIndex\": \"0\" }, { \"Font\": { \"IsItalic\": \"true\", \"Size\": \"15\" }, \"Length\": \"4\", \"StartIndex\": \"5\" } ] }" \
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

Utilizzare un SDK rappresenta il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello e consente di concentrarsi sulle attività del proprio progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
*Esempio SDK C#*  

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCellCharacters.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
*Esempio SDK Java*  

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCellCharacters.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
*Esempio SDK PHP*  

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCellCharacters.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
*Esempio SDK Ruby*  

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCellCharacters.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
*Esempio SDK Node.js*  

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCellCharacters.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
*Esempio SDK Python*  

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCellCharacters.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
*Esempio SDK Perl*  

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCellCharacters.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
*Esempio SDK Go*  

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCellCharacters.go" >}}
{{< /tab >}}

{{< /tabs >}}