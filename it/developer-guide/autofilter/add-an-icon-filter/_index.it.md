---
title: Aggiungi un filtro icona in un foglio di lavoro Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Aggiungi filtro icona
type: docs
url: /it/autofilter/add-icon-filter/
aliases: [/add-an-icon-filter/,/autofilter/add-an-icon-filter/]
keywords: Adds an icon filter on an Excel worksheet
description: Il Aspose.Cells Cloud API supporta l'aggiunta di un filtro icona su un foglio di lavoro Excel. L'SDK supporta tipi di linguaggi di sviluppo. Includono Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e swift
weight: 65
---
Questo REST API indica di aggiungere un `icon filter` su un foglio di lavoro Excel.

## RSET API

```bash

PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/iconFilter

```

I parametri della richiesta sono:

| Nome parametro| Tipo| Percorso/Stringa di query/HTTPBody|Descrizione|
|:- |:- |:- |:- |
| nome| corda| Sentiero|Il nome della cartella di lavoro.|
| foglioNome| corda| Sentiero| Il nome del foglio di lavoro.|
|allineare|corda| Domanda||
|fieldIndex|numero intero| Domanda||
|iconSetType|corda| Domanda| Frecce3/FrecceGrigio3/Bandiere3/Segnali3/Simboli3/Simboli32/Semaforo31/Semaforo32/Frecce4/FrecceGrigio4/Valutazione4/RossoAlNero4/Semaforo4/Frecce5/FrecceGrigio5/Quartieri5/Valutazione5/Stelle3/Riquadri5/Triangoli3/Nessuno/CustomSet/Smilies3 /ColoreSmilies3|
|ID icona|numero intero| Domanda||
|matchBlanks|corda| Domanda|vero falso|
|ricaricare|corda| Domanda|vero falso|
|cartella|corda| Domanda|Cartella di lavoro originale.|
|storageName| Domanda|corda|Nome di archiviazione.|

 IL[Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetIconFilter) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi Web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate a Cloud API con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash

curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/iconFilter?range=A1:B1&fieldIndex=0&iconSetType=ArrowsGray3&iconId=1" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```bash
{
  "Code": 200,
  "Status": "OK"
}

```

{{< /tab >}}

{{< /tabs >}}


## Famiglia di SDK cloud

 L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Si prega di controllare il[Deposito GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-Worksheet-AddIconFilter-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-filters-AddIconFilterExample-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-AutoFilter-PutWorksheetIconFilter-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-AutoFilter-put_worksheet_icon_filter-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-AddIconFilter-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}



{{< gist "aspose-cells-cloud-gists" "75ea6b5d2f6d82f9c2f9279fb37ebbdf" "Examples-Android-filters-AddIconFilterExample-1.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-AddIconFilter-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "a05cbd25e102b8369a2ad33d46252a07" >}}

{{< /tab >}}

{{< /tabs >}}
