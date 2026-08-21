---
title: "Imposta l'area di pagina per un foglio di calcolo"
second_title: "Document"
linktype: "Imposta l'area di pagina"
type: docs
url: /it/set-page-setup/
keywords: "Aspose.Cells, Excel, area di pagina, REST API, foglio di calcolo, SDK cloud"
description: "Scopri come impostare l'area di pagina per un foglio di calcolo Excel utilizzando l'API REST di Aspose.Cells Cloud. Include i dettagli della richiesta, un esempio cURL sicuro in HTTPS, i codici di stato della risposta e frammenti di codice SDK per numerosi linguaggi di programmazione."
weight: 20
ArticleTitle: "Imposta l'area di pagina per un foglio di calcolo – Guida API Aspose.Cells Cloud"
---

Prerequisiti: Per chiamare questa API è necessario disporre di un token JWT (OAuth) valido e del foglio di calcolo deve trovarsi in una posizione di archiviazione Aspose Cloud in cui si dispone di autorizzazioni di lettura/scrittura. Assicurarsi che il token sia incluso nell'intestazione **Authorization** e che l'account disponga della quota API necessaria.

Questa REST API imposta l'area di pagina per un foglio di calcolo Excel.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pagesetup
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### **Parametri della richiesta**

| Nome parametro | Tipo   | Posizione | Descrizione                    |
| -------------- | ------ | -------- | ------------------------------ |
| name           | string | path     | Nome del documento.            |
| sheetName      | string | path     | Nome del foglio di calcolo.    |
| pageSetup      | object | body     | Descrizione dell'area di pagina. |
| folder         | string | query    | Cartella del documento.        |
| storageName    | string | query    | Nome dell'archiviazione.       |

**Esempio di payload JSON per l'oggetto `pageSetup`**

```json
{
  "pageSetup": {
    "orientation": "Portrait",
    "paperSize": "A4",
    "fitToPagesTall": 1,
    "fitToPagesWide": 1,
    "centerHorizontally": true,
    "centerVertically": false
  }
}
```

La <a href="https://reference.aspose.cloud/cells/#/PageSetup/PostPageSetup" target="_blank" rel="noopener noreferrer">Specifiche OpenAPI</a> definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare direttamente interazioni REST da un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Tasks/pagesetup" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{
  "pageSetup": {
    "orientation": "Portrait",
    "paperSize": "A4",
    "fitToPagesTall": 1,
    "fitToPagesWide": 1,
    "centerHorizontally": true,
    "centerVertically": false
  }
}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

L'API restituisce un oggetto JSON che indica il risultato dell'operazione:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Possibili codici di stato della risposta**

| Codice | Significato                 | Quando                                                       |
|--------|-----------------------------|--------------------------------------------------------------|
| 200    | OK                          | Aggiornamento dell'area di pagina riuscito                   |
| 400    | Richiesta non valida        | Payload JSON non valido o campi obbligatori mancanti         |
| 401    | Non autorizzato             | Token JWT mancante o non valido                               |
| 404    | Non trovato                 | Il nome del foglio di calcolo o del foglio non esiste         |
| 500    | Errore interno del server   |Errore imprevisto nel server                                  |

## Famiglia di SDK Cloud

L'utilizzo di un SDK rappresenta il modo più efficace per velocizzare lo sviluppo. Un SDK gestisce i dettagli a basso livello e consente di concentrarsi sui compiti del proprio progetto. Consultare il <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostPageSetup.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostPageSetup.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostPageSetup.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostPageSetup.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostPageSetup.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostPageSetup.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostPageSetup.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostPageSetup.go" >}}

{{< /tab >}}

{{< /tabs >}}
---