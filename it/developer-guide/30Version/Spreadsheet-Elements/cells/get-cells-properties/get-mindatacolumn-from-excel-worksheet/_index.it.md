---
title: "Ottieni MinDataColumn – Riferimento API Aspose.Cells Cloud (v3.0)"
type: docs
url: /it/get-mindatacolumn-from-excel-worksheet/
weight: 110
keywords: "Aspose.Cells Cloud, MinDataColumn, foglio Excel, API REST, riferimento API, v3.0, colonna dati, API cloud"
description: "Recupera la colonna più a sinistra contenente dati in un foglio Excel tramite l'API REST Aspose.Cells Cloud (v3.0). Include dettagli sull'autenticazione, sintassi della richiesta, esempio di risposta JSON, codici di errore e frammenti SDK."
ArticleTitle: "Ottieni MinDataColumn – Riferimento API Aspose.Cells Cloud (v3.0)"
---

L'endpoint **`mindatacolumn`** restituisce l'indice in base zero della colonna più a sinistra contenente almeno una cella con dati in un foglio specificato.  
In altre parole, indica quale colonna è la prima a contenere effettivamente dati.

> **Definizione** – `mindatacolumn`: l'indice (a partire da 0) della prima colonna contenente dati nel foglio.

**Prerequisiti**  
- È richiesto un token di accesso OAuth2 valido.  
- Il file Excel deve essere caricato nello storage di Aspose Cloud.

**Parametri della richiesta**

| Parametro      | Tipo   | Obbligatorio | Descrizione                                 |
|----------------|--------|--------------|---------------------------------------------|
| `fileName`     | string | Sì           | Nome del file Excel memorizzato nello storage cloud. |
| `sheetName`    | string | Sì           | Nome del foglio dal quale recuperare l'indice della colonna. |
| `Authorization` (intestazione) | string | Sì | Token Bearer per l'autenticazione OAuth2. |

- **Esempio con cURL**

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/mindatacolumn" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/mindatacolumn" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MinDataColumn": 2
}
```

{{< /tab >}}

{{< /tabs >}}

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante. |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server   | Errore imprevisto del server. |
---

- Utilizzare gli SDK di Aspose.Cells Cloud

L'uso di un SDK rappresenta il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulla logica del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per l'elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinDataColumnWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinDataColumnWorksheet-get-min-data-column.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinDataColumn.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_data_column.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinDataColumnFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinDataColumnWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinDataColumnWorksheet-get-min-data-column.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinDataColumnWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "48105eac1e6a64ad3ae4f269c32f3a88" >}}

{{< /tab >}}

{{< /tabs >}}
---