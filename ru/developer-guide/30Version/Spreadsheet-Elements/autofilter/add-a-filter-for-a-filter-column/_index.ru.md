---
title: "Добавление фильтра в лист Excel"
second_title: "Документ"
linktype: "docs"
url: /ru/autofilter/add-filter/
aliases: [  /ru/add-a-filter-for-a-filter-column/ ]
keywords: "Aspose.Cells, Cloud, Excel, AutoFilter, добавление фильтра, REST API, SDK"
description: "Узнайте, как добавить автофильтр в столбец листа Excel с помощью Aspose.Cells Cloud REST API. Включает примеры cURL, SDK и руководство по параметрам."
weight: 60
ArticleTitle: "Добавление фильтра в лист Excel с помощью Aspose.Cells Cloud"
---

**Необходимые условия:** Перед вызовом этого API необходимо получить действительный JWT-токен, убедиться, что целевая рабочая книга загружена в указанный хранилище, и иметь необходимые права доступа к файлу. Для примеров командной строки рекомендуется использовать последнюю версию cURL (7.68 или выше).

Этот REST API добавляет фильтр для определённого столбца на листе Excel.

## API PutWorksheetFilter

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filter
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### Параметры запроса

| Имя параметра | Тип    | Расположение | Описание |
|---------------|--------|-------------|----------|
| name          | string | Path        | Имя рабочей книги. |
| sheetName     | string | Path        | Имя листа. |
| range         | string | Query       | Диапазон ячеек, содержащий фильтр (например, `A1:B1`). |
| fieldIndex    | integer| Query       | Индекс столбца (начиная с нуля), к которому применяется фильтр. |
| criteria      | string | Query       | Критерий фильтрации (например, значение или выражение). |
| matchBlanks   | boolean| Query       | Установите значение `true`, чтобы включить пустые ячейки в фильтр; иначе `false`. |
| refresh       | boolean| Query       | Установите значение `true`, чтобы обновить фильтр после применения; иначе `false`. |
| folder        | string | Query       | Папка, в которой хранится исходная рабочая книга. |
| storageName   | string | Query       | Имя сервиса хранилища. |

### **Ответ**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Коды HTTP-статуса**

| Код | Значение                     | Описание                                      |
|-----|------------------------------|-----------------------------------------------|
| 200 | OK (ОК)                      | Фильтр успешно применён; ответ содержит сведения о выполнении операции. |
| 400 | Bad Request (Неверный запрос)| Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизовано)| Недействительный или отсутствующий JWT-токен. |
| 413 | Payload Too Large (Слишком большой полезный载荷)| Загруженный файл превышает ограничение по размеру. |
| 500 | Internal Server Error (Внутренняя ошибка сервера)| Непредвиденная ошибка сервера. |

## Как использовать API PutWorksheetFilter с SDK

### Спецификация API PutWorksheetFilter

<a href="https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetFilter" target="_blank" rel="noopener noreferrer">Спецификация OpenAPI</a> определяет общедоступный программный интерфейс, позволяющий выполнять REST-взаимодействия непосредственно из веб-браузера.

Для удобного доступа к веб-сервисам Aspose.Cells Cloud вы можете использовать утилиту командной строки cURL. В следующем примере показано, как вызвать API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filter?range=A1:B1&fieldIndex=0&criteria=Year" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — самый быстрый способ разработки. SDK обрабатывает низкоуровневые детали, позволяя вам сосредоточиться на проекте. Полный список SDK Aspose.Cells Cloud доступен в <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">репозитории GitHub</a>.

Приведённые ниже примеры кода демонстрируют вызов веб-сервисов Aspose.Cells Cloud с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}