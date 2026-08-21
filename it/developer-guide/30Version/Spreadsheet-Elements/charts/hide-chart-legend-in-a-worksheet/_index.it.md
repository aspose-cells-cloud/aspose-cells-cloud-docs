---
title: "Nascondere la legenda di un grafico in un foglio di calcolo Excel – Aspose.Cells Cloud API"
type: docs
url: /it/charts/legend/hide/
aliases: [/it/hide-chart-legend-in-a-worksheet/]
weight: 110
keywords: "Aspose.Cells, Excel, nascondere legenda grafico, API REST, SDK cloud, legenda grafico"
description: "Scopri come nascondere la legenda di un grafico in un foglio di calcolo Excel utilizzando l'API REST Aspose.Cells Cloud. Include l'endpoint HTTPS, l'autenticazione richiesta, la sintassi della richiesta, i dettagli della risposta, la gestione degli errori ed esempi di SDK."
---

Questa API REST nasconde la legenda di un grafico. Una **legenda del grafico** è il riquadro che identifica le serie di dati rappresentate nel grafico.

L'API richiede un token JWT valido di Aspose Cloud, il workbook deve essere caricato nello storage Aspose Cloud e la versione dell'API utilizzata è **v3.0**.

## Sicurezza e autenticazione
Le API Aspose.Cells Cloud sono sicure e richiedono [l'autenticazione basata su token JWT](https://docs.aspose.cloud/it/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### Parametri della richiesta

| Nome parametro  | Tipo    | Posizione | Descrizione                          |
| --------------- | ------- | -------- | ------------------------------------ |
| **name**        | string  | path     | Nome del workbook.                   |
| **sheetName**   | string  | path     | Nome del foglio di calcolo.          |
| **chartIndex**  | integer | path     | Indice del grafico.                  |
| **folder**      | string  | query    | Cartella del workbook (opzionale).   |
| **storageName** | string  | query    | Nome dello storage (opzionale).      |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/it#/Charts/DeleteWorksheetChartLegend) definiscono questa interfaccia di programmazione accessibile pubblicamente.

Puoi utilizzare lo strumento a riga di comando cURL per chiamare facilmente l'API. L'esempio seguente mostra una richiesta che nasconde la legenda del grafico 0 in _Sample_Test_Book.xls_.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
  -X DELETE \
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

## Risposte

| Stato HTTP                    | Descrizione                                        | Esempio JSON                                                  |
| ----------------------------- | -------------------------------------------------- | ------------------------------------------------------------- |
| **200 OK**                    | Legenda nascosta correttamente.                    | `{ "Code": 200, "Status": "OK" }`                             |
| **401 Unauthorized**          | Token JWT mancante o non valido.                   | `{ "Code": 401, "Message": "Token di accesso non valido." }` |
| **404 Not Found**             | Il workbook, il foglio di calcolo o il grafico non esistono. | `{ "Code": 404, "Message": "Grafico non trovato." }`         |
| **500 Internal Server Error** | Errore imprevisto del server.                      | `{ "Code": 500, "Message": "Si è verificato un errore imprevisto." }` |

## FAQ

**Q:** _Come nascondo la legenda di un grafico utilizzando Aspose.Cells Cloud?_  
**A:** Invia una richiesta `DELETE` a `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend` con un token JWT valido nell'intestazione `Authorization`. Una risposta `200 OK` indica il successo.

**Q:** _Quale autenticazione è richiesta per l'API Nascondi legenda grafico?_  
**A:** Includi l'intestazione `Authorization: Bearer <jwt token>`. Ottieni il token tramite il flusso OAuth di Aspose Cloud.

**Q:** _Quale risposta di errore riceverò se l'indice del grafico non è valido?_  
**A:** Il servizio restituisce `404 Not Found` con un corpo JSON contenente `Code: 404` e un messaggio che descrive il grafico mancante.

**Q:** _Posso utilizzare HTTP invece di HTTPS?_  
**A:** No. Tutti gli endpoint Aspose Cloud richiedono HTTPS per motivi di sicurezza.

## Famiglia di SDK Cloud

Utilizzare un SDK è il modo più rapido per sviluppare. Un SDK astrae i dettagli di basso livello, permettendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-HideChartLegend-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-HideChartLegend-hide-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetChartLegend-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-hide_legend_in_chart-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "HideChartLegendInWorkSheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-HideChartLegend-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-HideChartLegend-hide-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}
**In arrivo presto** – L’esempio di SDK Swift verrà aggiunto a breve.  
{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-HideChartLegend-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3eb15aa10e3d2cd8931e60f8d001fd1c" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebPage",
  "name": "Nascondere la legenda di un grafico in un foglio di calcolo Excel – Aspose.Cells Cloud API",
  "description": "Guida passo passo per nascondere la legenda di un grafico in un foglio di calcolo Excel utilizzando l'API REST Aspose.Cells Cloud. Include endpoint HTTPS, autenticazione, sintassi della richiesta, dettagli della risposta, gestione degli errori ed esempi di SDK.",
  "breadcrumb": {
    "@type": "BreadcrumbList",
    "itemListElement": [
      { "@type": "ListItem", "position": 1, "name": "Home", "item": "https://docs.aspose.cloud/it/" },
      { "@type": "ListItem", "position": 2, "name": "Cells", "item": "https://docs.aspose.cloud/cells/" },
      { "@type": "ListItem", "position": 3, "name": "Grafici", "item": "https://docs.aspose.cloud/cells/charts/" },
      { "@type": "ListItem", "position": 4, "name": "Nascondi legenda grafico", "item": "https://docs.aspose.cloud/cells/charts/legend/hide/" }
    ]
  },
  "about": "Nascondere la legenda del grafico utilizzando l'API Aspose.Cells Cloud"
}
</script>