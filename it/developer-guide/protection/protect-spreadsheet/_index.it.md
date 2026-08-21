---
title: "Aspose.Cells Cloud Excel Password Protection Web API – Automatizzare la crittografia delle password di apertura e modifica"
second_title: "Guida per sviluppatori alla protezione di Excel"
ArticleTitle: "Strumento per la protezione di Excel – Imposta password di apertura e modifica – Sicurezza dei tuoi fogli di calcolo"
linktype: "Proteggi foglio di calcolo"
type: docs
url: /it/protect-spreadsheet/
keywords: "Aspose.Cells, protezione password Excel, API, password di apertura, password di modifica, archiviazione cloud, sicurezza dei fogli di calcolo"
description: "Proteggi i file Excel in modo programmatico con Aspose.Cells Cloud. Imposta sia la password di apertura che quella di modifica con una singola chiamata API. Supporta .xlsx, .xls e archiviazione cloud. Provalo gratuitamente."
weight: 100
---

Automatizza la protezione delle password di Excel su larga scala con la nostra API per sviluppatori — applica sia la password di apertura che quella di modifica in modo programmatico. Ideale per flussi di lavoro aziendali e compatibile con i formati .xlsx e quelli legacy. Consulta la documentazione e inizia subito la tua integrazione gratuita.

## **API per la protezione del foglio di calcolo**

### **API Web**

```http
PUT https://api.aspose.cloud/v4.0/cells/protection/spreadsheet
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione tramite token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Parametri della richiesta:**

| Nome parametro | Tipo   | Percorso/QueryString/Corpo HTTP | Descrizione                                                                                                                                   |
| :------------- | :----- | :---------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | File   | FormData                      | Il file di foglio di calcolo Excel da caricare e proteggere con la crittografia tramite password.                                           |
| openPassword   | String | Query                         | La password necessaria per aprire (decrittografare) il foglio di calcolo protetto.                                                           |
| modifyPassword | String | Query                         | La password necessaria per abilitare la modifica o la modifica dei contenuti del foglio di calcolo.                                           |
| outPath        | String | Query                         | (Opzionale) Specifica il percorso della cartella di output in cui verrà salvato il foglio di calcolo protetto. Se non fornito, il file viene restituito nella risposta. |
| outStorageName | String | Query                         | Il nome dell'archiviazione cloud utilizzata per memorizzare il file protetto in output.                                                     |
| region         | String | Query                         | Specifica le impostazioni regionali/culturali (ad esempio, formato data, formattazione numerica) applicate al foglio di calcolo durante l'elaborazione. |

**Autenticazione**  
Tutte le chiamate all'API per la protezione del foglio di calcolo richiedono un token di accesso OAuth 2.0 valido. Includi il token nell'intestazione `Authorization`:

```http
Authorization: Bearer {access_token}
```

Il token deve essere ottenuto dall'endpoint di autenticazione di Aspose Cloud e deve includere l'ambito **Cells**.

## **Risposta**

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

| Codice | Significato            | Descrizione                                                      |
| ------ | ---------------------- | ---------------------------------------------------------------- |
| 200    | OK                     | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida   | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato        | Token JWT non valido o mancante.                                 |
| 413    | Payload troppo grande  | Il file caricato supera il limite di dimensione.                |
| 500    | Errore interno del server | Errore imprevisto del server.                                   |

## Dove dovremmo utilizzare l'API per la protezione del foglio di calcolo?

- **Proteggi dati finanziari sensibili** – Proteggi i file Excel contenenti budget, fatture o informazioni sulla busta paga con password di apertura e modifica per impedire accessi o modifiche non autorizzate.
- **Condividi report confidenziali in sicurezza** – Garantisci che solo i destinatari autorizzati possano visualizzare o modificare report aziendali, di audit o di conformità durante la distribuzione interna o esterna.
- **Automatizza la sicurezza dei documenti nei flussi di lavoro** – Integra l'API nei sistemi aziendali (ad esempio, ERP, CRM) per proteggere automaticamente con password i fogli di calcolo generati prima del salvataggio o della consegna via email.
- **Applica accesso in sola lettura** – Consenti agli utenti di aprire i report solo per la visualizzazione, limitando le modifiche tramite una password di modifica separata — ideale per modelli o dataset finalizzati.
- **Raggiungi la conformità normativa** – Aiuta a soddisfare i requisiti GDPR, HIPAA o SOX crittografando i dati sensibili nei fogli di calcolo sia a riposo che in transito, tramite protezione automatizzata.

## Perché dovresti utilizzare l'API per la protezione del foglio di calcolo?

- **Facile da usare per sviluppatori** – Aspose.Cells Cloud offre librerie SDK in diversi linguaggi, consentendo uno sviluppo rapido e accompagnato da una documentazione completa. Rispetto alla creazione di soluzioni personalizzate, riduce significativamente il carico di lavoro di sviluppo.
- **Riduce la necessità di personale** – Automatizza la consolidation e la sicurezza dei documenti, riducendo la necessità di personale dedicato.
- **Pay-per-use (pagamento solo per l’uso)** – Nessun investimento iniziale; paghi solo per le chiamate API effettivamente utilizzate.
- **Costi di manutenzione nulli** – Nessun server da mantenere, nessun aggiornamento software e nessuna preoccupazione di compatibilità.
- **Preserva tutta la formattazione originale di Excel** durante l'applicazione della protezione tramite password, garantendo che il foglio di calcolo protetto abbia esattamente lo stesso aspetto del file sorgente.

## Come utilizzare l'API per la protezione del foglio di calcolo con gli SDK

### Specifica OpenAPI

La [specifiche dell'API per la protezione del foglio di calcolo](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Protection/ProtectSpreadsheet) fornisce un'interfaccia di programmazione accessibile pubblicamente per facilitare interazioni REST dirette da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/protection/spreadsheet?openPassword=MyOpenPwd&modifyPassword=MyModifyPwd" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/workbook.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (codificato in Base64)",
  "contentType": "tipo MIME",
  "fileDownloadName": "nome file opzionale"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo dell'SDK è il modo migliore per accelerare lo sviluppo. L'SDK gestisce i dettagli sottostanti, consentendoti di implementare semplicemente la funzionalità di protezione del foglio di calcolo con pochissimo codice. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per l'elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice illustrano come interagire con i servizi web di Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ProtectSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ProtectSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ProtectSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ProtectSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ProtectSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ProtectSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ProtectSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ProtectSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}