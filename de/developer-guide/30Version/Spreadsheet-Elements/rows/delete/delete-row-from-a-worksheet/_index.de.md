---
title: "Eine Zeile in einem Excel-Arbeitsblatt löschen"
second_title: "Dokument"
linktitle: "Zeile"
type: docs
url: /rows/delete/row/
aliases: [/delete-row-from-a-worksheet/]
description: "Verwenden Sie den DELETE /worksheets/{sheetName}/cells/rows/{rowIndex}-Endpunkt, um eine bestimmte Zeile aus einem Excel-Arbeitsblatt über die Aspose.Cells Cloud REST API zu entfernen. Enthält cURL-Befehl, SDK-Beispiele und vollständige Parameterreferenz."
keywords: "Aspose.Cells, Zeile löschen, Excel, API, REST, Cloud, SDK"
weight: 80
ArticleTitle: "Eine Zeile in einem Excel-Arbeitsblatt löschen – Anleitung zur Aspose.Cells Cloud API"
---

Diese REST API löscht eine Zeile aus einem Excel-Arbeitsblatt.

**Voraussetzungen**  
- Ein gültiges JWT **Authorization**-Token.  
- Die Arbeitsmappe muss in einem unterstützten Aspose-Cloud-Speicher abgelegt sein (Standard- oder benutzerdefinierter Speicher).  
- Der Zielordner (sofern angegeben) muss im gewählten Speicher vorhanden sein.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **Anforderungsparameter**

| Parametername       | Typ     | Pfad / Abfrage | Erforderlich | Beschreibung                                                                                       |
| ------------------- | ------- | -------------- | ------------ | -------------------------------------------------------------------------------------------------- |
| **name**            | string  | path           | Ja           | Name der Arbeitsmappe.                                                                             |
| **sheetName**       | string  | path           | Ja           | Name des Arbeitsblatts.                                                                            |
| **rowIndex**        | integer | path           | Ja           | Nullbasierter Index der zu löschenden Zeile.                                                      |
| **startrow**        | integer | query          | Nein         | Index der ersten zu löschenden Zeile (normalerweise identisch mit `rowIndex`).                    |
| **totalRows**       | integer | query          | Nein         | Anzahl der nacheinander zu löschenden Zeilen.                                                      |
| **updateReference** | boolean | query          | Nein         | Wenn `true` (Standard), werden Formeln, benannte Bereiche und andere Verweise nach dem Löschen aktualisiert. |
| **folder**          | string  | query          | Nein         | Ordner, der die Arbeitsmappe enthält.                                                              |
| **storageName**     | string  | query          | Nein         | Name des Speicherdienstes.                                                                         |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetRow) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webservices einfach zu nutzen. Das folgende Beispiel zeigt einen vollständigen, ausführbaren Aufruf.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=1&updateReference=true" \
  -X DELETE \
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

**Mögliche HTTP-Antwortcodes**

| Code | Bedeutung                            | Beschreibung                                                                 |
|------|--------------------------------------|------------------------------------------------------------------------------|
| 200  | OK                                   | Die Zeile wurde erfolgreich gelöscht.                                        |
| 400  | Bad Request (Ungültige Anforderung) | Fehlende oder ungültige Parameter (z. B. nicht-numerischer `rowIndex`).     |
| 401  | Unauthorized (Nicht autorisiert)    | Ungültiges oder fehlendes JWT-Token.                                        |
| 404  | Not Found (Nicht gefunden)          | Die angegebene Arbeitsmappe, das Arbeitsblatt oder die Zeile ist nicht vorhanden. |
| 500  | Internal Server Error (Interner Serverfehler) | Unerwarteter Serverfehler; Details finden Sie in der Fehlerantwort.      |

**Beispiel für Fehlerantwort**

```json
{
  "Code": 400,
  "Message": "Ungültiger Zeilenindex übermittelt."
}
```

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der beste Weg, die Entwicklungszeit zu verkürzen. Ein SDK abstractiert die niedrigstufigen Details, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webservices mithilfe verschiedener SDKs durchgeführt werden:

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=1&updateReference=true" \
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

**Verwandte Vorgänge**  
- [Eine Zeile hinzufügen](/cells/rows/add/row/)  
- [Mehrere Zeilen löschen](/cells/rows/delete/rows/)  
- [Zeilendetails abrufen](/cells/rows/get/row/)  
---