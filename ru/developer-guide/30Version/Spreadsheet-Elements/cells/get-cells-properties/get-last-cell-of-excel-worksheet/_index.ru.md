---
title: "Получение последней ячейки листа Excel — Aspose.Cells Cloud API (v4.0)"
type: docs
url: /ru/get-last-cell-of-excel-worksheet/
weight: 30
keywords: "Aspose.Cells, Excel API, получить последнюю ячейку, электронная таблица, облачные технологии"
description: "Получите адрес последней использованной ячейки листа Excel с помощью облачного REST API Aspose.Cells Cloud v4.0. Включает подробности запроса, пример cURL, JSON-ответ и примеры SDK."
ArticleTitle: "Получение последней ячейки листа Excel — Aspose.Cells Cloud API v4.0"
---

Этот REST API возвращает **последнюю ячейку** листа Excel, когда параметр `cellOrMethodName` установлен в значение `endcell`.

**Обзор**  
Операция **Get Last Cell** («Получить последнюю ячейку») возвращает адрес последней использованной ячейки в указанном листе. Это полезно для определения фактического диапазона данных на листе без необходимости просмотра всей книги.

- **Пример на cURL.**

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/endcell" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Cell": {
    "Name": "F341",
    "Row": 340,
    "Column": 5,
    "Value": "<More Info>",
    "Type": "IsString",
    "Formula": "=HYPERLINK(SUBSTITUTE(HelpURLTemplate,\"xxxxxxxxxx\",[Help Topic]),\"<More Info>\")",
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "IsStyleSet": false,
    "HtmlString": "<Font Style=\"TEXT-DECORATION: underline;FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">&lt;More Info&gt;</Font>",
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Параметры
| Параметр             | Тип    | Обязательный | Описание |
|----------------------|--------|--------------|----------|
| `fileName`           | string | Да           | Имя файла Excel, хранящегося в облаке. |
| `worksheetName`      | string | Да           | Имя листа, из которого требуется получить последнюю ячейку. |
| `cellOrMethodName`   | string | Да           | Должен быть установлен в **`endcell`**, чтобы вызвать эту операцию. |
| `folder` *(необязательно)* | string | Нет    | Путь к папке в облаке, где находится рабочая книга. |
| `storageName` *(необязательно)* | string | Нет | Имя хранилища. Если не указано, используется хранилище по умолчанию. |

**Коды HTTP-статусов**

| Код  | Значение                    | Описание                                         |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK (ОК)                     | Фильтр успешно применён; ответ содержит детали операции. |
| 400  | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized (Неавторизовано) | Недействительный или отсутствующий JWT-токен. |
| 413  | Payload Too Large (Слишком большой полезный груз) | Загружаемый файл превышает лимит размера. |
| 500  | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера. |

- **Использование SDK для Aspose.Cells Cloud**

Использование SDK — оптимальный способ ускорить разработку. SDK берёт на себя обработку низкоуровневых деталей, позволяя сосредоточиться на задачах проекта. Полный список SDK для Aspose.Cells Cloud доступен в репозитории <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub</a>.

Приведённые ниже примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetLastCellWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetEndCellWorksheet-get-last-cell-excel-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetLastCell.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_last_cell.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetLastCellOfExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetLastCellWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetEndCellWorksheet-get-last-cell-excel-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

_Скоро._

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetLastCellWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3cf3e145c223fd6f6f3d9f6377092db5" >}}

{{< /tab >}}

{{< /tabs >}}

Дополнительные операции по навигации по ячейкам описаны в разделах **[Получить первую ячейку](/ru/get-first-cell-of-excel-worksheet/)** и **[Получить максимальный номер строки](/ru/get-max-row-of-worksheet/)**.