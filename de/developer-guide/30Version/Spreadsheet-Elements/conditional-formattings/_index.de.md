---
title: "Arbeiten mit bedingter Formatierung in Excel"
second_title: "Dokument"
linktitle: "Bedingte Formatierung"
type: docs
url: /conditional-formattings/
aliases: [/working-with-conditional-formatting/]
keywords: "Excel, Bedingte Formatierung, Aspose.Cells Cloud, API"
description: "Die Aspose.Cells Cloud API für Excel bietet Endpunkte zum Abrufen, Hinzufügen, Ändern und Entfernen von bedingten Formatierungsregeln, sodass eine dynamische visuelle Analyse von Tabellendaten möglich ist."
weight: 100
ArticleTitle: "Arbeiten mit bedingter Formatierung in Excel – API-Leitfaden"
---

Mit der bedingten Formatierung in Excel können Sie Zellen basierend auf deren Wert mit einer bestimmten Farbe hervorheben.

Nutzen Sie die bedingte Formatierung, um Daten visuell zu erkunden und zu analysieren, kritische Probleme zu erkennen sowie Muster und Trends zu identifizieren.

Die bedingte Formatierung erleichtert das Hervorheben interessanter Zellen oder Zellbereiche, die Hervorhebung ungewöhnlicher Werte sowie die visuelle Darstellung von Daten mithilfe von Datenbalken, Farbverlaufsskalen und Symbolgruppen, die bestimmte Variationen in den Daten widerspiegeln.

Eine bedingte Formatierung ändert das Erscheinungsbild von Zellen basierend auf den von Ihnen festgelegten Bedingungen. Wenn die Bedingungen erfüllt sind (true), wird der Zellbereich formatiert; andernfalls (false) bleibt er unverändert. Es gibt viele integrierte Bedingungen, und Sie können auch eigene erstellen (einschließlich über eine Formel, die zu **TRUE** oder **FALSE** auswertet).

Die Aspose.Cells Cloud API stellt eine Reihe von Endpunkten bereit, um bedingte Formatierungsregeln programmatisch zu verwalten. Die folgenden Vorgänge sind verfügbar:

- **Bedingte Formatierungen eines Arbeitsblatts abrufen** – Ruft alle auf ein Arbeitsblatt angewendeten bedingten Formatierungsregeln ab.  
  - **Methode:** `GET`  
  - **Endpunkt:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings`  
  - **Parameter:** `fileName` (Zeichenkette, erforderlich), `sheetName` (Zeichenkette, erforderlich), optionale Abfrageparameter wie `folder`, `storageName`  
  - **Beispiel-cURL:**  
    ```bash
    curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings?folder=Docs&storageName=MyStorage" -H "Authorization: Bearer {access_token}"
    ```
- **Bedingte Formatierung abrufen** – Gibt eine spezifische bedingte Formatierungsregel anhand ihrer ID zurück.  
  - **Methode:** `GET`  
  - **Endpunkt:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}`  
  - **Parameter:** `index` (Integer, erforderlich) identifiziert die Position der Regel.  
  - **Beispiel-cURL:**  
    ```bash
    curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0" -H "Authorization: Bearer {access_token}"
    ```
- **Zellbereich für Formatbedingung hinzufügen** – Fügt einen Zellbereich hinzu, auf den die angegebene bedingte Formatierung angewendet wird.  
  - **Methode:** `POST`  
  - **Endpunkt:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}/cellarea`  
  - **Anforderungstext (JSON):** `{ "FirstRow": 1, "FirstColumn": 1, "RowCount": 5, "ColumnCount": 3 }`  
  - **Beispiel-cURL:**  
    ```bash
    curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0/cellarea" \
         -H "Authorization: Bearer {access_token}" \
         -H "Content-Type: application/json" \
         -d '{"FirstRow":1,"FirstColumn":1,"RowCount":5,"ColumnCount":3}'
    ```
- **Bedingung für Formatbedingung hinzufügen** – Definiert eine neue Bedingung (z. B. Wert, Formel) für eine bestehende Formatregel.  
  - **Methode:** `POST`  
  - **Endpunkt:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}/condition`  
  - **Anforderungstext (JSON):** `{ "Type": "CellValue", "Operator": "GreaterThan", "Formula1": "100" }`  
  - **Beispiel-cURL:**  
    ```bash
    curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0/condition" \
         -H "Authorization: Bearer {access_token}" \
         -H "Content-Type: application/json" \
         -d '{"Type":"CellValue","Operator":"GreaterThan","Formula1":"100"}'
    ```
- **Formatbedingung hinzufügen** – Erstellt eine vollständige bedingte Formatierungsregel, einschließlich Typ und Stil.  
  - **Methode:** `POST`  
  - **Endpunkt:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings`  
  - **Anforderungstext (JSON):**  
    ```json
    {
      "Priority": 0,
      "Type": "HighlightCells",
      "Style": { "ForegroundColor": "FFFF0000" },
      "Condition": { "Operator": "LessThan", "Formula1": "50" },
      "CellArea": { "FirstRow": 0, "FirstColumn": 0, "RowCount": 10, "ColumnCount": 5 }
    }
    ```  
  - **Beispiel-cURL:**  
    ```bash
    curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings" \
         -H "Authorization: Bearer {access_token}" \
         -H "Content-Type: application/json" \
         -d @condition.json
    ```
- **Alle bedingten Formatierungen löschen** – Entfernt alle bedingten Formatierungsregeln aus dem Zielarbeitsblatt.  
  - **Methode:** `DELETE`  
  - **Endpunkt:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings`  
  - **Beispiel-cURL:**  
    ```bash
    curl -X DELETE "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings" -H "Authorization: Bearer {access_token}"
    ```
- **Zellbereich aus bedingter Formatierung entfernen** – Löscht einen zuvor definierten Zellbereich aus einer bedingten Formatierungsregel.  
  - **Methode:** `DELETE`  
  - **Endpunkt:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}/cellarea`  
  - **Beispiel-cURL:**  
    ```bash
    curl -X DELETE "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0/cellarea" -H "Authorization: Bearer {access_token}"
    ```
- **Bedingte Formatierung entfernen** – Löscht eine gesamte bedingte Formatierungsregel aus dem Arbeitsblatt.  
  - **Methode:** `DELETE`  
  - **Endpunkt:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}`  
  - **Beispiel-cURL:**  
    ```bash
    curl -X DELETE "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0" -H "Authorization: Bearer {access_token}"
    ```

Diese Beispiele veranschaulichen die erforderliche HTTP-Methode, das URL-Muster, die wichtigsten Parameter und Beispielanforderungstexte für jeden Vorgang. Wenn gewünscht, können Sie das entsprechende SDK (C#, Java, Python usw.) verwenden, um sprachspezifische Codebeispiele abzurufen.