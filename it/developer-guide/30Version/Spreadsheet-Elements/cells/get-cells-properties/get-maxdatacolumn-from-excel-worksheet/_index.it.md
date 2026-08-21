---
title: "Aspose.Cells Cloud API – Ottieni MaxDataColumn di un foglio Excel (v3.0)"
type: docs
url: /get-maxdatacolumn-from-excel-worksheet/
weight: 70
keywords: "Aspose.Cells Cloud, Ottieni MaxDataColumn, foglio Excel, REST API, v3.0, SDK"
description: "Recupera l’indice della colonna più alta contenente dati in un foglio specificato utilizzando l’API REST di Aspose.Cells Cloud (v3.0). Include i dettagli della richiesta, una risposta di esempio ed esempi con SDK."
ArticleTitle: "Aspose.Cells Cloud API – Ottieni MaxDataColumn di un foglio Excel (v3.0)"
---

Questa API REST restituisce l’indice massimo della colonna di dati in un foglio Excel quando il parametro `cellOrMethodName` è impostato su `maxdatacolumn`.

## **Esempio cURL**

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/maxdatacolumn" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MaxDataColumn": 12
}
```

{{< /tab >}}

{{< /tabs >}}

**Dettagli della richiesta**  
- **Metodo HTTP:** `GET`  
- **Modello di endpoint:** `https://api.aspose.com/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/maxdatacolumn`  
- **Parametri di percorso:**  
  - `fileName` – Nome del file Excel (ad esempio, `myWorkbook.xlsx`).  
  - `sheetName` – Nome del foglio di calcolo (ad esempio, `Sheet1`).  
- **Intestazioni:**  
  - `Authorization: Bearer <access_token>` (obbligatorio)  
  - `Accept: application/json` (consigliato)  

**Parametri**

| Parametro | Posizione | Tipo   | Obbligatorio | Descrizione |
|-----------|-----------|--------|--------------|-------------|
| `fileName` | Path      | string | Sì           | Nome del file Excel memorizzato nell’archivio cloud. |
| `sheetName` | Path    | string | Sì           | Foglio di calcolo dal quale ottenere la colonna di dati massima. |
| `cellOrMethodName` | Path | string | Sì | Deve essere impostato su `maxdatacolumn` per richiamare questa operazione. |

**Risposte**

| Codice di stato | Descrizione                                    | Payload di esempio |
|-----------------|------------------------------------------------|--------------------|
| 200             | Esito positivo – restituisce l’indice della colonna di dati massima. | `{ "MaxDataColumn": 12 }` |
| 401             | Non autorizzato – token di accesso non valido o mancante. | `{ "error": "Invalid authentication." }` |
| 404             | Non trovato – il file o il foglio di calcolo non esistono. | `{ "error": "Resource not found." }` |
| 500             | Errore interno del server – condizione imprevista. | `{ "error": "Server error." }` |

**Gestione degli errori**  
In caso di fallimento della richiesta, controlla il codice di stato HTTP e il messaggio `error` nel corpo della risposta. Assicurati che il token di accesso sia valido e che il file e il foglio specificati esistano nel tuo archivio Aspose Cloud.

- **Utilizza gli SDK di Aspose.Cells Cloud**

L’utilizzo di un SDK è il modo più efficiente per accelerare lo sviluppo. Un SDK gestisce i dettagli a basso livello, consentendoti di concentrarti sulle attività del tuo progetto.Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells mediante vari SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMaxDataColumnWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMaxDataColumnWorksheet-get-max-data-column.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMaxDataColumn.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_max_data_column.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMaxDataColumnFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMaxDataColumnWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMaxDataColumnWorksheet-get-max-data-column.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMaxDataColumnWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "126f68818f671a2f6087ee334726c454" >}}

{{< /tab >}}

{{< /tabs >}}