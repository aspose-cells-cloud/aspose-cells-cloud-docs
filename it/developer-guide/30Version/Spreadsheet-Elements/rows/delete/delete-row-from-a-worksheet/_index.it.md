---
title: "Eliminare una riga in un foglio di lavoro Excel"
second_title: "Documento"
linktitle: "Riga"
type: docs
url: /rows/delete/row/
aliases: [/delete-row-from-a-worksheet/]
description: "Usa l'endpoint DELETE /worksheets/{sheetName}/cells/rows/{rowIndex} per rimuovere una riga specifica da un foglio di lavoro Excel tramite l'API REST Aspose.Cells Cloud. Include comandi cURL, esempi di SDK e riferimento completo ai parametri."
keywords: "Aspose.Cells, elimina riga, Excel, API, REST, Cloud, SDK"
weight: 80
ArticleTitle: "Eliminare una riga in un foglio di lavoro Excel – Guida all'API Aspose.Cells Cloud"
---

Questa REST API elimina una riga da un foglio di lavoro Excel.

**Prerequisiti**  
- Un token JWT valido per l'**autorizzazione**.  
- Il workbook deve essere memorizzato in uno storage supportato da Aspose Cloud (predefinito o personalizzato).  
- La cartella di destinazione (se specificata) deve esistere nello storage scelto.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **Parametri della richiesta**

| Nome parametro      | Tipo    | Path / Query | Obbligatorio | Descrizione                                                                                         |
| ------------------- | ------- | ------------ | ------------ | --------------------------------------------------------------------------------------------------- |
| **name**            | string  | path         | Sì           | Nome del workbook.                                                                                  |
| **sheetName**       | string  | path         | Sì           | Nome del foglio di lavoro.                                                                          |
| **rowIndex**        | integer | path         | Sì           | Indice in base zero della riga da eliminare.                                                       |
| **startrow**        | integer | query        | No           | Indice della prima riga da eliminare (normalmente uguale a `rowIndex`).                            |
| **totalRows**       | integer | query        | No           | Numero di righe consecutive da eliminare.                                                          |
| **updateReference** | boolean | query        | No           | Se `true` (valore predefinito), le formule, gli intervalli con nome e altri riferimenti vengono aggiornati dopo l'eliminazione. |
| **folder**          | string  | query        | No           | Cartella contenente il workbook.                                                                    |
| **storageName**     | string  | query        | No           | Nome del servizio di storage.                                                                       |

La [specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetRow) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra una chiamata completa ed eseguibile.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=1&updateReference=true" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

**Codici di risposta HTTP possibili**

| Codice | Significato                          | Descrizione                                                                 |
|--------|--------------------------------------|-----------------------------------------------------------------------------|
| 200    | OK                                   | La riga è stata eliminata correttamente.                                    |
| 400    | Richiesta non valida (Bad Request)  | Parametri mancanti o non validi (ad esempio, `rowIndex` non numerico).     |
| 401    | Non autorizzato (Unauthorized)       | Token JWT non valido o mancante.                                            |
| 404    | Non trovato (Not Found)             | Il workbook, il foglio di lavoro o la riga specificati non esistono.       |
| 500    | Errore interno del server (Internal Server Error) | Errore imprevisto del server; consultare la risposta di errore per i dettagli. |

**Esempio di risposta di errore**

```json
{
  "Code": 400,
  "Message": "Indice riga non valido fornito."
}
```

## Famiglia di SDK per il Cloud

Utilizzare un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK astrae i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=1&updateReference=true" \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

**Operazioni correlate**  
- [Aggiungere una riga](/cells/rows/add/row/)  
- [Eliminare più righe](/cells/rows/delete/rows/)  
- [Ottenere i dettagli di una riga](/cells/rows/get/row/)  
---