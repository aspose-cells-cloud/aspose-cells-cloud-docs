---
title: "Aggiungi una tabella pivot in un foglio di lavoro Excel"
second_title: "Documento"
linktitle: Aggiungi
type: docs
url: /it/pivot-tables/add/
aliases: [  /it/add-a-pivot-table-in-a-worksheet/ ]
keywords: "Aggiungi tabella pivot, foglio di lavoro Excel, Aspose.Cells Cloud, REST API, SDK, tabella pivot Excel"
description: "Utilizza l'API REST di Aspose.Cells Cloud per aggiungere una tabella pivot a un foglio di lavoro Excel. Disponibile tramite SDK per C#, Java, PHP, Python, Node.js, Android, Swift, Perl, Go."
weight: 30
ArticleTitle: "Come aggiungere una tabella pivot in un foglio di lavoro Excel usando Aspose.Cells Cloud"
---

Questa API REST aggiunge una tabella pivot in un foglio di lavoro.

**Prerequisiti:**  
- Un account Aspose.Cells Cloud con un token di accesso JWT valido.  
- Il libro di lavoro di destinazione deve essere memorizzato in una posizione di archiviazione supportata (archiviazione predefinita o archiviazione specificata dall'utente).  
- Il foglio di lavoro specificato da `sheetName` deve esistere nel libro di lavoro.  

## API PutWorksheetPivotTable

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### **Parametri della richiesta**

| Nome parametro | Tipo    | Posizione | Descrizione                                                                                                                         |
| -------------- | ------- | --------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| name           | string  | path      | Il nome del documento Excel.                                                                                                     |
| sheetName      | string  | path      | Il nome del foglio di lavoro in cui verrà creata la tabella pivot.                                                                    |
| request        | object  | body      | DTO `CreatePivotTableRequest` contenente la definizione della tabella pivot.                                                                |
| folder         | string  | query     | La cartella contenente il documento.                                                                                              |
| storageName    | string  | query     | Il nome dell'archivio in cui è situato il documento.                                                                              |
| sourceData     | string  | query     | L'intervallo che fornisce i dati di origine per la nuova cache della tabella pivot (ad esempio, `A5:E10`).                                             |
| destCellName   | string  | query     | L'indirizzo della cella in alto a sinistra dell'intervallo di destinazione per il report della tabella pivot.                                             |
| tableName      | string  | query     | Il nome assegnato alla nuova tabella pivot.                                                                                           |
| useSameSource  | boolean | query     | Se `true`, la nuova tabella pivot riutilizza una fonte di dati esistente, risparmiando memoria se un’altra tabella pivot ha già utilizzato questa fonte. |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/PutWorksheetPivotTable) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando **cURL** per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come chiamare l'API Cloud con cURL.

**Nota sulla sicurezza:** Utilizza sempre `https://` quando chiami l'API e mantieni il tuo token JWT confidenziale; trasmetterlo tramite HTTP non crittografato può esporlo al rischio di intercettazione.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/pivottables" \
-X PUT \
-d '{"Name":"MyPivot","SourceData":"A5:E10","DestCellName":"H20","UseSameSource":true,"PivotFieldRows":[1],"PivotFieldColumns":[1],"PivotFieldData":[1]}' \
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

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante. |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server   | Errore imprevisto del server. |

## Famiglia di SDK Cloud

L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-AddPivottableWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-AddPivottableWorksheet-add-pivot-table-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddPivotTableInw" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-AddPivottableWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-AddPivottableWorksheet-add-pivot-table-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-AddPivottableWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "980246b631d7816f257f2ad4664788ea" >}}

{{< /tab >}}

{{< /tabs >}}

Per altre operazioni, consulta le pagine API correlate: **[Ottenere una tabella pivot](https://docs.aspose.cloud/cells/it/pivot-tables/get/)**, **[Eliminare una tabella pivot](https://docs.aspose.cloud/cells/it/pivot-tables/delete/)** e **[Aggiornare una tabella pivot](https://docs.aspose.cloud/cells/it/pivot-tables/update/)**.