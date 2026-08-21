---
title: "Aspose.Cells Cloud – Rilevamento Link Rotti in un Intervallo Excel (API)"
second_title: "Documento"
ArticleTitle: "Individua e Risolvi Link Rotti in un Intervallo Excel Remoto – Controllore Link Foglio di Calcolo Cloud"
linktype: "Search Broken Links in Remote Range"
type: docs
url: /it/search-broken-links-in-remote-range/
keywords: "Aspose, Cells, link rotti, API, intervallo Excel, convalida, cloud, foglio di calcolo, riferimento esterno, controllore"
description: "Utilizza l'API Aspose.Cells Cloud per analizzare un intervallo specifico di Excel alla ricerca di link esterni rotti, formule non valide o origini dati mancanti. Sicuro, veloce e basato sul cloud."
weight: 100
---

## **Ricerca di Link Rotti in un Intervallo Remoto tramite API**

Rileva automaticamente i link rotti nei dati degli intervalli dei file Excel archiviati nell'archiviazione cloud. La nostra API analizza intervalli specifici alla ricerca di riferimenti esterni rotti, formule non valide e origini dati mancanti. Supporta la revisione di fogli di calcolo remoti, controlli automatici di qualità e integrazione con fornitori di archiviazione cloud. API RESTful per l'automazione dei flussi di lavoro aziendali.

### **API Web**

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/search/broken-links
```

### **Sicurezza e Autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Parametri della Richiesta

| Nome Parametro | Tipo   | Posizione | Descrizione                                                                                                                                                                      |
| ---------------- | ------ | --------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name             | String | Path      | **Obbligatorio.** Il nome del file di cartella di lavoro Excel (ad esempio `financial_report.xlsx`) archiviato nell'archiviazione cloud da analizzare per link rotti.            |
| worksheet        | String | Path      | **Obbligatorio.** Il nome del foglio di calcolo specifico (ad esempio `Sheet1`, `Q4_Data`) all'interno della cartella di lavoro in cui eseguire la ricerca dei link rotti.       |
| cellArea         | String | Path      | **Obbligatorio.** L'indirizzo dell'intervallo di celle di destinazione (ad esempio `A1:F100`) all'interno del foglio specificato da analizzare per riferimenti esterni rotti, formule o link. |
| folder           | String | Query     | **Facoltativo.** Il percorso della directory nell'archiviazione cloud in cui si trova la cartella di lavoro di destinazione. Se omesso, viene assunta la directory principale.  |
| storageName      | String | Query     | **Facoltativo.** Il nome del servizio di archiviazione cloud configurato (ad esempio `DropboxBusiness`, `S3Bucket`). Se non specificato, l'API utilizza l'archiviazione predefinita dell'account. |
| region           | String | Query     | **Facoltativo.** L'impostazione locale (ad esempio `en-GB`, `de-DE`) da applicare per l'interpretazione dei dati specifici della regione durante l'analisi.                      |
| password         | String | Query     | **Facoltativo.** La password di decriptazione necessaria per accedere a una cartella di lavoro protetta da password. Lasciare vuoto se il file non è criptato.                   |

**Esempio di Corpo della Richiesta**

```json
{
  "name": "financial_report.xlsx",
  "worksheet": "Sheet1",
  "cellArea": "A1:F100",
  "folder": "reports/2024",
  "storageName": "MyDropbox",
  "region": "en-US",
  "password": ""
}
```

### Risposta

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

L'insieme `BrokenLinks` contiene oggetti di tipo **BrokenLink**. Ciascun oggetto fornisce le seguenti proprietà:

- **CellName** – L’indirizzo della cella contenente il riferimento rotto (ad esempio `B12`).
- **LinkType** – Il tipo di link rotto (ad esempio `ExternalReference`, `Formula`).
- **ErrorMessage** – Una descrizione del motivo per cui il link è considerato rotto.

**Nota**: l'API è soggetta a limiti di frequenza. Consultare la pagina [Prezzi e Limiti di Frequenza](https://www.aspose.cloud/pricing) per ulteriori dettagli.

### Codici di Errore

- **400 Bad Request** – URI API Aspose.Cells Cloud non valido.
- **401 Unauthorized** – Token di accesso, ID client o secret client non validi.
- **404 Not Found** – Il file del foglio di calcolo non è accessibile.
- **500 Server Error** – Si è verificata un’anomalia nel foglio di calcolo durante il recupero dei dati di calcolo.

## Dove utilizzare la Ricerca di link rotti in un intervallo del foglio di calcolo tramite API?

- **Revisione regolare di modelli finanziari di grandi dimensioni** – Prima della pubblicazione di report mensili o trimestrali, analizzare automaticamente le aree chiave di calcolo (ad esempio `Dashboard!B5:K50`) contenenti molti riferimenti a dati esterni per verificare che tutti i link puntino a file di origine validi.
- **Integrazione dati in fusioni e acquisizioni** – Durante la fusione di più file di fogli di calcolo rappresentanti unità aziendali, analizzare il foglio “Overview” dopo l’integrazione per identificare link diventati non validi a causa di percorsi di file modificati o problemi di autorizzazione.
- **Preparazione di pacchetti dati per investitori** – Prima della finalizzazione di materiali presentativi contenenti grafici e tabelle collegati a database esterni o fonti di dati di mercato, verificare la validità di tutti i link.

## Perché utilizzare la Ricerca di link rotti in un intervallo del foglio di calcolo tramite API?

- **Facile da utilizzare per sviluppatori** – Aspose.Cells Cloud offre librerie SDK in diversi linguaggi, consentendo uno sviluppo rapido con documentazione completa. Rispetto alla creazione di una soluzione personalizzata, riduce significativamente lo sforzo di sviluppo.
- **Riduzione dei costi del personale** – Elimina la necessità di personale dedicato alla consolidazione manuale dei documenti.
- **Pagamento in base all’uso** – Nessun investimento iniziale: si paga solo per le chiamate API effettivamente effettuate.
- **Costi di manutenzione nulli** – Nessun server da mantenere, nessun aggiornamento software e nessun problema di compatibilità.
- **Preserva la formattazione complessa di Excel** – I risultati possono essere esportati in formato PDF universalmente accessibile senza perdita di stile.

## Come utilizzare la Ricerca di link rotti in un intervallo del foglio di calcolo tramite API con gli SDK

### Specifica OpenAPI

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchBrokenLinksInRemoteRange) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di eseguire interazioni REST direttamente da un browser web.

### Utilizzo degli SDK Aspose.Cells Cloud

L'utilizzo degli SDK è il modo migliore per accelerare lo sviluppo. Gli SDK gestiscono i dettagli sottostanti, consentendo di implementare la funzionalità “ricerca link rotti in un intervallo” con un codice minimo. Consultare il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteRange.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteRange.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteRange.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteRange.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteRange.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteRange.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteRange.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteRange.go" >}}
{{</tab>}}
{{< /tabs >}}