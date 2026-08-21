---
title: "Aspose.Cells Cloud Web API - Converti i dati locali di una tabella Excel in un file immagine - Strumento gratuito online"
second_title: "Documento"
ArticleTitle: "Come convertire i dati locali di una tabella in un file immagine: Guida passo-passo"
linktitle: "Converti tabella in immagine"
type: docs
url: /it/convert-table-to-image/
keywords: "Aspose.Cells, Cloud API, Converti tabella in immagine, Excel, PNG, JPEG, TIFF, BMP, SVG"
description: "Converti rapidamente una tabella di un file Excel locale in un file immagine utilizzando l'API Aspose.Cells Cloud. Supporta i formati PNG, JPEG, TIFF, BMP, SVG e altri."
weight: 100
---

Esporta i dati della tabella da un file Excel locale in un file [immagine](https://docs.fileformat.com/image/) utilizzando l'API Cloud.

**FORMATI IMMAGINE SUPPORTATI:**

- [PNG](https://docs.fileformat.com/image/png/)
- [SVG](https://docs.fileformat.com/page-description-language/svg/)
- [TIFF](https://docs.fileformat.com/image/tiff/)
- [JPEG](https://docs.fileformat.com/image/jpeg/)
- [BMP](https://docs.fileformat.com/image/bmp/)

## **Converti tabella in immagine - API**

Prima di utilizzare questo endpoint, assicurati di avere i seguenti prerequisiti:

- Un token di accesso JWT valido ottenuto tramite l'autenticazione di Aspose.Cells Cloud.
- Un account di archiviazione accessibile se intendi utilizzare i parametri `outPath` o `outStorageName`.
- Il foglio di calcolo sorgente (file Excel locale) deve essere leggibile e, se protetto, deve essere fornita la password corretta.

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/image
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### **Parametri della richiesta:**

| Nome parametro | Tipo   | Percorso/Query string/Corpo HTTP | Descrizione                                                                                                                             |
| :------------- | :----- | :------------------------------ | :-------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | File   | FormData                        | Carica il file di foglio di calcolo.                                                                                                    |
| worksheet      | String | Query                           | Nome del foglio di calcolo/Excel.                                                                                                       |
| tableName      | String | Query                           | Nome della tabella da convertire.                                                                                                       |
| format         | String | Query                           | Formato desiderato del file immagine (ad esempio, png, svg).                                                                            |
| outPath        | String | Query                           | (Opzionale) Percorso della cartella in cui verrà salvata l’immagine convertita. Il valore predefinito è null.                          |
| outStorageName | String | Query                           | Specifica il nome dell'archiviazione per il file di output.                                                                             |
| fontsLocation  | String | Query                           | Utilizza font personalizzati, se necessario.                                                                                            |
| region         | String | Query                           | Impostazione regione/lingua del foglio di calcolo (ad esempio, `it-IT`, `fr-FR`). Influenza la formattazione dei numeri, l’analisi delle date e il comportamento specifico della localizzazione. |
| password       | String | Query                           | Password richiesta per accedere al file di foglio di calcolo.                                                                           |

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

**Codici di stato HTTP**

| Codice | Significato             | Descrizione                                                       |
| ------ | ----------------------- | ----------------------------------------------------------------- |
| 200    | OK                      | Filtro applicato correttamente; la risposta contiene i dettagli dell’operazione. |
| 400    | Richiesta non valida    | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato         | Token JWT non valido o mancante.                                  |
| 413    | Payload troppo grande   | Il file caricato supera il limite di dimensione.                  |
| 500    | Errore interno del server | Errore imprevisto del server.                                     |

## **Dove dovresti utilizzare l’API Converti tabella in immagine?**

- **istantanee statiche di report**: converti tabelle finanziarie, risultati di calcoli o qualsiasi dato formattato in immagini da includere in report PDF, diapositive PowerPoint o documenti stampati, dove non è richiesta la modifica.
- **Visualizzazione dei dati nelle presentazioni**: trasforma tabelle di fogli di calcolo complesse—incluse formattazione condizionale o semplici visualizzazioni—in immagini da incorporare nelle presentazioni (PPTX, Google Slides).
- **Documentazione e materiali formativi**: cattura esempi di fogli di calcolo, modelli o moduli di immissione dati come immagini per manuali utente, tutorial o articoli della knowledge base.
- **anteprime in miniatura**: genera piccole anteprime immagine delle sezioni chiave dei fogli di calcolo per browser di file, librerie di documenti o risultati di ricerca.

## Perché dovresti utilizzare l’API Converti tabella in immagine?

- **Semplice per gli sviluppatori**: Aspose.Cells Cloud offre librerie SDK in molteplici linguaggi, consentendo uno sviluppo rapido e accompagnato da una documentazione completa. Rispetto alla costruzione di soluzioni di rendering personalizzate, riduce significativamente il carico di lavoro di sviluppo.
- **Conveniente**: puoi convertire i dati della tabella senza caricare preventivamente l’intero foglio di calcolo, risparmiando spazio di archiviazione e riducendo i costi.
- **Preservazione fedele dei dettagli**: riproduce fedelmente l'aspetto di Excel—including cell formatting, formulas (as displayed values), borders, colors, and conditional formatting—in the output image.
- **Compatibilità universale**: i formati immagine (PNG, JPEG, TIFF, BMP, SVG, ecc.) sono visualizzabili su qualsiasi dispositivo o piattaforma senza software specializzati, garantendo la massima accessibilità.

## Come utilizzare l’API Converti tabella in immagine con gli SDK?

### Specifica dell’API Converti tabella in immagine

La [Specifiche dell’API Converti tabella in immagine](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToImage) fornisce un'interfaccia di programmazione pubblicamente accessibile per effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L’esempio seguente mostra come effettuare chiamate all’API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/image?format=png&worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.png
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 encoded)",
  "contentType": "MIME type",
  "fileDownloadName": "optional file name"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo dell'SDK è il modo più rapido per sviluppare, poiché nasconde i dettagli a basso livello, consentendoti di convertire i dati della tabella di un foglio di calcolo in un'immagine con pochissimo codice. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per l'elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come richiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToSvg.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToSvg.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToSvg.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToSvg.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToSvg.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToSvg.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToSvg.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToSvg.go" >}}
{{</tab>}}
{{< /tabs >}}