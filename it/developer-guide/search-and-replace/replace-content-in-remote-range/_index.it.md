---
title: Aspose.Cells Cloud Web API - Sostituisci il contenuto dell'intervallo nel foglio di calcolo remoto
second_title: Documen
ArticleTitle: Replace Range Content in Remote a Spreadshee
linktitle: Sostituisci il contenuto del campo remoto
type: docs
url: /it/replace-content-in-remote-range/
keywords: API, Excel API, Replace Content, Remote Spreadsheet, Cloud Storage, Text Replacement, REST AP
description: Sostituisci in modo efficiente il testo all'interno di intervalli specificati di fogli di calcolo remoti utilizzando Aspose.Cells Cloud API
weight: 100
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, JSON, Markdown, Abbina tutte le celle vuote in un foglio di lavoro Excel, sostituzione di testo remoto, integrazione di archiviazione cloud
---
Sostituisci in modo efficiente il testo specificato all'interno di un intervallo di un file di foglio di calcolo remoto.

## **Sostituisci contenuto nell'intervallo remoto API**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/replace/content
```

### **Parametri di richiesta:**

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
| nome| Corda| Sentiero| Nome del file della cartella di lavoro da modificare.|
| testo di ricerca| Corda| Domanda| Il testo da cercare all'interno del foglio di calcolo.|
| sostituisciTesto| Corda| Domanda| Il testo con cui sostituire il testo cercato.|
| foglio di lavoro| Corda| Sentiero| Nome del foglio di lavoro in cui verrà effettuata la sostituzione.|
| area della cella| Corda| Sentiero| L'area cellulare specifica per la sostituzione.|
| cartella| Corda| Domanda| Percorso della cartella in cui è archiviata la cartella di lavoro.|
| Nome di archiviazione| Corda| Domanda|(Facoltativo) Il nome dell'archivio se si utilizza un archivio cloud personalizzato. Se omesso, utilizzare l'archivio predefinito.|
| regione| Corda| Domanda| Impostazione della regione del foglio di calcolo.|
| password| Corda| Domanda| La password per aprire il file del foglio di calcolo.|

### **Risposta**

```json
{
  "Name": "CellsCloudResponse",
  "Type": "Class",
  "Properties": [
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer",
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String",
      }
    }
  ]
}
```

### Codici di errore

- **400 Richiesta non valida**: URI Apose.Cells Cloud API non valido.
- **401 Non autorizzato**: Token di accesso non valido. Oppure ID client e segreto non validi.
- **404 Non trovato**: Il file del foglio di calcolo non è accessibile.
- **Errore del server 500**: Il foglio di calcolo ha riscontrato un'anomalia nell'ottenimento dei dati di calcolo.

## Dove dovremmo utilizzare il contenuto Sostituisci dell'intervallo nel foglio di calcolo remoto API?

Quando è necessario sostituire il contenuto di Range in un foglio di calcolo remoto, è possibile utilizzare questo API.

## Perché dovresti usare il contenuto Sostituisci dell'intervallo nel foglio di calcolo remoto API?

- Sostituisci rapidamente il contenuto di Range nei fogli di calcolo remoti.
- Lo sviluppo può essere completato rapidamente tramite l'SDK esistente.

## Come utilizzare il contenuto di sostituzione dell'intervallo nel foglio di calcolo remoto API con SDK

### Specifiche OpenAPI

 IL[Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/SearchControllor/ReplaceContentInRemoteRange) definisce un'interfaccia di programmazione accessibile al pubblico e consente di eseguire interazioni REST direttamente da un browser web.

### Utilizzare gli SDK cloud Aspose.Cells

Utilizzare l'SDK è il modo migliore per accelerare lo sviluppo. L'SDK gestisce i dettagli sottostanti, consentendo di implementare in modo semplice la sostituzione del contenuto nelle celle dei fogli di calcolo con un codice minimo.
 Si prega di controllare il[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ReplaceTextInRemoteRange.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ReplaceTextInRemoteRange.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ReplaceTextInRemoteRange.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ReplaceTextInRemoteRange.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ReplaceTextInRemoteRange.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ReplaceTextInRemoteRange.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ReplaceTextInRemoteRange.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ReplaceTextInRemoteRange.go" >}}
{{< /tab >}}
{{< /tabs >}}
