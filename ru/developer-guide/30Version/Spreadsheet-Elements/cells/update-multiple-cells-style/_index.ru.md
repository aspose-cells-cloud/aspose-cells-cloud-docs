---
title: "Обновление стиля нескольких ячеек – Справочник по API Aspose.Cells Cloud (v3.0)"
type: docs
url: /ru/update-multiple-cells-style/
weight: 20
keywords: ["Aspose.Cells", "обновление стиля нескольких ячеек", "API стилей ячеек Excel", "облачный SDK", "REST API", "пример cURL", "JSON-запрос", "аутентификация JWT"]
description: "Узнайте, как обновить стиль диапазона ячеек в книге Excel с помощью REST API Aspose.Cells Cloud v3.0. Включает endpoint, HTTP-метод, параметры, примеры cURL и SDK, аутентификацию, обработку ошибок и информацию о версии."
ArticleTitle: "Обновление стиля нескольких ячеек – Справочник по API Aspose.Cells Cloud (v3.0)"
---

## REST API

Этот REST API устанавливает **стиль** для диапазона ячеек в книге Excel.

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/style
```

## Безопасность и аутентификация

API Aspose.Cells Cloud защищены и требуют [аутентификации по токену JWT](https://docs.aspose.cloud/total/ru/getting-started/rest-api-overview/authenticating-api-requests/).


### Параметры запроса

| Имя параметра | Тип   | Местоположение | Описание |
|---------------|--------|----------------|----------|
| **name**      | string | path           | Имя книги. |
| **sheetName** | string | path           | Имя листа. |
| **range**     | string | query          | Диапазон ячеек (например, `A1:A10`). |
| **style**     | object | body           | JSON-объект, определяющий стиль, который нужно применить. |
| **folder**    | string | query          | Папка, содержащая книгу. |
| **storageName**| string | query         | Имя хранилища. |

#### Объект style
JSON-объект `style` представляет форматирование ячеек. Он может содержать любые из следующих необязательных свойств:

- **Font** – настройки шрифта (`Name`, `Size`, `IsBold`, `IsItalic`, `Color` и др.).  
- **BackgroundColor** – цвет фона в формате ARGB.  
- **ForegroundColor** – цвет переднего плана в формате ARGB.  
- **Name**, **CultureCustom**, **Custom** – дополнительные метаданные стиля.

## **Ответ**

Возвращает CellCloudResponse.

- **Обзор полей ответа**

| Поле              | Тип    | Описание                                           |
| ----------------- | ------ | -------------------------------------------------- |
| `Status`          | string |                                                    |
| `Code`            | integer| 200, 400, 401, 500, ...                            |


```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP-коды состояния**

| Код | Значение                    | Описание                                         |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK                          | Фильтр успешно применён; ответ содержит детали операции. |
| 400 | Bad Request                 | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized                | Некорректный или отсутствующий JWT-токен. |
| 413 | Payload Too Large           | Размер загружаемого файла превышает предельно допустимый. |
| 500 | Internal Server Error       | Непредвиденная ошибка сервера. |

## Как использовать API PostUpdateWorksheetRangeStyle с SDK

### Спецификация API PostUpdateWorksheetRangeStyle

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostUpdateWorksheetRangeStyle) предоставляет полную схему.

Для простого доступа к веб-сервисам Aspose.Cells Cloud вы можете использовать утилиту командной строки cURL. Пример ниже демонстрирует, как выполнять вызовы в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
cURL -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/style?range=a1%3Aa10" \
  -X POST \
  -d '{
        "Font": {
          "Color": { "A":255, "R":255, "G":255, "B":0 },
          "Size": 22,
          "IsBold": true,
          "IsItalic": true,
          "IsStrikeout": true,
          "IsSubscript": true,
          "IsSuperscript": true,
          "Name": "Arial"
        },
        "Name": "string",
        "CultureCustom": "string",
        "Custom": "string",
        "BackgroundColor": { "A":10, "R":10, "G":10, "B":10 },
        "ForegroundColor": { "A":255, "R":255, "G":255, "B":0 }
      }' \
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

Использование SDK — лучший способ ускорить разработку. SDK берёт на себя обработку низкоуровневых деталей, позволяя вам сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен на [GitHub-репозитории](https://github.com/aspose-cells-cloud).

Примеры кода ниже демонстрируют вызов веб-сервисов Aspose.Cells Cloud с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeStyle.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeStyle.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeStyle.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeStyle.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeStyle.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeStyle.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeStyle.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeStyle.go" >}}

{{< /tab >}}

{{< /tabs >}}