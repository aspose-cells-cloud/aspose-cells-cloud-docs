---
title: "Копирование столбцов в рабочем листе Excel"
second_title: "Документ"
linktitle: "Копирование"
type: docs
url: /ru/columns/copy/
aliases:
  [/copy-columns-in-excel-worksheet/, /copy-columns-in-an-excel-worksheet/]
keywords: "Aspose.Cells, копирование столбцов, API Excel, REST, облачный SDK, cURL, C#, Java, Python, Ruby, Node.js, Go, Perl"
description: "Узнайте, как скопировать один или несколько столбцов в рабочем листе Excel с помощью Aspose.Cells Cloud REST API (v3.0). Включает синтаксис запроса, необходимые параметры, данные об аутентификации, обработку ошибок и примеры SDK на языках C#, Java, Python, Ruby, Node.js, Go, Perl и других."
articleTitle: "Копирование столбцов в рабочем листе Excel с использованием Aspose.Cells Cloud API"
weight: 30
---

Этот REST API позволяет копировать **столбцы** в рабочем листе Excel. Операция **Copy Columns** (Копировать столбцы) позволяет дублировать один столбец или диапазон столбцов и вставить копию в указанное место того же рабочего листа. Используйте этот конечный пункт для эффективного копирования столбцов при работе с большими электронными таблицами. Дополнительные задачи управления столбцами можно выполнить с помощью связанных операций, таких как [Добавление столбца](/columns/add/) и [Скрытие столбца](/columns/hide/).

## Безопасность и аутентификация
API Aspose.Cells Cloud безопасны и требуют [аутентификации на основе JWT-токена](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/copy
```

### Параметры запроса

| Имя параметра            | Тип    | Расположение | Описание                                                                              |
| ------------------------ | ------ | ------------ | ------------------------------------------------------------------------------------- |
| **name**                 | string | path         | Имя рабочей книги.                                                                    |
| **sheetName**            | string | path         | Имя рабочего листа.                                                                   |
| **sourceColumnIndex**    | integer | query       | 0‑индексированный номер столбца, который нужно скопировать.                          |
| **destinationColumnIndex** | integer | query     | 0‑индексированный номер столбца, куда будут вставлены скопированные столбцы.         |
| **columnNumber**         | integer | query       | Количество последовательных столбцов для копирования.                                |
| **worksheet**            | string | query        | _(Опционально)_ Идентификатор рабочего листа, используемый, если имя отличается от пути. |
| **folder**               | string | query        | Путь к папке, содержащей рабочую книгу в облачном хранилище Aspose.                 |

Полный контракт для этой операции описан в [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/PostCopyWorksheetColumns).

### Пример cURL

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/copy?sourceColumnIndex=1&destinationColumnIndex=12&columnNumber=10" \
     -H "Authorization: Bearer $ASPOSE_TOKEN" \
     -H "accept: application/json"
```

### Ответ

```json
{
  "Code": 200,
  "Status": "OK"
}
```

## Обработка ошибок

API возвращает стандартные HTTP-коды состояния и JSON-тело с описанием ошибки.

| Код состояния | Значение                                          | Пример JSON-тела                                                    |
| ------------- | ------------------------------------------------ | ------------------------------------------------------------------- |
| **400**       | Неверный запрос — некорректные параметры         | `{ "Code": 400, "Message": "Invalid column index." }`               |
| **401**       | Неавторизован — отсутствует или недействителен токен | `{ "Code": 401, "Message": "Access token is invalid or expired." }` |
| **404**       | Не найдено — рабочая книга или лист не существуют | `{ "Code": 404, "Message": "Workbook not found." }`                 |
| **500**       | Внутренняя ошибка сервера — непредвиденное условие | `{ "Code": 500, "Message": "An unexpected error occurred." }`       |

> **Как устранить неполадки:** Убедитесь, что токен доступа актуален, имена рабочей книги и листа указаны верно, а значения `sourceColumnIndex`, `destinationColumnIndex` и `columnNumber` находятся в пределах допустимого диапазона столбцов рабочего листа.

## Семейство облачных SDK

Использование SDK — оптимальный способ ускорить разработку. SDK берёт на себя обработку низкоуровневых деталей, позволяя сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

В приведённых ниже примерах кода показано, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCopyWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCopyWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCopyWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCopyWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCopyWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCopyWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCopyWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCopyWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Как выполнить аутентификацию при вызове API Copy Columns?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Получите токен доступа OAuth2 в Aspose Cloud, используя ваш client ID и secret, и передайте его в заголовке запроса как `Authorization: Bearer <access_token>`."
      }
    },
    {
      "@type": "Question",
      "name": "В чём разница между `sourceColumnIndex` и `destinationColumnIndex`?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "`sourceColumnIndex` — это 0‑индексированный номер столбца, который нужно скопировать. `destinationColumnIndex` — это 0‑индексированный номер столбца, куда будут вставлены скопированные столбцы."
      }
    },
    {
      "@type": "Question",
      "name": "Какой ответ приходит, если операция копирования завершилась с ошибкой?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "API возвращает код состояния, отличный от 200 (например, 400 для неверного запроса, 401 для неавторизованного доступа). В теле ответа содержится JSON-объект с полями `Code` и `Message`, описывающий ошибку."
      }
    }
  ]
}
</script>
---