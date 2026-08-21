---
title: "Aspose.Cells Cloud API – Datei- und Ordnerverwaltung (Hochladen, Herunterladen, Kopieren, Verschieben)"
second_title: "Dokument"
ArticleTitle: "Cloud-basierte Dateiverwaltung für Excel – Eine effiziente und sichere Lösung für die Speicherung und intelligente Organisation von Excel-Dateien"
linktitle: "Dateien und Speicherung"
type: docs
url: /de/files-and-storage/
aliases: [/de/working-with-files-and-storage-using-aspose-cells-cloud/]
keywords: "Aspose.Cells Cloud, Dateispeicher-API, Excel-Datei hochladen, Excel-Datei herunterladen, Datei kopieren, Datei verschieben, Datei löschen, Ordnerverwaltung, REST-API, cURL-Beispiele"
description: "Umfassende Anleitung zur Verwaltung von Excel-Dateien und Ordnern im Aspose.Cells Cloud-Speicher. Enthält Hochladen, Herunterladen, Kopieren, Verschieben, Löschen und Ordneroperationen mit cURL-Beispielen, erforderlichen Parametern und Authentifizierungshinweisen."
weight: 100
---

Aspose.Cells Cloud stellt eine umfassende Reihe von Hilfsfunktionen für die Arbeit mit Dateien bereit, die im Aspose.Cells Cloud-Speicher oder in einer beliebigen third‑party Cloud‑Speicherlösung Ihrer Wahl gespeichert sind. Für Unterstützung bei der Einrichtung eines third‑party Speichers verweisen wir auf die [Aspose Cloud UI Hilfethemen](https://docs.aspose.cloud/display/totalcloud/Aspose+Cloud+UI+Help+Topics).

**Aspose.Cells Cloud bietet eine Reihe von APIs für Datei-, Ordner- und Speicheroperationen.**

> **Hinweis:** Alle API-Aufrufe müssen **HTTPS** verwenden. Details zum Beziehen eines JWT-Tokens finden Sie im [Authentifizierungsleitfaden](/de/authentication/).

**Voraussetzungen:** Um diese APIs nutzen zu können, benötigen Sie einen gültigen Aspose Cloud-Account, ein JWT-Zugriffstoken sowie einen konfigurierten Speicherort (entweder Aspose Cloud Storage oder ein verbundener third‑party Speicher).

**Zuletzt aktualisiert:** 2024‑12‑01

## **So laden Sie eine Datei hoch**

### API-Informationen zum Hochladen einer Datei

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

Die Anforderungsparameter sind wie folgt aufgelistet:

| Parametername | Typ   | Ort       | Beschreibung |
|---------------|-------|-----------|--------------|
| path          | string | path      | Pfad zur hochzuladenden Datei, einschließlich Dateiname und Erweiterung (z. B. `/Ordner1/Report.xlsx`). |
| file          | file   | formData  | Die hochzuladende Datei. |
| storageName   | string | query     | Name des zu verwendenden Speichers. |

**HTTP-Antworten**

| Code | Beschreibung |
|------|--------------|
| 200  | Datei erfolgreich hochgeladen. |
| 400  | Ungültige Anforderung – fehlende oder ungültige Parameter. |
| 401  | Nicht autorisiert – ungültiges oder fehlendes JWT-Token. |
| 404  | Speicher nicht gefunden. |
| 500  | Interner Serverfehler. |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/File/UploadFile) definiert eine öffentlich zugängliche Programmierschnittstelle, über die REST-Interaktionen direkt aus einem Webbrowser möglich sind.

