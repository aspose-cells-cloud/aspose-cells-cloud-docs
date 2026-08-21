---
title: "Aspose.Cells Cloud Web API – Convertire i dati locali di una tabella Excel in un file JSON"
second_title: "Documento"
ArticleTitle: "Come convertire i dati locali di una tabella in foglio elettronico in un file JSON: Guida passo-passo"
linktype: "Converti tabella in JSON"
type: docs
url: /convert-table-to-json/
keywords: "Excel, API, JSON, conversione, cloud, file, foglio elettronico"
description: "Utilizza l'API Aspose.Cells Cloud per trasformare una tabella Excel locale in un file JSON in una singola richiesta PUT. Include un esempio cURL, i parametri e frammenti di codice SDK per C#, Java, Python e altri linguaggi."
weight: 100
---

Converti una tabella in un foglio elettronico/Excel locale in un file **JSON** con l'API Web Aspose.Cells Cloud.

## **API per la conversione di tabelle in JSON**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/json
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro     | Tipo   | Posizione | Descrizione                                                                                      |
| ------------------ | ------ | --------- | ------------------------------------------------------------------------------------------------ |
| **Spreadsheet**    | File   | FormData  | Il file Excel da caricare.                                                                      |
| **worksheet**      | String | Query     | Nome del foglio di calcolo contenente la tabella.                                               |
| **tableName**      | String | Query     | Nome della tabella da convertire.                                                               |
| **outPath**        | String | Query     | (Opzionale) Percorso della cartella in cui verrà salvato il file JSON risultante; valore predefinito: **null**. |
| **outStorageName** | String | Query     | (Opzionale) Nome dello storage in cui verrà posizionato il file di output.                      |
| **fontsLocation**  | String | Query     | (Opzionale) Percorso dei caratteri personalizzati utilizzati durante la conversione.            |
| **region**         | String | Query     | (Opzionale) Impostazioni internazionali per il foglio di calcolo.                               |
| **password**       | String | Query     | (Opzionale) Password per aprire un foglio di calcolo protetto.                                  |

### Risposta

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
| 400    | Richiesta non valida    | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato         | Token JWT non valido o mancante.                                  |
| 413    | Payload troppo grande   | Il file caricato supera il limite di dimensione.                 |
| 500    | Errore interno del server | Errore imprevisto nel server.                                    |

## **Dove dovresti utilizzare l'API per la conversione di tabelle in JSON?**

- **Dashboard in tempo reale** – Converti i dati Excel in tempo reale in JSON per librerie di grafica come Chart.js o D3.js.
- **Foglio elettronico come servizio** – Esporre tabelle Excel come endpoint JSON per altri microservizi.
- **Payload di webhook** – Trasforma i dati dei fogli elettronici in JSON per notifiche webhook.
- **Prototipazione rapida dei dati** – Converti rapidamente dati Excel puliti in JSON per l'analisi con Python o R.
- **Pipeline di machine learning** – Preprocessa dati di addestramento memorizzati in fogli elettronici aziendali.
- **Operazioni e-commerce** – sincronizza cataloghi prodotti o fogli prezzi con siti web tramite JSON.
- **Automazione dei report** – Genera feed JSON da modelli finanziari per report automatizzati.
- **Configurazione di applicazioni** – Gestisci flag funzionali, impostazioni o parametri di test A/B in Excel → JSON.
- **Supporto multilingua** – Converti fogli elettronici di localizzazione in JSON per librerie i18n.
- **Menu/navigazione dinamica** – Memorizza strutture di navigazione di siti web in Excel e distribuiscile come JSON.

## Perché dovresti utilizzare l'API per la conversione di tabelle in JSON?

- **Facile da usare per sviluppatori** – Aspose.Cells Cloud fornisce SDK per molti linguaggi, riducendo lo sforzo di sviluppo e offrendo documentazione completa.
- **Conveniente** – Converti i dati della tabella senza caricare preventivamente il foglio di calcolo, risparmiando spazio di archiviazione e riducendo i costi.
- **Compatibilità con web e mobile moderni** – JSON è il linguaggio nativo dei dati sul web; l'API consente di alimentare direttamente dati di fogli elettronici in tempo reale in React, Vue, Angular, applicazioni mobili o applicazioni a pagina singola, senza complessa analisi.
- **Ampio supporto linguistico** – JSON funziona con praticamente ogni linguaggio di programmazione, database e servizio web.
- **Preservazione della struttura dei dati**
  - **Rilevamento intelligente della struttura** – Converte automaticamente i dati tabellari in array/oggetti JSON corretti.
  - **Mappatura intestazioni** – Utilizza la prima riga come chiavi JSON per strutture di oggetti pulite.
  - **Conservazione dei tipi di dati** – Preserva numeri, date e booleani (non solo testo).

_Cronologia versioni:_ L'endpoint per la conversione di tabelle in JSON è stato introdotto con la versione API **v4.0** (2024) e rimane l'attuale versione stabile. Gli endpoint precedenti v3.x sono deprecati.

## Come utilizzare l'API per la conversione di tabelle in JSON con gli SDK?

### Specifica dell'API per la conversione di tabelle in JSON

La [Specifiche dell'API per la conversione di tabelle in JSON](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToJson){:target="\_blank" rel="noopener noreferrer"} fornisce un'interfaccia di programmazione accessibile pubblicamente, consentendo interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/json?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.json
```

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/json?worksheet=Sheet1&tableName=MyTable" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/your/file.xlsx" \
     -F "outPath=output/folder" \
     -F "outStorageName=MyStorage"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (in Base64)",
  "contentType": "tipo MIME",
  "fileDownloadName": "nome file opzionale"
}
```

```
{
 "Code": 200,
 "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK astrae i dettagli a basso livello, consentendoti di convertire una tabella di foglio elettronico in un file JSON con un codice minimo. Consulta il repository GitHub ufficiale per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come interagire con i servizi web Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToJson.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToJson.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToJson.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToJson.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToJson.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToJson.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToJson.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToJson.go" >}}  
{{</tab>}}  
{{< /tabs >}}