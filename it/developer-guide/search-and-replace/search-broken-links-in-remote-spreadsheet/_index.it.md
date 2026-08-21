---
title: "Aspose.Cells Cloud – API per il rilevamento di link rotti in Excel – Analisi e convalida dei link in fogli di calcolo remoti"
second_title: "Documento"
ArticleTitle: "Individuare e risolvere link rotti in Excel remoti – Strumento di verifica link fogli di calcolo cloud"
linktitle: "Cercare link rotti in fogli di calcolo remoti"
type: docs
url: /it/search-broken-links-in-remote-spreadsheet/
keywords: "Excel, link rotti, API, cloud, foglio di calcolo, convalida, Aspose.Cells"
description: "Utilizza l'API Aspose.Cells Cloud per scansionare fogli di calcolo Excel remoti e individuare link esterni rotti, formule non valide e origini dati mancanti."
weight: 100
---

## **Cercare link rotti in un foglio di calcolo remoto tramite API**

Rileva automaticamente i link rotti nei file Excel archiviati in archiviazione cloud. La nostra API scansiona intervalli specificati alla ricerca di riferimenti esterni rotti, formule non valide e origini dati mancanti. Supporta la revisione di fogli di calcolo remoti, controlli di qualità automatizzati e l'integrazione con provider di archiviazione cloud. Utilizza l'API RESTful per automatizzare flussi di lavoro aziendali.

### **API Web**

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/search/broken-links
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione tramite token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Parametri della richiesta:**

| Nome parametro | Tipo   | Percorso/Query stringa/Corpo HTTP | Descrizione                                                                                                                                               |
| :------------- | :----- | :------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name           | String | Percorso                         | **Obbligatorio.** Il nome del file del foglio di calcolo Excel da scansionare per individuare i link rotti (ad esempio, `Quarterly_Report.xlsx`).        |
| worksheet      | String | Query                            | **Obbligatorio.** Il nome del foglio di calcolo in cui verrà eseguita l'operazione di ricerca. Specificare il nome esatto del foglio così come appare nel foglio di calcolo. |
| cellArea       | String | Query                            | **Obbligatorio.** L'intervallo di celle da analizzare per individuare i link rotti, espresso in notazione A1 (ad esempio, `C5:J50`). L'API esegue la ricerca solo all'interno di quest'area. |
| folder         | String | Query                            | **Facoltativo.** Il percorso della directory contenente il foglio di calcolo nella propria archiviazione cloud. Se omesso, si assume la directory principale. |
| storageName    | String | Query                            | **Facoltativo.** Il nome della configurazione personalizzata dell'archiviazione cloud. Se omesso, viene utilizzata l'archiviazione predefinita del sistema. |
| region         | String | Query                            | **Facoltativo.** Impostazione locale applicata durante l'elaborazione (ad esempio, `it-IT`). Può influenzare l'interpretazione della sintassi o dei riferimenti specifici della regione. |
| password       | String | Query                            | **Facoltativo.** Password necessaria per aprire un foglio di calcolo crittografato. Omettere se il file non è protetto da password.                       |

**Esempio di richiesta cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/Quarterly_Report.xlsx/search/broken-links?worksheet=Sheet1&cellArea=C5:J50" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

### **Risposta**

```json
{
  "Name": "BrokenLinksResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "Properties": [
    {
      "Name": "BrokenLinks",
      "DataType": {
        "Identifier": "Container",
        "Reference": "BrokenLink",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "BrokenLink"
        }
      }
    },
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer"
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String"
      }
    }
  ]
}
```

**Esempio di risposta JSON**

```json
{
  "BrokenLinks": [
    {
      "Worksheet": "Sheet1",
      "CellName": "D12",
      "Link": "https://example.com/data/source.xlsx",
      "IsValid": false,
      "ErrorMessage": "File non trovato"
    },
    {
      "Worksheet": "Sheet1",
      "CellName": "F30",
      "Link": "C:\\LocalFolder\\data.xlsx",
      "IsValid": false,
      "ErrorMessage": "Riferimento esterno non supportato in modalità cloud"
    }
  ],
  "Code": 200,
  "Status": "OK"
}
```

### Codici di errore

- **400 Bad Request** – URI dell'API Aspose.Cells Cloud non valido.  
- **401 Unauthorized** – Token di accesso, client ID o client secret non validi.  
- **404 Not Found** – Il file del foglio di calcolo non è accessibile.  
- **500 Server Error** – Si è verificato un’anomalia durante il recupero dei dati di calcolo.

## Dove utilizzare l'API per cercare link rotti in un foglio di calcolo?

- **Revisione regolare di modelli finanziari di grandi dimensioni** – Prima della pubblicazione di report mensili o trimestrali, scansionare automaticamente le aree di calcolo chiave (ad esempio, `Dashboard!B5:K50`) contenenti molti riferimenti a dati esterni, per verificare che tutti i link puntino a file sorgenti validi.  
- **Integrazione dati per fusioni e acquisizioni** – Dopo aver unito più fogli di calcolo che rappresentano unità aziendali, scansionare il foglio "Panoramica" per individuare i link diventati non validi a causa di percorsi di file modificati o problemi di autorizzazione.  
- **Preparazione di pacchetti dati per investitori** – Prima di finalizzare materiali presentabili contenenti grafici e tabelle collegati a database esterni o fonti di dati di mercato, verificare la validità di tutti i link.

## Perché utilizzare l'API per cercare link rotti in un foglio di calcolo?

- **Facile da usare per sviluppatori** – Aspose.Cells Cloud fornisce librerie SDK in molteplici linguaggi, consentendo uno sviluppo rapido con documentazione completa. Rispetto alla creazione di una soluzione personalizzata, ciò riduce significativamente lo sforzo di sviluppo.  
- **Riduzione dei costi del personale** – Automatizza la convalida dei link, eliminando la necessità di personale dedicato alla raccolta manuale di documenti.  
- **Pagamento in base all’uso** – Nessun investimento iniziale; si paga solo per le chiamate API effettivamente utilizzate.  
- **Costi di manutenzione nulli** – Nessun server da mantenere, nessun aggiornamento software e nessun problema di compatibilità.

## Come utilizzare l'API per cercare link rotti in un foglio di calcolo con gli SDK

### Specifica OpenAPI

La [specifica OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchBrokenLinksInRemoteSpreadsheet) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare interazioni REST direttamente da un browser web.

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK è il modo più efficiente per velocizzare lo sviluppo. L'SDK nasconde i dettagli HTTP sottostanti, consentendo di implementare il rilevamento dei link rotti con un numero minimo di righe di codice. Consultare la [repository GitHub](https://github.com/aspose-cells-cloud) per l'elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come interagire con i servizi web Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteSpreadsheet.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteSpreadsheet.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteSpreadsheet.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteSpreadsheet.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteSpreadsheet.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteSpreadsheet.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteSpreadsheet.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteSpreadsheet.go" >}}  
{{</tab>}}  
{{< /tabs >}}