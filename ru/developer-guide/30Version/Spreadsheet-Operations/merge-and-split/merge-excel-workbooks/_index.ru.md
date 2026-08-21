---
title: "Объединение рабочей книги Excel в другую рабочую книгу"
second_title: "Документ"
linktitle: "Объединение рабочей книги Excel в другую рабочую книгу"
type: docs
url: /ru/merge-an-excel-file-into-the-excel-file/
aliases: [  /ru/merge-excel-workbooks/ , /ru/workbook/merge/ ]
keywords: "объединение Excel, Aspose.Cells Cloud, API рабочей книги, REST API, объединение электронных таблиц, облачный SDK, аутентификация, mergeWith, пример cURL"
description: "Пошаговое руководство по объединению одной рабочей книги Excel в другую с использованием REST API Aspose.Cells Cloud (версия 3.0). Включает аутентификацию, обязательный параметр mergeWith, пример cURL и фрагменты кода SDK."
ArticleTitle: "Объединение рабочей книги Excel в другую рабочую книгу с использованием API Aspose.Cells Cloud"
weight: 50
---

## REST API

Этот REST API объединяет **рабочую книгу** Excel в другую рабочую книгу.

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/merge
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе токена JWT</a>.


### **Параметр запроса**

| Имя параметра | Тип   | Описание                                                        |
| ------------- | ----- | --------------------------------------------------------------- |
| folder        | string| Папка, содержащая исходную рабочую книгу.                       |
| storageName   | string| Имя хранилища.                                                  |
| **mergeWith** | string| Имя рабочей книги, которая будет объединена с целевой рабочей книгой. |

### **Ответ**

```json
{
    "Status":"OK",
    "Code":200,
      "Workbook": {
    "FileName": "test.xlsx",
    "Links": [
      {
        "Href": "/test.xlsx",
        "Rel": "self",
        "Title": null,
        "Type": null
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Скачать как CSV",
        "Type": "text/csv"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Скачать как HTML",
        "Type": "text/html"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Скачать как ODS",
        "Type": "application/vnd.oasis.opendocument.spreadsheet"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Скачать как PDF",
        "Type": "application/pdf"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Скачать как текст в табличном формате с разделителями",
        "Type": "text/plain"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Скачать как TIFF",
        "Type": "image/tiff"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Скачать как Microsoft Excel 2003",
        "Type": "application/vnd.ms-excel"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Скачать как Microsoft Excel 2007",
        "Type": "application/vnd.openxmlformats-officedocument.spreadsheetml.sheet"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Скачать как XPS",
        "Type": "application/vnd.ms-xpsdocument"
      }
    ],
    "Worksheets": {
      "link": {
        "Href": "/worksheets",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "DefaultStyle": {
      "link": {
        "Href": "/defaultstyle",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "DocumentProperties": {
      "link": {
        "Href": "/documentproperties",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "Names": {
      "link": {
        "Href": "/names",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "Settings": {
      "link": {
        "Href": "/settings",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "IsWriteProtected": "False",
    "IsProtected": "False",
    "IsEncryption": "false",
    "Password": null
  }
}
```

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                                         |
|-----|-----------------------------|------------------------------------------------------------------|
| 200 | OK (OK)                     | Фильтр применён успешно; ответ содержит детали операции.        |
| 400 | Bad Request (Неверный запрос)| Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизовано)| Недействительный или отсутствующий токен JWT.                   |
| 413 | Payload Too Large (Слишком большой полезный груз)| Загруженный файл превышает лимит размера.               |
| 500 | Internal Server Error (Внутренняя ошибка сервера)| Непредвиденная ошибка сервера.                             |

## Как использовать API PostWorkbooksMerge с SDK

### Спецификация API PostWorkbooksMerge

[OpenAPI-спецификация](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbooksMerge) определяет общедоступное программное интерфейсное API, позволяющее выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки **cURL** для простого доступа к веб-сервисам Aspose.Cells. Следующий пример показывает, как выполнять вызовы в облачный API с помощью cURL, включая обязательный заголовок аутентификации.


{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
# Объединить test2.xlsx в test.xlsx
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/merge?mergeWith=test2.xlsx" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access-token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Workbook": {
    "FileName": "test.xlsx",
    "Links": [
      {
        "Href": "/test.xlsx",
        "Rel": "self",
        "Title": null,
        "Type": null
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Скачать как CSV",
        "Type": "text/csv"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Скачать как HTML",
        "Type": "text/html"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Скачать как ODS",
        "Type": "application/vnd.oasis.opendocument.spreadsheet"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Скачать как PDF",
        "Type": "application/pdf"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Скачать как текст в табличном формате с разделителями",
        "Type": "text/plain"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Скачать как TIFF",
        "Type": "image/tiff"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Скачать как Microsoft Excel 2003",
        "Type": "application/vnd.ms-excel"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Скачать как Microsoft Excel 2007",
        "Type": "application/vnd.openxmlformats-officedocument.spreadsheetml.sheet"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Скачать как XPS",
        "Type": "application/vnd.ms-xpsdocument"
      }
    ],
    "Worksheets": {
      "link": {
        "Href": "/worksheets",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "DefaultStyle": {
      "link": {
        "Href": "/defaultstyle",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "DocumentProperties": {
      "link": {
        "Href": "/documentproperties",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "Names": {
      "link": {
        "Href": "/names",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "Settings": {
      "link": {
        "Href": "/settings",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "IsWriteProtected": "False",
    "IsProtected": "False",
    "IsEncryption": "false",
    "Password": null
  },
  "Code": 200,
  "Status": "OK"
}
```

В ответе возвращается объект `Workbook`, содержащий метаданные объединённой рабочей книги, включая ссылки для скачивания результата в различных форматах (CSV, PDF, HTML и др.).

Заголовки ответа

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — это лучший способ ускорить разработку. SDK абстрагирует низкоуровневые детали и позволяет сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud см. в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют, как выполнять вызовы в веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbooksMerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbooksMerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbooksMerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbooksMerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbooksMerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbooksMerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbooksMerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbooksMerge.go" >}}

{{< /tab >}}

{{< /tabs >}}