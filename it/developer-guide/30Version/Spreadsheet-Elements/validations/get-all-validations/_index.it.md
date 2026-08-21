---
title: "Ottenere tutte le convalidhe del foglio da un foglio Excel"
second_title: "Documenti"
linktype: "it"
type: docs
url: /it/validations/get-all/
keywords: "Aspose.Cells Cloud, Excel, convalidhe dei fogli, API REST, ottenere tutte le convalidhe, SDK"
description: "Recupera tutte le convalidhe dei fogli da un foglio Excel utilizzando l'API REST di Aspose.Cells Cloud. Supporta diversi SDK (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go) per un'integrazione rapida."
weight: 10
---

Le convalidhe dei fogli consentono di definire regole che limitano il tipo o l'intervallo di dati che possono essere inseriti nelle celle. Vengono comunemente utilizzate per garantire l'integrità dei dati, ad esempio limitando gli inserimenti a un elenco di valori, date entro un intervallo specifico o limiti numerici.

Questa API REST recupera tutte le convalidhe presenti su un foglio Excel.

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations
```

### **Parametri della richiesta**

| Nome parametro | Tipo   | Posizione | Descrizione                                   |
| -------------- | ------ | --------- | --------------------------------------------- |
| name           | string | path      | Nome del documento Excel.                     |
| sheetName      | string | path      | Nome del foglio di lavoro.                    |
| folder         | string | query     | Percorso della cartella in cui è memorizzato il documento. |
| storageName    | string | query     | Nome del servizio di archiviazione.           |

**Codici di stato della risposta**

| Codice | Descrizione                              |
|--------|------------------------------------------|
| 200    | Richiesta riuscita – elenco delle convalidhe |
| 401    | Non autorizzato – token non valido o mancante |
| 404    | Non trovato – documento o foglio mancante |
| 500    | Errore interno del server                 |

La [specifica OpenAPI](https://apireference.aspose.cloud/cells/#/WorksheetValidations/GetWorksheetValidations) definisce un'interfaccia di programmazione pubblicamente accessibile e consente di effettuare interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells Cloud. **Prerequisito:** è necessario includere un token JWT valido nell'header `Authorization`.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "validations": [
    {
      "name": "Validation1",
      "type": "WholeNumber",
      "operator": "Between",
      "formula1": "1",
      "formula2": "100",
      "showErrorMessage": true,
      "errorMessage": "Il valore deve essere compreso tra 1 e 100."
    },
    {
      "name": "Validation2",
      "type": "List",
      "formula1": "\"Opzione1,Opzione2,Opzione3\"",
      "showErrorMessage": true,
      "errorMessage": "Selezionare un valore dall'elenco."
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## Famiglia di SDK nel cloud

L'utilizzo di un SDK rappresenta il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli a basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice illustrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetValidations.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetValidations.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetValidations.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetValidations.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetValidations.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetValidations.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetValidations.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetValidations.go" >}}

{{< /tab >}}

{{< /tabs >}}