---
title: "Добавление фильтра по цвету в лист Excel"
second_title: "Документ"
linktitle: "Добавление фильтра по цвету"
type: docs
url: /ru/autofilter/add-color-filter/
aliases: [  /ru/filter-a-list-using-a-color-filter/ , /ru/autofilter/add-a-color-filter/ ]
keywords: "Excel, фильтр по цвету, Aspose.Cells Cloud, REST API, автофильтр, JWT-аутентификация"
description: "Узнайте, как применить фильтр по цвету к листу Excel с помощью API Aspose.Cells Cloud. Включает конечную точку, параметры, пример cURL, обработку ошибок и примеры SDK."
weight: 65
ArticleTitle: "Добавление фильтра по цвету в лист Excel с использованием Aspose.Cells Cloud API"
---

Узнайте, как добавить фильтр по цвету к листу Excel с помощью API Aspose.Cells Cloud. В этом руководстве описаны необходимая конечная точка, параметры, требования к аутентификации, пример запроса cURL, примеры SDK и обработка ответов.

Этот REST API добавляет **фильтр по цвету** к листу Excel.

## PutWorksheetColorFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/colorFilter
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### Параметры запроса:


| Имя параметра | Тип    | Расположение | Описание                                                                 |
|---------------|--------|-------------|-----------------------------------------------------------------------------|
| name          | string | path        | Имя файла Excel.                                                 |
| sheetName     | string | path        | Имя листа, содержащего данные, подлежащие фильтрации.           |
| range         | string | query       | Диапазон ячеек, к которому применяется фильтр (например, `A1:B10`).            |
| fieldIndex    | integer | query       | Индекс столбца (начиная с нуля), к которому применяется цветовой фильтр.       |
| colorFilter   | object | body        | JSON-объект, определяющий передний и задний цвета для фильтрации.   |
| matchBlanks   | boolean | query       | Следует ли включать строки с пустыми ячейками в результаты фильтрации.   |
| refresh       | boolean | query       | Если `true`, лист обновляется после применения фильтра.           |
| folder        | string | query       | Папка в хранилище, где расположен файл Excel.                      |
| storageName   | string | query       | Имя сервиса хранилища (например, Aspose Cloud Storage).              |

**Схема JSON для `colorFilter`**

| Свойство          | Тип    | Описание                                                                    | Обязательное |
|-------------------|--------|--------------------------------------------------------------------------------|----------|
| Pattern           | string | Шаблон фильтра (например, `"Solid"`).                                             | Да      |
| ForegroundColor   | object | Определяет передний цвет. Содержит подсвойства, такие как `Color`, `ColorIndex`, `IsShapeColor`, `ThemeColor` и `Type`. | Нет |
| BackgroundColor   | object | Определяет задний цвет. Те же подсвойства, что и у `ForegroundColor`.      | Нет |

### **Ответ**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Коды HTTP-статуса**

| Код | Значение                     | Описание                                      |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK                          | Фильтр успешно применён; ответ содержит детали операции. |
| 400 | Bad Request                 | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized                | Недействительный или отсутствующий JWT-токен. |
| 413 | Payload Too Large           | Загруженный файл превышает предельный размер. |
| 500 | Internal Server Error       | Непредвиденная ошибка сервера. |

## Как использовать API PutWorksheetColorFilter с SDK

### Спецификация API PutWorksheetColorFilter

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetColorFilter) определяет публично доступное программное интерфейсное определение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как делать вызовы в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/colorFilter?range=A1%3AB1&fieldIndex=0" \
-X PUT \
-d "{ \"Pattern\": \"Solid\", \"ForegroundColor\": { \"Color\": { \"A\": 255, \"R\": 0, \"G\": 255, \"B\": 255 }, \"ColorIndex\": 0, \"IsShapeColor\": true, \"ThemeColor\": { \"ColorType\": \"Text2\", \"Tint\": 1 }, \"Type\": \"Automatic\" }, \"BackgroundColor\": { \"Color\": { \"A\": 255, \"R\": 0, \"G\": 255, \"B\": 255 }, \"ColorIndex\": 0, \"IsShapeColor\": true, \"ThemeColor\": { \"ColorType\": \"Text2\", \"Tint\": 0 }, \"Type\": \"Automatic\" }}" \
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

Использование SDK — лучший способ ускорить разработку. SDK скрывает низкоуровневые детали, позволяя сосредоточиться на задачах вашего проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetColorFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetColorFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetColorFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetColorFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetColorFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetColorFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetColorFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetColorFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

**См. также:** [Добавление пользовательского фильтра](https://docs.aspose.cloud/cells/autofilter/add-custom-filter/), [Добавление фильтра по дате](https://docs.aspose.cloud/cells/autofilter/add-date-filter/), [Удаление автофильтра](https://docs.aspose.cloud/cells/autofilter/remove-auto-filter/).
---