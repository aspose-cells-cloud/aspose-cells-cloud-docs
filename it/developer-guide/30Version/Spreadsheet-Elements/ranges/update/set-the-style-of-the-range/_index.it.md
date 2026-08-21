---
title: "Imposta lo stile di un intervallo – Aspose.Cells Cloud API"
second_title: "Documentazione"
linktitle: "Imposta lo stile di un intervallo"
type: docs
url: /ranges/update/style/
aliases: [/set-the-style-of-the-range/]
keywords: "Aspose.Cells, stile intervallo, API, Excel, cloud"
description: "Scopri come impostare lo stile di un intervallo di celle in un foglio di calcolo Excel utilizzando l'API REST di Aspose.Cells Cloud. Include i passaggi per l'autenticazione, il formato della richiesta, i dettagli della risposta e esempi di SDK per .NET, Java, Python, Go e altro."
weight: 70
---  

## **Introduzione**  
Questo esempio mostra come impostare lo stile di un intervallo utilizzando l'API Aspose.Cells Cloud. È possibile chiamare l'API da molti linguaggi di programmazione, tra cui .NET, Java, PHP, Ruby, Python, JavaScript (jQuery) e altri.  

## **Informazioni sull'API**  

| API                                                   | Tipo | Descrizione                              | Link alla risorsa                                                                                                                             |
| ----------------------------------------------------- | ---- | ---------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| /cells/{name}/worksheets/{sheetName}/ranges/style     | POST | Imposta lo stile delle celle di un intervallo denominato | [PostWorksheetCellsRangeStyle](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeStyle) |

### **Esempio cURL**  

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

**Prerequisiti**  
1. Ottieni un token di accesso tramite il flusso client‑credentials di OAuth2 (`POST https://api.aspose.cloud/connect/token`).  
2. Includi l'intestazione `Authorization: Bearer <access_token>` in ogni richiesta.  

**Richiesta**  

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/style" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{
           "Range": {
               "FirstRow": 1,
               "FirstColumn": 1,
               "RowCount": 2,
               "ColumnCount": 2,
               "Worksheet": "Sheet1"
           },
           "Style": {
               "Font": {
                   "IsBold": true,
                   "IsItalic": true,
                   "IsStrikeout": true,
                   "IsSubscript": true,
                   "IsSuperscript": true,
                   "DoubleSize": 1
               }
           }
         }'
```

*L'oggetto `Range` specifica la cella in alto a sinistra e le dimensioni dell'intervallo. L'oggetto `Style` contiene le opzioni di formattazione da applicare.*  

{{< /tab >}}

{{< tab tabNum="2" >}}

**Risposta**  

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Gestione degli errori** – In caso di chiamate non riuscite, l'API restituisce un codice di stato HTTP appropriato (ad esempio, 400, 401, 500) insieme a un corpo JSON contenente i campi `Error` e `Message`. Esamina il valore di `Code`; qualsiasi risultato diverso da 200 deve essere registrato e gestito in base alla tua politica di gestione degli errori.  

{{< /tab >}}

{{< /tabs >}}

## **Codice sorgente dell'SDK**  
Gli SDK di Aspose.Cells Cloud possono essere scaricati dalla seguente pagina: [SDK disponibili](/cells/available-sdks/)

### **Esempi di SDK**  
{{< tabs tabTotal="4" tabID="4" tabName1="PHP" tabName2="Ruby" tabName3="Objective C" tabName4="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "81d7e60eaf43ae7192df00993997afde" >}}

{{< /tab >}}

{{< /tabs >}}