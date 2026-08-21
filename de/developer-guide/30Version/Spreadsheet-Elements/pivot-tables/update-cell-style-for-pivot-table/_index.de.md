---
title: "Zellenstil für Pivot-Tabelle aktualisieren"
second_title: "Dokument"
linktitle: Formatierung
type: docs
url: /de/pivot-tables/format/
aliases: [  /de/update-cell-style-for-pivot-table/ ]
keywords: "Aspose.Cells Cloud, Pivot-Tabellenstil, API zum Aktualisieren des Zellenstils, REST API, Excel API, Tabellenformatierung, Cloud SDK, Zellenstil, Pivot-Tabelle"
description: "Erfahren Sie, wie Sie den Stil einer bestimmten Zelle in einer Aspose.Cells Cloud-Pivot-Tabelle über die REST API aktualisieren. Enthält Endpunkt, Parameter, Authentifizierung, cURL-Beispiel, Go SDK-Code-Snippet und SEO-optimierte Anleitung."
weight: 90
ArticleTitle: "Zellenstil für Pivot-Tabelle aktualisieren – Aspose.Cells Cloud API-Dokumentation"
---

Diese REST API aktualisiert den **Stil** einer Zelle in einer Pivot-Tabelle.

**Voraussetzungen / Authentifizierung**  
Um diesen Endpunkt aufzurufen, benötigen Sie ein gültiges Aspose Cloud JWT-Access-Token. Holen Sie sich das Token über den OAuth 2.0-Fluss, der im [Authentifizierungsleitfaden](/authentication/) beschrieben ist. Geben Sie das Token im Anforderungsheader an:

```http
Authorization: Bearer <jwt token>
```

Das JWT-Token ist für alle Aspose.Cells Cloud API-Aufrufe erforderlich.

## PostPivotTableCellStyle API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/Format
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter**

| Parametername   | Typ     | Ort      | Beschreibung                                                                                             |
| --------------- | ------- | -------- | ------------------------------------------------------------------------------------------------------- |
| name            | string  | path     | Name des Dokuments (erforderlich).                                                                      |
| sheetName       | string  | path     | Name des Arbeitsblatts (erforderlich).                                                                  |
| pivotTableIndex | integer | path     | Index der Pivot-Tabelle (erforderlich).                                                                 |
| column          | integer | query    | Nullbasierter Spaltenindex der zu formatierenden Zelle (erforderlich).                                 |
| row             | integer | query    | Nullbasierter Zeilenindex der zu formatierenden Zelle (erforderlich).                                  |
| style           | object  | body     | Style DTO (Data-Transfer-Objekt), das den neuen Zellenstil definiert.                                   |
| needReCalculate | boolean | query    | Gibt an, ob die Pivot-Tabelle nach der Formatierung neu berechnet werden soll. Der Standardwert ist **false**. |
| folder          | string  | query    | Ordner, in dem das Dokument gespeichert ist (optional).                                                |
| storageName     | string  | query    | Name des Speichers (optional).                                                                          |
| Method          | string  | N/A      | Für die Anforderung verwendete HTTP-Methode (**POST**).                                                 |

Die <a href="https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableCellStyle" target="_blank" rel="noopener noreferrer">OpenAPI-Spezifikation</a> definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das Kommandozeilentool **cURL** verwenden, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie ein Aufruf an die Cloud-API mit cURL erfolgt.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/Format?column=1&row=1" \
  -X POST \
  -d '{"Font":{"Name":"Arial","Size":10}}' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
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

**Antwort**  
Im Erfolgsfall gibt der Dienst HTTP 200 mit einem leeren Body zurück, was anzeigt, dass der Stil erfolgreich angewendet wurde. Im Fehlerfall wird eine JSON-Nutzdatenstruktur mit einem Fehlercode und einer Fehlermeldung zurückgegeben.

| HTTP-Status | Beschreibung                                            |
|------------|---------------------------------------------------------|
| 200        | Stil erfolgreich angewendet.                            |
| 400        | Ungültige Anforderung – z. B. ungültiger Spalten-/Zeilenindex. |
| 401        | Nicht autorisiert – fehlendes oder ungültiges JWT-Token.    |
| 404        | Nicht gefunden – das angegebene Dokument, Arbeitsblatt oder die Pivot-Tabelle existiert nicht. |
| 500        | Interner Serverfehler – unerwarteter Zustand.            |

Der Antwortbody ist im Erfolgsfall leer.

Weitere Informationen finden Sie in der Dokumentation zur **Get Pivot Table** API.

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die schnellste Möglichkeit zur Entwicklung. Ein SDK abstrahiert die niederleveligen Details, sodass Sie sich auf Ihre Geschäftslogik konzentrieren können. Besuchen Sie das <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-Repository</a>, um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Das folgende Codebeispiel zeigt, wie Aspose.Cells-Webdienste mithilfe des **Go** SDK aufgerufen werden:

{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "3236805d26482f06f4656b14f2d00d79" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Zellenstil für Pivot-Tabelle aktualisieren",
  "description": "Anleitung zum Aktualisieren des Stils einer bestimmten Zelle in einer Aspose.Cells Cloud-Pivot-Tabelle über die REST API.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2026-07-30",
  "keywords": "Aspose.Cells Cloud, Pivot-Tabelle, Zellenstil, REST API, Go SDK",
  "url": "https://docs.aspose.cloud/cells/pivot-tables/format/",
  "publisher": {
    "@type": "Organization",
    "name": "Aspose"
  }
}
</script>