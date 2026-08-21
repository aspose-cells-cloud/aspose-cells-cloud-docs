---
title: "Обновление свойств рабочего листа – Справочник по API Aspose.Cells Cloud (v3.0)"
second_title: "Документ"
linktitle: "Обновление"
type: docs
url: /ru/worksheets/update-properties/
aliases: [  /ru/update-excel-worksheet-properties/ ]
weight: 20
keywords:
  [
    "Aspose.Cells",
    "Excel",
    "рабочий лист",
    "обновление свойств",
    "REST API",
    "облако",
    "v3.0",
  ]
description: "Узнайте, как обновлять базовые свойства рабочего листа Excel (например, отображение нулей, видимость линейки) с помощью Aspose.Cells Cloud REST API v3.0. Примеры запросов cURL, кода SDK, параметров и обработки ошибок."
ArticleTitle: "Обновление свойств рабочего листа – Справочник по API Aspose.Cells Cloud (v3.0)"
---

Этот REST API обновляет базовые свойства рабочего листа.

## REST API

**Необходимые условия:** У вас должна быть действующая учётная запись Aspose Cloud, вы должны получить JWT-токен доступа и убедиться, что целевая рабочая книга хранится в поддерживаемом хранилище. Все запросы должны отправляться по протоколу **HTTPS**.

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### **Параметры запроса**

| Имя параметра | Тип   | Путь/Строка запроса/HTTP-тело | Описание                                                                                      |
|---------------|-------|-------------------------------|-----------------------------------------------------------------------------------------------|
| name          | string| путь                          | Имя файла рабочей книги (с расширением).                                                      |
| sheetName     | string| путь                          | Имя рабочего листа, свойства которого требуется обновить.                                     |
| sheet         | object| тело                          | JSON-объект, содержащий пары «ключ-значение» свойств рабочего листа (например, `DisplayZeros`, `IsRulerVisible`). |
| folder        | string| запрос                        | Путь к папке в хранилище, где находится рабочая книга.                                        |
| storageName   | string| запрос                        | Имя используемого хранилища.                                                                  |

Объект **sheet** отправляется в теле запроса в формате JSON. Свойства, которые можно изменить, включают, например, `DisplayZeros`, `IsRulerVisible`, `IsGridlinesVisible`, а также другие, определённые в спецификации API.

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostUpdateWorksheetProperty) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как выполнять вызовы облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1" \
-X POST \
-d '{"DisplayZeros":"true","IsRulerVisible":"true"}' \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

Типичные коды ответов:

- **200** — Успешно. Свойства рабочего листа обновлены.
- **400** — Неверный запрос (например, некорректный JSON или отсутствие обязательного параметра).
- **401** — Неавторизовано — отсутствует или недействителен JWT-токен.
- **404** — Рабочая книга или рабочий лист не найдены.
- **500** — Внутренняя ошибка сервера.

| Код | Значение |
|-----|----------|
| 200 | Успех — свойства рабочего листа обновлены. |
| 400 | Неверный запрос — некорректный JSON или отсутствие обязательного параметра. |
| 401 | Неавторизовано — отсутствует или недействителен JWT-токен. |
| 404 | Не найдено — рабочая книга или рабочий лист не существуют. |
| 500 | Внутренняя ошибка сервера. |

## Семейство облачных SDK

Использование SDK — самый быстрый способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя вам сосредоточиться на задачах проекта. Полный список облачных SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

В следующих примерах показано, как выполнять вызовы веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostUpdateWorksheetProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UpdateWorksheetProperties-update-worksheet-properties.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostUpdateWorksheetProperty-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-update_worksheet_property-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-UpdateWorksheetProperties-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-UpdateWorksheetProperties-update-worksheet-properties.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-UpdateWorksheetProperties-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "ce38cb4feb118132fada7801c7f5cd43" >}}

{{< /tab >}}

{{< /tabs >}}