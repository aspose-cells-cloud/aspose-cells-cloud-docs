---
title: "Aspose.Cells Cloud Excel-Entschutz-Web-API – Öffnen und Ändern von Passwörtern programmgesteuert entfernen"
second_title: "Dokument"
ArticleTitle: "Excel-Passwortschutz entfernen – Öffnen und Ändern von Passwörtern sofort entsperren"
linktitle: "Tabellendokument entsperren"
type: docs
url: /de/unprotect-spreadsheet/
keywords: "entsperren, Tabellendokument, Aspose.Cells, API, Excel, Passwortentfernung"
description: "Entfernen Sie öffnende und ändernde Passwörter aus Excel-Dateien programmgesteuert mit der Aspose.Cells Cloud-Entschutz-API für Tabellendokumente. Unterstützt .xlsx/.xls, OAuth2-Authentifizierung und Stapelverarbeitung."
weight: 100
---

Die Entschutz-API für Tabellendokumente entfernt den Passwortschutz zum Öffnen und Bearbeiten von Excel-Dateien mit einem einzigen Aufruf. Sie eignet sich ideal für Datenpipelines, Dokumentenverwaltungssysteme und Migrationsworkflows.

## **Entschutz-API für Tabellendokumente**

### **Web-API**

```http
PUT https://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Anforderungsparameter**

| Parametername     | Typ    | Speicherort | Beschreibung                                                                                      |
| ----------------- | ------ | ----------- | ------------------------------------------------------------------------------------------------- |
| Spreadsheet       | Datei  | FormData    | Die zu entsperrende Excel-Datei.                                                                 |
| password          | String | Query       | Das Passwort zum Öffnen der Datei.                                                               |
| modifyPassword    | String | Query       | Das Passwort zum Ändern der Datei (optional, falls nur ein Öffnungspasswort gesetzt ist).        |
| outPath           | String | Query       | (Optional) Pfad zum Ordner, in dem die entsperrte Arbeitsmappe gespeichert werden soll.         |
| outStorageName    | String | Query       | (Optional) Name des Speichers, in den die Ausgabedatei geschrieben werden soll.                 |
| region            | String | Query       | (Optional) Regionaleinstellungen für das Tabellendokument.                                      |

### **Antwort**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

Bei erfolgreicher Ausführung wird die entsperrte Datei als Stream zurückgegeben. Die Datei kann am durch `outPath`/`outStorageName` angegebenen Speicherort gespeichert oder direkt aus dem Antwortinhalt abgerufen werden.

**HTTP-Statuscodes**

| Code | Bedeutung             | Beschreibung                                                      |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails.  |
| 400  | Ungültige Anforderung | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Nicht autorisiert     | Ungültiger oder fehlender JWT-Token.                             |
| 413  | Anforderung zu groß   | Die hochgeladene Datei überschreitet die Größenbeschränkung.     |
| 500  | Interner Serverfehler | Unerwarteter Serverfehler.                                        |

## Wann sollten Sie die Entschutz-API für Tabellendokumente verwenden?

- **Zugriff auf gesperrte Arbeitsmappen wiederherstellen** – Vergessene Öffnungs- oder Änderungspasswörter schnell und ohne manuellen Aufwand entfernen.
- **Große Mengen entsperren** – Viele Dateien in Datenmigrationen oder Archivierungsprojekten automatisiert verarbeiten.
- **In bestehende Workflows integrieren** – Mit Speicher- oder Konvertierungs-APIs kombinieren, um End-to-End-Pipelines zu erstellen (z. B. hochladen → entsperren → in PDF konvertieren).
- **Datensicherheit gewährleisten** – Der Vorgang erfolgt serverseitig, sodass die Originaldateien sicher bleiben, während die entsperrte Version in Ihrem Cloud-Speicher abgelegt wird.

## Verwendung der Entschutz-API für Tabellendokumente mit SDKs

### **OpenAPI-Spezifikation**

Die [OpenAPI-Spezifikation für die Entschutz-API für Tabellendokumente](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Protection/ProtectSpreadsheet) bietet eine öffentlich zugängliche Programmierschnittstelle, um direkte REST-Aufrufe aus einem Webbrowser zu ermöglichen.

Sie können das cURL-Befehlszeilentool nutzen, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet?password=OldPass&modifyPassword=ModPass" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@myfile.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64-kodiert)",
  "contentType": "MIME-Typ",
  "fileDownloadName": "optionaler Dateiname"
}
```

{{< /tab >}}

{{< /tabs >}}

### **Verwendung der Aspose.Cells Cloud SDKs**

Ein SDK vereinfacht den Aufruf, da es die Authentifizierung, Anforderungserstellung und Antwortverarbeitung übernimmt. Die SDKs stehen für viele Sprachen zur Verfügung und enthalten bereits fertige Methoden zum Entsperrten von Tabellendokumenten.

Die folgenden Codebeispiele zeigen, wie Sie die Entschutz-API für Tabellendokumente mit verschiedenen SDKs aufrufen:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UnprotectSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UnprotectSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UnprotectSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UnprotectSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UnprotectSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UnprotectSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UnprotectSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UnprotectSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}