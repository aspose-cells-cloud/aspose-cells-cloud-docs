---
title: "Rimuovi collegamenti ipertestuali"
type: docs
url: /it/hyperlinks/clear/
aliases: [/add-hyperlinks-to-excel-worksheet/]
keywords: "Aspose.Cells Cloud, Excel, rimuovi collegamenti ipertestuali, elimina collegamenti ipertestuali, REST API, foglio di lavoro, SDK"
description: "Scopri come rimuovere tutti i collegamenti ipertestuali da un foglio di lavoro Excel utilizzando l'API REST Aspose.Cells Cloud o uno qualsiasi degli SDK supportati (C#, Java, Python, Node.js, Go, PHP, Ruby, Perl, ecc.)."
weight: 40
ArticleTitle: "Rimuovi collegamenti ipertestuali – Documentazione API Aspose.Cells Cloud"
---

Questa API REST elimina **tutti i collegamenti ipertestuali** in un foglio di lavoro Excel.

## Sicurezza e autenticazione
Le API Aspose.Cells Cloud sono sicure e richiedono l'[autenticazione basata su token JWT](https://docs.aspose.cloud/it/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
```

### Parametri della richiesta

| Nome parametro | Tipo   | Posizione | Descrizione                           |
| -------------- | ------ | --------- | ------------------------------------- |
| name           | string | path      | Il nome del file Excel.               |
| sheetName      | string | path      | Il nome del foglio di lavoro.         |
| folder         | string | query     | La cartella che contiene il documento.|
| storageName    | string | query     | Il nome del servizio di archiviazione.|

### Risposte di errore

| Codice HTTP | Motivo                                              | Corpo di esempio                                                     |
| ----------- | --------------------------------------------------- | -------------------------------------------------------------------- |
| **400**     | Richiesta non valida – parametri mancanti o non validi. | `{ "Code":"400", "Message":"Valore di parametro non valido." }`     |
| **401**     | Non autorizzato – token JWT mancante o non valido.  | `{ "Code":"401", "Message":"Token di accesso mancante o non valido." }` |
| **404**     | Non trovato – cartella di lavoro o foglio di lavoro non esistenti. | `{ "Code":"404", "Message":"File non trovato." }`                  |
| **500**     | Errore interno del server – errore imprevisto sul server. | `{ "Code":"500", "Message":"Si è verificato un errore imprevisto." }` |

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Hyperlinks/DeleteWorksheetHyperlinks) definisce un'interfaccia di programmazione pubblicamente accessibile, consentendoti di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando **cURL** per chiamare i servizi web Aspose.Cells. L'esempio seguente mostra come eliminare tutti i collegamenti ipertestuali da un foglio di lavoro.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test1.xlsx/worksheets/Sheet1/hyperlinks" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

## Famiglia di SDK Cloud

L'utilizzo di un SDK accelera lo sviluppo gestendo per te i dettagli a basso livello. Per un elenco completo degli SDK Aspose.Cells Cloud, visita il [repository GitHub](https://github.com/aspose-cells-cloud).

I seguenti esempi di codice mostrano come eliminare i collegamenti ipertestuali dei fogli di lavoro utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetHyperlinks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetHyperlinks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetHyperlinks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetHyperlinks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetHyperlinks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetHyperlinks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetHyperlinks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetHyperlinks.go" >}}

{{< /tab >}}

{{< /tabs >}}