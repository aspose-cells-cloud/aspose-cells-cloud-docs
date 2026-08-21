---
title: "Einstieg in die Aspose.Cells Cloud API – Verarbeiten von Excel-Dateien in 3 einfachen Schritten"
second_title: "Dokument"
ArticleTitle: "Aspose.Cells Cloud Einstieg"
linktype: "Einstieg"
type: docs
url: /de/getting-started/
description: "Erfahren Sie, wie Sie Excel-Dateien mithilfe der Aspose.Cells Cloud REST API in drei einfachen Schritten hochladen, konvertieren und herunterladen. Enthält cURL-Codebeispiele."
weight: 10
keywords: "Aspose.Cells Cloud, Excel API, Tabellenkalkulationskonvertierung, Excel zu PDF, Cloud-Tabellenkalkulation, Aspose.Cells Cloud API"
---

- [Übersicht](/cells/overview/)
- [Schnellstart](/cells/quickstart/)
- [Verfügbare SDKs](/cells/available-sdks/)
- [Unterstützte Plattformen](/cells/supported-platforms/)
- [Unterstützte Dateiformate](/cells/supported-file-formats/)
- [Aspose.Cells Cloud testen](/cells/evaluate-aspose-cells/)
- [Preisplan](/cells/pricing-plan/)
- [Technischer Support](/cells/technical-support/)
- [So führen Sie einen Docker-Container aus](/cells/how-to-run-docker-container/)

**Leitfaden zum Einstieg**

Bevor Sie beginnen, stellen Sie sicher, dass Sie über einen gültigen **Aspose Cloud API-Schlüssel** und einen **Speichernamen** verfügen. Diese Anmeldeinformationen sind für alle nachfolgenden API-Aufrufe erforderlich.

**Schritt 1: Excel-Datei hochladen**  
Laden Sie Ihre Quellarbeitsmappe in den Aspose Cloud-Speicher hoch.

```curl
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/{path}" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/octet-stream" \
     --data-binary @sample.xlsx
```

*Anforderungstext*: Die Datei wird als Binärstream (`application/octet‑stream`) gesendet.  
*Erforderliche Parameter*:

- `path` – Speicherpfad, unter dem die Datei gespeichert wird (z. B. `folder/sample.xlsx`).

**Schritt 2: Arbeitsmappe in PDF konvertieren**  
Senden Sie eine Konvertierungsanforderung, nachdem die Datei gespeichert wurde.

```curl
curl -X POST "https://api.aspose.cloud/v4.0/cells/{name}/saveas?format=pdf&outPath={outputPath}" \
     -H "Authorization: Bearer {access_token}"
```

*Erforderliche Parameter*:

- `name` – Name der hochgeladenen Arbeitsmappe (z. B. `sample.xlsx`).
- `format` – Zielformat (`pdf`).
- `outputPath` – Speicherpfad für die konvertierte Datei (z. B. `folder/result.pdf`).

*Beispiel für Antwortnachricht* (JSON):

```json
{
  "status": "OK",
  "outputPath": "folder/result.pdf"
}
```

**Schritt 3: Konvertiertes PDF herunterladen**  
Rufen Sie die resultierende PDF-Datei aus dem Speicher ab.

```curl
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/file/{outputPath}" \
     -H "Authorization: Bearer {access_token}" \
     -o result.pdf
```

*Erforderliche Parameter*:

- `outputPath` – Pfad der im vorherigen Schritt generierten PDF-Datei.

**Zusammenfassung der Beispielanforderung / Antwort**

| Vorgang | HTTP-Methode | Endpoint (Beispiel) | Parameter | Erfolgsstatus |
|---------|--------------|----------------------|-----------|----------------|
| Upload  | PUT          | /cells/storage/file/{path} | `path` (Speicherort) | 200 OK |
| Konvertierung | POST | /cells/{name}/saveas?format=pdf&outPath={outputPath} | `name`, `format`, `outPath` | 200 OK |
| Download | GET         | /cells/storage/file/{outputPath} | `outputPath` | 200 OK |

**Häufige Fehlercodes**

- **400 Bad Request** – Fehlende oder ungültige Parameter.  
- **401 Unauthorized** – Ungültiger oder fehlender Zugriffstoken.  
- **404 Not Found** – Die angegebene Datei oder der angegebene Pfad existiert nicht.  
- **500 Internal Server Error** – Unerwarteter Serverfehler; erneut versuchen oder Support kontaktieren.  
---