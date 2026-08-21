---
title: "Aspose.Cells Cloud AI – API zur Zerlegung von Benutzeraufgaben (v4.0) | SMART-Aufgabenplanung"
second_title: "Dokument"
ArticleTitle: "Wie Sie Benutzerziele mit der Aspose.Cells Cloud AI-Aufgabenzerlegungs-API in sequenzielle Aktionspläne umwandeln"
linktitle: "Benutzeraufgabe zerlegen"
type: docs
url: /de/decompose-user-task/
keywords: "Aspose.Cells AI, API zur Aufgabenzerlegung, SMART-Aufgabenplanung, Redmine-Import, Projektautomatisierung"
description: "Wandeln Sie freiformulierte Ziele mit Aspose.Cells Cloud AI in SMART-Aufgabenlisten mit Zeitschätzungen um. Erhalten Sie CSV/XLSX-Ausgaben für Redmine, Jira oder Azure DevOps mit einem einzigen PUT-Aufruf."
weight: 100
---

Der Endpunkt **DecomposeUserTask** stellt einen REST-Endpunkt bereit, der eine freie Aufgabenbeschreibung in einen detaillierten, sequenziellen Aktionsplan umwandelt, der den SMART-Kriterien entspricht. Er weist automatisch stundenbasierte Zeitschätzungen zu, formatiert die Ausgabe für den importkompatiblen Einsatz mit Redmine und erstellt Projektmilensteinknoten. Bei Angabe der rohen Aufgabenliste und optionaler Zeitschätzungen liefert die API eine sofort verwendbare Datei (CSV, XLSX usw.), die direkt in Projektmanagement-Tools importiert werden kann – dadurch wird die Aufgabenzerlegung automatisiert und manueller Aufwand reduziert.

## **API zur Zerlegung von Benutzeraufgaben**

### Web-API

