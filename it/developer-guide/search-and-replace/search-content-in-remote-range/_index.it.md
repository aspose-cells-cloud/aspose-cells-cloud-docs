---
title: "Aspose.Cells Cloud Excel Text Search API – Trova testo in intervalli di fogli di calcolo remoti"
second_title: "Documento"
ArticleTitle: "Cerca testo in fogli di calcolo Excel remoti – Trova dati in intervalli specifici"
linktitle: "Cerca contenuto in intervallo remoto"
type: docs
url: /it/search-content-in-remote-range/
keywords: "Aspose.Cells, API Excel, ricerca testo, intervallo remoto, foglio di calcolo cloud, API REST, individuazione dati"
description: "Cerca testo, numeri o formule in un intervallo specifico di un file Excel archiviato su Aspose Cloud."
weight: 100
---

## **Cerca contenuto in intervallo remoto**

Cerca programmaticamente un testo specifico all’interno di qualsiasi intervallo di fogli di calcolo Excel utilizzando l’API Aspose.Cells Cloud. Trova testo, numeri o formule in file remoti archiviati nello spazio di archiviazione cloud. API RESTful per flussi di lavoro automatizzati di individuazione dati, analisi dei contenuti e revisione dei fogli di calcolo.

### **API Web**

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/search/content
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono l’<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```


**Esempio cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Orders_2024/ranges/B2:H100/search/content?searchText=Report&ignoreCase=true" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Content-Type: application/json"
```

### Parametri della richiesta

| Nome parametro | Tipo    | Percorso/Query/Stringa/HTTPBody | Descrizione                                                                                                                                         |
| :------------- | :------ | :------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------- |
| name           | String  | Percorso                       | **Obbligatorio**. Nome del file (inclusa l’estensione) del file Excel da cercare, ad esempio `customer_data.xlsx`.                                       |
| worksheet      | String  | Percorso                       | **Obbligatorio**. Nome esatto del foglio all’interno del file Excel in cui eseguire la ricerca, ad esempio `Orders_2024`.                                                |
| cellArea       | String  | Percorso                       | **Obbligatorio**. Intervallo di celle target per la ricerca, specificato in notazione A1 (ad esempio `B2:H100`). La ricerca è limitata a questa area.                |
| searchText     | String  | Query                      | **Obbligatorio**. Stringa di testo, numero o contenuto parziale specifico da trovare nell’intervallo di celle definito.                                            |
| ignoreCase     | Boolean | Query                      | **Opzionale**. Se impostato su `true`, la ricerca ignora le differenze di maiuscole/minuscole (ad esempio, “Report” trova anche “report”). Il valore predefinito è `false` (distinzione tra maiuscole e minuscole).       |
| folder         | String  | Query                      | **Opzionale**. Percorso della directory nello spazio di archiviazione cloud in cui si trova il file Excel. Se omesso, viene utilizzata la directory radice.                       |
| storageName    | String  | Query                      | **Opzionale**. Identificatore di una configurazione personalizzata di archiviazione cloud. Se non specificato, viene utilizzata l’archiviazione predefinita dell’account.               |
| region         | String  | Query                      | **Opzionale**. Impostazione cultura/regione (ad esempio `it-IT`) che può influenzare l’interpretazione di caratteri o formati specifici della regione durante la ricerca. |
| password       | String  | Query                      | **Opzionale**. Password per decrittografare e accedere a un file di foglio di calcolo protetto da password. Omettere se il file non è crittografato.                          |

### Risposta

```json
{
  "Code": 200,
  "Status": "OK",
  "TextItems": [
    {
      "Filename": "string",
      "Worksheet": "string",
      "Position": "string",
      "Content": "string"
    }
  ]
}
```

### Codici di errore

- **400 Bad Request** – URI dell’API Aspose.Cells Cloud non valido.  
- **401 Unauthorized** – Token di accesso, client ID o client secret non validi.  
- **404 Not Found** – Il file del foglio di calcolo non è accessibile.  
- **500 Server Error** – Una condizione imprevista ha impedito al server di soddisfare la richiesta.

## Dove utilizzare la funzionalità di ricerca del contenuto all’interno di un intervallo del foglio di calcolo?

- **Controllo della qualità su larga scala dei dati** – Durante la fase di accettazione del processo ETL del data warehouse, cerca descrizioni di campi mancanti, abbreviazioni non definite o testo segnaposto (ad esempio `"TBD"` o `"NULL"`) nella tabella di mappatura dei dati (`DataDictionary!B2:F1000`) per identificare definizioni di dati incomplete.  
- **Generazione dinamica di report ed estrazione di contenuti** – Nei sistemi di generazione automatica di report, cerca in modo intelligente ed estrai blocchi di dati del periodo corrente contrassegnati con identificatori specifici (ad esempio `"[KPI]"`) da fogli modello contenenti dati misti (`Monthly_Metrics!C10:G50`) per compilare il report finale.  
- **Analisi di contratti e documenti legali** – Durante la revisione di allegati in fogli di calcolo contenenti molte clausole, individua in modo efficiente termini giuridici specifici (ad esempio `"limite di responsabilità"`), nomi di parti o date all’interno di un intervallo definito (`Contract_Terms!A:A`) per velocizzare il processo di revisione.

## Perché utilizzare la funzionalità di ricerca del contenuto all’interno di un intervallo del foglio di calcolo?

- **Semplice per gli sviluppatori** – Aspose.Cells Cloud offre librerie SDK in molteplici linguaggi, consentendo uno sviluppo rapido e dotato di documentazione completa, riducendo significativamente il carico di lavoro rispetto alla creazione di soluzioni personalizzate.  
- **Riduzione dei costi del personale** – Elimina la necessità di figure dedicate alla gestione della consolidazione dei documenti.  
- **Pay-per-use** – Nessun investimento iniziale; si paga solo per le chiamate API effettivamente utilizzate.  
- **Nessun costo di manutenzione** – Nessun server da gestire, nessun aggiornamento software e nessun problema di compatibilità.

## Come utilizzare la funzionalità di ricerca del contenuto all’interno di un intervallo del foglio di calcolo con gli SDK

### Specifica OpenAPI

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchContentInRemoteRange) definiscono un’interfaccia di programmazione pubblicamente accessibile e consentono di effettuare interazioni REST direttamente da un browser web.

### Utilizzare gli SDK Aspose.Cells Cloud

L’utilizzo dell’SDK rappresenta il modo più efficiente per accelerare lo sviluppo. L’SDK gestisce i dettagli sottostanti, consentendo di implementare facilmente la ricerca di contenuti in un intervallo di fogli di calcolo con pochissimo codice. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per l’elenco completo degli SDK Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInRemoteRange.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInRemoteRange.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInRemoteRange.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInRemoteRange.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInRemoteRange.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInRemoteRange.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInRemoteRange.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInRemoteRange.go" >}}
{{</tab>}}
{{< /tabs >}}