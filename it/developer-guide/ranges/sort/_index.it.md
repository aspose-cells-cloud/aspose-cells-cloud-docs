---
title:  Ordinamento intervallo
second_title: Aspose.Cells Cloud Documen
linktitle: Sor
type: docs
keywords: Range Sort
url: /it/ranges/sort/
description:  Imposta il bordo del contorno attorno a un intervallo di celle.
weight: 20
---
Questo REST API indica l'ordinamento dell'intervallo.

## RSETAPI


```bash

POST http://api.aspose.cloud/v3.0//cells/{name}/worksheets/{sheetName}/ranges/sort

```

 I parametri della richiesta sono:

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
|nome|Corda|Sentiero|Il nome della cartella di lavoro.|
|nomefoglio|Corda|Sentiero|Il nome del foglio di lavoro.|
|rangeOperate|Classe|Corpo| Richiesta di ordinamento dell'intervallo|
|cartella|Corda|Domanda|Cartella della cartella di lavoro originale.|
|storageName|Corda|Domanda|Nome dell'archivio.|



 IL[Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/RangesController/PostWorksheetCellsRangeSort) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi Web Aspose.Cells. Nell'esempio seguente viene illustrato come effettuare chiamate al Cloud API con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}
```powershell
curl -v "http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/sort" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
```
{{< /tab >}}
{{< tab tabNum="2" >}}
```powershell

```
{{< /tab >}}

{{< /tabs >}}

## Famiglia di SDK Cloud

Utilizzare un SDK è il modo migliore per accelerare lo sviluppo. Un SDK si prende cura dei dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Controlla il repository GitHub per un elenco completo degli SDK Cloud Aspose.Cells.

I seguenti esempi di codice dimostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