```http
PUT https://api.aspose.cloud/v4.0/cells/ai/task/decompose
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter:**

| Parametername     | Typ    | Ort  | Erforderlich/Optional | Beschreibung                                                                                                                                                                                                                              |
| :---------------- | :----- | :--- | :------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| TaskDescription   | string | Body | Erforderlich         | Eine Textbeschreibung des Gesamtziels des Benutzers. Der Dienst analysiert die Beschreibung und erzeugt einzelne Aufgaben. Beispiel: „Marketingkampagne für Q3 starten, einschließlich Erstellung von Inhalten, E-Mail-Versand und Social-Media-Anzeigen.“ |

### **Antwort**

Erfolgreiche Antwort (200 OK)  
Content-Type: `application/octet-stream` (Binärdateistream)

Header:

- `Content-Disposition: attachment; filename="DecomposedTaskPlan.xlsx"`
- `Content-Length: <Größe in Bytes>`

Die gleiche Struktur wird für XLSX/ODS-Formate verwendet, wobei die Spalten im ersten Arbeitsblatt platziert werden.

**HTTP-Statuscodes**

| Code | Bedeutung               | Beschreibung                                                      |
| ---- | ----------------------- | ----------------------------------------------------------------- |
| 200  | OK                      | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails.  |
| 400  | Bad Request             | Fehlende oder ungültige Parameter (z.�B. nicht unterstützter Dateityp). |
| 401  | Unauthorized            | Ungültiges oder fehlendes JWT-Token.                             |
| 413  | Payload Too Large       | Die hochgeladene Datei überschreitet die Größenbeschränkung.     |
| 500  | Internal Server Error   | Unerwarteter Serverfehler.                                        |

**Beispiel für Fehlerantwort (400 Bad Request)**

```json
{
  "code": "InvalidParameter",
  "message": "Das Feld 'TaskDescription' ist erforderlich und darf nicht leer sein."
}
```

**Beispiel für Anforderungstext (JSON)**

```json
{
  "TaskDescription": "Entwicklung einer Web-API für die Aufgabenzerlegungsfunktion im bestehenden System."
}
```

**Beispielantwort**  
Die API gibt einen Binärstream zurück, der die generierte Datei enthält. Um die ersten Zeilen einer CSV-Antwort anzuzeigen, dekodieren Sie den Stream und zeigen Sie die Kopfzeile an, z.�B.:

```
ID,Betreff,Ressource,geschätzte Dauer,Beschreibung
1	Erfassung der Anforderungen für die Aufgabenzerlegungs-API	Business Analyst	8	Funktionale und nichtfunktionale Anforderungen, User Stories und Akzeptanzkriterien für den neuen Aufgabenzerlegungsendpoint sammeln.
2	API-Spezifikation (OpenAPI)	Business Analyst	6	Den OpenAPI-Vertrag für POST /tasks/split definieren, einschließlich Anforderungsschema, Antwortformaten, Fehlercodes und Sicherheitsanforderungen.
3	Entwurf des Zerlegungsalgorithmus und Datenmodells	Lösungsarchitekt	5	Den Kernalgorithmus entwerfen, der eine übergeordnete Aufgabe in Teilaufgaben zerlegt, und das Datenmodell (Datenbanktabellen/Entitäten) erweitern, um Hierarchie und Metadaten zu speichern.
4	Überprüfung der Architekturintegration	Lösungsarchitekt	4	Auswirkungen auf bestehende Services, Ereignisflüsse und Datenbankmigrationen analysieren; Integrationsplan erstellen.
...
```

## Wofür sollte die API zur Zerlegung von Benutzeraufgaben verwendet werden?

- **Projektstart**: Wandeln Sie eine hochgradige Projektbeschreibung in eine Redmine-kompatible Aufgabenliste mit Zeitschätzungen um, um sofortige Sprintplanung zu ermöglichen.
- **Marketingautomatisierung**: Zerlegen Sie Kampagnenziele in ausführbare Schritte, exportieren Sie diese als CSV und importieren Sie sie in Aufgabenverwaltungs-Tools für die teamübergreifende Koordination.
- **Ressourcenzuteilung**: Generieren Sie stundenbasierte Schätzungen für jede Teilaufgabe, damit Manager die Arbeitslast vor Projektbeginn auf die Teammitglieder verteilen können.
- **Milensteinverfolgung**: Automatisch Milensteinknoten erstellen, die mit Gantt-Diagramm-Tools synchronisiert werden können, sodass jede Phase ein klar definiertes Ergebnis hat.

## Warum sollten Sie die API zur Zerlegung von Benutzeraufgaben verwenden?

- **SMART-konforme Ausgabe**: Jede erzeugte Aufgabe erfüllt die Kriterien Specific (spezifisch), Measurable (messbar), Achievable (erreichbar), Relevant (relevant) und Time-bound (zeitlich begrenzt).
- **Integrierte stundenbasierte Zeitschätzung**: Entfernt den Bedarf an manuellen Berechnungen und verbessert die Genauigkeit von Prognosen.
- **Sofort importierbare Dateiformate** (CSV, XLSX usw.) erleichtern die Integration mit Redmine, Jira, Azure DevOps und anderen Projektmanagement-Plattformen.
- **Einzelner Anforderungsautomatisierung**: Ermöglicht die Aufgabenzerlegung über einen einzigen Aufruf, beschleunigt den Projektstart und minimiert manuellen Aufwand.

## Wie Sie die API zur Zerlegung von Benutzeraufgaben mit SDKs verwenden

### API-Spezifikation zur Zerlegung von Benutzeraufgaben

Die <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/AI/DecomposeUserTask" target="_blank" rel="noopener noreferrer">API-Spezifikation zur Zerlegung von Benutzeraufgaben</a> bietet eine öffentlich zugängliche Programmierschnittstelle für die Ausführung von REST-Interaktionen direkt aus einem Webbrowser.

## Excel-API-SDK

### Aspose.Cells Cloud SDKs verwenden

Die Verwendung des SDKs ist der schnellste Weg zur Entwicklung, da sie detaillierte Low-Level-Details abstrahiert und es Ihnen ermöglicht, den DecomposeUserTask-Endpunkt mit prägnantem Code aufzurufen.  
Bitte besuchen Sie das <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.  
Die folgenden Codebeispiele zeigen, wie Sie mit verschiedenen SDKs mit Aspose.Cells-Webservices interagieren:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v4.0_DecomposeUserTask.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v4.0_DecomposeUserTask.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v4.0_DecomposeUserTask.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v4.0_DecomposeUserTask.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v4.0_DecomposeUserTask.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v4.0_DecomposeUserTask.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v4.0_DecomposeUserTask.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v4.0_DecomposeUserTask.go" >}}
{{</tab>}}
{{< /tabs >}}

---