---
title: "Aspose.Cells Cloud Web API – Textdatei mit KI-gestützter Sprachumwandlung übersetzen"
secondtitle: "Dokument"
ArtikelTitel: "So übersetzen Sie Textdateien mit der Aspose.Cells Cloud KI-Übersetzungs-API"
linktitle: "Textdatei übersetzen"
type: docs
url: /de/translate-text-file/
keywords: "Aspose.Cells, Cloud API, KI-Übersetzung, Textdatei übersetzen, mehrsprachige Umwandlung, REST PUT, ZielSprachCode, Datei-Upload-Übersetzung, RohText-Übersetzung, Tabellenkalkulation KI"
description: "Erfahren Sie, wie Sie den Aspose.Cells Cloud AI TranslateTextFile-Endpunkt verwenden, um Textdateien in jede unterstützte Sprache zu übersetzen. Unterstützt sowohl den Upload von Dateien über multipart/form-data als auch die Übergabe von RohText im Anforderungstext. Beibehaltung der Formatierung und Rückgabe einer herunterladbaren übersetzten Datei."
weight: 100
---

Der **TranslateTextFile**-Endpunkt nutzt die KI-Dienste von Aspose.Cells Cloud, um den Inhalt einer Textdatei in eine angegebene Zielsprache zu übersetzen. Er unterstützt zwei Betriebsmodi: (1) **Datei-Upload-Modus** – senden Sie eine Textdatei über multipart/form-data und erhalten eine übersetzte Datei zurück; (2) **Direkter Inhalt-Modus** – senden Sie RohText im Anforderungstext und erhalten den übersetzten Text direkt zurück. Der Dienst bewahrt die ursprünglichen Zeilenumbrüche und die Formatierung bei, fügt automatisch den Suffix „_translated“ an den Dateinamen an und gibt das Ergebnis als herunterladbaren Stream zurück. Ideal für die Massenübersetzung von Dokumenten, die Integration in mehrsprachige Arbeitsabläufe oder die Echtzeitübersetzung von benutzergenerierten Inhalten.

## **Translate Text File API**

### Web-API

```http
PUT https://api.aspose.cloud/v4.0/cells/ai/translate/text-file
```

### **Anforderungsparameter:**

| Parametername     | Typ    | Speicherort | Erforderlich / Optional | Beschreibung                                                                                                                                                                                                 |
| :---------------- | :----- | :---------- | :---------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet       | Datei  | Erforderlich | FormData                | Die zu übersetzende Quell-Textdatei. Muss eine reine Textdatei (.txt) oder ein unterstütztes Tabellenkalkulationsformat sein. Beispiel: Hochladen von `dokument.txt` über das FormData-Feld mit dem Namen „file“. |
| targetLanguage    | String | Erforderlich | Query                   | ISO-639-1-Sprachcode der gewünschten Ausgabesprache (z. B. „es“ für Spanisch, „fr“ für Französisch, „de“ für Deutsch). Der Code ist case-insensitiv.                                                       |
| region            | String | Optional    | Query                   | Regionenkennung für die Tabellenkalkulation, die lokalspezifische Formatierungen wie Daten, Zahlen und Währungen beeinflusst. Übliche Werte: „US“, „EU“, „CN“. Falls nicht angegeben, wird die ursprüngliche Regions-Einstellung der Arbeitsmappe verwendet. |
| password          | String | Optional    | Query                   | Passwort zur Entschlüsselung verschlüsselter Tabellenkalkulationsdateien. Für reine Textdateien nicht erforderlich.                                                                                         |

### **Antwort**

Erfolgreiche Antwort (200 OK)
Header:
Content-Type: application/octet-stream // Binärstrom der übersetzten Datei  
Content-Disposition: attachment; filename="<originaler_name>\_translated.txt"  
Content-Length: <Größe in Bytes>

Body: Binärstrom mit dem übersetzten Text, wobei die ursprünglichen Zeilenumbrüche und die Formatierung beibehalten werden.

**HTTP-Statuscodes**

| Code | Bedeutung             | Beschreibung                                                      |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Operationsdetails. |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized          | Ungültiger oder fehlender JWT-Token.                              |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet die Größeinschränkung.       |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                        |

## Wofür sollte man die Translate Text File API verwenden?

- **Mehrsprachige Dokumentationsportale** – Übersetzen Sie Benutzerhandbücher oder Hilfedateien automatisch, die als Textdokumente hochgeladen wurden, und liefern Sie lokalisierte Versionen nach Bedarf aus.
- **Content-Management-Systeme (CMS)** – Integrieren Sie die API in einen CMS-Arbeitsablauf, um Blogposts oder Artikel vor der Veröffentlichung an internationale Zielgruppen zu übersetzen.
- **Unternehmensdatenpipelines** – Verwenden Sie sie in Batch-Jobs zur Verarbeitung großer Mengen an CSV- oder TXT-Berichten, um sie in die Sprache regionaler Niederlassungen zu übersetzen, ohne die ursprüngliche Formatierung zu beeinträchtigen.
- **Kundensupport-Plattformen** – Übersetzen Sie eingehende Texttickets oder Chat-Protokolle in Echtzeit, um Supportmitarbeiter in verschiedenen Sprachen zu unterstützen.

## Warum sollten Sie die Translate Text File API verwenden?

- **KI-gesteuerte Genauigkeit** – Nutzt modernste neuronale Übersetzungsmodelle für natürliche, kontextbewusste Ergebnisse.
- **Doppelte Eingabeflexibilität** – Akzeptiert sowohl Datei-Uploads als auch RohText-Inhalte, was die Integration in vielfältige Clientanwendungen vereinfacht.
- **Beibehaltung des ursprünglichen Layouts** – Behält Zeilenumbrüche, Einzüge und Sonderzeichen bei, sodass keine Nachbearbeitung nötig ist.
- **Nahtlose Dateiverarbeitung** – Liefert eine sofort herunterladbare Datei mit einem automatisch generierten Suffix „_translated“ und reduziert so den Aufwand für Client-Code.

## Wie man die Translate Text File API mit SDKs verwendet

### API-Spezifikation der Translate Text File API

Die [Translate Text File API-Spezifikation](https://reference.aspose.cloud/cells/#/AIController/TranslateTextFile) bietet eine öffentlich zugängliche Programmierschnittstelle, um REST-Interaktionen direkt aus einem Webbrowser auszuführen.

## Excel-API-SDK

### Verwenden der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung, da dabei die Detailtiefe der Low-Level-Implementierung abstrahiert wird und Sie so mit wenig Code eine Tabellenkalkulation in eine andere zusammenführen können.
Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).
Die folgenden Codebeispiele zeigen, wie Sie mit verschiedenen SDKs mit den Aspose.Cells-Webdiensten interagieren:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v4.0_TranslateTextFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v4.0_TranslateTextFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v4.0_TranslateTextFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v4.0_TranslateTextFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v4.0_TranslateTextFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v4.0_TranslateTextFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v4.0_TranslateTextFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v4.0_TranslateTextFile.go" >}}
{{</tab>}}
{{< /tabs >}}