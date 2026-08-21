---
---
title: "Aspose.Cells Cloud Web API - Converti i dati locali di una tabella Excel in un file PDF - Strumento online gratuito"
second_title: "Documento"
ArticleTitle: "Come convertire i dati di una tabella in un foglio di calcolo locale in un file PDF: Guida passo-passo"
linktitle: "Converti tabella in PDF"
type: docs
url: /convert-table-to-pdf/
keywords: "Aspose.Cells, Excel in PDF, conversione tabella, API cloud"
description: "Converti rapidamente una tabella Excel locale in un file PDF utilizzando l'API REST Aspose.Cells Cloud."
weight: 100
---

Esporta i dati della tabella da un file Excel locale in un file PDF utilizzando l'API Cloud.

## **Converti tabella in PDF - API**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/pdf
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### **Parametri della richiesta:**

| Nome parametro | Tipo   | Percorso/Query string/Corpo HTTP | Descrizione                                                                                      |
| :------------- | :----- | :------------------------------- | :----------------------------------------------------------------------------------------------- |
| Spreadsheet    | File   | FormData                         | Carica il file del foglio di calcolo da convertire.                                              |
| worksheet      | String | Query                            | Nome del foglio di calcolo.                                                                      |
| tableName      | String | Query                            | Nome della tabella da convertire.                                                                |
| outPath        | String | Query                            | (Opzionale) Il percorso della cartella in cui verrà salvato il PDF convertito. Il valore predefinito è null. |
| outStorageName | String | Query                            | Specifica il nome dell'archiviazione di output.                                                  |
| fontsLocation  | String | Query                            | Usa font personalizzati per il PDF.                                                               |
| region         | String | Query                            | Specifica l'impostazione della regione per il foglio di calcolo.                                 |
| password       | String | Query                            | Password per accedere al file del foglio di calcolo.                                             |

### **Risposta**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**Intestazioni di esempio della risposta**

```http
HTTP/1.1 200 OK
Content-Type: application/pdf
Content-Disposition: attachment; filename="ConvertedTable.pdf"
Content-Length: 124578
```

**Codici di stato HTTP**

| Codice | Significato             | Descrizione                                                                |
| ------ | ----------------------- | -------------------------------------------------------------------------- |
| 200    | OK                      | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida    | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato         | Token JWT non valido o mancante.                                           |
| 413    | Payload troppo grande   | Il file caricato supera il limite di dimensione.                          |
| 500    | Errore interno del server | Errore imprevisto sul server.                                              |

## **Dove dovresti utilizzare l'API Converti tabella in PDF?**

- **Bilanci finanziari**: Converti i fogli di sintesi, i conti economici (tabelle specifiche) in PDF per documenti pronti per l'audit.
- **Rapporti di vendita**: Trasforma i dashboard di vendita o i calcoli delle provvigioni in PDF distribuibili.
- **Metriche operative**: Esporta tabelle KPI e metriche di performance come report PDF formali.
- **Dati contrattuali**: Esporta tabelle dei prezzi e accordi sul livello di servizio dai fogli di calcolo in allegati PDF.
- **Tracciabilità di audit**: Conserva tabelle di dati finanziari come prove PDF non modificabili.
- **Riepiloghi di portafoglio**: Esporta tabelle di performance degli investimenti come estratti conto PDF pronti per il cliente.
- **Rapporti di controllo qualità**: Esporta tabelle di dati di ispezione in PDF per i record di conformità.
- **Riepiloghi di inventario**: Trasforma tabelle di livello di magazzino in PDF per la revisione da parte della direzione.

## **Perché dovresti utilizzare l'API Converti tabella in PDF?**

- **Facile per gli sviluppatori**: Aspose.Cells Cloud offre librerie SDK in diversi linguaggi, consentendo uno sviluppo rapido e accompagnato da documentazione esaustiva. Rispetto alla creazione di soluzioni personalizzate per il rendering dei grafici, ciò riduce significativamente il carico di lavoro.
- **Conveniente**: Puoi convertire i dati delle tabelle senza caricare preventivamente il file del foglio di calcolo, risparmiando spazio di archiviazione e riducendo i costi.
- **Mantiene la formattazione complessa di Excel** in un formato PDF universalmente accessibile.

## **Come utilizzare l'API Converti tabella in PDF con gli SDK?**

### Specifica dell'API Converti tabella in PDF

La [Specifica dell'API Converti tabella in PDF](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToPDF) fornisce un'interfaccia di programmazione pubblicamente accessibile per eseguire interazioni REST direttamente da un browser web.
Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/pdf?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.pdf
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (codificato in Base64)",
  "contentType": "tipo MIME",
  "fileDownloadName": "nome file opzionale"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK Aspose.Cells Cloud

L'utilizzo dell'SDK rappresenta il modo più rapido per sviluppare, poiché nasconde i dettagli di basso livello, consentendo di convertire i dati delle tabelle dei fogli di calcolo in un file PDF con un numero minimo di righe di codice. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}