---
title: "Rimuovi righe duplicate da un ListObject – Documentazione API Aspose.Cells Cloud"
second_title: "Documento"
linktitle: "Rimuovi duplicati"
type: docs
keywords: "rimuovi duplicati, listobject, API Aspose.Cells Cloud, Excel, REST"
url: /it/list-objects/remove-duplicates/
description: "Scopri come eliminare le righe duplicate da un ListObject in un foglio di calcolo Excel utilizzando l'API REST di Aspose.Cells Cloud. Include endpoint, parametri, autenticazione e esempi di richieste e risposte."
weight: 20
---

Questa API REST rimuove le righe duplicate da un **ListObject** in un foglio di calcolo Excel.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates
```

### **Parametri della richiesta**

| Nome del parametro  | Tipo    | Posizione | Descrizione                                              |
| ------------------- | ------- | -------- | -------------------------------------------------------- |
| **name**            | Stringa | Path     | Il nome del file Excel.                                  |
| **sheetName**       | Stringa | Path     | Il nome del foglio di calcolo contenente l'oggetto elenco. |
| **listObjectIndex** | Intero  | Path     | L'indice in base zero dell'oggetto elenco da elaborare.  |
| **folder**          | Stringa | Query    | (Facoltativo) Il percorso della cartella in cui è memorizzato il file. |
| **storageName**     | Stringa | Query    | (Facoltativo) Il nome del servizio di archiviazione.     |

### Esempio di richiesta (cURL)

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "DuplicateRowsRemoved": 12,
  "Message": "Le righe duplicate sono state rimosse correttamente."
}
```

{{< /tab >}}
{{< /tabs >}}

### Risposta

In caso di esito positivo, il servizio restituisce un oggetto JSON simile all'esempio precedente. I campi sono:

- **Code** – Codice di stato HTTP (`200` per successo).
- **Status** – Descrizione testuale dello stato.
- **DuplicateRowsRemoved** – Numero di righe rimosse.
- **Message** – Ulteriori informazioni sull'operazione.

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante. |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server   | Errore imprevisto del server. |

## Famiglia di SDK Cloud

L'uso di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il repository GitHub per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectRemoveDuplicates.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectRemoveDuplicates.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectRemoveDuplicates.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectRemoveDuplicates.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectRemoveDuplicates.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectRemoveDuplicates.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectRemoveDuplicates.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectRemoveDuplicates.go" >}}

{{< /tab >}}

{{< /tabs >}}