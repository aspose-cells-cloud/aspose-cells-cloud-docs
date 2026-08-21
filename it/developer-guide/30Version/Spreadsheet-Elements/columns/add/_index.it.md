---
title: "Aggiungi una colonna vuota a un foglio di calcolo Excel - API Aspose.Cells Cloud"
second_title: "Documento"
linktitle: "Aggiungi"
type: docs
url: /columns/add/
aliases:
  - /add-an-empty-column-in-an-excel-worksheet/
  - /add-an-empty-column-in-a-worksheet/
keywords: "aggiungi, colonna, Excel, API, Aspose.Cells, Cloud, REST, inserisci"
description: "Scopri come inserire una nuova colonna in un foglio Excel utilizzando l'API REST Aspose.Cells Cloud. Include la sintassi della richiesta, un esempio cURL e campioni di codice SDK."
weight: 20
ArticleTitle: "Aggiungi una colonna vuota a un foglio di calcolo Excel tramite l'API Aspose.Cells Cloud"
---

Questa API REST inserisce una o più colonne in un foglio di calcolo.

**Prerequisiti**  
Prima di chiamare questo endpoint, assicurati di aver completato i seguenti passaggi:

- Ottenere un token di accesso OAuth 2.0 valido e includerlo nell'intestazione `Authorization`.
- Archiviare il workbook di destinazione nell'archivio selezionato (quello predefinito = “Default”) oppure specificare i parametri `folder` e `storageName` appropriati.
- Verificare che il nome del foglio di calcolo fornito in `sheetName` esista nel workbook.

## API PutInsertWorksheetColumns

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}?totalColumns=1
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro      | Tipo    | Posizione | Descrizione                                                          |
| ------------------- | ------- | --------- | -------------------------------------------------------------------- |
| **name**            | string  | path      | Nome del file workbook.                                              |
| **sheetName**       | string  | path      | Nome del foglio di calcolo.                                          |
| **columnIndex**     | integer | path      | Indice in base zero della colonna da cui inizia l'inserimento.      |
| **totalColumns**    | integer | query     | Numero di colonne da inserire.                                       |
| **updateReference** | boolean | query     | Se **true**, i riferimenti alle celle vengono aggiornati per riflettere l'inserimento. |
| **folder**          | string  | query     | Percorso della cartella contenente il workbook.                      |
| **storageName**     | string  | query     | Nome del servizio di archiviazione.                                  |

**Note**

- Il valore `columnIndex` deve essere compreso tra 0 e il numero attuale di colonne nel foglio di calcolo. L'inserimento oltre l'intervallo esistente espanderà automaticamente il foglio.  
- L'inserimento di più colonne (`totalColumns` > 1) sposta le colonne esistenti verso destra.  
- L'opzione `updateReference` è impostata su `false` per impostazione predefinita; impostarla su `true` per aggiornare formule e intervalli denominati.

La [specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PutInsertWorksheetColumns) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per chiamare i servizi web Aspose.Cells. L'esempio seguente mostra una richiesta completa, inclusa l'autenticazione e il corretto parametro di percorso.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/1?totalColumns=1&updateReference=true" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Codici di risposta**

| Codice | Descrizione                                 |
|--------|---------------------------------------------|
| 200    | Colonna/e inserita/e correttamente.         |
| 400    | Richiesta non valida – parametri mancanti o non validi. |
| 401    | Non autorizzato – token non valido o mancante. |
| 404    | Workbook o foglio di calcolo non trovato.   |
| 500    | Errore interno del server.                  |

**Esempi di risposte di errore**

```json
// 400 Bad Request – parametri mancanti o non validi
{
  "Code": 400,
  "Message": "Parametro non valido: totalColumns deve essere un intero positivo."
}

// 401 Unauthorized – token non valido o mancante
{
  "Code": 401,
  "Message": "Autenticazione non riuscita. Il token di accesso è mancante o non valido."
}

// 404 Not Found – workbook o foglio di calcolo non esistente
{
  "Code": 404,
  "Message": "Workbook 'test.xlsx' non trovato."
}

// 500 Internal Server Error
{
  "Code": 500,
  "Message": "Si è verificato un errore imprevisto sul server."
}
```

## Famiglia di SDK Cloud

L'utilizzo di un SDK è il modo più rapido per sviluppare. Un SDK gestisce i dettagli a basso livello, consentendoti di concentrarti sulla logica del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutInsertWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutInsertWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutInsertWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutInsertWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutInsertWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutInsertWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutInsertWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutInsertWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}
---