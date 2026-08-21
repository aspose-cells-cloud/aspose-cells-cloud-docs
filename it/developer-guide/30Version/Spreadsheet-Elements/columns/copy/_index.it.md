---
title: "Copia di colonne in un foglio di lavoro Excel"
second_title: "Documento"
linktitle: "Copia"
type: docs
url: /it/columns/copy/
aliases:
  [/copy-columns-in-excel-worksheet/, /copy-columns-in-an-excel-worksheet/]
keywords: "Aspose.Cells, copia colonne, API Excel, REST, Cloud SDK, cURL, C#, Java, Python, Ruby, Node.js, Go, Perl"
description: "Scopri come copiare una o più colonne in un foglio di lavoro Excel utilizzando l'API REST di Aspose.Cells Cloud (v3.0). Include la sintassi della richiesta, i parametri obbligatori, i dettagli sull'autenticazione, la gestione degli errori ed esempi di SDK in C#, Java, Python, Ruby, Node.js, Go, Perl e altri."
articleTitle: "Copia di colonne in un foglio di lavoro Excel tramite l'API Aspose.Cells Cloud"
weight: 30
---

Questa API REST consente di copiare **colonne** in un foglio di lavoro Excel. L'operazione **Copia colonne** ti permette di duplicare una singola colonna o un intervallo di colonne e inserire la copia in una posizione specificata all'interno dello stesso foglio di lavoro. Utilizza questo endpoint per copiare in modo efficiente colonne quando lavori con fogli di calcolo di grandi dimensioni e consulta le operazioni correlate come [Aggiungi colonna](/columns/add/) e [Nascondi colonna](/columns/hide/) per ulteriori attività di gestione delle colonne.

## Sicurezza e autenticazione
Le API di Aspose.Cells Cloud sono sicure e richiedono [autenticazione basata su token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/copy
```

### Parametri della richiesta

| Nome del parametro         | Tipo    | Posizione | Descrizione                                                                           |
| -------------------------- | ------- | --------- | ------------------------------------------------------------------------------------- |
| **name**                   | string  | path      | Nome del workbook.                                                                    |
| **sheetName**              | string  | path      | Nome del foglio di lavoro.                                                            |
| **sourceColumnIndex**      | integer | query     | Indice in base zero della colonna da copiare.                                         |
| **destinationColumnIndex** | integer | query     | Indice in base zero in corrispondenza del quale verranno inserite le colonne copiate. |
| **columnNumber**           | integer | query     | Numero di colonne consecutive da copiare.                                             |
| **worksheet**              | string  | query     | _(Opzionale)_ Identificatore del foglio di lavoro utilizzato quando il nome del foglio differisce da quello nel percorso. |
| **folder**                 | string  | query     | Percorso della cartella contenente il workbook nell'archivio Aspose Cloud.            |

La [specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostCopyWorksheetColumns) definiscono l'intero contratto per questa operazione.

### Esempio cURL

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/copy?sourceColumnIndex=1&destinationColumnIndex=12&columnNumber=10" \
     -H "Authorization: Bearer $ASPOSE_TOKEN" \
     -H "accept: application/json"
```

### Risposta

```json
{
  "Code": 200,
  "Status": "OK"
}
```

## Gestione degli errori

L'API restituisce i codici di stato HTTP standard con un payload JSON che descrive l'errore.

| Codice di stato | Significato                                          | Esempio di corpo JSON                                               |
| --------------- | ---------------------------------------------------- | ------------------------------------------------------------------- |
| **400**         | Richiesta non valida – parametri non corretti        | `{ "Code": 400, "Message": "Indice di colonna non valido." }`       |
| **401**         | Non autorizzato – token mancante o non valido        | `{ "Code": 401, "Message": "Token di accesso non valido o scaduto." }` |
| **404**         | Non trovato – workbook o foglio di lavoro inesistenti | `{ "Code": 404, "Message": "Workbook non trovato." }`                 |
| **500**         | Errore interno del server – condizione imprevista    | `{ "Code": 500, "Message": "Si è verificato un errore imprevisto." }` |

> **Come risolvere i problemi:** Verifica che il token di accesso sia aggiornato, che i nomi del workbook e del foglio di lavoro siano corretti e che `sourceColumnIndex`, `destinationColumnIndex` e `columnNumber` rientrino nell'intervallo di colonne del foglio di lavoro.

## Famiglia di SDK Cloud

L'utilizzo di un SDK rappresenta il modo più rapido per accelerare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCopyWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCopyWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCopyWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCopyWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCopyWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCopyWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCopyWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCopyWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Come effettuo l'autenticazione quando chiamo l'API Copia colonne?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Ottieni un token di accesso OAuth2 da Aspose Cloud utilizzando il tuo client ID e secret, quindi includilo nell'intestazione della richiesta come `Authorization: Bearer <access_token>`."
      }
    },
    {
      "@type": "Question",
      "name": "Qual è la differenza tra `sourceColumnIndex` e `destinationColumnIndex`?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "`sourceColumnIndex` è l'indice in base zero della colonna che desideri copiare. `destinationColumnIndex` è l'indice in base zero in corrispondenza del quale verranno inserite le colonne copiate."
      }
    },
    {
      "@type": "Question",
      "name": "Che risposta ricevo se l'operazione di copia ha esito negativo?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "L'API restituisce un codice di stato diverso da 200 (ad esempio, 400 per una richiesta non valida, 401 per accesso non autorizzato). Il corpo della risposta contiene un oggetto JSON con i campi `Code` e `Message` che descrivono l'errore."
      }
    }
  ]
}
</script>
---