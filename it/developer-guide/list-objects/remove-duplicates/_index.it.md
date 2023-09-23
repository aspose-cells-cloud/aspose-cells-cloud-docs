---
title:  L'oggetto elenco rimuove i duplicati
description:  Rimuovi i duplicati sull'oggetto dell'elenco.
url: /it/list-objects/remove-duplicates/
weight: 20
---
 Questo REST API indica la rimozione dei duplicati sull'oggetto dell'elenco.

## RSETAPI


```bash

POST http://api.aspose.cloud/v3.0//cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates

```

 I parametri della richiesta sono:

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
|nome|Corda|Sentiero||
|nomefoglio|Corda|Sentiero||
|elencoOggettoIndice|Numero intero|Sentiero||
|cartella|Corda|Domanda||
|storageName|Corda|Domanda||



 IL[Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/ListObjectsController/PostWorksheetListObjectRemoveDuplicates) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi Web Aspose.Cells. Nell'esempio seguente viene illustrato come effettuare chiamate al Cloud API con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}
```powershell
curl -v "http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates" \
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
