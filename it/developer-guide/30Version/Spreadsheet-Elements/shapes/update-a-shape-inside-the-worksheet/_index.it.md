---
title: "Aggiorna una forma in un foglio di lavoro Excel"
second_title: "Document"
linktype: "Aggiorna"
type: docs
url: /it/shapes/update/
aliases: [  /it/update-a-shape-inside-the-worksheet/ ]
keywords: "aggiornare forma Excel API, Aspose.Cells Cloud, aggiornamento forma Excel, REST API, SDK, C#, Java, Python, Node.js, Go, Ruby, PHP, Perl, Swift"
description: "Scopri come aggiornare una forma in un foglio di lavoro Excel utilizzando l'API REST di Aspose.Cells Cloud. Include l'endpoint HTTPS, i dettagli di autenticazione, lo schema DTO, un'illustrazione passo-passo, un esempio cURL e codici di esempio per SDK in diversi linguaggi."
ArticleTitle: "Aggiorna una forma in un foglio di lavoro Excel - API Aspose.Cells Cloud"
weight: 31
---

Questa API REST aggiorna una forma in un foglio di lavoro Excel.

## Sicurezza e autenticazione

Le API di Aspose.Cells Cloud sono sicure e richiedono l'[autenticazione tramite token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes/{shapeindex}
```

### Parametri della richiesta

| Nome del parametro | Tipo    | Posizione | Descrizione                                                                                   |
| ------------------ | ------- | --------- | --------------------------------------------------------------------------------------------- |
| **name**           | stringa | percorso  | Il nome del file del workbook.                                                                |
| **sheetName**      | stringa | percorso  | Il nome del foglio di lavoro che contiene la forma.                                           |
| **shapeindex**     | intero  | percorso  | L'indice in base zero della forma all'interno del foglio di lavoro.                           |
| **dto**            | oggetto | corpo     | L'oggetto di trasferimento dati della forma che contiene le proprietà aggiornate (vedi _Schema DTO_ di seguito). |
| **folder**         | stringa | query     | La cartella in cui è memorizzato il workbook.                                                 |
| **storageName**    | stringa | query     | Il nome dello storage di Aspose Cloud.                                                        |

### Schema DTO

L'oggetto `dto` contiene le proprietà che è possibile aggiornare. Tutti i campi sono facoltativi, salvo quanto indicato esplicitamente.

| Campo               | Tipo    | Obbligatorio | Descrizione                                                                         |
| ------------------- | ------- | ------------ | ----------------------------------------------------------------------------------- |
| **Name**            | stringa | No           | Nuovo nome per la forma.                                                            |
| **UpperLeftRow**    | intero  | No           | Indice di riga dell'angolo superiore sinistro della forma.                          |
| **UpperLeftColumn** | intero  | No           | Indice di colonna dell'angolo superiore sinistro della forma.                       |
| **Width**           | intero  | No           | Larghezza della forma (in punti).                                                   |
| **Height**          | intero  | No           | Altezza della forma (in punti).                                                     |
| **RotationAngle**   | intero  | No           | Angolo di rotazione in gradi.                                                       |
| **IsHidden**        | booleano| No           | `true` per nascondere la forma.                                                     |
| **IsLocked**        | booleano| No           | `true` per bloccare la forma.                                                       |
| **Font**            | oggetto | No           | Impostazioni del carattere (vedi specifica OpenAPI per le sottoproprietà).          |
| **...**             | …       | No           | Altre proprietà, come `HtmlText`, `AlternativeText`, `ZOrderPosition`, ecc.        |

> Per un elenco completo, fare riferimento alla specifica OpenAPI ufficiale: <https://apireference.aspose.cloud/cells/#/Shapes/PostWorksheetShape>.

### Intestazioni della richiesta

- `Content-Type: application/json`
- `Accept: application/json`
- `Authorization: Bearer <accessToken>` _(il token JWT ottenuto nel passo di _Autenticazione_)_

### Corpo della richiesta (esempio)

```json
{
  "Name": "MyShape",
  "UpperLeftRow": 2,
  "UpperLeftColumn": 3,
  "Width": 150,
  "Height": 80,
  "RotationAngle": 0,
  "IsHidden": false,
  "IsLocked": false,
  "Font": {
    "Name": "Calibri",
    "Size": 12,
    "IsBold": true,
    "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }
  }
}
```

## Esempio con cURL (strumento a riga di comando)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes/0?folder=Temp" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <accessToken>" \
  -d '{
        "Name": "UpdatedShape",
        "UpperLeftRow": 1,
        "UpperLeftColumn": 1,
        "Width": 120,
        "Height": 60,
        "IsHidden": false,
        "IsLocked": false
      }'
```

### Risposta

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Gestione degli errori** – L’API può restituire i seguenti codici di stato:

| Codice | Significato            | Causa tipica                                        |
| ------ | ---------------------- | --------------------------------------------------- |
| 400    | Richiesta non valida   | JSON non valido o campi obbligatori mancanti.      |
| 401    | Non autorizzato        | Token JWT mancante o non valido.                    |
| 404    | Non trovato            | Il workbook, il foglio di lavoro o l'indice della forma non esistono. |
| 500    | Errore interno del server | Problema imprevisto lato server.                  |

**Esempi di risposte di errore**

*400 – Richiesta non valida*

```json
{
  "Code": 400,
  "Message": "Payload della richiesta non valido. Il campo 'Name' supera la lunghezza massima."
}
```

*401 – Non autorizzato*

```json
{
  "Code": 401,
  "Message": "Autenticazione non riuscita. Token JWT non valido o scaduto."
}
```

*404 – Non trovato*

```json
{
  "Code": 404,
  "Message": "Il workbook, il foglio di lavoro o l'indice della forma specificati non sono stati trovati."
}
```

*500 – Errore interno del server*

```json
{
  "Code": 500,
  "Message": "Si è verificato un errore imprevisto sul server."
}
```

## Famiglia di SDK per il cloud

Utilizzare un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells Cloud utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}