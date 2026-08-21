---
title: "Excel-Bereich in Bild konvertieren – Aspose.Cells Cloud API"
description: "Konvertieren Sie einen bestimmten Bereich aus einer lokalen Excel-Datei in PNG, JPEG, SVG, TIFF oder BMP über die Aspose.Cells Cloud REST API – es ist kein vollständiger Upload der Arbeitsmappe erforderlich."
keywords: "Aspose.Cells Cloud, Bereich in Bild konvertieren, Excel API, Bildformate, PNG, JPEG, SVG, TIFF, BMP"
slug: bereich-in-bild-konvertieren
api_version: "v4.0"
date: 2026-07-30
---

Der Aufruf liest eine lokale Tabellendatei, konvertiert den angegebenen Bereich und gibt das Bild als binären Stream zurück.

## Methode zum Konvertieren eines Bereichs in ein Bild

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/image
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

## Anforderungsparameter

| Name               | Ort                               | Typ     | Erforderlich | Beschreibung                                                                                       |
|--------------------|-----------------------------------|---------|--------------|----------------------------------------------------------------------------------------------------|
| **Spreadsheet**    | Formular‑Daten (`multipart/form-data`) | Datei   | **Ja**       | Die zu verarbeitende Excel-Datei.                                                                 |
| **worksheet**      | Abfrageparameter                  | String  | **Ja**       | Name des Arbeitsblatts, das den Bereich enthält (z. B. `Tabelle1`).                              |
| **range**          | Abfrageparameter                  | String  | **Ja**       | Zellbereich zur Konvertierung, z. B. `A1:C10`.                                                    |
| **format**         | Abfrageparameter                  | String  | **Ja**       | Ausgabe-Bildformat (`png`, `jpeg`, `svg`, `tiff`, `bmp`).                                         |
| **printHeadings**  | Abfrageparameter                  | Boolean | Nein         | `true`, um Zeilen-/Spaltenüberschriften im Bild einzuschließen.                                  |
| **outPath**        | Abfrageparameter                  | String  | Nein         | Ordnerpfad für die erzeugte Datei, falls Sie diese im Cloud-Speicher speichern möchten.          |
| **outStorageName** | Abfrageparameter                  | String  | Nein         | Name des Speicherdienstes (z. B. `MeinSpeicher`).                                                 |
| **fontsLocation**  | Abfrageparameter                  | String  | Nein         | URL oder Pfad zu benutzerdefinierten Schriftarten, die während der Konvertierung verwendet werden. |
| **region**         | Abfrageparameter                  | String  | Nein         | Gebietsschema-ID (z. B. `de-DE`, `fr-FR`). Beeinflusst die Formatierung von Zahlen und Daten.    |
| **password**       | Abfrageparameter                  | String  | Nein         | Passwort für verschlüsselte Arbeitsmappen.                                                        |
| **AutoRowsFit**    | Abfrageparameter                  | Boolean | Nein         | Zeilen vor dem Rendern automatisch anpassen.                                                      |
| **AutoColumnsFit** | Abfrageparameter                  | Boolean | Nein         | Spalten vor dem Rendern automatisch anpassen.                                                     |

## Antwort

Die API gibt die konvertierte HTML-Datei als **binären Stream** (`application/octet-stream`) zurück.

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

### Beispiel für eine erfolgreiche Antwort (HTTP)

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="bericht.png"
Content-Length: 8423
```

Speichern Sie den Antworttext in einer Datei (z. B. `bericht.png`), um das gerenderte Bild in einem Browser anzuzeigen.

---

**HTTP-Statuscodes**

| Code | Bedeutung             | Beschreibung                                                     |
|------|-----------------------|------------------------------------------------------------------|
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails. |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized          | Ungültiges oder fehlendes JWT-Token.                            |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet die Größeinschränkung.     |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                      |

## Wie verwendet man die „Bereich in Bild konvertieren“-API mit SDKs?

### OpenAPI-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToImage) beschreibt eine öffentlich zugängliche API, die REST-basierte Interaktionen direkt aus einem Webbrowser ermöglicht.

Sie können das cURL-Befehlszeilentool nutzen, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/image?format=png&worksheet=Tabelle1&range=A1:C10&AutoRowsFit=true&AutoColumnsFit=true" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Bericht.xlsx" \
     -F "outPath=output/bericht.png"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="bericht.png"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

## Aspose.Cells Cloud SDKs verwenden

Die Verwendung eines SDK ist der schnellste Weg zur Entwicklung, da sie die Details auf niedriger Ebene abstrahieren und es Ihnen ermöglichen, einen Datenbereich mit minimalem Code in eine Bilddatei zu konvertieren.  
Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie in unserem [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Sie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufrufen. Falls das Laden aus Gist blockiert ist, können Sie die Beispiele direkt aus dem Repository herunterladen.

---