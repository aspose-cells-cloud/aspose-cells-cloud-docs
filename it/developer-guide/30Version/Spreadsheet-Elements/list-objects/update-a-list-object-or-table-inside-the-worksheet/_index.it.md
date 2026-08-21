---
title: "Aggiorna un oggetto elenco in un foglio di calcolo Excel"
ArticleTitle: "Aggiorna un oggetto elenco in un foglio di calcolo Excel – Documentazione dell'API Aspose.Cells Cloud"
second_title: "Documento"
linktitle: "Aggiorna"
type: docs
url: /list-objects/update/
aliases:
  - /update-a-list-object-or-table-inside-the-worksheet/
  - /tables/update/
keywords: "Aspose.Cells, ListObject, Aggiorna tabella, API Excel, REST, SDK cloud, aggiornamento oggetto elenco, foglio di calcolo Excel, tabella"
description: "Scopri come aggiornare una tabella Excel utilizzando l'API Aspose.Cells Cloud (v3.0). Include endpoint, parametri, esempio cURL, codici di errore ed esempi di SDK."
weight: 20
---

Questa REST API consente di aggiornare le proprietà di un **oggetto elenco** (tabella) in un foglio di calcolo Excel.

## Sicurezza e autenticazione

Le API Aspose.Cells Cloud sono sicure e richiedono l'[autenticazione basata su token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## Schema del corpo della richiesta

Il DTO `listObject` contiene i campi seguenti. Sono richiesti nel corpo della richiesta soltanto i campi che si desidera modificare.

| Campo                                           | Tipo               | Obbligatorio | Descrizione                                                                |
| ----------------------------------------------- | ------------------ | ------------ | -------------------------------------------------------------------------- |
| **DisplayName**                                 | stringa            | opzionale    | Nome visualizzato per la tabella.                                          |
| **StartRow** / **StartColumn**                  | intero             | opzionale    | Indice in base zero della prima riga/colonna della tabella.               |
| **EndRow** / **EndColumn**                      | intero             | opzionale    | Indice in base zero dell'ultima riga/colonna della tabella.               |
| **Range**                                       | stringa            | opzionale    | Indirizzo in stile A1 che definisce l'intervallo della tabella (es. `A1:D10`). |
| **ShowHeaderRow**                               | booleano           | opzionale    | `true` per visualizzare la riga di intestazione.                          |
| **ShowTotals**                                  | booleano           | opzionale    | `true` per visualizzare la riga dei totali.                               |
| **TableStyleName**                              | stringa            | opzionale    | Nome dello stile di tabella predefinito da applicare.                     |
| **TableStyleType**                              | stringa            | opzionale    | Tipo di stile (`TableStyleLight`, `TableStyleMedium`, ecc.).              |
| **ListColumns**                                 | array di oggetti   | opzionale    | Collezione di definizioni di colonne (`Name`, `TotalsCalculation`).       |
| **Sorter**, **AutoFilter**, **ShowTableStyle…** | oggetto            | opzionale    | Opzioni avanzate di formattazione e filtraggio (vedere il DTO completo nella specifica OpenAPI). |

### Payload di esempio minimo

```json
{
  "DisplayName": "SalesData",
  "Range": "A1:E20",
  "ShowHeaderRow": true,
  "ShowTotals": false
}
```

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}
```

### **Parametri della richiesta**

| Nome del parametro  | Tipo    | Posizione | Descrizione                             |
| ------------------- | ------- | --------- | --------------------------------------- |
| **name**            | stringa | path      | Nome del documento.                     |
| **sheetName**       | stringa | path      | Nome del foglio di calcolo.             |
| **listObjectIndex** | intero  | path      | Indice dell'oggetto elenco da aggiornare. |
| **listObject**      | oggetto | body      | DTO `ListObject` nel corpo della richiesta. |
| **folder**          | stringa | query     | Cartella contenente il documento.       |
| **storageName**     | stringa | query     | Nome dello storage.                     |

La [specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObject) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

### Richiesta

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet7/listobjects/0" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
    "DisplayName": "SalesData",
    "Range": "A1:E20",
    "ShowHeaderRow": true,
    "ShowTotals": false,
    "ListColumns": [
      { "Name": "Product", "TotalsCalculation": "None" },
      { "Name": "Quantity", "TotalsCalculation": "Sum" },
      { "Name": "Price", "TotalsCalculation": "Average" }
    ]
  }'
```

{{< /tab >}}

### Risposta

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

La risposta in caso di esito positivo include i campi seguenti:

| Campo                     | Tipo   | Descrizione                                                      |
| ------------------------- | ------ | ---------------------------------------------------------------- |
| **Code**                  | intero | Codice di stato HTTP (200 per successo).                         |
| **Status**                | stringa| Descrizione testuale dello stato.                                |
| **UpdatedObject** *(opzionale)* | oggetto | Rappresentazione dell’`ListObject` aggiornato, contenente i campi modificati. |

{{< /tab >}}

{{< /tabs >}}

## Risposte di errore

| Codice HTTP | Descrizione                                                            | Payload di esempio                                      |
| ----------- | ---------------------------------------------------------------------- | ------------------------------------------------------- |
| **400**     | Richiesta non valida – campi obbligatori mancanti o JSON malformato.  | `{ "Code": 400, "Message": "Invalid request body." }`   |
| **401**     | Non autorizzato – token JWT mancante o non valido.                    | `{ "Code": 401, "Message": "Authentication failed." }`  |
| **404**     | Non trovato – il foglio di calcolo, il foglio o l'oggetto elenco specificati non esistono. | `{ "Code": 404, "Message": "Resource not found." }` |
| **500**     | Errore interno del server – condizione imprevista lato server.        | `{ "Code": 500, "Message": "Server error." }`           |

## Domande frequenti (FAQ)

<details>  
<summary>Come aggiorno un oggetto elenco utilizzando l'API Aspose.Cells Cloud?</summary>

Utilizzare l'endpoint `POST /cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}`. Includere nel corpo JSON le proprietà da modificare (es. `DisplayName`, `ShowHeaderRow`). Eseguire l'autenticazione tramite token JWT nell'intestazione `Authorization`.

</details>

<details>  
<summary>Che risposta ricevo dopo un aggiornamento riuscito?</summary>

Viene restituito un oggetto JSON con `Code: 200` e `Status: "OK"`. In caso di errore, la risposta contiene il codice di stato HTTP appropriato e un oggetto `Error` che descrive il problema.

</details>

<details>  
<summary>Posso aggiornare solo un sottoinsieme delle proprietà dell'oggetto elenco?</summary>

Sì. Includere nel corpo della richiesta soltanto i campi che si desidera modificare; tutti gli altri campi rimangono invariati.

</details>

## Documentazione correlata

- [Aggiungi un oggetto elenco](https://docs.aspose.cloud/cells/list-objects/add/)
- [Ottieni oggetto elenco](https://docs.aspose.cloud/cells/list-objects/get/)
- [Elimina oggetto elenco](https://docs.aspose.cloud/cells/list-objects/delete/)

## Famiglia di SDK cloud

L'utilizzo di un SDK rappresenta il modo più rapido per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObject.go" >}}

{{< /tab >}}

{{< /tabs >}}