---
title: "Разделение рабочей книги Excel на несколько файлов"
ArticleTitle: "Как разделить рабочую книгу Excel на несколько файлов с помощью API Aspose.Cells Cloud"
second_title: "Документ"
linktitle: "Разделение файла Excel"
type: docs
url: /ru/split-multi-excel-files/
aliases: [  /ru/split/multi-files/ ]
keywords: "Excel, Aspose.Cells Cloud, REST API, разделение рабочей книги, несколько файлов, JPEG, PNG, PDF, CSV, JSON"
description: "REST API Aspose.Cells Cloud позволяет разделить рабочую книгу Excel на несколько файлов в различных форматах. В данном документе приведены параметры запроса, пример cURL и примеры кода SDK для языков C#, Java, PHP, Ruby, Node.js, Python, Perl и Go."
weight: 130
---

Этот REST API позволяет разделить **рабочую книгу** Excel на несколько файлов в различных форматах.

> **Необходимые условия** — Для использования этого API необходимо получить действующий токен JWT, убедиться, что используется поддерживаемая версия SDK и проверить, что ваша рабочая книга хранится в поддерживаемом хранилище. API также накладывает ограничения на размер файла, описанные в руководстве платформы.

## API PostWorkbookSplit

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/split
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе токена JWT</a>.

### Параметры запроса

| Имя параметра       | Тип    | Расположение | Описание                                                                                     | Обязательный |
| -------------------- | ------- | ------------ | ----------------------------------------------------------------------------------------------- | ------------ |
| files[]              | файл    | formData     | Одна или несколько рабочих книг Excel для **разделения**. Используйте `file1`, `file2`, … в запросе. | Да           |
| format               | строка  | Query        | Желаемый выходной формат для разделённых файлов.                                               | Нет          |
| from                 | целое   | Query        | Индекс начального листа.                                                                       | Нет          |
| to                   | целое   | Query        | Индекс конечного листа.                                                                        | Нет          |
| horizontalResolution | целое   | Query        | Горизонтальное разрешение изображения.                                                         | Нет          |
| verticalResolution   | целое   | Query        | Вертикальное разрешение изображения.                                                           | Нет          |
| outFolder            | строка  | Query        | Папка вывода для разделённых файлов.                                                           | Нет          |
| splitNameRule        | строка  | Query        | Правило именования для разделённых файлов.                                                     | Нет          |
| folder               | строка  | Query        | Папка, содержащая исходную рабочую книгу.                                                      | Нет          |
| storageName          | строка  | Query        | Имя хранилища, которое следует использовать.                                                   | Нет          |

### **Ответ**

```json
{
    "Status":"OK",
    "Code":200,
    "Files": [
      {
        "Filename" : "[имя файла1]",
        "Filesize" : [размер файла],
        "FileContent" : "[Base64String]"
      },
      {
        "Filename" : "[имя файла2]",
        "Filesize" : [размер файла],
        "FileContent" : "[Base64String]"
      },
      {
        "Filename" : "[имя файла3]",
        "Filesize" : [размер файла],
        "FileContent" : "[Base64String]"
      }
    ]
}
```

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                           |
|-----|-----------------------------|----------------------------------------------------|
| 200 | OK                          | Фильтр успешно применён; в ответе содержатся сведения об операции. |
| 400 | Bad Request                 | Отсутствуют или неверны параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized                | Неверный или отсутствующий токен JWT. |
| 413 | Payload Too Large           | Загруженный файл превышает ограничение по размеру. |
| 500 | Internal Server Error       | Непредвиденная ошибка сервера. |

## Как использовать API PostWorkbookSplit с SDK

### Спецификация API PostWorkbookSplit

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookSplit) определяет публично доступное программное интерфейсное определение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки **cURL** для лёгкого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как выполнять вызовы в Cloud API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/test.xlsx/split?format=jpeg&from=1&to=1&horizontalResolution=0&verticalResolution=0" -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Result": {
    "Documents": [
      {
        "Id": 1,
        "link": {
          "Href": "413e3375-c163-4d5c-8b84-8f95f63902f6.png",
          "Rel": null,
          "Title": null,
          "Type": null
        }
      }
    ]
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя вам сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен на [GitHub-репозитории](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют, как выполнять вызовы в веб-сервисы Aspose.Cells с помощью различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookSplit.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookSplit.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookSplit.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookSplit.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookSplit.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookSplit.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookSplit.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookSplit.go" >}}

{{< /tab >}}

{{< /tabs >}}