---
title: "Hinzufügen einer Arbeitsblattvalidierung zu einem Excel-Arbeitsblatt"
second_title: "Dokument"
linktitle: "Hinzufügen"
type: docs
url: /validations/add/
keywords: "Arbeitsblattvalidierung hinzufügen, Excel, Aspose.Cells Cloud, REST-API, Tabellenkalkulation, Validierungsregel"
description: "Verwenden Sie die Aspose.Cells Cloud REST-API, um einer Excel-Datei eine Arbeitsblattvalidierung hinzuzufügen. SDKs sind für C#, Java, PHP, Ruby, Node.js, Python, Perl, Go und Swift verfügbar."
weight: 10
---

Diese REST API fügt einem Excel-Arbeitsblatt eine Arbeitsblattvalidierung hinzu.

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations
```

### **Anforderungsparameter**

| Parametername | Typ    | Speicherort | Beschreibung                                               |
| ------------- | ------ | ----------- | ---------------------------------------------------------- |
| name          | string | path        | Name der Excel-Datei.                                      |
| sheetName     | string | path        | Name des Arbeitsblatts.                                    |
| range         | string | query       | Zellbereich, auf den die Validierung angewendet wird (z. B. A1:B10). |
| validation    | object | body        | Definition der Validierungsregel.                          |
| folder        | string | query       | Ordner, der das Dokument enthält.                          |
| storageName   | string | query       | Name des Speicherdienstes.                                 |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/WorksheetValidations/PutWorksheetValidation) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser heraus durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie mithilfe von cURL Aufrufe an die Cloud-API durchgeführt werden.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie

Die Verwendung eines SDK ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details und ermöglicht es Ihnen, sich auf Ihre ProjektAufgaben zu konzentrieren. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PutWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}