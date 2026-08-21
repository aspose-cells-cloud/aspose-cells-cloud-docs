---
title: "Aggiornamento dello stile della cella per una tabella pivot"
second_title: "Document"
linktype: "Format"
type: docs
url: /it/pivot-tables/format/
aliases: [  /it/update-cell-style-for-pivot-table/ ]
keywords: "Aspose.Cells Cloud, stile tabella pivot, API per l’aggiornamento dello stile della cella, API REST, API Excel, formattazione foglio di calcolo, SDK cloud, stile cella, tabella pivot"
description: "Scopri come aggiornare lo stile di una cella specifica in una tabella pivot di Aspose.Cells Cloud tramite l’API REST. Include endpoint, parametri, autenticazione, esempio cURL, frammento di codice Go SDK e indicazioni ottimizzate per il SEO."
weight: 90
ArticleTitle: "Aggiornamento dello stile della cella per una tabella pivot - Documentazione API Aspose.Cells Cloud"
---

Questa API REST aggiorna lo **stile** di una cella in una tabella pivot.

**Prerequisiti / Autenticazione**  
Per chiamare questo endpoint è necessario disporre di un token di accesso JWT Aspose Cloud valido. Ottenilo tramite il flusso OAuth 2.0 descritto nella [Guida all’autenticazione](/it/authentication/). Includi il token nell’header della richiesta:

```http
Authorization: Bearer <token jwt>
```

Il token JWT è obbligatorio per tutte le chiamate alle API Aspose.Cells Cloud.

## API PostPivotTableCellStyle

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/Format
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l’autenticazione tramite token JWT</a>.

### **Parametri della richiesta**

| Nome parametro  | Tipo    | Posizione | Descrizione                                                                                             |
| --------------- | ------- | --------- | ------------------------------------------------------------------------------------------------------- |
| name            | string  | path      | Nome del documento (obbligatorio).                                                                      |
| sheetName       | string  | path      | Nome del foglio di lavoro (obbligatorio).                                                               |
| pivotTableIndex | integer | path      | Indice della tabella pivot (obbligatorio).                                                              |
| column          | integer | query     | Indice della colonna (in base zero) della cella da formattare (obbligatorio).                           |
| row             | integer | query     | Indice della riga (in base zero) della cella da formattare (obbligatorio).                              |
| style           | object  | body      | DTO dello stile (oggetto di trasferimento dati) che definisce il nuovo stile della cella.               |
| needReCalculate | boolean | query     | Indica se la tabella pivot debba essere ricalcolata dopo la formattazione. Il valore predefinito è **false**. |
| folder          | string  | query     | Cartella in cui è memorizzato il documento (opzionale).                                                  |
| storageName     | string  | query     | Nome dell’archiviazione (opzionale).                                                                     |
| Method          | string  | N/A       | Metodo HTTP utilizzato per la richiesta (**POST**).                                                      |

La <a href="https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableCellStyle" target="_blank" rel="noopener noreferrer">Specifica OpenAPI</a> definisce un’interfaccia di programmazione accessibile pubblicamente e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando **cURL** per accedere facilmente ai servizi web Aspose.Cells. L’esempio seguente mostra come effettuare una chiamata all’API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/Format?column=1&row=1" \
  -X POST \
  -d '{"Font":{"Name":"Arial","Size":10}}' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <token jwt>"
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

**Risposta**  
In caso di esito positivo, il servizio restituisce HTTP 200 con un corpo vuoto, indicando che lo stile è stato applicato. In caso di errore, viene restituito un payload JSON contenente un codice di errore e un messaggio.

| Stato HTTP | Descrizione                                                           |
|-----------|-----------------------------------------------------------------------|
| 200       | Stile applicato con successo.                                         |
| 400       | Richiesta non valida – ad esempio, indice di colonna/riga non valido. |
| 401       | Non autorizzato – token JWT mancante o non valido.                    |
| 404       | Non trovato – il documento, il foglio di lavoro o la tabella pivot specificati non esistono. |
| 500       | Errore interno del server – condizione imprevista.                    |

Il corpo della risposta è vuoto in caso di esito positivo.

Per ulteriori informazioni, consulta la documentazione dell’API **Get Pivot Table**.

## Famiglia di SDK cloud

L’utilizzo di un SDK rappresenta il metodo più rapido per lo sviluppo. Un SDK astrae i dettagli di basso livello, consentendoti di concentrarti sulla logica di business. Consulta il <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK Aspose.Cells Cloud.

Il codice seguente illustra come chiamare i servizi web Aspose.Cells utilizzando l’SDK **Go**:

{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "3236805d26482f06f4656b14f2d00d79" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Aggiornamento dello stile della cella per una tabella pivot",
  "description": "Guida all’aggiornamento dello stile di una cella specifica in una tabella pivot di Aspose.Cells Cloud tramite l’API REST.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2026-07-30",
  "keywords": "Aspose.Cells Cloud, tabella pivot, stile cella, API REST, Go SDK",
  "url": "https://docs.aspose.cloud/it/cells/pivot-tables/format/",
  "publisher": {
    "@type": "Organization",
    "name": "Aspose"
  }
}
</script>
---