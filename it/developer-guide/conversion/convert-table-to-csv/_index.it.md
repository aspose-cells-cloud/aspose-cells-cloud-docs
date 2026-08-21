---
title: "Aspose.Cells Cloud Web API - Convertire i dati di una tabella di un foglio di calcolo in un file CSV - Strumento online gratuito"
second_title: "Documento"
ArticleTitle: "Come convertire i dati di una tabella di un foglio di calcolo in un file CSV: guida passo-passo"
linktitle: "Converti tabella in CSV"
type: docs
url: /convert-table-to-csv/
keywords: "Aspose.Cells Cloud, tabella in CSV, conversione foglio di calcolo, Excel in CSV, API, REST, esportazione dati"
description: "Converte rapidamente una tabella da un foglio di calcolo Excel in un file CSV utilizzando l'API Aspose.Cells Cloud."
weight: 100
---

Esporta i dati di una tabella da un file Excel locale in un file CSV utilizzando l'API Cloud.

## **Converti tabella in CSV API**

### Web API

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/csv
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Parametri della richiesta:**

| Nome parametro | Tipo   | Percorso/Query string/Corpo HTTP | Descrizione                                                                                                                             |
| -------------- | ------ | -------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | File   | FormData                         | Carica il file del foglio di calcolo.                                                                                                   |
| worksheet      | String | Query                            | Nome del foglio di calcolo all'interno del foglio di calcolo.                                                                           |
| tableName      | String | Query                            | Nome della tabella da convertire.                                                                                                       |
| outPath        | String | Query                            | (Facoltativo) Percorso della cartella in cui è memorizzato il foglio di calcolo; valore predefinito: null.                              |
| outStorageName | String | Query                            | Nome dell'archiviazione per il file di output.                                                                                          |
| fontsLocation  | String | Query                            | Percorso per l'utilizzo dei caratteri personalizzati.                                                                                  |
| region         | String | Query                            | Impostazione di regione/lingua del foglio di calcolo (ad es. `en-US`, `fr-FR`). Influenza la formattazione dei numeri, l'analisi delle date e il comportamento specifico della località. |
| password       | String | Query                            | Password per aprire il file del foglio di calcolo.                                                                                      |

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
| 200    | OK                      | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida    | Parametri mancanti o non validi (ad es. tipo di file non supportato). |
| 401    | Non autorizzato         | Token JWT non valido o mancante.                                  |
| 413    | Payload troppo grande   | Il file caricato supera il limite di dimensione.                  |
| 500    | Errore interno del server | Errore imprevisto del server.                                     |

## **Dove dovresti utilizzare l'API Converti tabella in CSV?**

- **Migrazione database**: Converti tabelle Excel in CSV per l'importazione in batch su database SQL (MySQL, PostgreSQL, SQL Server).
- **Caricamento data warehouse**: Trasforma tabelle di reporting basate su Excel in CSV per il caricamento in Snowflake, Redshift o BigQuery.
- **Payload API in batch**: Converti i dati delle tabelle Excel in CSV per il caricamento in batch su servizi REST.
- **Comunicazione tra servizi**: Utilizza CSV come formato leggero per lo scambio di dati tra microservizi.
- **Preparazione dati per machine learning**: Converti tabelle di caratteristiche da Excel in CSV per librerie di machine learning in Python/R.
- **Analisi statistica**: Trasforma tabelle di dati di ricerca in CSV per l'importazione in SPSS, SAS o Stata.
- **Migrazione di contenuti**: Sposta contenuti strutturati da Excel a sistemi CMS tramite CSV.

## Perché dovresti utilizzare l'API Converti tabella in CSV?

- **Facile per gli sviluppatori**: Aspose.Cells Cloud offre librerie SDK in diversi linguaggi, consentendo uno sviluppo rapido e accompagnato da una documentazione completa. Rispetto alla creazione di soluzioni personalizzate, questo riduce notevolmente il carico di lavoro di sviluppo.
- **Conveniente**: Puoi convertire i dati delle tabelle senza caricare preventivamente il foglio di calcolo, risparmiando spazio di archiviazione e riducendo i costi.
- **Estrazione pura dei dati, senza formattazione**.
- **CSV è supportato praticamente da ogni sistema**:
  - Database (tutti i principali RDBMS)
  - Linguaggi di programmazione (parser nativi in tutti)
  - Strumenti di business intelligence (Tableau, Power BI, Looker)
  - Software per fogli di calcolo (Excel, Google Sheets, LibreOffice)
  - Strumenti a riga di comando (awk, sed, grep)

## Come utilizzare l'API Converti tabella in CSV con gli SDK?

### Specifica dell'API Converti tabella in CSV

La [Specifiche dell'API Converti tabella in CSV](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToCSV) fornisce un'interfaccia di programmazione accessibile pubblicamente, consentendo interazioni REST direttamente da un browser web.
Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/csv?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.csv
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 encoded)",
  "contentType": "tipo MIME",
  "fileDownloadName": "nome file opzionale"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo degli SDK è il modo più veloce per sviluppare, poiché astrae i dettagli a basso livello, consentendoti di convertire i dati delle tabelle di un foglio di calcolo in un file CSV con un codice minimo. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice illustrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToCSV.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToCSV.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToCSV.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToCSV.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToCSV.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToCSV.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToCSV.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToCSV.go" >}}
{{</tab>}}
{{< /tabs >}}