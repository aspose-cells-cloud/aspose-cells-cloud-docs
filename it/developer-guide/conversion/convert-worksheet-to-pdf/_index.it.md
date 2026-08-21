---
title: "Aspose.Cells Cloud Web API – Convertire un foglio di calcolo locale in un file PDF – Strumento gratuito online"
second_title: "Documento"
ArticleTitle: "Come convertire un foglio di calcolo locale in un file PDF: Guida passo-passo"
linktitle: "Converti foglio in PDF"
type: docs
url: /it/convert-worksheet-to-pdf/
keywords: "Aspose.Cells, Excel in PDF, conversione foglio, API REST, conversione cloud, PDF foglio di calcolo, endpoint API, generazione PDF"
description: "Usa l'API Aspose.Cells Cloud per convertire rapidamente e in modo sicuro un foglio da un file Excel locale in un documento PDF."
weight: 100
---

Esporta un foglio da un file Excel locale in un file [PDF](https://docs.fileformat.com/pdf/) tramite l'API Cloud.

## **Converti foglio in PDF – API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### **Parametri della richiesta:**

| Nome parametro | Tipo   | Percorso/Query string/HTTPBody | Descrizione                                                                 |
| -------------- | ------ | ----------------------------- | --------------------------------------------------------------------------- |
| Spreadsheet    | File   | FormData                      | Carica il file del foglio di calcolo.                                       |
| worksheet      | String | Query                         | Nome del foglio nel foglio di calcolo.                                      |
| outPath        | String | Query                         | (Opzionale) Percorso della cartella in cui salvare il workbook; valore predefinito: null. |
| outStorageName | String | Query                         | Nome dell'archiviazione per il file di output.                              |
| fontsLocation  | String | Query                         | Usa font personalizzati per il PDF.                                          |
| region         | String | Query                         | Definisce l'impostazione della regione del foglio di calcolo.               |
| password       | String | Query                         | Password necessaria per aprire il file del foglio di calcolo.               |

### **Risposta**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

**Codici di stato HTTP**

| Codice | Significato             | Descrizione                                                        |
| ------ | ----------------------- | ------------------------------------------------------------------ |
| 200    | OK                      | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida    | Parametri mancanti o non validi (es. tipo di file non supportato). |
| 401    | Non autorizzato         | Token JWT non valido o mancante.                                   |
| 413    | Payload troppo grande   | Il file caricato supera il limite di dimensione.                  |
| 500    | Errore interno del server | Errore imprevisto del server.                                    |

## **Dove dovresti usare l’API Converti foglio in PDF?**

- **Bilanci finanziari**: Converti in PDF fogli di stato patrimoniale e conto economico (tabelle specifiche) per documenti pronti per un audit.
- **Report di vendita**: Trasforma dashboard di vendita o calcoli di commissione in PDF distribuibili.
- **Metriche operative**: Esporta tabelle KPI e metriche di prestazione come report PDF ufficiali.
- **Dati contrattuali**: Esporta tabelle prezzi e accordi sul livello di servizio dai fogli di calcolo in allegati PDF.
- **Tracciabilità di audit**: Conserva fogli di calcolo finanziari come prove PDF non modificabili.
- **Sintesi portafoglio**: Esporta tabelle sul rendimento degli investimenti in report PDF pronti per il cliente.
- **Report controllo qualità**: Esporta fogli di ispezione in PDF per i record di conformità.
- **Sintesi inventario**: Trasforma fogli di magazzino in PDF per la revisione da parte della direzione.

## **Perché dovresti usare l’API Converti foglio in PDF?**

- **Semplice per gli sviluppatori**: Aspose.Cells Cloud offre librerie SDK in diversi linguaggi, consentendo uno sviluppo rapido e accompagnato da una documentazione completa. Rispetto alla creazione di soluzioni personalizzate per il rendering dei grafici, riduce notevolmente il carico di lavoro.
- **Conveniente**: Puoi convertire i dati delle tabelle senza caricare preventivamente l’intero workbook, risparmiando spazio di archiviazione e riducendo i costi.
- **Preservazione della formattazione**: Mantiene la formattazione complessa di Excel in un formato PDF universalmente accessibile.

## **Come usare l’API Converti foglio in PDF con gli SDK?**

### Specifica dell’API Converti foglio in PDF

La [Specifica dell’API Converti foglio in PDF](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToPDF) fornisce un'interfaccia di programmazione pubblicamente accessibile e consente interazioni REST direttamente da un browser web.

Puoi usare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L’esempio seguente mostra come effettuare chiamate all’API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/json?worksheet=Sheet1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.json
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

### Usare gli SDK di Aspose.Cells Cloud

L’uso di un SDK rappresenta il modo più rapido per sviluppare, poiché nasconde i dettagli a basso livello, consentendoti di convertire i dati delle tabelle di un foglio di calcolo in un file PDF con un codice minimo. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells usando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorksheetToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorksheetToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorksheetToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorksheetToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorksheetToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorksheetToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorksheetToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorksheetToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}