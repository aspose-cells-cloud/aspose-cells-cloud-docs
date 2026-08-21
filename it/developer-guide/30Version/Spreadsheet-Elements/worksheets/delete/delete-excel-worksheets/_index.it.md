---
title: "Elimina più fogli di calcolo Excel"
second_title: "Documento"
linktitle: "Più fogli di calcolo"
type: docs
url: /it/worksheets/delete-multiple/
aliases: [  /it/delete-excel-worksheets/ ]
keywords: "Aspose.Cells Cloud, elimina più fogli di calcolo, API Excel, API REST, v3.0, elimina fogli di calcolo"
description: "Scopri come eliminare diversi fogli di calcolo da un file Excel utilizzando l'API REST di Aspose.Cells Cloud (v3.0). Include un endpoint HTTPS sicuro, i parametri obbligatori, un esempio corretto di cURL e frammenti di codice SDK per diversi linguaggi di programmazione."
weight: 20
ArticleTitle: "Elimina più fogli di calcolo Excel utilizzando l'API REST di Aspose.Cells Cloud"
---

Questa API REST elimina più fogli di calcolo da un file di lavoro.

## Sicurezza e autenticazione
Le API di Aspose.Cells Cloud sono sicure e richiedono l'[autenticazione basata su token JWT](https://docs.aspose.cloud/it/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets
```

### **Parametri della richiesta**

| Nome parametro | Tipo   | Posizione | Descrizione                                                                 |
| -------------- | ------ | --------- | --------------------------------------------------------------------------- |
| name           | string | path      | Nome del file Excel.                                                        |
| matchCondition | object | body      | Oggetto `MatchConditionRequest` che specifica quali fogli di calcolo eliminare. |
| folder         | string | query     | Percorso della cartella nello storage in cui si trova il file.              |
| storageName    | string | query     | Nome del servizio di storage.                                               |

**Proprietà di MatchConditionRequest**

| Nome                | Tipo     | Descrizione                                  | Note     |
| ------------------- | -------- | -------------------------------------------- | -------- |
| RegexPattern        | string   | Espressione regolare per abbinare i nomi dei fogli di calcolo. | opzionale |
| FullMatchConditions | string[] | Nomi esatti dei fogli di calcolo da eliminare. | opzionale |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheets) definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API cloud con cURL. **È richiesto un token JWT valido nell'intestazione `Authorization`.**

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets?folder=Temp" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>" \
  -d '{"FullMatchConditions":["Foglio1","Foglio2","Foglio3"]}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

La richiesta può inoltre restituire risposte di errore comuni, ad esempio:

| Stato HTTP | Significato                                     | Payload di esempio                                      |
| ---------- | ----------------------------------------------- | ------------------------------------------------------- |
| 400        | Richiesta non valida – JSON o parametri non validi | `{"Code":400,"Message":"Payload della richiesta non valido."}` |
| 401        | Non autorizzato – token JWT mancante o non valido | `{"Code":401,"Message":"Autenticazione non riuscita."}` |
| 403        | Accesso negato – permessi insufficienti         | `{"Code":403,"Message":"Accesso negato."}`             |
| 404        | Non trovato – file o foglio di calcolo inesistente | `{"Code":404,"Message":"Risorsa non trovata."}`        |
| 500        | Errore interno del server                       | `{"Code":500,"Message":"Si è verificato un errore imprevisto."}` |

{{< /tab >}}

{{< /tabs >}}

## Famiglia di SDK cloud

L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheets.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheets.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheets.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheets.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheets.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheets.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Vedi anche:**  
- [Elimina un singolo foglio di calcolo](https://docs.aspose.cloud/cells/it/worksheets/delete/)  
- [Copia foglio di calcolo](https://docs.aspose.cloud/cells/it/worksheets/copy/)  
- [Sposta foglio di calcolo](https://docs.aspose.cloud/cells/it/worksheets/move/)  
---