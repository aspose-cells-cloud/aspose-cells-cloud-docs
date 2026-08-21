---
title: "Aspose.Cells Cloud – API per il rilevamento dei link rotti in Excel – Analisi e convalida dei link in fogli di calcolo remoti"
second_title: "Documento"
ArticleTitle: "Individuazione e correzione dei link rotti in un foglio di calcolo Excel remoto – Controlla link foglio di calcolo cloud"
linktitle: "Ricerca link rotti in fogli di calcolo remoti"
type: docs
url: /it/search-broken-links-in-remote-worksheet/
keywords: "Aspose Cells, link rotti, API Excel, foglio di calcolo cloud, convalida link"
description: "Rileva e correggi link esterni rotti in fogli di calcolo Excel archiviati nello storage cloud. Usa l’API Aspose.Cells Cloud per analizzare intervalli, restituire dettagli sui link e automatizzare controlli di qualità."
weight: 100
---

## **API per la ricerca di link rotti in un foglio di calcolo remoto**

Rileva automaticamente i link rotti in un foglio di calcolo Excel archiviato nello storage cloud. La nostra API analizza intervalli specificati per individuare riferimenti esterni rotti, formule non valide e origini dati mancanti. Supporta la verifica remota dei fogli di calcolo, controlli di qualità automatizzati e integrazione con provider di storage cloud. API RESTful per l’automazione dei flussi di lavoro aziendali.

### **API Web**

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/broken-links
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono l’<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione tramite token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Parametri della richiesta:**

| Nome parametro | Tipo   | Percorso / Stringa di query / Corpo HTTP | Descrizione                                                                                                                                                                                                                                |
| :------------- | :----- | :---------------------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name           | Stringa | Percorso                                  | **Obbligatorio.** Nome del file (esteso) del workbook Excel in cui cercare link rotti (es. `Annual_Report.xlsx`).                                                                                                                         |
| worksheet      | Stringa | Percorso                                  | **Obbligatorio.** Nome esatto del foglio di calcolo in cui verrà effettuata l’analisi dei link (es. `DataSheet1`).                                                                                                                        |
| folder         | Stringa | Query                                     | **Facoltativo.** Percorso della directory all’interno dello storage cloud in cui è posizionato il workbook di destinazione. Se omesso, viene usata la cartella radice.                                                                  |
| storageName    | Stringa | Query                                     | **Facoltativo.** Identificatore dello storage cloud configurato personalmente. Se non fornito, l’API usa lo storage predefinito dell’account.                                                                                             |
| region         | Stringa | Query                                     | **Facoltativo.** Impostazione locale da applicare durante la ricerca (es. `fr-FR`). Può influenzare l’interpretazione di determinate formule o formati di dati regionali. _I codici locali supportati includono `en-US`, `fr-FR`, `de-DE`, `es-ES`, ecc._ |
| password       | Stringa | Query                                     | **Facoltativo.** Password di decrittazione per un foglio di calcolo protetto da password. Ignorare se il file non è crittografato.                                                                                                        |

**Esempio di richiesta cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/Annual_Report.xlsx/worksheets/DataSheet1/search/broken-links?folder=Reports&storageName=MyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

### **Risposta**

```json
{
  "Code": 200,
  "Status": "OK",
  "BrokenLinks": [
    {
      "Address": "='C:\\Data\\Source.xlsx'!A1",
      "ErrorCode": "404",
      "ErrorMessage": "File di origine non trovato"
    }
  ]
}
```

L’oggetto di risposta è di tipo **BrokenLinksResponse** e contiene:

- **BrokenLinks** – una raccolta di elementi `BrokenLink`, ognuno dei quali descrive il riferimento problematico (indirizzo, codice di errore e messaggio).
- **Code** – codice numerico di stato restituito dal servizio.
- **Status** – descrizione testuale del risultato.

**Note**: l’API non effettua la paginazione dei risultati. Per ogni richiesta è possibile restituire fino a 10.000 link rotti. Il limite di frequenza è di 100 richieste al minuto per account.

### Codici di errore

- **400 Bad Request** – URI API Aspose.Cells Cloud non valido.
- **401 Unauthorized** – Token di accesso non valido o mancante.
- **404 Not Found** – Il file del foglio di calcolo non è accessibile.
- **500 Server Error** – Si è verificato un’anomalia durante il recupero dei dati di calcolo.

## Dove conviene usare l’API per la ricerca di link rotti all’interno del foglio di calcolo?

- **Audit regolari di modelli finanziari di grandi dimensioni**: Prima della pubblicazione di report mensili o trimestrali, esegui automaticamente la scansione delle aree chiave di calcolo (come `Dashboard!B5:K50`) contenenti molti riferimenti a dati esterni, per verificare che tutti i link puntino a file di origine validi.
- **Integrazione dati in fusioni e acquisizioni**: Durante la fusione di più file di calcolo rappresentanti unità aziendali, analizza il foglio "Panoramica" dopo il processo di integrazione per individuare link diventati non validi a causa di modifiche nei percorsi dei file di origine o di problemi di autorizzazione.
- **Preparazione di pacchetti dati per investitori**: Prima di finalizzare materiali presentativi contenenti grafici e tabelle collegati a database esterni o fonti di dati di mercato, verifica la validità di tutti i link.

## Perché usare l’API per la ricerca di link rotti all’interno del foglio di calcolo?

- **Semplice per gli sviluppatori**: Aspose.Cells Cloud offre librerie SDK in molteplici linguaggi, consentendo uno sviluppo rapido e accompagnato da una documentazione completa. Rispetto alla creazione di soluzioni personalizzate per il rendering dei grafici, riduce significativamente il carico di sviluppo.
- **Riduzione dei costi del personale**: Elimina la necessità di personale dedicato alla consolidazione manuale dei documenti e alla verifica dei link.
- **Pay-per-use**: Nessun investimento iniziale; si paga soltanto per le chiamate API effettivamente utilizzate.
- **Costi di manutenzione nulli**: Nessun server da mantenere, nessun aggiornamento software, nessun problema di compatibilità da gestire.
- **Preserva la formattazione complessa di Excel** in formato PDF universalmente accessibile.

## Come usare l’API per la ricerca di link rotti all’interno del foglio di calcolo con gli SDK

### Specifica OpenAPI

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceContentInRemoteWorksheet) definiscono un’interfaccia di programmazione pubblicamente accessibile e consentono di effettuare direttamente interazioni REST da un browser web.

### Utilizzo degli SDK Aspose.Cells Cloud

L’uso degli SDK rappresenta il modo migliore per accelerare lo sviluppo. L’SDK gestisce i dettagli sottostanti, consentendo di implementare semplicemente la ricerca di link rotti all’interno dei fogli di calcolo con un numero minimo di righe di codice. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per l’elenco completo degli SDK Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web Aspose.Cells Cloud usando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}
---