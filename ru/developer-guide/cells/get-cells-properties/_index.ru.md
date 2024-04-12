---
title: Получите недвижимость Cells
type: docs
url: /ru/get-cells-properties/
weight: 130
---
Этот REST API показывает, как использовать `get a specific cell` в файле Excel.

## РСЕТ API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}
 
```
 Параметры запроса:
 
| Имя параметра| Тип| Путь/строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| имя| нить| путь| Название документа.|
| имя листа| нить| путь| Имя рабочего листа.|
| ячейкаорметоднаме| нить| путь|Имя ячейки или метода. (Значение имени метода: firstcell, endcell, maxrow, maxdatarow, maxcolumn, maxdatacolumn, minrow, mindatarow, mincolumn, mindatacolumn и cellName.)|
| папка| нить| запрос| Папка документа.|
| имя_хранилища| нить| запрос| имя хранилища.|
 
[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell) определяет общедоступный интерфейс программирования и позволяет выполнять взаимодействие с REST непосредственно из веб-браузера.


- **Как получить конкретную ячейку**

   - [Получить данные ячейки из рабочего листа](/cells/ru/get-cell-data-from-a-worksheet/)
   - [Получить первую ячейку из рабочего листа Excel](/cells/ru/get-first-cell-from-excel-worksheet/)
   - [Получить последнюю ячейку рабочего листа Excel](/cells/ru/get-last-cell-of-excel-worksheet/)
   - [Получите MaxRow из рабочего листа Excel.](/cells/ru/get-maxrow-from-excel-worksheet/)
   - [Получите MaxDataRow из листа Excel.](/cells/ru/get-maxdatarow-from-excel-worksheet/)
   - [Получите MaxColumn из рабочего листа Excel.](/cells/ru/get-maxcolumn-from-excel-worksheet/)
   - [Получить MaxDataColumn из листа Excel.](/cells/ru/get-maxdatacolumn-from-excel-worksheet/)
   - [Получите MinRow из рабочего листа Excel.](/cells/ru/get-minrow-from-excel-worksheet/)
   - [Получите MinDataRow из листа Excel.](/cells/ru/get-mindatarow-from-excel-worksheet/)
   - [Получить MinColumn из рабочего листа Excel](/cells/ru/get-mincolumn-from-excel-worksheet/)
   - [Получить MinDataColumn из листа Excel](/cells/ru/get-mindatacolumn-from-excel-worksheet/)
