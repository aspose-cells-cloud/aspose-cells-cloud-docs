---
title: "Inserire un filtro di selezione in un oggetto elenco di Excel – Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "Inserire filtro di selezione"
type: docs
keywords: "Aspose.Cells, filtro di selezione Excel, oggetto elenco, API REST, SDK cloud"
description: "Scopri come aggiungere un filtro di selezione a un oggetto elenco di Excel utilizzando l'API REST di Aspose.Cells Cloud (v3.0). Include endpoint, parametri, autenticazione, richiesta cURL di esempio e risposta JSON."
weight: 20
ArticleTitle: "Inserire un filtro di selezione in un oggetto elenco di Excel – Aspose.Cells Cloud API"
---

Questa API REST inserisce un filtro di selezione per un oggetto elenco in un foglio di calcolo Excel.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/InsertSlicer
```

### Parametri della richiesta

| Nome parametro  | Tipo    | Posizione | Descrizione                                                                 |
| --------------- | ------- | --------- | --------------------------------------------------------------------------- |
| name            | Stringa | Path      | Nome del file Excel.                                                       |
| sheetName       | Stringa | Path      | Nome del foglio di calcolo contenente l'oggetto elenco.                    |
| listObjectIndex | Integer | Path      | Indice in base zero dell'oggetto elenco a cui verrà aggiunto il filtro.    |
| columnIndex     | Integer | Query     | Indice in base zero della colonna su cui si basa il filtro.                |
| destCellName    | Stringa | Query     | Riferimento alla cella (ad esempio **A1**) in cui verrà posizionato il filtro. |
| folder          | Stringa | Query     | Cartella nello storage contenente il file Excel.                           |
| storageName     | Stringa | Query     | Nome del servizio di storage Aspose Cloud.                                 |

È possibile utilizzare lo strumento a riga di comando cURL per chiamare l'API:

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/InsertSlicer" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **Nota:** La richiesta richiede un token bearer JWT valido ottenuto dal servizio di autenticazione Aspose Cloud. Questo endpoint non richiede un corpo di richiesta; inviare un oggetto JSON vuoto `{}` se la libreria client richiede un payload.

{{< /tab >}}
{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Slicer": {
    "Name": "Slicer1",
    "ColumnIndex": 2,
    "Position": "A1"
  }
}
```

> **Intestazione di risposta:** `Content-Type: application/json`

{{< /tab >}}
{{< /tabs >}}

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                                   |
|--------|-----------------------------|---------------------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante.                              |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione.              |
| 500    | Errore interno del server   | Errore imprevisto nel server.                                 |

### Gestione degli errori

Quando si verifica un errore, l'API restituisce un oggetto JSON contenente un campo `ErrorMessage` che descrive il problema. Esaminare il codice di stato HTTP e il campo `ErrorMessage` per determinare l'azione correttiva.

## Famiglia di SDK cloud

L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello e consente di concentrarsi sulle attività del proprio progetto. Consultare il repository GitHub per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice illustrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectInsertSlicer.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectInsertSlicer.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectInsertSlicer.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectInsertSlicer.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectInsertSlicer.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectInsertSlicer.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectInsertSlicer.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectInsertSlicer.go" >}}
{{< /tab >}}

{{< /tabs >}}