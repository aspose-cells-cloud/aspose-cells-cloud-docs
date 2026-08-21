---
title: "Spalten gruppieren – Aspise.Cells Cloud API-Dokumentation"
description: "Gruppieren Sie Arbeitsblattspalten in einer Excel-Datei mithilfe der Aspose.Cells Cloud REST-API (v3.0). Enthält Anforderungssyntax, Parameter, cURL- und SDK-Beispiele sowie Antwortdetails."
keywords: "Aspose.Cells, Spalten gruppieren, Excel-API, REST, Cloud-SDK"
weight: 60
type: docs
aliases:
  - /group-columns-in-an-excel-worksheet/
  - /group-columns-in-excel-worksheet/
---

# Spalten in einem Excel-Arbeitsblatt gruppieren

**API-Version:** v3.0  
**Vorgang:** `PostGroupWorksheetColumns` – Gruppiert Spalten in einem Arbeitsblatt.

---

## Übersicht

Diese REST-API ermöglicht das Gruppieren eines Bereichs von Spalten in einem Arbeitsblatt. Gruppierte Spalten können ein- oder ausgeblendet werden, sodass Sie einklappbare Abschnitte erstellen können, die denen in Microsoft Excel ähneln.

---

## Voraussetzungen

- Ein gültiges **JWT-Zugriffstoken**, das beim Aspose Cloud-Authentifizierungsdienst abgerufen wurde.  
- Die Arbeitsmappe muss an einem Ort gespeichert sein, der für Aspose.Cells Cloud zugänglich ist (Standardspeicher oder benutzerdefinierter Speichername).  
- Erforderliche SDK-Version (falls ein SDK verwendet wird): Die neueste Veröffentlichung, die API-Version **v3.0** unterstützt.  

---

## Authentifizierung

Alle Anforderungen erfordern eine **Bearer-Token**-Authentifizierung.

```http
Authorization: Bearer <access_token>
```

Einzelheiten zum Abrufen eines Tokens finden Sie im [JWT-Authentifizierungsleitfaden](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

---

## HTTP-Anforderung

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/group
```

| Parameter | Ort | Erforderlich | Beschreibung |
|-----------|-----|--------------|-------------|
| `name` | Pfad | Ja | Der Dateiname der Arbeitsmappe (z. B. `test.xlsx`). |
| `sheetName` | Pfad | Ja | Das Arbeitsblatt, das die zu gruppierenden Spalten enthält. |
| `firstIndex` | Abfrage | Ja | Nullbasiertes Index der ersten Spalte, die in die Gruppe einzubeziehen ist. |
| `lastIndex` | Abfrage | Ja | Nullbasiertes Index der letzten Spalte, die in die Gruppe einzubeziehen ist. |
| `hide` | Abfrage | Nein | Wenn `true`, werden die gruppierten Spalten ausgeblendet; andernfalls bleiben sie sichtbar. |
| `folder` | Abfrage | Nein | Pfad zum Ordner, der die Arbeitsmappe enthält. |
| `storageName` | Abfrage | Nein | Name des Speicherdiensts, in dem sich die Datei befindet. |

---

## Anforderungsbeispiel (cURL)

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/group?firstIndex=1&lastIndex=2&hide=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

> **Hinweis:** Die Anforderung verwendet **HTTPS**, um eine verschlüsselte Übertragung sicherzustellen.

---

## Antwort

### Erfolg (200)

| Feld | Typ | Beschreibung |
|------|-----|-------------|
| `Code` | Integer | HTTP-Statuscode (`200`). |
| `Status` | String | Textuelle Statusangabe des Vorgangs (`OK`). |

**Beispiel**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Fehler (z. B. 400 Bad Request)

| Feld | Typ | Beschreibung |
|------|-----|-------------|
| `Code` | Integer | HTTP-Statuscode (`400`, `401`, `404`, `500`, …). |
| `Status` | String | Textuelle Statusangabe (`Error`). |
| `ErrorMessage` | String | Menschlich lesbare Beschreibung des Problems. |
| `ErrorCode` | String | Programmatischer Fehlerbezeichner. |

**Beispiel – Bad Request**

```json
{
  "Code": 400,
  "Status": "Error",
  "ErrorMessage": "Ungültiger Spaltenindex.",
  "ErrorCode": "InvalidParameter"
}
```

---

## SDK-Beispiele

Die folgenden Codeausschnitte zeigen, wie der Vorgang **Group Worksheet Columns** mithilfe der unterstützten SDKs aufgerufen wird.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostGroupWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostGroupWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostGroupWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostGroupWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostGroupWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostGroupWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostGroupWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostGroupWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}

---

## Hinweise

- **Gruppierungsverhalten:** Die API erstellt eine Spaltengruppe, die in Excel erweitert oder eingeklappt werden kann. Durch Festlegen von `hide=true` wird die Gruppe sofort eingeklappt.  
- **Nullbasierte Indizierung:** Sowohl `firstIndex` als auch `lastIndex` beginnen bei **0**; die erste Spalte in einem Arbeitsblatt hat den Index 0.  
- **Speicherüberlegungen:** Wenn sich die Arbeitsmappe in einem Nicht-Standard-Speicher befindet, müssen sowohl die Abfrageparameter `folder` als auch `storageName` angegeben werden.  

---

## Siehe auch

- [Authentifizierung – JWT-Token-basiert](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [OpenAPI-Spezifikation für Group Worksheet Columns](https://apireference.aspose.cloud/cells/#/Cells/PostGroupWorksheetColumns)  
- [Aspose.Cells Cloud SDKs (GitHub)](https://github.com/aspose-cells-cloud)  
- [Zeilen in einem Excel-Arbeitsblatt gruppieren](/rows/group/)  

---

> *Abbildung:* ![Screenshot mit gruppierten Spalten in einem Excel-Arbeitsblatt](./images/group-columns.png){: .img-fluid alt="Screenshot mit gruppierten Spalten in einem Excel-Arbeitsblatt" }

*Das obige Platzhalterbild sollte durch einen echten Screenshot ersetzt werden, der das visuelle Ergebnis des Spaltengruppierens zeigt.*