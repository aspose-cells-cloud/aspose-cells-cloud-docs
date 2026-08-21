---
title: "Ottenere intervallo con nome in un foglio di calcolo Excel"
second_title: "Documento"
linktitle: "Nome"
type: docs
url: /ranges/get/name/
aliases: [/get-named-ranges-inside-the-workbook/]
keywords: "intervallo con nome, Excel, Aspose.Cells, API cloud, fogli di lavoro"
description: "Recupera gli intervalli con nome da un foglio di calcolo Excel utilizzando l'API REST di Aspose.Cells Cloud. Include i dettagli della richiesta, comandi cURL di esempio ed esempi di SDK per diversi linguaggi di programmazione."
ArticleTitle: "Ottenere intervalli con nome in un foglio di calcolo Excel – Aspose.Cells Cloud API"
weight: 10
---

Questa REST API restituisce informazioni sugli intervalli con nome definiti all'interno dei fogli di lavoro.

**Panoramica** – Un *intervallo con nome* è un identificatore definito dall'utente che fa riferimento a una cella specifica o a un blocco di celle in un foglio di lavoro. Gli intervalli con nome semplificano la creazione di formule, migliorano la leggibilità e consentono l'accesso programmatico ad aree frequentemente utilizzate di un foglio di calcolo.

**Prerequisiti** – L'accesso all'API REST di Aspose.Cells Cloud richiede un token di accesso JWT valido. Ottieni il token effettuando l'autenticazione con il tuo client ID e client secret Aspose Cloud tramite l'endpoint del token OAuth 2.0. Includi il token nell'intestazione di ogni richiesta come `Authorization: Bearer <token JWT>`.

## API GetNamedRanges

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/ranges
```

### **Sicurezza e autenticazione**

Le API REST di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro | Tipo   | Posizione     | Descrizione                                       |
| -------------- | ------ | ------------- | ------------------------------------------------- |
| name           | string | Path          | Il nome del documento Excel.                      |
| folder         | string | Query string  | La cartella contenente il documento.              |
| storageName    | string | Query string  | Il nome dell'archiviazione in cui risiede il documento. |

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                          |
|--------|-----------------------------|------------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante.                    |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione.    |
| 500    | Errore interno del server   | Errore imprevisto nel server.                       |

La [specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetNamedRanges) definiscono un'interfaccia di programmazione pubblicamente accessibile che consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per chiamare i servizi web di Aspose.Cells. L'esempio seguente mostra come recuperare gli intervalli con nome utilizzando cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/ranges" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Ranges": {
    "RangeList": [
      {
        "ColumnCount": 7,
        "ColumnWidth": 8.428571428571429,
        "FirstColumn": 1,
        "FirstRow": 9,
        "Name": "data",
        "RefersTo": "=Sheet1!$B$10:$H$10",
        "RowCount": 1,
        "RowHeight": 15,
        "Worksheet": "Sheet1"
      }
    ]
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Modello di risposta**

| Campo          | Tipo    | Descrizione                                              |
|----------------|---------|----------------------------------------------------------|
| `ColumnCount`  | integer | Numero di colonne nell'intervallo.                       |
| `ColumnWidth`  | number  | Larghezza di ciascuna colonna (in punti).                |
| `FirstColumn`  | integer | Indice in base zero della prima colonna nell'intervallo. |
| `FirstRow`     | integer | Indice in base zero della prima riga nell'intervallo.    |
| `Name`         | string  | Nome definito dall'utente per l'intervallo.              |
| `RefersTo`     | string  | Formula che definisce il riferimento alla cella (es. `=Sheet1!$B$10:$H$10`). |
| `RowCount`     | integer | Numero di righe nell'intervallo.                         |
| `RowHeight`    | number  | Altezza di ciascuna riga (in punti).                     |
| `Worksheet`    | string  | Nome del foglio di lavoro che contiene l'intervallo.     |

## Famiglia di SDK cloud

L'utilizzo di un SDK è il modo più rapido per integrare questa funzionalità. Gli SDK gestiscono i dettagli di basso livello, consentendoti di concentrarti sulla logica di business. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per l'elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetNamedRanges.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetNamedRanges.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetNamedRanges.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetNamedRanges.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetNamedRanges.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetNamedRanges.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetNamedRanges.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetNamedRanges.go" >}}

{{< /tab >}}

{{< /tabs >}}