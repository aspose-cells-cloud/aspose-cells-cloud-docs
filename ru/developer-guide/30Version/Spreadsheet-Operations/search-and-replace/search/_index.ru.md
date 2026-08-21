---
title: "Поиск текста в файлах Excel — Aspose.Cells Cloud API"
description: "Ищите конкретный текст в файлах Excel (XLS, XLSX, XLSM, XLSB) и ODS с помощью Aspose.Cells Cloud API. Включает детали запроса, примеры cURL и SDK, а также обработку ошибок."
keywords: "Aspose.Cells, Excel, поиск, API, REST"
type: docs
url: /ru/cells/search/
aliases:
  - /search/
  - /search-without-using-storage/
  - /search-without-storage/
weight: 50
---

# Поиск текста в файлах Excel — Aspose.Cells Cloud API

## Обзор
Aspose.Cells Cloud предоставляет **POST**-эндпоинт для поиска заданной строки текста внутри файлов рабочих книг Excel (XLS, XLSX, XLSM, XLSB) и электронных таблиц OpenDocument (ODS). API возвращает все ячейки, содержащие запрошенный текст, вместе со ссылкой на лист, где было найдено совпадение.

> **Сценарии использования**  
> - Проверка наличия конкретного значения в отчёте перед дальнейшей обработкой.  
> - Создание быстрого инструмента «поиск и замена», который сначала выводит все вхождения.  
> - Генерация индекса ключевых терминов по пакету электронных таблиц.

---

## Предварительные требования
| Требование | Подробности |
|------------|-------------|
| **Аутентификация** | JWT-токен, полученный через OAuth-процесс Aspose Cloud. Токен должен включать область **Cells**. |
| **Поддерживаемые форматы** | XLS, XLSX, XLSM, XLSB, ODS |
| **Максимальный размер файла** | 150 МБ (в сжатом виде). Файлы большего размера вызывают ошибку **413 Payload Too Large**. |
| **Обязательные заголовки** | `Authorization: Bearer <jwt-token>`  <br> `Accept: application/json` |
| **Права доступа** | Токен должен иметь разрешение на *чтение* в целевом хранилище (если используется удалённое хранилище) — не требуется, если файл загружается как `multipart/form-data`. |

*Совет:* Используйте эндпоинт **/connect/token** для генерации JWT-токена. Подробности см. в [Руководстве по аутентификации](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

---

## Эндпоинт

| Параметр | Значение |
|----------|----------|
| **HTTP-метод** | `POST` |
| **URL** | `https://api.aspose.cloud/v3.0/cells/search` |
| **Назначение** | Поиск заданного текста в загруженной рабочей книге Excel. |
| **Безопасность** | JWT-токен (Bearer) — см. *Предварительные требования* выше. |

---

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

## Параметры запроса

| Имя | Тип | Местоположение | Обязательный | Описание |
|-----|-----|----------------|-------------|----------|
| `file` | **file** | `formData` (multipart) | **Да** | Файл электронной таблицы для загрузки. |
| `text` | **string** | Строка запроса | **Да** | Строка текста для поиска. |
| `password` | **string** | Строка запроса | Нет | Пароль для открытия защищённой рабочей книги, если требуется. |
| `sheetname` | **string** | Строка запроса | Нет | Имя листа, в котором ограничить поиск. Если опущено, поиск выполняется по всем листам. |
| `checkExcelRestriction` | **boolean** | Строка запроса | Нет (по умолчанию: `true`) | Если `true`, API проверяет ограничения, специфичные для Excel (например, ячейки только для чтения), перед поиском. |

---

## Пример запроса (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/search?text=Invoice&sheetname=Sheet1" \
  -X POST \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>" \
  -F "file=@InvoiceReport.xlsx"
```

*Замените `<jwt-token>` на действительный токен и при необходимости скорректируйте параметры запроса.*

---

## Успешный ответ

**HTTP 200 — поиск выполнен успешно; ответ содержит найденные элементы текста.**

```json
{
  "Status": "OK",
  "Code": 200,
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "Text": "Invoice #12345",
        "link": {
          "Href": "InvoiceReport.xlsx/worksheets/Sheet1",
          "Rel": "parent",
          "Title": "Sheet1",
          "Type": "string"
        }
      },
      {
        "Text": "Invoice #12346",
        "link": {
          "Href": "InvoiceReport.xlsx/worksheets/Sheet1",
          "Rel": "parent",
          "Title": "Sheet1",
          "Type": "string"
        }
      }
    ]
  }
}
```

### Поля ответа

| Поле | Тип | Описание |
|------|-----|----------|
| `Status` | string | Общий статус запроса (`OK` при успехе). |
| `Code` | integer | HTTP-код статуса (200). |
| `TextItems.link` | object | Гиперссылка на ресурс коллекции. |
| `TextItems.TextItemList` | array | Список совпадений. Каждый элемент содержит: |
| `Text` | string | Значение ячейки, совпавшее с искомым текстом. |
| `link` | object | Гиперссылка на лист, где найдено совпадение (`Href` указывает на `Workbook/worksheets/SheetName`). |

---

## Ответы об ошибках

| HTTP-код | Значение | Типичная причина | Пример тела ответа |
|----------|----------|------------------|---------------------|
| **400** | Неверный запрос | Отсутствуют обязательные параметры, неподдерживаемый тип файла или недопустимые значения параметров запроса. | `{ "Status":"Error","Code":400,"Message":"Параметр запроса 'text' обязателен." }` |
| **401** | Неавторизовано | Отсутствует или недействителен JWT-токен. | `{ "Status":"Error","Code":401,"Message":"Недействительный или просроченный токен доступа." }` |
| **413** | Загруженные данные слишком большие | Загруженный файл превышает лимит в 150 МБ. | `{ "Status":"Error","Code":413,"Message":"Размер файла превышает допустимый предел." }` |
| **500** | Внутренняя ошибка сервера | Непредвиденная проблема на стороне сервера. | `{ "Status":"Error","Code":500,"Message":"Произошла непредвиденная ошибка." }` |

---

## Примеры SDK

Ниже приведены минимальные фрагменты кода для операции **PostSearch** с использованием официальных SDK Aspose.Cells Cloud. Замените `YOUR_JWT_TOKEN` и путь к файлу на свои значения.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;
using System.IO;

class Program
{
    static void Main()
    {
        var config = new Configuration
        {
            AccessToken = "YOUR_JWT_TOKEN",
            BaseUrl = "https://api.aspose.cloud"
        };
        var cellsApi = new CellsApi(config);

        using var stream = File.OpenRead("InvoiceReport.xlsx");
        var result = cellsApi.PostSearch(
            file: stream,
            text: "Invoice",
            sheetname: "Sheet1",
            password: null,
            checkExcelRestriction: true
        );

        foreach (var item in result.TextItems.TextItemList)
        {
            Console.WriteLine($"{item.Text}  ->  {item.Link.Href}");
        }
    }
}
```