### Beispiel zum Hochladen einer Datei

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie eine Datei mit cURL hochgeladen wird.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}
{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/MeinOrdner/Report.xlsx" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F "File=@Report.xlsx"
```

{{< /tab >}}
{{< tab tabNum="12" >}}

```json
{
  "Uploaded": [
    "MeinOrdner/Report.xlsx"
  ],
  "Errors": []
}
```

{{< /tab >}}
{{< /tabs >}}

*Hinweis: Die maximale Dateigröße für den Upload beträgt 100 MB. Rate-Limits können gelten.*

## **So laden Sie eine Datei herunter**

### API-Informationen zum Herunterladen einer Datei

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

Die Anforderungsparameter sind wie folgt aufgelistet:

| Parametername | Typ   | Ort       | Beschreibung |
|---------------|-------|-----------|--------------|
| path          | string | path      | Dateipfad (z. B. `/Ordner/Report.xlsx`). |
| storageName   | string | query     | Name des zu verwendenden Speichers. |
| versionId     | string | query     | ID der herunterzuladenden Dateiversion (optional). |

**HTTP-Antworten**

| Code | Beschreibung |
|------|--------------|
| 200  | Datei erfolgreich heruntergeladen; Binärstrom wird zurückgegeben. |
| 400  | Ungültige Anforderung – ungültige Parameter. |
| 401  | Nicht autorisiert – fehlendes oder ungültiges JWT. |
| 404  | Datei nicht gefunden. |
| 500  | Interner Serverfehler. |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/File/DownloadFile) definiert eine öffentlich zugängliche Programmierschnittstelle, über die REST-Interaktionen direkt aus einem Webbrowser möglich sind.

### Beispiel zum Herunterladen einer Datei

{{< tabs tabTotal="2" tabID="13" tabName13="Anforderung" tabName14="Antwort" >}}
{{< tab tabNum="13" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/MeinOrdner/Report.xlsx" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="14" >}}

```json
{
  "Stream": "<binäre Daten>"
}
```

{{< /tab >}}
{{< /tabs >}}

*Hinweis: Die Antwort enthält den Binärstrom der Datei. Speichern Sie die Ausgabe mit cURL (`-o filename.xlsx`) in einer Datei.*

## **So löschen Sie eine Datei**

### API-Informationen zum Löschen einer Datei

```bash
DELETE https://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

Die Anforderungsparameter sind wie folgt aufgelistet:

| Parametername | Typ   | Ort       | Beschreibung |
|---------------|-------|-----------|--------------|
| path          | string | path      | Dateipfad (z. B. `/Ordner/Report.xlsx`). |
| storageName   | string | query     | Name des zu verwendenden Speichers. |
| versionId     | string | query     | ID der zu löschenden Dateiversion (optional). |

**HTTP-Antworten**

| Code | Beschreibung |
|------|--------------|
| 200  | Datei erfolgreich gelöscht. |
| 400  | Ungültige Anforderung – fehlende oder ungültige Parameter. |
| 401  | Nicht autorisiert – ungültiges JWT-Token. |
| 404  | Datei nicht gefunden. |
| 500  | Interner Serverfehler. |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/File/DeleteFile) definiert eine öffentlich zugängliche Programmierschnittstelle, über die REST-Interaktionen direkt aus einem Webbrowser möglich sind.

### Beispiel zum Löschen einer Datei

