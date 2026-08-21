---
title: "Alle Arbeitsblattvalidierungen aus einem Excel-Arbeitsblatt abrufen"
second_title: "Dokument"
linktitle: "Alle abrufen"
type: docs
url: /validations/get-all/
keywords: "Aspose.Cells Cloud, Excel, Arbeitsblattvalidierungen, REST-API, Alle Validierungen abrufen, SDKs"
description: "Rufen Sie alle Arbeitsblattvalidierungen aus einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST-API ab. Unterstützt mehrere SDKs (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go) für eine schnelle Integration."
weight: 10
---

Mit Arbeitsblattvalidierungen können Sie Regeln definieren, die den Typ oder Bereich der in Zellen eingebaren Daten einschränken. Sie werden häufig verwendet, um die Datenintegrität sicherzustellen, z. B. durch Einschränkung der Eingaben auf eine Liste von Werten, Daten innerhalb eines bestimmten Bereichs oder numerische Grenzwerte.

Diese REST-API ruft alle Arbeitsblattvalidierungen in einem Excel-Arbeitsblatt ab.

## REST-API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations
```

### **Anforderungsparameter**

| Parametername | Typ   | Ort     | Beschreibung                                      |
| ------------- | ----- | ------- | ------------------------------------------------- |
| name          | string | path    | Name der Excel-Datei.                             |
| sheetName     | string | path    | Name des Arbeitsblatts.                           |
| folder        | string | query   | Ordnerpfad, in dem das Dokument gespeichert ist.  |
| storageName   | string | query   | Name des Speicherdienstes.                        |

**Antwortstatuscodes**

| Code | Beschreibung                                   |
|------|------------------------------------------------|
| 200  | Erfolgreiche Anforderung – Liste der Validierungen |
| 401  | Nicht autorisiert – ungültiges oder fehlendes Token |
| 404  | Nicht gefunden – Dokument oder Arbeitsblatt fehlt |
| 500  | Interner Serverfehler                          |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/WorksheetValidations/GetWorksheetValidations) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt über einen Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf die Aspose.Cells Cloud-Webdienste zuzugreifen. **Voraussetzung:** Sie müssen ein gültiges JWT-Token im `Authorization`-Header angeben.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "validations": [
    {
      "name": "Validation1",
      "type": "WholeNumber",
      "operator": "Between",
      "formula1": "1",
      "formula2": "100",
      "showErrorMessage": true,
      "errorMessage": "Wert muss zwischen 1 und 100 liegen."
    },
    {
      "name": "Validation2",
      "type": "List",
      "formula1": "\"Option1,Option2,Option3\"",
      "showErrorMessage": true,
      "errorMessage": "Wählen Sie einen Wert aus der Liste aus."
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt Low-Level-Details, sodass Sie sich auf die Aufgaben Ihres Projekts konzentrieren können. Weitere Informationen finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetValidations.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetValidations.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetValidations.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetValidations.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetValidations.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetValidations.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetValidations.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetValidations.go" >}}

{{< /tab >}}

{{< /tabs >}}