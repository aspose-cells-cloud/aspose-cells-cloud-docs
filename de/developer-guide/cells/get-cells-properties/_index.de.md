---
title: Holen Sie sich Cells Property
type: docs
url: /de/get-cells-properties/
weight: 130
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdwon, Cells Eigenschaften abrufen
---
Dieser REST API zeigt, wie `get a specific cell` in einer Excel-Datei verwendet wird.

## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}
 
```
 Die Anforderungsparameter sind:
 
| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Name| Schnur| Weg| Dokumentname.|
| Blattname| Schnur| Weg| Arbeitsblattname.|
| Zellen-OderMethodenname| Schnur| Weg|Der Name der Zelle oder Methode. (Wert des Methodennamens: firstcell, endcell, maxrow, maxdatarow, maxcolumn, maxdatacolumn, minrow, mindatarow, mincolumn, mindatacolumn und cellName.)|
| Ordner| Schnur| Abfrage| Ordner des Dokuments.|
| Speichername| Schnur| Abfrage| Speichername.|
 
 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen, REST-Interaktionen direkt von einem Webbrowser aus durchzuführen.


- **So erhalten Sie eine bestimmte Zelle**

   - [Abrufen von Zelldaten aus einem Arbeitsblatt](/cells/de/get-cell-data-from-a-worksheet/)
   - [Erste Zelle aus dem Arbeitsblatt Excel holen](/cells/de/get-first-cell-from-excel-worksheet/)
   - [Letzte Zelle des Arbeitsblatts Excel abrufen](/cells/de/get-last-cell-of-excel-worksheet/)
   - [Holen Sie sich MaxRow aus dem Arbeitsblatt Excel](/cells/de/get-maxrow-from-excel-worksheet/)
   - [Holen Sie sich MaxDataRow aus dem Arbeitsblatt Excel](/cells/de/get-maxdatarow-from-excel-worksheet/)
   - [Holen Sie sich MaxColumn aus dem Arbeitsblatt Excel](/cells/de/get-maxcolumn-from-excel-worksheet/)
   - [Holen Sie sich MaxDataColumn aus dem Arbeitsblatt Excel](/cells/de/get-maxdatacolumn-from-excel-worksheet/)
   - [Holen Sie sich MinRow aus dem Arbeitsblatt Excel](/cells/de/get-minrow-from-excel-worksheet/)
   - [MinDataRow aus dem Arbeitsblatt Excel abrufen](/cells/de/get-mindatarow-from-excel-worksheet/)
   - [Holen Sie sich MinColumn aus dem Arbeitsblatt Excel](/cells/de/get-mincolumn-from-excel-worksheet/)
   - [MinDataColumn aus dem Arbeitsblatt Excel abrufen](/cells/de/get-mindatacolumn-from-excel-worksheet/)
