---
title: "Aspose.Cells Cloud Remove Duplicate Substrings Web-API – Redundanten Text in Excel entfernen"
second_title: "Dokument"
ArticleTitle: "Excel-Duplikat-Substring-Entferner – Redundanten Text in Zellen bereinigen"
linktitle: "Redundante Substrings entfernen"
type: docs
url: /remove-duplicate-substrings/
keywords: "Aspose.Cells, redundante Substrings, Excel-API, Textbereinigung, Cloud"
description: "Entfernen Sie redundante Substrings aus Excel-Zellen über die Aspose.Cells Cloud-API, während Formatierung und Validierung erhalten bleiben."
weight: 100
---

Entfernen Sie redundante Substrings aus Excel-Zellen mit intelligenter Erkennung. Behalten Sie die ursprüngliche Formatierung bei, während redundanter Text mithilfe der Aspose.Cells-Deduplizierungs-API entfernt wird.

## **Einführung**: Unerwünschte Zeichen präzise entfernen

Die „Repeat Substring Cleaner“-API entfernt redundante Substrings innerhalb einzelner Zellen eines Excel-Bereichs, wobei die Zellformatierung, Datenvalidierung und andere Arbeitsmappenstrukturen erhalten bleiben. Sie verarbeitet jede Zelle unabhängig und behält nur den ersten Vorkommenswert jedes redundanten Substrings bei.

### **Datenquellenoptionen**

| Feld       | Typ    | Erforderlich | Beschreibung                                           |
| ---------- | ------ | ------------ | ------------------------------------------------------ |
| `workbook` | Datei  | Ja           | Excel-Arbeitsmappendatei (.xlsx, .xlsm)               |
| `range`    | String | Ja           | Zielbereich zur Verarbeitung (z. B. „A1:D100“, „Sheet1!A:D“) |

### **Trennzeichenoptionen**

| Feld                               | Typ     | Standardwert | Beschreibung                                                                                                                                            |
| ---------------------------------- | ------- | ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `delimiters`                       | String  | `"preset"`   | Optionen: `preset`, `custom`, `comma`, `semicolon`, `space`, `tab`, `line-break` oder eine benutzerdefinierte Trennzeichenfolge (mehrere Zeichen gelten als zusammengesetzt) |
| `treatConsecutiveDelimitersAsOne` | Boolean | `false`      | Reduziert benachbarte Trennzeichen zu einem einzigen Separator                                                                                         |
| `caseSensitive`                    | Boolean | `false`      | Legt fest, ob der Vergleich groß-/kleinschreibungsabhängig ist. Bei `false` wird die Groß-/Kleinschreibung bei der Duplikaterkennung ignoriert.        |

## **RemoveDuplicateSubstrings API**

### Web-API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/duplicate-substrings
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Anforderungsparameter der **RemoveDuplicateSubstrings**-API

| Parametername                   | Typ     | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                                                                                                                |
| :------------------------------ | :------ | :--------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet                     | Datei   | FormData                           | Die zu verarbeitende Tabellendatei. Unterstützte Formate sind u. a. XLSX, XLS, ODS, CSV usw.                                                                                               |
| delimiters                      | String  | Query                              | Gibt ein oder mehrere Trennzeichen an, die zur Aufteilung des Zellinhalts in Substrings für Duplikaterkennung und -entfernung verwendet werden. Mehrere Trennzeichen können angegeben werden (z. B. `",;"`). |
| treatConsecutiveDelimitersAsOne | Boolean | Query                              | Wenn auf `true` gesetzt, werden aufeinanderfolgende Trennzeichen als ein einziger Separator behandelt. Bei `false` wird jedes Trennzeichen einzeln verarbeitet.                              |
| caseSensitive                   | Boolean | Query                              | Wenn `true`, berücksichtigt die Duplikaterkennung die Groß-/Kleinschreibung (z. B. „Text“ ≠ „text“). Bei `false` wird die Groß-/Kleinschreibung bei der Duplikatsuche ignoriert.              |
| worksheet                       | String  | Query                              | _(Optional)_ Der Name des Arbeitsblatts, auf das die Entfernung redundanter Substrings angewendet werden soll. Falls weggelassen, gilt der Vorgang für das erste Arbeitsblatt.               |
| range                           | String  | Query                              | _(Optional)_ Der Zellbereich, auf den die Entfernung redundanter Substrings angewendet werden soll (z. B. `"A1:C10"`). Falls weggelassen, gilt der Vorgang für alle genutzten Zellen im angegebenen Arbeitsblatt. |
| outPath                         | String  | Query                              | _(Optional)_ Der Cloud-Speicherordnerpfad, in dem die verarbeitete Arbeitsmappe gespeichert wird. Falls weggelassen, wird die Datei im Ursprungsordner gespeichert.                         |
| outStorageName                  | String  | Query                              | Der Name des Cloud-Speichers, in dem die Ausgabedatei gespeichert wird.                                                                                                                    |
| region                          | String  | Query                              | _(Optional)_ Legt das Gebietsschema für die Textverarbeitung fest, was die Interpretation von Trennzeichen und die Groß-/Kleinschreibungsregeln für bestimmte Sprachen beeinflussen kann (z. B. `"en-US"`, `"tr-TR"`). |
| password                        | String  | Query                              | _(Optional)_ Falls die hochgeladene Tabellendatei passwortgeschützt ist, geben Sie das Passwort an, um die Datei zu öffnen und zu verarbeiten.                                              |

