---
title: "So fügen Sie Zeilen zu einem Excel-Arbeitsblatt hinzu"
second_title: "Dokument"
linktitle: "Hinzufügen"
type: docs
url: /rows/add/
keywords: "Aspose.Cells, Zeilen hinzufügen, Excel-API, REST, C#, Java, Python, Node.js"
description: "Schritt-für-Schritt-Anleitung zum Hinzufügen einer einzelnen oder mehrerer Zeilen zu einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API, einschließlich Codebeispielen für C#, Java, Python und Node.js."
weight: 20
ArticleTitle: "Zeilen zu Excel-Arbeitsblatt mit Aspose.Cells Cloud API hinzufügen – Schritt-für-Schritt-Anleitung"
---

## So fügen Sie Zeilen zu einem Excel-Arbeitsblatt hinzu

Dieser Artikel erklärt, wie Sie mithilfe der Aspose.Cells Cloud REST API eine einzelne leere Zeile oder mehrere Zeilen in ein bestehendes Arbeitsblatt einfügen. Stellen Sie sicher, dass Sie über einen gültigen API-Schlüssel und das entsprechende SDK verfügen, bevor Sie beginnen.

**Voraussetzungen**  
- [ ] Aspose.Cells Cloud-Konto mit aktiver Subscription.  
- [ ] API-Schlüssel / Zugriffstoken, das aus dem Aspose Cloud-Dashboard generiert wurde.  
- [ ] Eines der unterstützten SDKs (C#, Java, Python, Node.js) installiert und konfiguriert.  

**API-Referenz**  
- **HTTP-Methode:** `POST`  
- **Endpunkt:** `https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/rows`  
- **Erforderliche Pfadparameter:**  
  - `fileName` – Name der Excel-Datei, die in der Cloud gespeichert ist.  
  - `sheetName` – Name des Arbeitsblatts, zu dem die Zeilen hinzugefügt werden sollen.  
- **Abfrageparameter:**  
  - `startrow` – Nullbasiert Index der Zeile, ab der die Einfügung beginnt.  
  - `totalRows` – Anzahl der einzufügenden Zeilen.  
  - `folder` – (Optional) Cloud-Ordnerpfad der Datei.  
  - `storage` – (Optional) Speichername, wenn ein nicht-standardmäßiger Speicher verwendet wird.  
- **Anforderungstext (JSON-Beispiel):**  

  ```json
  {
    "startrow": 5,
    "totalRows": 3
  }
  ```

  **cURL-Beispiel**

  ```bash
  curl -X POST "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/rows?startrow=5&totalRows=3&folder=MyFolder&storage=MyStorage" \
      -H "Authorization: Bearer {access_token}" \
      -H "Content-Type: application/json" \
      -d '{"startrow":5,"totalRows":3}'
  ```

- **Erfolgreiche Antwort (HTTP 200):** Gibt die aktualisierten Informationen des Arbeitsblatts zurück, einschließlich der neuen Zeilenzahl.  

  ```json
  {
    "Code": 200,
    "Status": "OK",
    "Worksheet": {
      "Name": "Sheet1",
      "RowsCount": 30
    }
  }
  ```

- **Fehlerantwortbeispiel (HTTP 400):**  

  ```json
  {
    "Code": 400,
    "Status": "Bad Request",
    "Message": "Ungültiger startrow-Parameter. Dieser muss eine nichtnegative Ganzzahl sein."
  }
  ```

- **Statuscodes:**  

  | Code | Bedeutung                              |
  |------|----------------------------------------|
  | 200  | Zeilen erfolgreich hinzugefügt         |
  | 400  | Ungültige Parameter oder fehlerhaftes JSON |
  | 401  | Authentifizierung fehlgeschlagen       |
  | 404  | Datei oder Arbeitsblatt nicht gefunden |
  | 500  | Serverfehler                           |

Nachfolgend finden Sie Kurzlinks zu den detaillierten Beispielen zum Hinzufügen von Zeilen:

- [So fügen Sie eine leere Zeile zu einem Excel-Arbeitsblatt hinzu](/cells/rows/add/row/)
- [So fügen Sie mehrere Zeilen zu einem Excel-Arbeitsblatt hinzu](/cells/rows/add/rows/)