### Java

```java
import com.aspose.cells.cloud.sdk.api.CellsApi;
import com.aspose.cells.cloud.sdk.model.*;
import java.io.File;

public class PostSearchDemo {
    public static void main(String[] args) throws Exception {
        CellsApi api = new CellsApi("YOUR_JWT_TOKEN");
        File file = new File("InvoiceReport.xlsx");

        TextItemsResponse response = api.postSearch(
                file,
                "Invoice",
                null,          // password
                "Sheet1",      // sheetname
                true           // checkExcelRestriction
        );

        response.getTextItems().getTextItemList()
                .forEach(item -> System.out.println(item.getText() + " -> " + item.getLink().getHref()));
    }
}
```

### Python

```python
import asposecellscloudsdk
from asposecellscloudsdk import CellsApi, ApiException, Configuration
from asposecellscloudsdk.models import TextItemsResponse
import pathlib

config = Configuration()
config.access_token = "YOUR_JWT_TOKEN"
config.host = "https://api.aspose.cloud"

api_instance = CellsApi(configuration=config)

file_path = pathlib.Path("InvoiceReport.xlsx")
with open(file_path, "rb") as f:
    result: TextItemsResponse = api_instance.post_search(
        file=f,
        text="Invoice",
        password=None,
        sheetname="Sheet1",
        check_excel_restriction=True
    )

for item in result.text_items.text_item_list:
    print(f"{item.text} -> {item.link.href}")
```

### Node.js (TypeScript)

```typescript
import { CellsApi, Configuration } from "@asposecells-cloud/sdk";

const config = new Configuration({
    accessToken: "YOUR_JWT_TOKEN",
    basePath: "https://api.aspose.cloud"
});

const api = new CellsApi(config);

api.postSearch({
    file: fs.createReadStream("InvoiceReport.xlsx"),
    text: "Invoice",
    sheetname: "Sheet1",
    checkExcelRestriction: true
}).then(response => {
    response.textItems?.textItemList?.forEach(item => {
        console.log(`${item.text} -> ${item.link?.href}`);
    });
}).catch(err => console.error(err));
```

*(SDK для PHP, Ruby, Go и Perl доступны в [репозитории Aspose.Cells Cloud на GitHub](https://github.com/aspose-cells-cloud).)*

---

## Дополнительные примечания

- **`checkExcelRestriction`** по умолчанию равен `true`. Установите значение `false` только в случае, если вы уверены, что рабочая книга не содержит защищённых ячеек, которые могут мешать поиску.
- API возвращает **гиперссылки** (`Href`), которые можно использовать с другими эндпоинтами Aspose.Cells Cloud (например, для скачивания листа или получения форматирования ячейки).
- При поиске в больших рабочих книгах рекомендуется сузить область поиска с помощью параметра `sheetname`, чтобы улучшить время отклика.

---

## См. также

- **Руководство по аутентификации** – <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>
- **OpenAPI-спецификация для PostSearch** – <https://apireference.aspose.cloud/cells/#/LightCells/PostSearch>
- **SDK Aspose.Cells Cloud** – <https://github.com/aspose-cells-cloud>
- **Ограничения скорости и квоты** – <https://docs.aspose.cloud/total/getting-started/limits/>

---