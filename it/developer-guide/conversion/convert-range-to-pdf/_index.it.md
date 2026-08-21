---
title: "Converti un intervallo di Excel in PDF con Aspose.Cells Cloud API"
second_title: "Documenti"
ArticleTitle: "Come convertire dati di intervallo da un foglio di calcolo locale in un file PDF: Guida passo-passo"
linktitle: "Converti intervallo in PDF"
type: docs
url: /it/convert-range-to-pdf/
keywords: "Aspose.Cells Cloud, converti intervallo Excel in PDF, Excel in PDF, conversione cloud"
description: "Converti un intervallo specifico da un foglio di calcolo Excel locale in PDF utilizzando l'API REST di Aspose.Cells Cloud."
weight: 100
---

Esporta un intervallo di dati da un file Excel locale in un file [PDF](https://docs.fileformat.com/pdf/) utilizzando l'API cloud.

**Prerequisiti**: Prima di utilizzare questa API è necessario disporre di un account Aspose.Cells Cloud valido, di un token di accesso JWT e, facoltativamente, di un SDK Aspose.Cells Cloud per il proprio linguaggio di programmazione. Assicurati che lo storage di destinazione (predefinito o personalizzato) sia configurato se intendi utilizzare il parametro `outStorageName`.

## **API Converti intervallo in PDF**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/pdf
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### **Parametri della richiesta:**

| Nome parametro | Tipo   | Percorso/Query string/Corpo HTTP | Descrizione                                                                 |
|----------------|--------|----------------------------------|------------------------------------------------------------------------------|
| Spreadsheet    | File   | FormData                         | Carica il file del foglio di calcolo.                                        |
| worksheet      | String | Query                            | Nome del foglio di calcolo all'interno del documento.                        |
| range          | String | Query                            | Area di celle da convertire, ad esempio A1:C10.                             |
| outPath        | String | Query                            | (Opzionale) Percorso della cartella in cui è memorizzato il foglio di calcolo. Il valore predefinito è null. |
| outStorageName | String | Query                            | Nome dello storage per il file di output.                                   |
| fontsLocation  | String | Query                            | Posizione per memorizzare i caratteri personalizzati per uso personale.     |
| region         | String | Query                            | Impostazione della regione del foglio di calcolo.                           |
| password       | String | Query                            | Password per aprire il file del foglio di calcolo.                          |

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

_La risposta tipica è un flusso binario PDF restituito come download di file._

**Codici di stato HTTP**

| Codice | Significato             | Descrizione                                                      |
|--------|-------------------------|------------------------------------------------------------------|
| 200    | OK                      | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida    | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato         | Token JWT non valido o mancante.                                 |
| 413    | Payload troppo grande   | Il file caricato supera il limite di dimensione.                |
| 500    | Errore interno del server | Errore imprevisto nel server.                                    |

## **Dove dovresti utilizzare l'API Converti intervallo in PDF?**

- **Bilanci finanziari**: Converti in PDF, per documenti pronti per l'audit, voci specifiche come stato patrimoniale, conto economico (intervalli specifici).
- **Rapporti di vendita**: Trasforma dashboard di vendita o calcoli di commissione in PDF distribuibili.
- **Metriche operative**: Esporta tabelle KPI e metriche di performance come rapporti PDF formali.
- **Dati contrattuali**: Esporta tabelle prezzi e accordi sul livello di servizio dai fogli di calcolo in allegati PDF.
- **Tracciabilità di audit**: Conserva intervalli di dati finanziari come prove PDF non modificabili.
- **Riepiloghi di portafoglio**: Esporta intervalli di performance degli investimenti come statement PDF pronti per il cliente.
- **Rapporti di controllo qualità**: Esporta intervalli di dati ispettivi in PDF per archiviare registri di conformità.
- **Riepiloghi di inventario**: Trasforma tabelle di livello di magazzino in PDF per la revisione da parte della direzione.

## **Perché dovresti utilizzare l'API Converti intervallo in PDF?**

- **Facile per lo sviluppatore**: Aspose.Cells Cloud offre librerie SDK in molteplici linguaggi, consentendo uno sviluppo rapido e documentazione completa. Rispetto alla creazione di soluzioni personalizzate di rendering dei grafici, riduce notevolmente il carico di sviluppo.
- **Conveniente**: Puoi convertire dati di intervallo senza dover prima caricare l'intero foglio di calcolo, risparmiando spazio di archiviazione e riducendo i costi.
- **Preserva la formattazione complessa di Excel** in un formato PDF universalmente accessibile.

## **Come utilizzare l'API Converti intervallo in PDF con gli SDK?**

### Specifica dell'API Converti intervallo in PDF

La [Specifica dell'API Converti intervallo in PDF](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToPDF) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/pdf?worksheet=Sheet1&range=A1:C10" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result.pdf"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo degli SDK rappresenta il modo più rapido per sviluppare, poiché astrae i dettagli a basso livello, consentendo di convertire un intervallo di dati in un file PDF con un codice conciso. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}