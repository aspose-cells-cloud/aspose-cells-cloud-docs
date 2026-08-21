---
title: "Verschlüsseln, Entschlüsseln und digital Signieren von Excel-Dateien"
second_title: "Dokument"
linktitle: "Excel schützen"
type: docs
url: /de/protect/
aliases: [  /de/workbook/password/ ]
keywords: "Excel, schützen, verschlüsseln, entschlüsseln, digitale Signatur, Aspose.Cells Cloud, REST API, Passwort, Sicherheit"
description: "Erfahren Sie, wie Sie Excel-Arbeitsmappen mit der Aspose.Cells Cloud REST API schützen, verschlüsseln, entschlüsseln und digital signieren – Codebeispiele für Android, C#, Java, Python und mehr."
ArticleTitle: "Excel-Dateien mit der Aspose.Cells Cloud API verschlüsseln, entschlüsseln, digital signieren und schützen"
weight: 36
---

## **Schützen und Entsperren von Excel-Dateien**

**Was bedeutet „Schützen“ in Aspose.Cells Cloud?**  
Der Vorgang **Protect** sichert eine Excel-Arbeitsmappe durch Anwendung eines Passworts, wodurch das Öffnen, Bearbeiten oder Ändern der Dateistruktur eingeschränkt wird. Die API unterstützt außerdem das Verschlüsseln und Entschlüsseln der Arbeitsmappe sowie das Hinzufügen einer digitalen Signatur zur manipulationssicheren Verifizierung.

**API-Referenz**  

| HTTP-Methode | Endpunkt | Erforderliche Abfrage- oder Body-Parameter | Beispiel-Body-Anfrage | Typische Antworten |
|-------------|----------|-------------------------------------------|-------------------------|--------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/protect` | `fileName` (Pfad), `password` (Abfrage) | `{ "password": "MeinGeheimes123" }` | `200 OK` – Schutz angewendet, `400 Bad Request`, `401 Unauthorized`, `500 Internal Server Error` |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/unprotect` | `fileName` (Pfad), `password` (Abfrage) | Entfällt | `200 OK` – Schutz entfernt, Fehlercodes wie oben |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/encrypt` | `fileName` (Pfad), `password` (Abfrage) | Entfällt | `200 OK` – Datei verschlüsselt |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/decrypt` | `fileName` (Pfad), `password` (Abfrage) | Entfällt | `200 OK` – Datei entschlüsselt |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/sign` | `fileName` (Pfad) | `{ "certificatePath": "/certs/mycert.pfx", "certificatePassword": "certPass" }` | `200 OK` – digitale Signatur hinzugefügt |

**Codebeispiel (C#)**  
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// API-Client initialisieren
var config = new Configuration
{
    AppSid = "IHR_APP_SID",
    AppKey = "IHR_APP_KEY",
    BaseUrl = "https://api.aspose.cloud"
};
var api = new CellsApi(config);

// Arbeitsmappe schützen
var protectRequest = new PostProtectWorkbookRequest(
    name: "Sample.xlsx",
    password: "MeinGeheimes123"
);
api.PostProtectWorkbook(protectRequest);
```

**Voraussetzungen**  
- Ein aktiver Aspose.Cells Cloud-Abonnement.  
- `AppSid` und `AppKey` zur Authentifizierung.  

**Authentifizierung**  
Alle Anfragen müssen den `Authorization`-Header mit einem gültigen JWT-Token enthalten, das vom Authentifizierungsendpunkt von Aspose Cloud bezogen wurde.

**Fehlerbehandlung**  
Prüfen Sie den HTTP-Statuscode und das `Error`-Objekt, das im Antwortbody zurückgegeben wird. Häufige Fehler sind ungültiges Passwort (`400`), fehlende Datei (`404`) und Authentifizierungsfehler (`401`).

**Hinweise**  
- Derselbe Endpunkt kann zum **Verschlüsseln** oder **Entschlüsseln** verwendet werden, indem der Aktionssegment geändert wird (`/encrypt`, `/decrypt`).  
- Digitale Signaturen erfordern eine gültige Zertifikatdatei, auf die die API zugreifen kann.

- [Excel-Datei mit der Aspose.Cells Cloud API verschlüsseln](/cells/excel-file-encrypt/)
- [Excel-Datei mit der Aspose.Cells Cloud API schützen](/cells/protect-excel-file/)
- [Digitale Signatur zu einer Excel-Datei hinzufügen](/cells/excel-digital-signature/)
- [Excel-Dateien schützen – detaillierte Anleitung](/cells/protect-excel-files/)
- [Passwort für eine Excel-Datei festlegen](/cells/workbook/password/modify/)
- [Excel-Datei entschlüsseln](/cells/excel-file-decrypt/)
- [Excel-Datei entsperren](/cells/excel-file-unprotect/)
- [Excel-Dateien entsperren](/cells/unlock-excel-files/)
- [Passwort einer Excel-Datei löschen](/cells/clear-excel-files-password/)