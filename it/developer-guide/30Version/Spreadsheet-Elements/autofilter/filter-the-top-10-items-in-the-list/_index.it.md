---
title: "Aggiungi il filtro Top 10 a un foglio di lavoro Excel (Aspose.Cells Cloud)"
ArticleTitle: "Aggiungi il filtro Top 10 a un foglio di lavoro Excel – Aspose.Cells Cloud"
second_title: "Documento"
linktype: "docs"
url: /it/autofilter/add-top-10-filter/
aliases:
  [/filter-the-top-10-items-in-the-list/, /autofilter/add-a-top-10-filter/]
keywords: "Aspose.Cells, AutoFilter, Filtro Top 10, API Excel"
description: "Scopri come applicare un filtro AutoFilter Top 10 a un foglio di lavoro Excel utilizzando l'API REST di Aspose.Cells Cloud. Include endpoint, parametri, esempio HTTPS cURL, dettagli sull'autenticazione, gestione degli errori e frammenti di codice SDK per C#, Java, Python e altri linguaggi."
weight: 65
---

Questa API REST filtra gli elementi **Top 10** in un elenco.

> **Prerequisiti**  
> • Ottenere un token JWT valido tramite l'autenticazione di Aspose.Cells Cloud.  
> • Caricare il file Excel nello storage di Aspose Cloud (o specificare lo storage/cartella in cui si trova).  
> • Conoscere il nome del foglio di lavoro e l'intervallo di celle da filtrare.

## API PutWorksheetFilterTop10

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filterTop10
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro  | Tipo    | Posizione | Obbligatorio | Valore predefinito | Descrizione                                                                 |
| --------------- | ------- | --------- | ------------ | ------------------ | --------------------------------------------------------------------------- |
| **name**        | string  | path      | Sì           | —                  | Nome del file Excel.                                                        |
| **sheetName**   | string  | path      | Sì           | —                  | Nome del foglio di lavoro contenente i dati.                                |
| **range**       | string  | query     | Sì           | —                  | Intervallo di celle a cui viene applicato il filtro (ad es. `A1:B10`).      |
| **fieldIndex**  | integer | query     | Sì           | —                  | Indice in base zero della colonna su cui viene applicato il filtro.        |
| **isTop**       | boolean | query     | Sì           | `true`             | `true` per filtrare gli elementi superiori; `false` per quelli inferiori.  |
| **isPercent**   | boolean | query     | No           | `false`            | `true` per interpretare `itemCount` come percentuale; `false` per un conteggio assoluto. |
| **itemCount**   | integer | query     | No           | `10`               | Numero di elementi da includere nel filtro.                                 |
| **matchBlanks** | boolean | query     | No           | `false`            | `true` per includere le celle vuote nei risultati del filtro.              |
| **refresh**     | boolean | query     | No           | `false`            | `true` per aggiornare il filtro dopo averlo applicato.                     |
| **folder**      | string  | query     | No           | —                  | Cartella nello storage in cui si trova il file Excel.                      |
| **storageName** | string  | query     | No           | —                  | Nome dello storage Aspose Cloud.                                            |

### **Risposta**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Risposte di errore tipiche**

```json
{
    "Code":400,
    "Message":"Richiesta non valida – parametri mancanti o non validi."
}
```

```json
{
    "Code":401,
    "Message":"Non autorizzato – token JWT non valido o mancante."
}
```

```json
{
    "Code":413,
    "Message":"Payload troppo grande – il file caricato supera la dimensione consentita."
}
```

```json
{
    "Code":500,
    "Message":"Errore interno del server – condizione imprevista del server."
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                              |
|--------|-----------------------------|----------------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad es. tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante.                         |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione.        |
| 500    | Errore interno del server   | Errore imprevisto del server.                            |

## Come utilizzare l'API PutWorksheetFilterTop10 con gli SDK

### Specifica dell'API PutWorksheetFilterTop10

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetFilterTop10) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come chiamare l'API con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filterTop10?range=A1:B10&fieldIndex=0&isTop=true&itemCount=10" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzo degli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK rappresenta il modo più rapido per sviluppare. Un SDK gestisce i dettagli a basso livello, consentendoti di concentrarti sul tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetFilterTop10.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetFilterTop10.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetFilterTop10.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetFilterTop10.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetFilterTop10.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetFilterTop10.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetFilterTop10.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetFilterTop10.go" >}}

{{< /tab >}}

{{< /tabs >}}