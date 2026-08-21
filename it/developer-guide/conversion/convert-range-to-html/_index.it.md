---
title: "Aspose.Cells Cloud – Converti un intervallo Excel in HTML"
description: "Converti un intervallo specifico di un file Excel (ad esempio A1:C10) in un file HTML utilizzando l'API REST di Aspose.Cells Cloud. Include autenticazione, esempi di richiesta, gestione della risposta, frammenti di SDK e codici di errore."
keywords: "Aspose.Cells, Excel in HTML, conversione intervallo, API cloud, foglio di calcolo"
slug: convert-range-to-html
date: 2026-07-30
type: docs
weight: 100
---

Converti un intervallo selezionato di un foglio di calcolo Excel locale in un file HTML direttamente tramite Aspose.Cells Cloud. La conversione avviene interamente sul server cloud, pertanto non è mai necessario caricare l'intero foglio di calcolo né avere Excel installato localmente.

## API Converti Intervallo in HTML

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/html
```

Il corpo della richiesta è `multipart/form-data` contenente il file del foglio di calcolo. Tutte le altre opzioni vengono fornite come parametri di query.

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome               | Tipo    | Posizione | Obbligatorio | Descrizione                                                                 |
|--------------------|---------|-----------|--------------|-----------------------------------------------------------------------------|
| **Spreadsheet**    | File    | FormData  | Sì           | Il foglio di calcolo Excel da convertire.                                  |
| **worksheet**      | String  | Query     | Sì           | Nome del foglio di calcolo contenente l'intervallo.                        |
| **range**          | String  | Query     | Sì           | Area di celle da convertire, ad esempio `A1:C10`.                          |
| **outPath**        | String  | Query     | No           | Percorso della cartella in cui salvare il file HTML risultante (default `null`). |
| **outStorageName** | String  | Query     | No           | Nome del servizio di archiviazione per il file di output.                  |
| **fontsLocation**  | String  | Query     | No           | Percorso di una cartella personalizzata per i font.                        |
| **AutoRowsFit**    | Boolean | Query     | No           | Adatta automaticamente tutte le righe nel foglio di calcolo.               |
| **AutoColumnsFit** | Boolean | Query     | No           | Adatta automaticamente tutte le colonne nel foglio di calcolo.             |
| **region**         | String  | Query     | No           | Identificatore di impostazioni locali (ad esempio `it-IT`, `en-US`). Influisce sulla formattazione di numeri e date. |
| **password**       | String  | Query     | No           | Password per aprire un foglio di calcolo protetto.                         |
| **fontsLocation**  | String  | Query     | No           | Percorso personalizzato dei font.                                           |
| **region**         | String  | Query     | No           | Impostazione di regione/lingua del foglio di calcolo.                      |
| **password**       | String  | Query     | No           | Password per aprire il file del foglio di calcolo.                         |

## Risposta

L'API restituisce il file HTML convertito come **stream binario** (`application/octet-stream`).

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

### Esempio di risposta positiva (HTTP)

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.html"
Content-Length: 8423

<table>
  <tr><th>Prodotto</th><th>Prezzo</th></tr>
  <tr><td>Widget A</td><td>$10</td></tr>
  <tr><td>Widget B</td><td>$15</td></tr>
</table>
```

Salva il corpo della risposta in un file (ad esempio `report.html`) per visualizzare la tabella renderizzata in un browser.

---

**Codici di stato HTTP**

| Codice | Significato            | Descrizione                                                     |
|--------|------------------------|-----------------------------------------------------------------|
| 200    | OK                     | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida   | Parametri mancanti o non validi (ad esempio tipo di file non supportato). |
| 401    | Non autorizzato        | Token JWT non valido o mancante.                                |
| 413    | Payload troppo grande  | Il file caricato supera il limite di dimensione.               |
| 500    | Errore interno del server | Errore imprevisto sul server.                                  |

## Come utilizzare l'API Converti Intervallo in HTML con gli SDK?

### Specifica OpenAPI

La [Specifica OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToHTML) descrive un'API pubblicamente accessibile, consentendo interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/html?worksheet=Sheet1&range=A1:C10&AutoRowsFit=true&AutoColumnsFit=true" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Report.xlsx" \
     -F "outPath=output/report.html"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.html"
Content-Length: 8423

<table>
  <tr><th>Prodotto</th><th>Prezzo</th></tr>
  <tr><td>Widget A</td><td>$10</td></tr>
  <tr><td>Widget B</td><td>$15</td></tr>
</table>
```

{{< /tab >}}

{{< /tabs >}}

## Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo dell'SDK rappresenta il metodo più rapido per lo sviluppo, poiché astrae i dettagli di basso livello, consentendo di convertire un intervallo di dati in un file HTML con un numero minimo di righe di codice.  
Esplora l'elenco completo degli SDK di Aspose.Cells Cloud nel nostro [repository GitHub](https://github.com/aspose-cells-cloud).

I seguenti esempi di codice illustrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK. Se il caricamento da Gist è bloccato, puoi scaricare direttamente gli esempi dal repository.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToHtml.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToHtml.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToHtml.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToHtml.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToHtml.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToHtml.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToHtml.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToHtml.go" >}}
{{</tab>}}
{{< /tabs >}}