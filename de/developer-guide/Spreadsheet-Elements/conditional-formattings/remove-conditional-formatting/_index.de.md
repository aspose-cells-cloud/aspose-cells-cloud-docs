---
title: Bedingte Formatierung löschen
type: docs
url: /de/conditional-formattings/delete/
aliases: [/remove-conditional-formatting/]
keywords: REST API, spreadsheets, excel, delete cell area from condition formattin
description: "Cells.Cloud API für Excel bedienen: Zellbereich aus Bedingungsformatierung löschen"
weight: 60
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdown, Bedingte Formatierung löschen
---
Dieser REST API zeigt an, dass die bedingte Formatierung entfernt werden soll.
 
## RSET API
 
```bash
 
DELETE http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}
 
```
 Die Anforderungsparameter sind:
 
| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Name| Schnur| Weg||
| Blattname| Schnur| Weg||
| Index| ganze Zahl| Weg||
| Ordner| Schnur| Abfrage||
| Speichername| Schnur| Abfrage| Speichername.|
 
 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormatting) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen die Durchführung von REST-Interaktionen direkt von einem Webbrowser aus.
 
Mit dem Befehlszeilentool cURL können Sie problemlos auf die Webdienste Aspose.Cells zugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud API tätigen.


{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings/0" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

{
  "Code": "200",
  "Status": "OK"
}

```

{{< /tab >}}

{{< /tabs >}}
 
## Cloud SDK-Familie
 
 Die Verwendung eines SDKs beschleunigt die Entwicklung am besten. Ein SDK kümmert sich um grundlegende Details und ermöglicht Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Bitte beachten Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.
 
Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}



{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-RemoveConditionalFormatting-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-remove-conditional-formatting.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}



{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-delete_worksheet_conditional_formatting-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}



{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-RemoveConditionalFormatting-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}



{{< /tab >}}

{{< tab tabNum="7" >}}



{{< /tab >}}

{{< tab tabNum="8" >}}



{{< /tab >}}

{{< tab tabNum="9" >}}



{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-RemoveConditionalFormatting-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "fa6aed4b68d309d8de12d91ff7c0111d" >}}

{{< /tab >}}

{{< /tabs >}}
