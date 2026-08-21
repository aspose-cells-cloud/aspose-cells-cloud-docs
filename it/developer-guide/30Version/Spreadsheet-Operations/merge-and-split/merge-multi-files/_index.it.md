---
title: "Unire più file Excel in un unico libro di lavoro"
second_title: "Documento"
linktype: "Unire più file Excel"
type: docs
url: /merge-multi-files-into-excel/
aliases: [/merge/multi-files/]
keywords: "Aspose.Cells Cloud, unire più file Excel, API REST, unione fogli di calcolo, SDK cloud"
description: "Scopri come unire più libri di lavoro Excel in un singolo file utilizzando l'API REST Aspose.Cells Cloud (v3.0). Include endpoint HTTPS, comando cURL, esempi di SDK, parametri obbligatori e dettagli sulla gestione degli errori."
weight: 32
---

## API REST

Questa API REST unisce più file Excel in un unico libro di lavoro Excel.

```bash
POST https://api.aspose.cloud/v3.0/cells/merge
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.


### Parametri della richiesta

| Nome parametro  | Tipo    | Posizione | Descrizione                                                                                    | Obbligatorio |
| ---------------- | ------- | --------- | ---------------------------------------------------------------------------------------------- | ------------ |
| files[]          | file    | formData  | Uno o più libri di lavoro Excel da unire. Utilizzare `file1`, `file2`, … nella richiesta.     | Sì           |
| format           | string  | query     | Formato di output desiderato (es. `xlsx`).                                                     | Sì           |
| mergeToOneSheet  | boolean | query     | Impostare su `true` per combinare tutti i fogli in un singolo foglio; il valore predefinito è `false`. | No           |

### **Risposta**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[nome file unito]",
    "Filesize" : [dimensione file],
    "FileContent" : "[Base64String]"
}
```

**Codici di stato HTTP**

| Codice | Significato                  | Descrizione                                             |
|--------|------------------------------|---------------------------------------------------------|
| 200    | OK                           | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida         | Parametri mancanti o non validi (es. tipo di file non supportato). |
| 401    | Non autorizzato              | Token JWT non valido o mancante. |
| 413    | Payload troppo grande        | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server    | Errore imprevisto del server. |
## Come utilizzare l'API PostMerge con gli SDK

### Specifica dell'API PostMerge

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostMerge) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare direttamente interazioni REST da un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/merge?format=xlsx" \
  -X POST \
  -H "Authorization: Bearer <jwt token>" \
  -F "file1=@file1.xlsx" \
  -F "file2=@file2.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  {
    "Filename": "file1.xlsx",
    "FileSize": 274022,
    "FileContent": "-----Base64String--------"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK Aspose.Cells Cloud

L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Merge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-Merge.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LightCells-Merge.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "LightCellsMerge.py" >}}
{{< /tab >}}

{{< /tabs >}}

---