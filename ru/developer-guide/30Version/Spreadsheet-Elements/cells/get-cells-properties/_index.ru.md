---
title: Получить Cells Недвижимость
type: docs
url: /ru/get-cells-properties/
weight: 130
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdown, Получить Cells Свойства
---
Этот REST API показывает, как сделать `get a specific cell` в файле Excel.

## РСЕT API

```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}
 
```

Параметры запроса:

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| имя| нить| путь| Название документа.|
| Имя_листа| нить| путь| Название рабочего листа.|
| cellOrMethodName| нить| путь|Имя ячейки или метода. (Значение имени метода: firstcell, endcell, maxrow, maxdatarow, maxcolumn, maxdatacolumn, minrow, mindatarow, mincolumn, mindatacolumn и cellName.)|
| папка| нить| запрос| Папка документов.|
| имя_хранилища| нить| запрос| имя хранилища.|

 The[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell) определяет общедоступный программный интерфейс и позволяет осуществлять REST-взаимодействие непосредственно из веб-браузера.

### **Семейство облачных SDK**

 Использование SDK — лучший способ ускорить разработку. SDK берёт на себя решение низкоуровневых задач и позволяет вам сосредоточиться на задачах проекта. Ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как совершать вызовы веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCell.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCell.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCell.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCell.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCell.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCell.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCell.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCell.go" >}}

{{< /tab >}}

{{< /tabs >}}

### **Как получить конкретную ячейку**

- [Получить данные ячеек из рабочего листа](/cells/ru/get-cell-data-from-a-worksheet/)
- [Получить первую ячейку из рабочего листа Excel](/cells/ru/get-first-cell-from-excel-worksheet/)
- [Получить последнюю ячейку рабочего листа Excel](/cells/ru/get-last-cell-of-excel-worksheet/)
- [Получить MaxRow из рабочего листа Excel](/cells/ru/get-maxrow-from-excel-worksheet/)
- [Получить MaxDataRow из листа Excel](/cells/ru/get-maxdatarow-from-excel-worksheet/)
- [Получить MaxColumn из рабочего листа Excel](/cells/ru/get-maxcolumn-from-excel-worksheet/)
- [Получить MaxDataColumn из листа Excel](/cells/ru/get-maxdatacolumn-from-excel-worksheet/)
- [Получить MinRow из рабочего листа Excel](/cells/ru/get-minrow-from-excel-worksheet/)
- [Получить MinDataRow из листа Excel](/cells/ru/get-mindatarow-from-excel-worksheet/)
- [Получить MinColumn из рабочего листа Excel](/cells/ru/get-mincolumn-from-excel-worksheet/)
- [Получить MinDataColumn из листа Excel](/cells/ru/get-mindatacolumn-from-excel-worksheet/)