{{< tabs tabTotal="2" tabID="15" tabName15="Anforderung" tabName16="Antwort" >}}
{{< tab tabNum="15" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/MeinOrdner/OldReport.xlsx" \
  -X DELETE \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="16" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*Hinweis: Das Löschen einer Datei ist dauerhaft; stellen Sie sicher, dass Sie bei Bedarf ein Backup besitzen.*

## **So kopieren Sie eine Datei**

### API-Informationen zum Kopieren einer Datei

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/file/copy/{srcPath}
```

Die Anforderungsparameter sind wie folgt aufgelistet:

| Parametername     | Typ   | Ort       | Beschreibung |
|-------------------|-------|-----------|--------------|
| srcPath           | string | path      | Quellpfad der Datei (z. B. `/Ordner/Quelle.xlsx`). |
| destPath          | string | query     | Ziel Pfad der Datei (z. B. `/Ordner/Ziel.xlsx`). |
| srcStorageName    | string | query     | Name des Quellspeichers (optional). |
| destStorageName   | string | query     | Name des Ziel-speichers (optional). |
| versionId         | string | query     | ID der zu kopierenden Dateiversion (optional). |

**HTTP-Antworten**

| Code | Beschreibung |
|------|--------------|
| 200  | Datei erfolgreich kopiert. |
| 400  | Ungültige Anforderung – ungültige Parameter. |
| 401  | Nicht autorisiert – fehlendes oder ungültiges JWT. |
| 404  | Quelldatei nicht gefunden. |
| 500  | Interner Serverfehler. |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/File/CopyFile) definiert eine öffentlich zugängliche Programmierschnittstelle, über die REST-Interaktionen direkt aus einem Webbrowser möglich sind.

### Beispiel zum Kopieren einer Datei

{{< tabs tabTotal="2" tabID="17" tabName17="Anforderung" tabName18="Antwort" >}}
{{< tab tabNum="17" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/copy/MeinOrdner/Report.xlsx?destPath=MeinOrdner/ReportKopie.xlsx" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="18" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*Hinweis: Der Kopiervorgang entfernt die Quelldatei nicht.*

## **So verschieben Sie eine Datei**

### API-Informationen zum Verschieben einer Datei

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/file/move/{srcPath}
```

Die Anforderungsparameter sind wie folgt aufgelistet:

| Parametername     | Typ   | Ort       | Beschreibung |
|-------------------|-------|-----------|--------------|
| srcPath           | string | path      | Quellpfad der Datei (z. B. `/Ordner/Quelle.xlsx`). |
| destPath          | string | query     | Ziel-Pfad der Datei (z. B. `/Ordner/Ziel.xlsx`). |
| srcStorageName    | string | query     | Name des Quellspeichers (optional). |
| destStorageName   | string | query     | Name des Ziel-speichers (optional). |
| versionId         | string | query     | ID der zu verschiebenden Dateiversion (optional). |

**HTTP-Antworten**

| Code | Beschreibung |
|------|--------------|
| 200  | Datei erfolgreich verschoben. |
| 400  | Ungültige Anforderung – ungültige Parameter. |
| 401  | Nicht autorisiert – fehlendes oder ungültiges JWT. |
| 404  | Quelldatei nicht gefunden. |
| 500  | Interner Serverfehler. |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/File/MoveFile) definiert eine öffentlich zugängliche Programmierschnittstelle, über die REST-Interaktionen direkt aus einem Webbrowser möglich sind.

### Beispiel zum Verschieben einer Datei

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/move/MeinOrdner/Report.xlsx?destPath=MeinOrdner/ReportVerschoben.xlsx" \
  -X PUT \
  -H "accept: application/json" \
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

*Hinweis: Beim Verschieben einer Datei bleibt deren Versionsverlauf erhalten.*

## **So erstellen Sie einen Ordner**

### API-Informationen zum Erstellen eines Ordners

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

Die Anforderungsparameter sind wie folgt aufgelistet:

| Parametername | Typ   | Ort       | Beschreibung |
|---------------|-------|-----------|--------------|
| path          | string | path      | Pfad des zu erstellenden Ordners (z. B. `ordner1/ordner2/`). |
| storageName   | string | query     | Name des zu verwendenden Speichers. |

**HTTP-Antworten**

| Code | Beschreibung |
|------|--------------|
| 200  | Ordner erfolgreich erstellt. |
| 400  | Ungültige Anforderung – ungültiger Pfad oder Parameter. |
| 401  | Nicht autorisiert – fehlendes oder ungültiges JWT. |
| 500  | Interner Serverfehler. |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Folder/CreateFolder) definiert eine öffentlich zugängliche Programmierschnittstelle, über die REST-Interaktionen direkt aus einem Webbrowser möglich sind.

### Beispiel zum Erstellen eines Ordners

