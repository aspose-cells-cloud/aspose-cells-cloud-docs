---
---
title: "Aspose.Cells Cloud Web API - Convertire i dati locali di un intervallo Excel in un file JSON - Strumento online gratuito"
second_title: "Documento"
ArticleTitle: "Come convertire i dati di un intervallo locale in un file JSON: Guida passo dopo passo"
linktitle: "Converti intervallo in JSON"
type: docs
url: /convert-range-to-json/
keywords: "converti intervallo in json, Aspose.Cells Cloud, Excel in JSON, conversione foglio di calcolo, API"
description: "Converti un intervallo specifico da un foglio di calcolo Excel locale in JSON utilizzando l'API Aspose.Cells Cloud."
weight: 100
---

Esporta i dati di un intervallo da un file Excel locale in un file JSON utilizzando l'API Cloud.

## **Converti intervallo in JSON API**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/json
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### **Parametri della richiesta:**

| Nome parametro | Tipo   | Percorso/Query string/Corpo HTTP | Descrizione                                                                 |
| -------------- | ------ | -------------------------------- | --------------------------------------------------------------------------- |
| Spreadsheet    | File   | FormData                         | Carica il file del foglio di calcolo.                                       |
| worksheet      | String | Query                            | Nome del foglio di calcolo all'interno del file.                            |
| range          | String | Query                            | Area delle celle da convertire, ad esempio A1:C10.                         |
| outPath        | String | Query                            | (Facoltativo) Percorso della cartella dove è memorizzato il foglio di calcolo; default è null. |
| outStorageName | String | Query                            | Nome dell'archiviazione di output.                                          |
| fontsLocation  | String | Query                            | Posizione per memorizzare i caratteri personalizzati per uso domestico.     |
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

**Codici di stato HTTP**

| Codice | Significato             | Descrizione                                                             |
| ------ | ----------------------- | ----------------------------------------------------------------------- |
| 200    | OK                      | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida    | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato         | Token JWT non valido o mancante.                                        |
| 413    | Payload troppo grande   | Il file caricato supera il limite di dimensione.                       |
| 500    | Errore interno del server | Errore imprevisto del server.                                          |

## **Dove dovresti utilizzare l'API Converti intervallo in JSON?**

- Dashboard in tempo reale: Converti i dati Excel in tempo reale in JSON per librerie di grafica come Chart.js o D3.js.
- Foglio di calcolo come servizio (Spreadsheet-as-a-Service): Esporre intervalli Excel come endpoint JSON per altri servizi.
- Payload di webhook: Trasforma i dati del foglio di calcolo in JSON per notifiche webhook.
- Prototipazione rapida dei dati: Converti velocemente dati Excel puliti in JSON per analisi con Python o R.
- Pipeline di machine learning: Preprocessa dati di addestramento da fogli di calcolo gestiti dall'azienda.
- Operazioni di e-commerce: Sincronizza cataloghi prodotti o fogli prezzi con siti web tramite JSON.
- Automazione dei report: Genera feed di dati JSON da modelli finanziari per report automatici.
- Configurazione applicativa: Gestisci flag funzionali, impostazioni o parametri per test A/B in Excel → JSON.
- Supporto multilingua: Converti fogli di calcolo di localizzazione in JSON per librerie i18n.
- Menu/navigazione dinamica: Memorizza strutture di navigazione per il sito web in Excel e distribuiscile come JSON.

_Per altre opzioni di conversione, consulta la guida [Converti intervallo in CSV](/convert-range-to-csv/)._

## Perché utilizzare l'API Converti intervallo in JSON?

- **Supporto SDK**: Aspose.Cells Cloud fornisce librerie per molteplici linguaggi, riducendo la quantità di codice personalizzato necessario.
- **Riduzione dei costi di archiviazione**: L'intervallo può essere convertito senza caricare preventivamente l'intero foglio di calcolo, risparmiando spazio di archiviazione.
- **Compatibilità con app web e mobile**: JSON è il formato dati nativo per i moderni framework JavaScript come React, Vue e Angular.
- **Ampio supporto linguistico**: praticamente ogni linguaggio di programmazione e database può consumare JSON.
- **Conservazione della struttura dei dati**
  - **Rilevamento intelligente della struttura**: converte automaticamente i dati tabellari in array o oggetti JSON appropriati.
  - **Mapping delle intestazioni**: utilizza la prima riga come chiavi JSON per strutture di oggetti pulite.
  - **Mantenimento del tipo dati**: conserva tipi numerici, data e booleani invece di semplice testo.

## Come utilizzare l'API Converti intervallo in JSON con gli SDK?

### Specifica dell'API Converti intervallo in JSON

La [Specifiche dell'API Converti intervallo in JSON](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToJson) definisce un'interfaccia di programmazione pubblicamente accessibile e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/json?worksheet=Sheet1&range=A1:C10" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/percorso/del/tuo/file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result.json"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo dell'SDK rappresenta il modo più veloce per sviluppare, poiché astrae i dettagli a basso livello, consentendo di convertire un intervallo di dati in un file JSON con codice conciso.  
Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToJson.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToJson.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToJson.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToJson.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToJson.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToJson.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToJson.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToJson.go" >}}
{{</tab>}}
{{< /tabs >}}