**Beispielanforderung (cURL)**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/remove/duplicate-substrings?delimiters=comma&caseSensitive=false" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Sample.xlsx" \
     -F "range=A1:D100"
```

### **Antwort**

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

### **Statuscodes**

| Code | Bedeutung               | Beschreibung                                                                                   |
|------|-------------------------|------------------------------------------------------------------------------------------------|
| 200  | OK                      | Die Anforderung war erfolgreich, und die verarbeitete Arbeitsmappe wird zurückgegeben.        |
| 202  | Accepted                | Die Anforderung wurde für die asynchrone Verarbeitung akzeptiert.                             |
| 400  | Bad Request             | Die Anforderung ist fehlerhaft oder enthält ungültige Parameter.                             |
| 401  | Unauthorized            | Die Authentifizierung ist fehlgeschlagen oder das Token fehlt/ist ungültig.                   |
| 404  | Not Found               | Die angegebene Arbeitsmappe oder Ressource konnte nicht gefunden werden.                      |
| 500  | Internal Server Error   | Auf der Serverseite ist ein unerwarteter Fehler aufgetreten.                                 |

## Wofür sollte die Remove Duplicate Substrings API verwendet werden?

- **Datenbereinigungs- und -standardisierungsszenarien**: Bereinigen Sie Tags wie `"VIP,Premium,VIP,Gold"` → `"VIP,Premium,Gold"`.
- **Technische und operative Daten**: Bereinigen Sie Protokolleinträge mit wiederholten Fehlercodes, entfernen Sie doppelte Behälter-/Regalbezeichnungen usw.
- **Inhalts- und Medienverwaltung**: Reduzieren Sie doppelte Skill-Tags, entfernen Sie redundante Zertifizierungseinträge.

## Warum sollten Sie die Remove Duplicate Substrings API verwenden?

- **Manuelle Aufgaben automatisieren**: Eliminieren Sie lästiges manuelles Bearbeiten und reduzieren Sie menschliche Fehler.  
- **Datenintegrität erhalten**: Zellfarben, Schriftarten, Rahmen und bedingte Formatierungen bleiben unverändert; Dropdown-Listen und Validierungsregeln werden beibehalten.  
- **Flexible Verarbeitung**: Trennzeichenunabhängig mit optionaler Kontrolle der Groß-/Kleinschreibung und Header-Schutz.  
- **Entwicklerfreundlich**: Aspose.Cells Cloud stellt SDK-Bibliotheken in verschiedenen Sprachen zur Verfügung, sodass eine schnelle Entwicklung mit umfassender Dokumentation möglich ist.  
- **Kosteneffizient**: Der Vorgang erfolgt in der Cloud, wodurch die Notwendigkeit entfällt, Zwischendateien lokal zu speichern.  

## OpenAPI-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveDuplicateSubstrings) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, um die Entwicklung zu beschleunigen. Das SDK übernimmt die zugrunde liegenden Details, sodass Sie die Redundanz von Substrings in Zellen mit minimalem Codeaufwand implementieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele veranschaulichen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RemoveCharactersWithFirstNCharacters.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RemoveCharactersWithFirstNCharacters.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RemoveCharactersWithFirstNCharacters.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RemoveCharactersWithFirstNCharacters.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RemoveCharactersWithFirstNCharacters.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RemoveCharactersWithFirstNCharacters.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RemoveCharactersWithFirstNCharacters.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RemoveCharactersWithFirstNCharacters.go" >}}
{{</tab>}}
{{< /tabs >}}
---