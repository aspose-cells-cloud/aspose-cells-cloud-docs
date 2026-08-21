---
title: "Adattamento automatico delle righe in un workbook Excel"
second_title: "Documento"
linktitle: "Righe"
type: docs
url: /it/autofit-rows-on-an-excel-file/
aliases: [  /it/auto-fit-rows-in-excel-workbooks/ , /it/workbook/autofit/rows/ ]
keywords: "adattamento automatico righe, workbook Excel, Aspose.Cells Cloud, REST API, opzioni di adattamento automatico"
description: "Scopri come regolare automaticamente l’altezza delle righe in un workbook Excel utilizzando l’API REST di Aspose.Cells Cloud. Include endpoint, parametri, esempio cURL e frammenti di codice SDK per C#, Java, Python e altro."
weight: 90
ArticleTitle: "Adattamento automatico delle righe in un workbook Excel – Aspose.Cells Cloud API"
---

**Prerequisiti**  
Prima di chiamare l’API, ottieni un token Bearer JWT valido dal servizio di autenticazione Aspose e assicurati che il workbook di destinazione sia memorizzato in una posizione di archiviazione supportata (archiviazione predefinita o una personalizzata da te configurata).

Questa API REST ti consente di **adattare automaticamente le righe** in un workbook Excel, regolando automaticamente l’altezza delle righe dopo l’inserimento o la modifica dei dati.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/autofitrows
```

I parametri della richiesta sono i seguenti:

| Nome Parametro    | Tipo              | Posizione | Descrizione                                                                 |
| ----------------- | ----------------- | -------- | --------------------------------------------------------------------------- |
| name              | string            | path     | Nome del file del workbook.                                                 |
| autoFitterOptions | AutoFitterOptions | body     | Opzioni che controllano il comportamento dell’adattamento automatico.      |
| startRow          | integer           | query    | Indice della prima riga da adattare automaticamente.                        |
| endRow            | integer           | query    | Indice dell’ultima riga da adattare automaticamente.                        |
| firstColumn       | integer           | query    | Indice della prima colonna considerata per l’adattamento automatico.       |
| lastColumn        | integer           | query    | Indice dell’ultima colonna considerata per l’adattamento automatico.       |
| onlyAuto          | boolean           | query    | Se **true**, vengono elaborate solo le righe con il flag AutoFit (default **false**). |
| folder            | string            | query    | Percorso della cartella in cui è memorizzato il workbook.                  |
| storageName       | string            | query    | Nome del servizio di archiviazione.                                         |

**AutoFitterOptions** è un oggetto che specifica come si comporta l’operazione di adattamento automatico (ad esempio, `AutoFitMergedCells`, `IgnoreHidden`).

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                                   |
|--------|-----------------------------|---------------------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell’operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante.                              |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione.             |
| 500    | Errore interno del server   | Errore imprevisto sul server.                                 |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostAutofitWorkbookRows) definiscono un’interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per chiamare i servizi web Aspose.Cells. Sostituisci `<jwt token>` con un token Bearer JWT valido ottenuto dal servizio di autenticazione Aspose.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/autofitrows" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells":true, "IgnoreHidden":true}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*Esempio di risposta di errore (ad esempio, workbook mancante):*

```json
{
  "Code": 404,
  "Status": "Not Found",
  "Message": "Il workbook specificato 'myWorkbook.xlsx' non esiste."
}
```

{{< /tab >}}

{{< /tabs >}}

**Note**  
- Quando `AutoFitMergedCells` è impostato su **true**, le celle unite vengono considerate come un’unica entità durante l’operazione di adattamento automatico.  
- Impostando `IgnoreHidden` su **true**, vengono ignorate righe e colonne nascoste, preservandone le dimensioni attuali.

## Famiglia di SDK Cloud

L’utilizzo di un SDK rappresenta il metodo più rapido per lo sviluppo. Un SDK nasconde i dettagli a basso livello, consentendoti di concentrarti sul tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorkbookRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorkbookRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorkbookRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorkbookRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorkbookRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorkbookRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorkbookRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorkbookRows.go" >}}

{{< /tab >}}

{{< /tabs >}}