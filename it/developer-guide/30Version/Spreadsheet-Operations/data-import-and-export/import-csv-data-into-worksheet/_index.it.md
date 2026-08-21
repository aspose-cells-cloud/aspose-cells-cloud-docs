---
title: "Importa dati CSV in un foglio di lavoro Excel"
second_title: "Document"
linktype: "Importa dati CSV"
type: docs
url: /import-CSV-data-into-excel/
aliases:
  - /import-CSV-data-into-worksheet/
  - /import-data/csv-data/
  - /import/csv-data/
keywords: "Importa dati CSV, Excel, Aspose.Cells Cloud, REST API, Foglio di calcolo, Importazione CSV"
description: "L'API REST di Aspose.Cells Cloud consente di importare dati CSV in fogli di lavoro Excel. I SDK supportati includono Android, .NET, Go, Java, Node.js, Perl, PHP, Python, Ruby e Swift."
weight: 19
---

Questa REST API **importa dati CSV** in un foglio di lavoro Excel.

La richiesta è una richiesta HTTP con contenuto multipart (vedere [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) o [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La prima parte del contenuto multipart contiene i dati `ImportCSVDataOption`, mentre la seconda parte contiene il file CSV.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

I parametri principali sono descritti nelle tabelle seguenti.

### ImportCSVDataOption

| Nome parametro     | Tipo                       | Descrizione                                                                 |
| ------------------ | -------------------------- | --------------------------------------------------------------------------- |
| SeparatorString    | string                     | Carattere utilizzato per separare i campi nel file CSV (ad es., `,` o `;`). |
| ConvertNumericData | string (`true`/`false`)    | Indica se le stringhe numeriche devono essere convertite in valori numerici. |
| FirstRow           | int                        | Indice in base 1 della prima riga in cui verranno inseriti i dati.         |
| FirstColumn        | int                        | Indice in base 1 della prima colonna in cui verranno inseriti i dati.      |
| SourceFile         | string                     | Nome del file CSV sorgente da importare.                                   |
| CustomParsers      | List\<CustomParserConfig\> | Collezione di configurazioni di parser personalizzati per colonne specifiche. |

### CustomParserConfig

| Nome parametro | Tipo   | Descrizione                                                                  |
| -------------- | ------ | ---------------------------------------------------------------------------- |
| ColumnIndex    | int    | Indice in base 0 della colonna a cui si applica il parser personalizzato.    |
| ParseMethod    | string | Metodo di parsing per la colonna (ad es., `ToString`, `ToDate`, `ToNumber`). |
| CustomStyle    | string | Stile personalizzato (ad es., formato numero) applicato alle celle analizzate. |

**Esempio**

```xml
<ImportCSVDataOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>true</IsInsert>
    <ImportDataType>CSVData</ImportDataType>
    <SeparatorString>;</SeparatorString>
    <ConvertNumericData>true</ConvertNumericData>
    <FirstRow>1</FirstRow>
    <FirstColumn>2</FirstColumn>
    <SourceFile>TestImportDataCSV.CSV</SourceFile>
    <CustomParsers>
        <CustomParserConfig>
            <ColumnIndex>0</ColumnIndex>
            <ParseMethod>ToString</ParseMethod>
            <CustomStyle>#</CustomStyle>
        </CustomParserConfig>
    </CustomParsers>
</ImportCSVDataOption>
```
### Risposta

```json
{
  "Status":"OK",
  "Code":200
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                                     |
|--------|-----------------------------|-----------------------------------------------------------------|
| 200  | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400  | Richiesta non valida        | Parametri mancanti o non validi (ad es., tipo di file non supportato). |
| 401  | Non autorizzato             | Token JWT non valido o mancante. |
| 413  | Payload troppo grande       | Il file caricato supera il limite di dimensione. |
| 500  | Errore interno del server   | Errore imprevisto del server. |

## Come utilizzare l'API PostImportData con i SDK

### Specifica dell'API PostImportData

La [Specifica OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) definisce un'interfaccia di programmazione pubblicamente accessibile che consente di effettuare interazioni REST direttamente da un browser web.

### Utilizzo dei SDK di Aspose.Cells Cloud

L'utilizzo di un SDK è il modo migliore per accelerare lo sviluppo. Un SDK astrae i dettagli di basso livello, consentendoti di concentrarti sulla logica di business. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo dei SDK di Aspose.Cells Cloud.

Il seguente esempio di codice mostra come chiamare il servizio web Aspose.Cells utilizzando il SDK PHP:

{{< tabs tabTotal="1" tabID="1" tabName1="PHP" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportCSVData.php" >}}
{{< /tab >}}
{{< /tabs >}}

---