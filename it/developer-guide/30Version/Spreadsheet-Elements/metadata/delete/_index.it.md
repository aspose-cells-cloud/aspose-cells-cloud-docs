---
title: "Elimina i metadati dai file Excel"
second_title: "Documento"
linktitle: "Elimina senza utilizzare l'archiviazione"
type: docs
url: /metadata/delete/
keywords: "Aspose.Cells, eliminazione metadati, API Excel, proprietà del workbook"
description: "Elimina i metadati del workbook (autore, titolo, personalizzati) tramite l'API Aspose.Cells Cloud. Include endpoint, autenticazione, parametri e esempi cURL e SDK."
weight: 55
ArticleTitle: "Elimina i metadati dai file Excel – Documentazione Aspose.Cells Cloud"
---

**Panoramica**  
L'operazione *Delete Metadata* rimuove in modo permanente tutte le proprietà del workbook (standard e personalizzate) dal/i file Excel caricato/i e restituisce il/i file elaborato/i nella risposta.

**Prerequisiti**  
- Un token JWT valido di Aspose.Cells Cloud (ottenibile tramite il flusso di autenticazione OAuth 2.0).  
- Versione API **v3.0** (l'endpoint utilizzato in questo esempio).  
- Per l'uso degli SDK, installa l'SDK Aspose.Cells Cloud appropriato per il tuo linguaggio (ad esempio tramite NuGet, Maven, npm, pip, CPAN o moduli Go).

Questa API REST elimina i **metadati** da uno o più file Excel. Rimuove le proprietà del workbook come autore, titolo e dati personalizzati, restituendo i file puliti.

## API

```http
POST https://api.aspose.cloud/v3.0/cells/metadata/delete
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione tramite token JWT</a>.

### **Parametri della richiesta**

| Nome parametro | Tipo   | Posizione | Descrizione                                                |
| -------------- | ------ | --------- | ---------------------------------------------------------- |
| file           | file   | formData  | File Excel da caricare per l'eliminazione dei **metadati** |
| type           | string | query     | Tipo di operazione; impostare su **all** per eliminare tutti i **metadati** |

La <a href="https://apireference.aspose.cloud/cells/#/DeleteMetadata" target="_blank" rel="noopener noreferrer">specifiche OpenAPI</a> definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di effettuare direttamente interazioni REST da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud tramite cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/metadata/delete?type=all" \
  -X POST \
  -H "Authorization: Bearer <jwt token>" \
  -F "file=@file1.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "file1.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

**Risposte di errore** possono includere:

- **400 Bad Request** – file mancante o valore `type` non valido.
- **401 Unauthorized** – token JWT non valido o mancante.
- **500 Internal Server Error** – errore di elaborazione lato server.

L'API restituisce un oggetto JSON contenente un campo `Error` con i dettagli per ciascun caso.

| Codice | Significato | Descrizione |
|--------|-------------|-------------|
| 200 | OK | Metadati eliminati, file restituito |
| 400 | Bad Request | File mancante o `type` non valido |
| 401 | Unauthorized | JWT non valido o mancante |
| 500 | Internal Server Error | Errore di elaborazione lato server |

## Famiglia di SDK Cloud

L'utilizzo di un SDK rappresenta il modo più rapido per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come richiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}