---
title: "Получить MinColumn из рабочего листа Excel"
type: docs
url: /ru/get-mincolumn-from-excel-worksheet/
weight: 100
keywords: Excel, Aspose.Cells Cloud, REST API, Get MinColumn, Worksheet, SDK, Cloud API
description: Получить минимальный индекс столбца, содержащего данные, в рабочем листе файла Excel через REST API Aspose.Cells Cloud.
ArticleTitle: "Получить MinColumn из рабочего листа Excel — Aspose.Cells Cloud API"
---

Этот REST API возвращает минимальный индекс столбца, содержащего данные в рабочем листе Excel, когда параметр `cellOrMethodName` установлен в значение `mincolumn`.

- **Пример cURL**

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/mincolumn" \
     -H "Authorization: Bearer <YOUR_ACCESS_TOKEN>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MinColumn": 2
}
```

{{< /tab >}}

{{< /tabs >}}

**Сведения о запросе**

| Параметр | Тип | Обязательный | Описание |
|----------|-----|-------------|----------|
| `cellOrMethodName` | string | Да | Фиксированное значение `mincolumn`, указывающее операцию. |
| `folder` | string | Нет | Путь к папке, содержащей рабочую книгу (если не корневая). |
| `storageName` | string | Нет | Имя хранилища Aspose Cloud, которое следует использовать. |

**Сведения об ответе**

API возвращает объект JSON с одним свойством:

```json
{
  "MinColumn": integer   // Нулевой индекс самого левого столбца, содержащего данные.
}
```

Типичные коды HTTP-статуса:

- **200 OK** — Запрос выполнен успешно, возвращается значение `MinColumn`.  
- **401 Unauthorized** — Отсутствует или недействителен токен аутентификации.  
- **404 Not Found** — Указанная рабочая книга, рабочий лист или диапазон ячеек не существует.  
- **500 Internal Server Error** — Непредвиденная ошибка сервера.

- **Использование SDK Aspose.Cells Cloud**

Использование SDK — наиболее эффективный способ разработки. SDK абстрагирует низкоуровневые детали, позволяя сосредоточиться на логике вашего проекта. Ознакомьтесь с полным списком SDK Aspose.Cells Cloud на <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">репозитории GitHub</a>.

Следующие примеры кода демонстрируют вызов веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinColumnWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinColumnWorksheet-get-min-column-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinColumn.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_column.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinColumnFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinColumnWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinColumnWorksheet-get-min-column-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinColumnWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "108bf3803d41abd988a29cdbd39aee44" >}}

{{< /tab >}}

{{< /tabs >}}
---