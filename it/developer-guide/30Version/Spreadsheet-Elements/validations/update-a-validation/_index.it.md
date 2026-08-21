---
title: "Aggiornare una convalida di un foglio di calcolo Excel"
second_title: "Documento"
linktitle: "Aggiornamento"
type: docs
url: /it/validations/update/
keywords: "Aspose.Cells Cloud, aggiornamento convalida Excel, API REST, convalida foglio di calcolo, API Excel"
description: "Come aggiornare una convalida di un foglio di calcolo in un file Excel utilizzando l'API REST di Aspose.Cells Cloud, con esempi in cURL e frammenti di codice SDK per diversi linguaggi di programmazione."
weight: 10
ArticleTitle: "Aggiornare la convalida del foglio di calcolo usando l'API Aspose.Cells Cloud"
---

Questa API REST aggiorna una convalida di un foglio di calcolo tramite il suo indice in un foglio di calcolo Excel.

Prima di chiamare questo endpoint, ottieni un token di accesso JWT con gli ambiti appropriati (ad esempio `Cells.ReadWrite`). Includi il token nell'intestazione `Authorization`, come mostrato negli esempi.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
```

### **Parametri della richiesta**

| Nome parametro  | Tipo    | Posizione | Descrizione                                                    |
| --------------- | ------- | --------- | -------------------------------------------------------------- |
| name            | string  | path      | Il nome del file del workbook.                                 |
| sheetName       | string  | path      | Il nome del foglio di calcolo che contiene la convalida.       |
| validationIndex | integer | path      | L'indice in base zero della convalida da aggiornare.           |
| validation      | object  | body      | Un oggetto JSON che definisce le impostazioni aggiornate della convalida. |
| folder          | string  | query     | La cartella nello storage cloud in cui si trova il workbook.   |
| storageName     | string  | query     | Il nome del servizio di storage (se viene utilizzato uno storage personalizzato). |

La <a href="https://apireference.aspose.cloud/cells/#/WorksheetValidations/PostWorksheetValidation" target="_blank" rel="noopener noreferrer">Specifiche OpenAPI</a> definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per chiamare facilmente i servizi web Aspose.Cells. L'esempio seguente mostra come effettuare una chiamata all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations/0" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{ "AlertStyle":"Warning" }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Codici di stato HTTP possibili**

| Codice | Significato                             | Descrizione |
|--------|-----------------------------------------|-------------|
| 200    | OK                                      | La convalida è stata aggiornata correttamente. |
| 400    | Richiesta non valida                    | La richiesta è malformata o mancano parametri obbligatori. |
| 401    | Non autorizzato                         | Il token JWT non è valido o mancante. |
| 403    | Vietato                                 | Il token non dispone di ambiti sufficienti. |
| 404    | Non trovato                             | Il workbook, il foglio di calcolo o l'indice di convalida specificati non esistono. |
| 500    | Errore interno del server               | Si è verificato un errore imprevisto sul server. |

Per ulteriori dettagli sulla gestione degli errori, consulta la <a href="https://apireference.aspose.cloud/cells/#/Errors" target="_blank" rel="noopener noreferrer">documentazione sugli errori di Aspose.Cells Cloud</a>.

Potresti voler esplorare anche operazioni correlate, come l'aggiunta di una nuova convalida o l'eliminazione di una esistente:

- [Aggiungere una convalida di un foglio di calcolo](https://docs.aspose.cloud/cells/validations/add/)
- [Eliminare una convalida di un foglio di calcolo](https://docs.aspose.cloud/cells/validations/delete/)

## Famiglia di SDK Cloud

Utilizzare un SDK è il modo più rapido per sviluppare. Un SDK astrae i dettagli di basso livello, consentendoti di concentrarti sulla logica di business. Consulta il <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}
---