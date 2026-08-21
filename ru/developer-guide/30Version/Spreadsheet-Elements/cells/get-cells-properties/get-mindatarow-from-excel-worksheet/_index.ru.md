---
title: "Получение MinDataRow из рабочего листа Excel"
type: docs
url: /ru/get-mindatarow-from-excel-worksheet/
weight: 90
keywords: "Aspose Cells, MinDataRow, Excel API, облачный SDK"
description: "Получение индекса первой строки с данными на рабочем листе с помощью Aspose.Cells Cloud API v3.0. Включает шаблон запроса, параметры, пример cURL, пример ответа, коды состояния и фрагменты SDK."
ArticleTitle: "Получение MinDataRow из рабочего листа Excel – Aspose.Cells Cloud API"
---

Эндпоинт **Get MinDataRow** API **Aspose.Cells Cloud API v3.0** возвращает индекс первой строки, содержащей данные, в указанном рабочем листе. Для выполнения операции требуется действующий токен доступа (аутентификация Bearer) и параметр запроса `cellOrMethodName`, установленный в значение `mindatarow`.

**Версия API: 3.0**

### Пример cURL

Запрос использует HTTP-метод GET. Замените плейсхолдеры `{fileName}` и `{sheetName}` на фактические имена рабочей книги и рабочего листа.

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/mindatarow?cellOrMethodName=mindatarow" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

**Параметры запроса**

| Параметр           | Место     | Тип    | Обязательный | Описание                                             |
|--------------------|-----------|--------|-------------|------------------------------------------------------|
| `fileName`         | Путь      | string | Да          | Имя рабочей книги Excel (с расширением).            |
| `sheetName`        | Путь      | string | Да          | Имя рабочего листа внутри рабочей книги.            |
| `cellOrMethodName` | Запрос    | string | Да          | Должен быть установлен в `mindatarow` для вызова данной операции. |

**Пример ответа**

```json
{
  "MinDataRow": 5
}
```

**Коды HTTP-статусов**

| Код  | Значение                    | Описание                                                |
|------|-----------------------------|---------------------------------------------------------|
| 200  | OK                          | Фильтр применён успешно; ответ содержит детали операции. |
| 400  | Bad Request                 | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized                | Недействительный или отсутствующий JWT-токен.         |
| 413  | Payload Too Large           | Загруженный файл превышает ограничение по размеру.     |
| 500  | Internal Server Error       | Непредвиденная ошибка сервера.                         |

### Примеры SDK

Использование SDK — самый быстрый способ разработки. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на логике вашего проекта. Полный список SDK для Aspose.Cells Cloud доступен в <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener">репозитории на GitHub</a>.

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinDataRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinDataRowWorksheet-get-min-data-row.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinDataRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_data_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinDataRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinDataRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinDataRowWorksheet-get-min-data-row.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinDataRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "85f2a886ba296b8abf640c0638b4eec1" >}}

{{< /tab >}}

{{< /tabs >}}

**См. также**

- [Получение MaxDataRow](https://docs.aspose.cloud/cells/ru/get-maxdatarow-from-excel-worksheet/)
- [Получение MinColumn](https://docs.aspose.cloud/cells/ru/get-mincolumn-from-excel-worksheet/)
- [Получение MaxColumn](https://docs.aspose.cloud/cells/ru/get-maxcolumn-from-excel-worksheet/)