---
title: "Получить MinDataColumn – Справочник по API Aspose.Cells Cloud (v3.0)"
type: docs
url: /ru/get-mindatacolumn-from-excel-worksheet/
weight: 110
keywords: "Aspose.Cells Cloud, MinDataColumn, рабочий лист Excel, REST API, справочник по API, v3.0, столбец данных, облачный API"
description: "Получить левый столбец, содержащий данные, в рабочем листе Excel с помощью REST API Aspose.Cells Cloud (v3.0). Включает данные об аутентификации, синтаксис запроса, пример JSON-ответа, коды ошибок и фрагменты SDK."
ArticleTitle: "Получить MinDataColumn – Справочник по API Aspose.Cells Cloud (v3.0)"
---

Эндпоинт **`mindatacolumn`** возвращает индекс левого столбца, содержащего любые данные ячеек в указанном рабочем листе, отсчитываемый от нуля.  
Другими словами, он показывает, какой столбец является первым, содержащим данные.

> **Определение** – `mindatacolumn`: индекс (начинающийся с 0) первого столбца, содержащего данные в рабочем листе.

**Необходимые условия**  
- Требуется действующий токен доступа OAuth2.  
- Файл Excel должен быть загружен в облачное хранилище Aspose Cloud.

**Параметры запроса**

| Параметр                       | Тип    | Обязательный | Описание                                           |
|--------------------------------|--------|--------------|----------------------------------------------------|
| `fileName`                     | string | Да           | Имя файла Excel, хранящегося в облачном хранилище. |
| `sheetName`                    | string | Да           | Имя рабочего листа, из которого требуется получить индекс столбца. |
| `Authorization` (заголовок)    | string | Да           | Bearer-токен для аутентификации OAuth2.            |

- **Пример cURL**

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/mindatacolumn" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/mindatacolumn" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MinDataColumn": 2
}
```

{{< /tab >}}

{{< /tabs >}}

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                            |
|-----|-----------------------------|-----------------------------------------------------|
| 200 | OK (ОК)                     | Фильтр применён успешно; ответ содержит данные об операции. |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизован) | Недействительный или отсутствующий JWT-токен.     |
| 413 | Payload Too Large (Слишком большой полезный груз) | Загруженный файл превышает допустимый размер. |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера. |

---

- Используйте SDK Aspose.Cells Cloud

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на логике вашего проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Приведённые ниже примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinDataColumnWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinDataColumnWorksheet-get-min-data-column.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinDataColumn.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_data_column.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinDataColumnFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinDataColumnWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinDataColumnWorksheet-get-min-data-column.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinDataColumnWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "48105eac1e6a64ad3ae4f269c32f3a88" >}}

{{< /tab >}}

{{< /tabs >}}
---