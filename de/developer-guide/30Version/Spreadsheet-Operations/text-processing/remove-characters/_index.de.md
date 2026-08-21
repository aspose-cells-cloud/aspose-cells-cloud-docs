---
title: "Zeichen aus Excel entfernen – Aspose.Cells Cloud API (POST /cells/removecharacters)"
second_title: "Dokument"
linktitle: "Zeichen entfernen"
type: docs
url: /excel-remove-characters/
keywords: "Zeichen entfernen, Aspose.Cells, Excel API, Textverarbeitung, Cloud"
description: "Erfahren Sie, wie Sie Zeichen, Zeichensätze oder Teilzeichenfolgen mit der Aspose.Cells Cloud API aus Excel-Arbeitsblättern entfernen. Enthält Anforderungsschema, cURL-Beispiel, SDK-Code und Fehlerbehandlung."
weight: 100
ArticleTitle: "Zeichen aus Excel entfernen – Aspose.Cells Cloud API (POST /cells/removecharacters)"
---

## Zeichen aus Excel Web-API entfernen

Ein umfassender Satz von Tools zur Bereinigung von Textinhalten in ausgewählten Zellen. Die API entfernt spezifische Zeichen, vordefinierte Zeichensätze oder Teilzeichenfolgen, um sicherzustellen, dass der Text in Arbeitsblättern standardisiert und frei von unerwünschten Symbolen ist.

**Voraussetzungen**

- Ein aktives Aspose Cloud-Konto.  
- Ein gültiges JWT-Zugriffstoken, das gemäß der Anleitung zur Authentifizierung abgerufen wurde.  
- Die Excel-Datei muss vor dem Aufruf dieses Endpunkts in den Speicher hochgeladen werden.  
- Unterstützte Dateiformate sind `.xlsx`, `.xls`, `.xlsm` und andere gängige Excel-Typen.

```http
POST https://api.aspose.cloud/v3.0/cells/removecharacters
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Funktionsbeschreibung

- **Benutzerdefinierte Zeichen entfernen** – Geben Sie alle Zeichen an, die Sie löschen möchten. Geben Sie jedes Zeichen im Feld *Benutzerdefinierte Zeichen entfernen* ein; die API löscht alle Vorkommen dieser Zeichen in den ausgewählten Zellen.  
- **Zeichensätze entfernen** – Wählen Sie aus den vordefinierten Sätzen aus:  
  - **Nicht-druckbare Zeichen** – Löscht Zeilenumbrüche und die ersten 32 nicht-druckbaren ASCII-Zeichen (0–31) sowie zusätzliche Codes (127, 129, 141, 143, 144, 157).  
  - **Textzeichen** – Entfernt alle Buchstaben.  
  - **Numerische Zeichen** – Löscht alle Ziffern.  
  - **Symbole** – Entfernt mathematische, geometrische, technische, Währungs- und buchstabenähnliche Symbole wie „?“, „1“ und „™“.  
  - **Satzzeichen** – Entfernt alle Satzzeichen.  
- **Teilzeichenfolge entfernen** – Löscht jede angegebene Teilzeichenfolge (z. B. ein Wort) aus den ausgewählten Zellen.

### Anforderungsparameter

| Parametername           | Typ   | Ort   | Beschreibung                                                                 |
| ----------------------- | ----- | ----- | ---------------------------------------------------------------------------- |
| removeCharactersOptions | Klasse | Body  | Optionen, die definieren, welche Zeichen, Zeichensätze oder Teilzeichenfolgen entfernt werden sollen. |

**Schema von `removeCharactersOptions`**

| Eigenschaft        | Typ     | Erforderlich | Beschreibung                                                                                          |
| ------------------ | ------- | ------------ | ----------------------------------------------------------------------------------------------------- |
| Range              | string  | Ja           | A1-Notation oder benannter Bereich, der die zu verarbeitenden Zellen identifiziert (z. B. `"A1:C10"`). |
| CustomCharacters   | string  | Nein         | Zeichenkette mit jedem benutzerdefinierten Zeichen, das gelöscht werden soll (z. B. `"@#$"`).         |
| CharacterSet       | string  | Nein         | Enum-Wert zur Angabe eines vordefinierten Sets (`"NonPrinting"`, `"Text"`, `"Numeric"`, `"Symbols"`, `"Punctuation"`). |
| Substring          | string  | Nein         | Die exakte Teilzeichenfolge, die entfernt werden soll (z. B. `"USD"`).                                 |
| IgnoreCase         | boolean | Nein         | Wenn `true`, erfolgt die Zeichenentfernung groß-/kleinschreibungsunabhängig.                           |

**Beispiel für JSON-Anforderungstext**

```json
{
  "Range": "A1:B20",
  "CustomCharacters": "@#$",
  "CharacterSet": "NonPrinting",
  "Substring": "USD",
  "IgnoreCase": true
}
```

**Beispiel-cURL-Anforderung**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/removecharacters" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "Range": "A1:B20",
           "CustomCharacters": "@#$",
           "CharacterSet": "NonPrinting",
           "Substring": "USD",
           "IgnoreCase": true
         }'
```

### **Antwort**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[merged filename]",
    "Filesize" : [file size],
    "FileContent" : "[Base64String]"
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                     |
|------|-----------------------------|------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                             |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet die Größenbeschränkung.     |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                       |

## Verwendung der PostRemoveCharacters API mit SDKs

### PostRemoveCharacters API-Spezifikation

Die <a href="https://reference.aspose.cloud/cells/#/TextProcessingController/PostRemoveCharacters" rel="noopener noreferrer">vollständige OpenAPI-Spezifikation für den PostRemoveCharacters-Endpunkt</a> definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK übernimmt die Details der unteren Schichten und ermöglicht es Ihnen, sich auf Ihre Projektziele zu konzentrieren. Weitere Informationen finden Sie im <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a> mit einer vollständigen Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webservices mit verschiedenen SDKs durchgeführt werden:
---