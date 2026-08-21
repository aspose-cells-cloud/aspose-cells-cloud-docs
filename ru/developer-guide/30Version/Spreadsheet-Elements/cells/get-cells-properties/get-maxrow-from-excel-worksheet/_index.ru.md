---
title: "Получение MaxRow из рабочего листа Excel"
type: docs
url: /ru/get-maxrow-from-excel-worksheet/
weight: 40
ArticleTitle: "Получение максимального номера строки в рабочем листе Excel с помощью API Aspose.Cells Cloud"
keywords: "Aspose.Cells, Excel, MaxRow, REST API, облачный SDK, электронная таблица, рабочий лист, GetMaxRow"
description: "Узнайте, как получить максимальный номер строки рабочего листа в файле Excel с помощью REST API Aspose.Cells Cloud. Примеры синтаксиса запроса, схемы ответов, кода SDK и примечания по использованию."
---

Этот REST API возвращает **максимальный номер строки** в рабочем листе Excel при установке параметра `cellOrMethodName` в значение `maxrow`.

- **Пример cURL**

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/maxrow" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MaxRow": 1048576
}
```

{{< /tab >}}

{{< /tabs >}}

- **Использование облачных SDK Aspose.Cells**

Использование SDK — наиболее эффективный способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на логике вашего проекта. Полный список облачных SDK Aspose.Cells представлен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Приведённые ниже примеры кода показывают, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMaxRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMaxRowWorksheet-get-max-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMaxRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_max_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMaxRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMaxRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMaxRowWorksheet-get-max-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMaxRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "afcfd72b172e9c3e2d283a9ac059c8c7" >}}

{{< /tab >}}

{{< /tabs >}}

**Справочник по API**

| Элемент | Подробности |
|--------|-------------|
| **Метод** | `GET` |
| **Конечная точка** | `/cells/{fileName}/worksheets/{sheetName}/cells/maxrow` |
| **Параметры пути** | `fileName` — имя файла Excel (обязательный параметр) <br> `sheetName` — имя рабочего листа (обязательный параметр) |
| **Параметры запроса** | `folder` — путь к папке в хранилище (необязательный параметр) <br> `storageName` — имя хранилища (необязательный параметр) |
| **Успешный ответ** | `200 OK` <br> ```json { "MaxRow": целое число } ``` |
| **Ответы об ошибках** | `400 Bad Request` — неверные параметры <br> `401 Unauthorized` — ошибка аутентификации <br> `404 Not Found` — файл или рабочий лист не найдены |

**Необходимые условия**

- Действующий токен аутентификации Aspose Cloud.  
- Целевая рабочая книга должна быть загружена в облачное хранилище Aspose Cloud или быть доступной по открытому URL.  

**Примечания**

- Операция доступна в версии API **v3.0** и выше.  
- Возвращаемое значение `MaxRow` соответствует максимальному индексу используемой строки (нумерация с 1). Для пустого рабочего листа значение обычно равно `1`.  

Приведённые ниже примеры SDK демонстрируют вызов операции на различных языках программирования.