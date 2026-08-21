---
title: "Aspose.Cells Cloud Excel-Passwortschutz-Web-API – Automatisieren Sie den Öffnen- und Bearbeitungspasswortschutz"
second_title: "Entwicklerhandbuch für Excel-Schutz"
ArticleTitle: "Excel-Passwortschutz-Tool – Öffnen- und Bearbeitungspasswörter festlegen – Sichern Sie Ihre Tabellenkalkulationen"
linktitle: "Tabellenkalkulation schützen"
type: docs
url: /de/protect-spreadsheet/
keywords: "Aspose.Cells, Excel-Passwortschutz, API, Öffnungspasswort, Bearbeitungspasswort, Cloud-Speicherung, Tabellenkalkulationssicherheit"
description: "Schützen Sie Excel-Dateien programmgesteuert mit Aspose.Cells Cloud. Legen Sie sowohl Öffnungs- als auch Bearbeitungspasswörter mit einem einzigen API-Aufruf fest. Unterstützt .xlsx, .xls und Cloud-Speicherung. Kostenlos testen."
weight: 100
---

Automatisieren Sie den Excel-Passwortschutz in großem Maßstab mit unserer Developer-API – wenden Sie sowohl Öffnungs- als auch Bearbeitungspasswörter programmgesteuert an. Ideal für Unternehmensworkflows und kompatibel mit .xlsx sowie veralteten Formaten. Holen Sie sich die Dokumentation und starten Sie noch heute Ihre kostenlose Integration.

## **API zum Schützen von Tabellenkalkulationen**

### **Web-API**

```http
PUT https://api.aspose.cloud/v4.0/cells/protection/spreadsheet
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Anforderungsparameter:**

| Parametername      | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                                                                   |
| :----------------- | :----- | :--------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet        | Datei  | FormData                           | Die Excel-Tabellenkalkulationsdatei, die hochgeladen und mit einer Passwortverschlüsselung geschützt werden soll.                             |
| openPassword       | String | Query                              | Das Passwort, das zum Öffnen (Entschlüsseln) der geschützten Tabellenkalkulation erforderlich ist.                                             |
| modifyPassword     | String | Query                              | Das Passwort, das erforderlich ist, um das Bearbeiten oder Ändern des Tabellenkalkulationsinhalts zu ermöglichen.                             |
| outPath            | String | Query                              | (Optional) Gibt den Ausgabepfad an, in dem die geschützte Arbeitsmappe gespeichert wird. Falls nicht angegeben, wird die Datei in der Antwort zurückgegeben. |
| outStorageName     | String | Query                              | Der Name des Cloud-Speichers, der zum Speichern der geschützten Ausgabedatei verwendet wird.                                                  |
| region             | String | Query                              | Gibt die regionalen/kulturellen Einstellungen (z. B. Datumsformat, Zahlenformatierung) an, die während der Verarbeitung auf die Tabellenkalkulation angewendet werden. |

**Authentifizierung**  
Alle Aufrufe der API zum Schützen von Tabellenkalkulationen erfordern ein gültiges OAuth 2.0-Zugriffstoken. Geben Sie das Token im `Authorization`-Header an:

```http
Authorization: Bearer {access_token}
```

Das Token muss vom Authentifizierungsendpunkt von Aspose Cloud abgerufen werden und muss den **Cells**-Scope enthalten.

## **Antwort**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**HTTP-Statuscodes**

| Code | Bedeutung             | Beschreibung                                                           |
| ---- | --------------------- | ---------------------------------------------------------------------- |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails.       |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized          | Ungültiges oder fehlendes JWT-Token.                                   |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet die Größenbeschränkung.          |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                             |

## Wo sollte die API zum Schützen von Tabellenkalkulationen eingesetzt werden?

- **Sichere sensible Finanzdaten** – Schützen Sie Excel-Dateien mit Budgets, Rechnungen oder Lohnabrechnungsdaten durch Öffnungs- und Bearbeitungspasswörter, um unbefugten Zugriff oder Änderungen zu verhindern.
- **Vertrauliche Berichte sicher teilen** – Stellen Sie sicher, dass nur autorisierte Empfänger interne oder externe Geschäfts-, Audit- oder Compliance-Berichte anzeigen oder ändern können.
- **Dokumentensicherheit in Workflows automatisieren** – Integrieren Sie die API in Unternehmenssysteme (z. B. ERP, CRM), um generierte Tabellenkalkulationen automatisch vor dem Speichern oder Versenden per E-Mail mit einem Passwort zu schützen.
- **Nur-Lese-Zugriff erzwingen** – Ermöglichen Sie Benutzern das Anzeigen von Berichten, während Änderungen durch ein separates Bearbeitungspasswort eingeschränkt werden – ideal für Vorlagen oder abgeschlossene Datensätze.
- **Regulatorische Anforderungen erfüllen** – Unterstützen Sie die Einhaltung von GDPR, HIPAA oder SOX, indem sensible Tabellenkalkulationsdaten in Ruhe und im Transit durch automatisierten Schutz verschlüsselt werden.

## Warum sollten Sie die API zum Schützen von Tabellenkalkulationen verwenden?

- **Entwicklerfreundlich** – Aspose.Cells Cloud bietet SDK-Bibliotheken in mehreren Sprachen, die eine schnelle Entwicklung ermöglichen und umfangreiche Dokumentation bereitstellen. Im Vergleich zum Aufbau benutzerdefinierter Lösungen reduziert dies den Entwicklungsaufwand erheblich.
- **Reduziert Personalbedarf** – Automatisiert die Dokumentenkonsolidierung und -sicherheit und verringert den Bedarf an speziell dafür zuständigen Mitarbeitern.
- **Pay-per-Use** – Keine Anfangsinvestition; Sie zahlen nur für die tatsächlich genutzten API-Aufrufe.
- **Keine Wartungskosten** – Keine Server zu warten, keine Softwareupdates und keine Kompatibilitätsprobleme.
- **Beibehaltung aller ursprünglichen Excel-Formatierungen** beim Anwenden des Passwortschutzes, sodass die geschützte Arbeitsmappe genauso aussieht wie die Originaldatei.

## So verwenden Sie die API zum Schützen von Tabellenkalkulationen mit SDKs

### OpenAPI-Spezifikation

Die [OpenAPI-Spezifikation für die API zum Schützen von Tabellenkalkulationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Protection/ProtectSpreadsheet) bietet eine öffentlich zugängliche Programmierschnittstelle, um direkte REST-Interaktionen über einen Webbrowser zu ermöglichen.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webservices einfach aufzurufen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/protection/spreadsheet?openPassword=MyOpenPwd&modifyPassword=MyModifyPwd" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/workbook.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64-codiert)",
  "contentType": "MIME-Typ",
  "fileDownloadName": "optionaler Dateiname"
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwenden von Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, um die Entwicklung zu beschleunigen. Das SDK übernimmt die zugrunde liegenden Details, sodass Sie die Funktion zum Schützen von Tabellenkalkulationen mit minimalem Code implementieren können. Besuchen Sie das <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a>, um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mit verschiedenen SDKs verwendet werden:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ProtectSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ProtectSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ProtectSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ProtectSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ProtectSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ProtectSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ProtectSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ProtectSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}