{{< tabs tabTotal="2" tabID="3" tabName3="Anforderung" tabName4="Antwort" >}}
{{< tab tabNum="3" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/neuerordner" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="4" >}}

```json
{
  "Uploaded": [
    "neuerordner"
  ],
  "Errors": []
}
```

{{< /tab >}}
{{< /tabs >}}

*Hinweis: Ordnerpfade unterscheiden zwischen Groß- und Kleinschreibung.*

## **So rufen Sie Dateien in einem Ordner ab**

### API-Informationen zum Abrufen von Dateien

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

Die Anforderungsparameter sind wie folgt aufgelistet:

| Parametername | Typ   | Ort       | Beschreibung |
|---------------|-------|-----------|--------------|
| path          | string | path      | Ordnerpfad (z. B. `/ordner`). |
| storageName   | string | query     | Name des zu verwendenden Speichers. |

**HTTP-Antworten**

| Code | Beschreibung |
|------|--------------|
| 200  | Liste der Dateien und Unterordner zurückgegeben. |
| 400  | Ungültige Anforderung – ungültiger Pfad. |
| 401  | Nicht autorisiert – fehlendes oder ungültiges JWT. |
| 404  | Ordner nicht gefunden. |
| 500  | Interner Serverfehler. |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Folder/GetFilesList) definiert eine öffentlich zugängliche Programmierschnittstelle, über die REST-Interaktionen direkt aus einem Webbrowser möglich sind.

### Beispiel zum Abrufen von Dateien

{{< tabs tabTotal="2" tabID="5" tabName5="Anforderung" tabName6="Antwort" >}}
{{< tab tabNum="5" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/zielordner" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="6" >}}

```json
{
  "Value": [
    {
      "Name": "Report.xlsx",
      "IsFolder": false,
      "ModifiedDate": "2021-12-08T12:38:45.739Z",
      "Size": 102400,
      "Path": "/zielordner/Report.xlsx"
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}

*Hinweis: Die Antwort listet sowohl Dateien als auch Unterordner im angegebenen Pfad auf.*

## **So löschen Sie einen Ordner**

### API-Informationen zum Löschen eines Ordners

```bash
DELETE https://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

Die Anforderungsparameter sind wie folgt aufgelistet:

| Parametername | Typ    | Ort       | Beschreibung |
|---------------|--------|-----------|--------------|
| path          | string | path      | Ordnerpfad (z. B. `/ordner`). |
| storageName   | string | query     | Name des zu verwendenden Speichers. |
| recursive     | boolean | query    | Auf `true` setzen, um den Ordner rekursiv zu löschen. |

**HTTP-Antworten**

| Code | Beschreibung |
|------|--------------|
| 200  | Ordner erfolgreich gelöscht. |
| 400  | Ungültige Anforderung – ungültige Parameter. |
| 401  | Nicht autorisiert – fehlendes oder ungültiges JWT. |
| 404  | Ordner nicht gefunden. |
| 500  | Interner Serverfehler. |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Folder/DeleteFolder) definiert eine öffentlich zugängliche Programmierschnittstelle, über die REST-Interaktionen direkt aus einem Webbrowser möglich sind.

### Beispiel zum Löschen eines Ordners

{{< tabs tabTotal="2" tabID="7" tabName7="Anforderung" tabName8="Antwort" >}}
{{< tab tabNum="7" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/zielordner" \
  -X DELETE \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="8" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*Hinweis: Das Löschen eines Ordners mit `recursive=true` entfernt dessen gesamten Inhalt dauerhaft.*

## **So kopieren Sie einen Ordner**

### API-Informationen zum Kopieren eines Ordners

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/folder/copy/{srcPath}
```

Die Anforderungsparameter sind wie folgt aufgelistet:

| Parametername     | Typ   | Ort       | Beschreibung |
|-------------------|-------|-----------|--------------|
| srcPath           | string | path      | Quellpfad des Ordners (z. B. `/quelle`). |
| destPath          | string | query     | Ziel-Pfad des Ordners (z. B. `/ziel`). |
| srcStorageName    | string | query     | Name des Quellspeichers (optional). |
| destStorageName   | string | query     | Name des Ziel-speichers (optional). |

**HTTP-Antworten**

| Code | Beschreibung |
|------|--------------|
| 200  | Ordner erfolgreich kopiert. |
| 400  | Ungültige Anforderung – ungültige Parameter. |
| 401  | Nicht autorisiert – fehlendes oder ungültiges JWT. |
| 404  | Quellordner nicht gefunden. |
| 500  | Interner Serverfehler. |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Folder/CopyFolder) definiert eine öffentlich zugängliche Programmierschnittstelle, über die REST-Interaktionen direkt aus einem Webbrowser möglich sind.

### Beispiel zum Kopieren eines Ordners

{{< tabs tabTotal="2" tabID="21" tabName21="Anforderung" tabName22="Antwort" >}}
{{< tab tabNum="21" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/copy/quellordner?destPath=zielordner" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="22" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*Hinweis: Der Kopiervorgang erstellt einen neuen Ordner mit denselben Inhalten wie der Quellordner.*

## **So verschieben Sie einen Ordner**

### API-Informationen zum Verschieben eines Ordners

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/folder/move/{srcPath}
```

Die Anforderungsparameter sind wie folgt aufgelistet:

| Parametername     | Typ   | Ort       | Beschreibung |
|-------------------|-------|-----------|--------------|
| srcPath           | string | path      | Quellpfad des Ordners (z. B. `/ordner`). |
| destPath          | string | query     | Ziel-Pfad des Ordners (z. B. `/ziel`). |
| srcStorageName    | string | query     | Name des Quellspeichers (optional). |
| destStorageName   | string | query     | Name des Ziel-speichers (optional). |

**HTTP-Antworten**

| Code | Beschreibung |
|------|--------------|
| 200  | Ordner erfolgreich verschoben. |
| 400  | Ungültige Anforderung – ungültige Parameter. |
| 401  | Nicht autorisiert – fehlendes oder ungültiges JWT. |
| 404  | Quellordner nicht gefunden. |
| 500  | Interner Serverfehler. |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Folder/MoveFolder) definiert eine öffentlich zugängliche Programmierschnittstelle, über die REST-Interaktionen direkt aus einem Webbrowser möglich sind.

### Beispiel zum Verschieben eines Ordners

{{< tabs tabTotal="2" tabID="23" tabName23="Anforderung" tabName24="Antwort" >}}
{{< tab tabNum="23" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/move/zielordner?destPath=ziel2ordner" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="24" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*Hinweis: Beim Verschieben eines Ordners bleibt dessen interne Struktur und die Dateiversionen erhalten.*

## **So prüfen Sie, ob ein Speicher vorhanden ist**

### API-Informationen zur Prüfung auf Speichervorhandensein

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/{storageName}/exist
```

Die Anforderungsparameter sind wie folgt aufgelistet:

| Parametername | Typ   | Ort       | Beschreibung |
|---------------|-------|-----------|--------------|
| storageName   | string | path      | Name des zu prüfenden Speichers. |

**HTTP-Antworten**

| Code | Beschreibung |
|------|--------------|
| 200  | Vorhandensein des Speichers zurückgegeben (`true` oder `false`). |
| 401  | Nicht autorisiert – fehlendes oder ungültiges JWT. |
| 404  | Speicher nicht gefunden. |
| 500  | Interner Serverfehler. |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Storage/StorageExists) definiert eine öffentlich zugängliche Programmierschnittstelle, über die REST-Interaktionen direkt aus einem Webbrowser möglich sind.

### Beispiel zur Prüfung auf Speichervorhandensein

{{< tabs tabTotal="2" tabID="33" tabName33="Anforderung" tabName34="Antwort" >}}
{{< tab tabNum="33" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/MeinSpeicher/exist" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="34" >}}

```json
{
  "Exists": true
}
```

{{< /tab >}}
{{< /tabs >}}

## **So prüfen Sie, ob eine Datei oder ein Ordner vorhanden ist**

### API-Informationen zur Prüfung auf Vorhandensein eines Objekts

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/exist/{path}
```

Die Anforderungsparameter sind wie folgt aufgelistet:

| Parametername | Typ   | Ort       | Beschreibung |
|---------------|-------|-----------|--------------|
| path          | string | path      | Datei- oder Ordnerpfad (z. B. `/datei.xlsx` oder `/ordner`). |
| storageName   | string | query     | Name des zu prüfenden Speichers. |
| versionId     | string | query     | ID der Dateiversion (optional). |

**HTTP-Antworten**

| Code | Beschreibung |
|------|--------------|
| 200  | Vorhandenseinsinformationen zurückgegeben. |
| 401  | Nicht autorisiert – fehlendes oder ungültiges JWT. |
| 404  | Datei oder Ordner nicht gefunden. |
| 500  | Interner Serverfehler. |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Storage/ObjectExists) definiert eine öffentlich zugängliche Programmierschnittstelle, über die REST-Interaktionen direkt aus einem Webbrowser möglich sind.

### Beispiel zur Prüfung auf Vorhandensein eines Objekts

{{< tabs tabTotal="2" tabID="37" tabName37="Anforderung" tabName38="Antwort" >}}
{{< tab tabNum="37" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/exist/Book1.xlsx" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="38" >}}

```json
{
  "Exists": true,
  "IsFolder": false
}
```

{{< /tab >}}
{{< /tabs >}}

## **So rufen Sie die Speicherauslastung ab**

### API-Informationen zur Ermittlung der Speicherauslastung

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/disc
```

Die Anforderungsparameter sind wie folgt aufgelistet:

| Parametername | Typ   | Ort       | Beschreibung |
|---------------|-------|-----------|--------------|
| storageName   | string | query     | Name des abzufragenden Speichers. |

**HTTP-Antworten**

| Code | Beschreibung |
|------|--------------|
| 200  | Informationen zur Speicherauslastung zurückgegeben. |
| 401  | Nicht autorisiert – fehlendes oder ungültiges JWT. |
| 500  | Interner Serverfehler. |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Storage/GetDiscUsage) definiert eine öffentlich zugängliche Programmierschnittstelle, über die REST-Interaktionen direkt aus einem Webbrowser möglich sind.

### Beispiel zur Ermittlung der Speicherauslastung

{{< tabs tabTotal="2" tabID="40" tabName40="Anforderung" tabName41="Antwort" >}}
{{< tab tabNum="40" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/disc?storageName=MeinSpeicher" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="41" >}}

```json
{
  "UsedSize": 12345678,
  "TotalSize": 987654321
}
```

{{< /tab >}}
{{< /tabs >}}

## **So rufen Sie Dateiversionen ab**

### API-Informationen zum Abrufen von Dateiversionen

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/version/{path}
```

Die Anforderungsparameter sind wie folgt aufgelistet:

| Parametername | Typ   | Ort       | Beschreibung |
|---------------|-------|-----------|--------------|
| path          | string | path      | Dateipfad (z. B. `/datei.xlsx`). |
| storageName   | string | query     | Name des abzufragenden Speichers. |

**HTTP-Antworten**

| Code | Beschreibung |
|------|--------------|
| 200  | Liste der Dateiversionen zurückgegeben. |
| 401  | Nicht autorisiert – fehlendes oder ungültiges JWT. |
| 404  | Datei nicht gefunden. |
| 500  | Interner Serverfehler. |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Storage/GetFileVersions) definiert eine öffentlich zugängliche Programmierschnittstelle, über die REST-Interaktionen direkt aus einem Webbrowser möglich sind.

### Beispiel zum Abrufen von Dateiversionen

{{< tabs tabTotal="2" tabID="46" tabName46="Anforderung" tabName47="Antwort" >}}
{{< tab tabNum="46" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/version/Report.xlsx?storageName=MeinSpeicher" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="47" >}}

```json
{
  "Value": [
    {
      "Name": "Report.xlsx",
      "IsFolder": false,
      "ModifiedDate": "2021-12-08T18:57:46.128Z",
      "Size": 102400,
      "Path": "/Report.xlsx",
      "VersionId": "1",
      "IsLatest": true
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}