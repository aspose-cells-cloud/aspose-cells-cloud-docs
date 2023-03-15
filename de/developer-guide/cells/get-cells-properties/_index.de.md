---
title: Holen Sie sich Cells Property
type: docs
url: /de/get-cells-properties/
weight: 130
---
Dieser REST API gibt an, wie `get a specific cell` in einer Excel-Datei erstellt wird.

## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}
 
```
 Die Anforderungsparameter sind:
 
| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Name| Schnur| Weg| Dokumentname.|
| Tabellenname| Schnur| Weg| Arbeitsblattname.|
| cellOrMethodName| Schnur| Weg| Der Zellen- oder Methodenname. (Wert des Methodennamens: firstcell, endcell, maxrow, maxdatarow, maxcolumn, maxdatacolumn, minrow, mindatarow, mincolumn, mindatacolumn und cellName.)|
| Ordner| Schnur| Anfrage| Ordner des Dokuments.|
| Speichername| Schnur| Anfrage| Speichername.|
 
 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell) definiert eine öffentlich zugängliche Programmierschnittstelle und lässt Sie REST-Interaktionen direkt von einem Webbrowser ausführen.


- **So erhalten Sie eine bestimmte Zelle**

   - [Abrufen von Zelldaten aus einem Arbeitsblatt](/cells/de/get-cell-data-from-a-worksheet/)
   - [Holen Sie sich die erste Zelle aus dem Arbeitsblatt Excel](/cells/de/get-first-cell-from-excel-worksheet/)
   - [Holen Sie sich die letzte Zelle des Arbeitsblatts Excel](/cells/de/get-last-cell-of-excel-worksheet/)
   - [Holen Sie sich MaxRow aus dem Arbeitsblatt Excel](/cells/de/get-maxrow-from-excel-worksheet/)
   - [Holen Sie sich MaxDataRow aus dem Arbeitsblatt Excel](/cells/de/get-maxdatarow-from-excel-worksheet/)
   - [Holen Sie sich MaxColumn aus dem Arbeitsblatt Excel](/cells/de/get-maxcolumn-from-excel-worksheet/)
   - [Holen Sie sich MaxDataColumn aus dem Arbeitsblatt Excel](/cells/de/get-maxdatacolumn-from-excel-worksheet/)
   - [Holen Sie sich MinRow aus dem Arbeitsblatt Excel](/cells/de/get-minrow-from-excel-worksheet/)
   - [Holen Sie sich MinDataRow aus dem Arbeitsblatt Excel](/cells/de/get-mindatarow-from-excel-worksheet/)
   - [Holen Sie sich MinColumn aus dem Arbeitsblatt Excel](/cells/de/get-mincolumn-from-excel-worksheet/)
   - [Holen Sie sich MinDataColumn aus dem Arbeitsblatt Excel](/cells/de/get-mindatacolumn-from-excel-worksheet/)
