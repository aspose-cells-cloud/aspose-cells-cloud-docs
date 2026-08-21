---
title: "Aggiornare lo stile di più celle – Riferimento API Aspose.Cells Cloud (v3.0)"
type: docs
url: /update-multiple-cells-style/
weight: 20
keywords: ["Aspose.Cells", "aggiornare lo stile di più celle", "API stile celle Excel", "SDK cloud", "API REST", "esempio cURL", "richiesta JSON", "autenticazione JWT"]
description: "Scopri come aggiornare lo stile di un intervallo di celle in un foglio di calcolo Excel utilizzando l'API REST Aspose.Cells Cloud v3.0. Include endpoint, metodo HTTP, parametri, esempi cURL e SDK, autenticazione, gestione degli errori e informazioni sulla versione."
ArticleTitle: "Aggiornare lo stile di più celle – Riferimento API Aspose.Cells Cloud (v3.0)"
---

## API REST

Questa API REST imposta lo **stile** per un intervallo di celle in un foglio di calcolo Excel.

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/style
```

## Sicurezza e autenticazione

Le API Aspose.Cells Cloud sono sicure e richiedono [autenticazione basata su token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).


### Parametri della richiesta

| Nome parametro | Tipo   | Posizione | Descrizione |
|----------------|--------|-----------|-------------|
| **name**       | string | path      | Nome del foglio di calcolo. |
| **sheetName**  | string | path      | Nome del foglio di lavoro. |
| **range**      | string | query     | L'intervallo di celle (ad esempio, `A1:A10`). |
| **style**      | object | body      | Oggetto JSON che definisce lo stile da applicare. |
| **folder**     | string | query     | Cartella contenente il foglio di calcolo. |
| **storageName**| string | query     | Nome dell'archiviazione. |

#### Oggetto style
L'oggetto JSON `style` rappresenta la formattazione delle celle. Può contenere una qualsiasi delle seguenti proprietà opzionali:

- **Font** – Impostazioni del font (`Name`, `Size`, `IsBold`, `IsItalic`, `Color`, ecc.).  
- **BackgroundColor** – Colore di sfondo in formato ARGB.  
- **ForegroundColor** – Colore di primo piano in formato ARGB.  
- **Name**, **CultureCustom**, **Custom** – Metadati aggiuntivi dello stile.

## **Risposta**

Restituisce un oggetto CellCloudResponse.

- **Panoramica dei campi della risposta**

| Campo             | Tipo    | Descrizione                                           |
| ----------------- | ------- | ----------------------------------------------------- |
| `Status`          | string  | Stato della risposta                                  |
| `Code`            | integer | Codici di stato HTTP: 200, 400, 401, 500, ...         |


```json
{
  "Status":"OK",
  "Code":200
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante. |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server   | Errore imprevisto nel server. |

## Come utilizzare l'API PostUpdateWorksheetRangeStyle con gli SDK

### Specifica dell'API PostUpdateWorksheetRangeStyle

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostUpdateWorksheetRangeStyle) fornisce lo schema completo.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
cURL -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/style?range=a1%3Aa10" \
  -X POST \
  -d '{
        "Font": {
          "Color": { "A":255, "R":255, "G":255, "B":0 },
          "Size": 22,
          "IsBold": true,
          "IsItalic": true,
          "IsStrikeout": true,
          "IsSubscript": true,
          "IsSuperscript": true,
          "Name": "Arial"
        },
        "Name": "string",
        "CultureCustom": "string",
        "Custom": "string",
        "BackgroundColor": { "A":10, "R":10, "G":10, "B":10 },
        "ForegroundColor": { "A":255, "R":255, "G":255, "B":0 }
      }' \
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


### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeStyle.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeStyle.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeStyle.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeStyle.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeStyle.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeStyle.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeStyle.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeStyle.go" >}}

{{< /tab >}}

{{< /tabs >}}