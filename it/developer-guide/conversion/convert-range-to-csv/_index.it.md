---
title: "Convertire Intervallo Excel in CSV – Aspose.Cells Cloud API"
second_title: "Documento"
ArticleTitle: "Come convertire un intervallo locale di un foglio di calcolo in un file CSV: Guida passo-passo"
linktype: "Converti intervallo in CSV"
type: docs
url: /it/convert-range-to-csv/
keywords: "Aspose Cells, Convertire intervallo in CSV, Excel in CSV, API Excel, Foglio di calcolo cloud, Convertire, Excel, CSV, Aspose.Cells, API cloud"
description: "Scopri come convertire un intervallo specifico da un file Excel locale (XLSX o XLS) in CSV utilizzando l’API REST Aspose.Cells Cloud. Include sintassi delle richieste, parametri, gestione degli errori ed esempi di SDK."
---

Esporta un intervallo specifico da un file Excel locale in CSV utilizzando l’API Aspose.Cells Cloud.

## **Convertire intervallo in CSV – API**

**Prerequisiti**  
Per chiamare questo endpoint è necessario disporre di un **client ID** e di un **client secret** Aspose Cloud validi, ottenere un **token di accesso JWT** e accertarsi che il foglio di calcolo di origine sia in formato **XLSX** o **XLS**.

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/csv
```

**Esempio cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/csv?worksheet=Foglio1&range=A1:C10" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@esempio.xlsx"
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono l’<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### **Parametri della richiesta:**

| Nome parametro | Tipo   | Percorso/QueryString/Corpo HTTP | Descrizione                                                                     |
| :------------- | :----- | :----------------------------- | :------------------------------------------------------------------------------ |
| Spreadsheet    | File   | FormData                       | Carica il file del foglio di calcolo.                                           |
| worksheet      | String | Query                          | Nome del foglio di calcolo.                                                     |
| range          | String | Query                          | Specifica l’area di celle (ad esempio, A1:C10).                                 |
| outPath        | String | Query                          | Percorso della cartella in cui verrà salvato il foglio di calcolo (opzionale). Default: null. |
| outStorageName | String | Query                          | Nome dello storage di output.                                                   |
| fontsLocation  | String | Query                          | Specifica i caratteri personalizzati, se necessari.                             |
| region         | String | Query                          | Definisce l’impostazione della regione del foglio di calcolo.                   |
| password       | String | Query                          | Password necessaria per aprire il file del foglio di calcolo.                   |

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

_Esempio di contenuto CSV restituito (prime righe):_

```csv
Nome,Data,Importo
Mario Rossi,2023-01-15,1250,00
Giulia Bianchi,2023-01-16,980,50
```

**Codici di stato HTTP**

| Codice | Significato              | Descrizione                                                       |
| ------ | ------------------------ | ----------------------------------------------------------------- |
| 200    | OK                       | Filtro applicato correttamente; la risposta contiene i dettagli dell’operazione. |
| 400    | Richiesta non valida     | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato          | Token JWT non valido o mancante.                                  |
| 413    | Payload troppo grande    | Il file caricato supera il limite di dimensione.                 |
| 500    | Errore interno del server | Errore imprevisto del server.                                     |

## Dove utilizzare l’API Converti intervallo in CSV?

### **1. Esportazione e migrazione di dati**

- **Integrazione con database**: Esporta intervalli specifici di Excel direttamente nei sistemi di database.
- **Integrazione con applicazioni**: Fornisci dati selezionati del foglio di calcolo alle applicazioni SaaS.
- **Migrazione di sistemi**: Trasferisci intervalli specifici di dati tra sistemi legacy e moderni.
- **Condivisione cross-platform**: Condividi sottoinsiemi di dati mirati tra diverse piattaforme.

### **2. Reporting e analisi**

- **Reporting mirato**: Esporta sezioni specifiche di report in CSV per un’analisi mirata.
- **Feed di dati per dashboard**: Fornisci intervalli di dati specifici agli strumenti BI per dashboard.
- **Metriche di performance**: Estrai intervalli di KPI per sistemi di monitoraggio delle prestazioni.
- **Reporting finanziario**: Esporta sezioni di bilanci per audit esterni.

### **3. Sviluppo e testing**

- **Gestione dati di test**: Esporta intervalli specifici per scopi di test.
- **Ambienti di sviluppo**: Condividi intervalli di dati di esempio con i team di sviluppo.
- **Testing API**: Genera dati di test in formato CSV da sezioni specifiche del foglio di calcolo.
- **Sviluppo di prototipi**: Fornisci set di dati mirati per prototipi di applicazioni.

### **4. Operazioni aziendali**

- **Condivisione selettiva di dati**: Condividi intervalli specifici con partner esterni.
- **Backup parziale dei dati**: Esegui il backup di intervalli critici in formato CSV.
- **Trasferimento dati tra reparti**: Condividi dati specifici tra reparti diversi.
- **Reporting per conformità**: Esporta intervalli di dati normativi per la presentazione di report di conformità.

### **5. Automazione dei flussi di lavoro**

- **Esportazione pianificata di intervalli**: Esporta automaticamente intervalli specifici su base pianificata.
- **Estrazione basata su trigger**: Esporta intervalli in base a eventi o trigger aziendali.
- **Integrazione nei flussi di lavoro**: Integra l’esportazione di intervalli nei processi aziendali.
- **Elaborazione batch di intervalli**: Elabora più intervalli specifici in operazioni batch.

## Perché utilizzare l’API Converti intervallo in CSV?

- Puoi convertire un intervallo di un foglio di calcolo senza caricare preventivamente l’intero file, risparmiando spazio di archiviazione e riducendo i costi.
- Lo sviluppo può essere completato rapidamente utilizzando gli SDK esistenti di Aspose.Cells Cloud.
- **Integrazione semplice**: API REST con documentazione chiara.
- **Architettura scalabile**: Gestisce operazioni da piccole a di scala enterprise.

## Come utilizzare l’API Converti intervallo in CSV con gli SDK?

### Specifica OpenAPI

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToCSV) definiscono un’API pubblicamente accessibile, che consente interazioni REST direttamente da un browser web.

## Utilizzare gli SDK di Aspose.Cells Cloud

Utilizzare gli SDK è il modo più rapido per sviluppare, poiché nasconde i dettagli di basso livello, consentendo di convertire un intervallo di dati in un file CSV con un codice minimo.  
Esplora l’elenco completo degli SDK di Aspose.Cells Cloud nel nostro [repository GitHub](https://github.com/aspose-cells-cloud).

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK. Se il caricamento da Gist è bloccato, puoi scaricare gli esempi direttamente dal repository.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToCSV.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToCSV.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToCSV.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToCSV.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToCSV.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToCSV.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToCSV.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToCSV.go" >}}
{{</tab>}}
{{< /tabs >}}