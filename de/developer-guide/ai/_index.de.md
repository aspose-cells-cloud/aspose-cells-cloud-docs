---
title: "Aspose.Cells Cloud AI – Aufgabenzerlegung, Tabellenkalkulation & Textübersetzung"
second_title: "Dokument"
ArticleTitle: "Steigern Sie Ihre KI-Fähigkeiten: Lernen Sie Excel-Übersetzung, Aufgabenzerlegung und mehr kennen"
linktitle: "KI"
type: docs
url: /de/ai/
keywords: "Aspose.Cells, Cloud KI, Excel-Übersetzung, Aufgabenzerlegung, REST API"
description: "Erforschen Sie Aspose.Cells Cloud KI zur Aufgabenzerlegung sowie zur Übersetzung von Excel-Arbeitsmappen und Textdateien. Enthält REST-Endpunkte, Beispielcode und Best Practices."
weight: 20
---

Aspose.Cells Cloud KI bietet drei leistungsstarke KI-gestützte Dienste, die die Arbeit mit Excel- und Textdaten vereinfachen: **Benutzeraufgabe zerlegen**, **Tabellenkalkulation übersetzen** und **Textdatei übersetzen**. Diese APIs ermöglichen Entwicklern, komplexe Benutzerziele programmgesteuert in ausführbare Schritte zu gliedern, ganze Arbeitsmappen oder Textdateien zu übersetzen und die Ergebnisse in benutzerdefinierte Anwendungen zu integrieren. Nutzen Sie die unten aufgeführten Endpunkte, um schnell loszulegen, und beziehen Sie sich auf die detaillierten Anforderungs-/Antwortspezifikationen für jeden Dienst.

- **[Benutzeraufgabe zerlegen](https://docs.aspose.cloud/cells/decompose-user-task/)** – Wandeln Sie Benutzerziele mit Aspose.Cells Cloud KI in sequenzielle Aktionspläne um.  
  - **Anforderungsmethode:** `POST`  
  - **Endpunkt-URL:** `https://api.aspose.cloud/v4.0/cells/ai/decompose-task`  
  - **Header:** `Authorization: Bearer <access_token>`, `Content-Type: application/json`  
  - **Anforderungstext (JSON):**  
    ```json
    {
      "task": "Erstellen Sie einen quartalsweisen Verkaufsbericht mit Diagrammen und Pivot-Tabellen"
    }
    ```  
  - **Antwort:** Gibt die Arbeitsmappe zurück, die die Aufgabenliste als herunterladbare Datei enthält.  
  - **Statuscodes:** `200 OK`, `400 Bad Request`, `401 Unauthorized`, `500 Internal Server Error`  
  - **Voraussetzungen:** Ein gültiges Zugriffstoken mit dem Scope **CellsAI**.  
  - **Beispielantwort (JSON-Auszug):**  
    ```json
    {
      "fileId": "12345abcde",
      "downloadUrl": "https://api.aspose.cloud/v4.0/cells/ai/files/12345abcde"
    }
    ```  
  - **Hinweise:** Die generierte Arbeitsmappe enthält ein Arbeitsblatt mit dem Namen **TaskList**, das die geordneten Schritte enthält. Ratenbegrenzung: 100 Anfragen pro Minute.

- **[Tabellenkalkulation übersetzen](https://docs.aspose.cloud/cells/translate-spreadsheet/)** – Übersetzen Sie eine gesamte Tabellenkalkulation mit Aspose.Cells Cloud KI.  
  - **Anforderungsmethode:** `POST`  
  - **Endpunkt-URL:** `https://api.aspose.cloud/v4.0/cells/ai/translate-spreadsheet`  
  - **Header:** `Authorization: Bearer <access_token>`, `Content-Type: multipart/form-data`  
  - **Anforderungsparameter:**  
    - `file` – Die zu übersetzende Excel-Datei (binär).  
    - `targetLanguage` – ISO-Sprachcode (z. B. `fr`, `de`).  
  - **Antwort:** Gibt die übersetzte Arbeitsmappe als herunterladbare Datei zurück.  
  - **Statuscodes:** `200 OK`, `400 Bad Request`, `401 Unauthorized`, `415 Unsupported Media Type`, `500 Internal Server Error`  
  - **Voraussetzungen:** Zugriffstoken mit Scope **CellsAI** und ausreichend Speicherplatzkontingent.  
  - **Beispielantwort (JSON-Auszug):**  
    ```json
    {
      "translatedFileId": "f9d8c7b6",
      "downloadUrl": "https://api.aspose.cloud/v4.0/cells/ai/files/f9d8c7b6"
    }
    ```  
  - **Hinweise:** Alle Zellwerte, Kommentare und Blattnamen werden übersetzt. Ratenbegrenzung: 100 Anfragen pro Minute.

- **[Textdatei übersetzen](https://docs.aspose.cloud/cells/translate-text-file/)** – Übersetzen Sie eine gesamte Textdatei mit Aspose.Cells Cloud KI.  
  - **Anforderungsmethode:** `POST`  
  - **Endpunkt-URL:** `https://api.aspose.cloud/v4.0/cells/ai/translate-text`  
  - **Header:** `Authorization: Bearer <access_token>`, `Content-Type: multipart/form-data`  
  - **Anforderungsparameter:**  
    - `file` – Die zu übersetzende Textdatei (binär).  
    - `targetLanguage` – ISO-Sprachcode (z. B. `es`, `ja`).  
  - **Antwort:** Gibt die übersetzte Textdatei zurück.  
  - **Statuscodes:** `200 OK`, `400 Bad Request`, `401 Unauthorized`, `415 Unsupported Media Type`, `500 Internal Server Error`  
  - **Voraussetzungen:** Gültiges Zugriffstoken mit Scope **CellsAI**.  
  - **Beispielantwort (JSON-Auszug):**  
    ```json
    {
      "translatedFileId": "a1b2c3d4",
      "downloadUrl": "https://api.aspose.cloud/v4.0/cells/ai/files/a1b2c3d4"
    }
    ```  
  - **Hinweise:** Unterstützt UTF-8-kodierte Textdateien bis zu 5 MB. Ratenbegrenzung: 100 Anfragen pro Minute.