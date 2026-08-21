---
title: "Добавление фонового изображения в рабочую книгу"
second_title: "Документ"
linktitle: "Добавить"
type: docs
url: /add-background-in-excel-file/
aliases:
  - /add-background-in-workbook/
  - /workbook/add-background/
  - /workbook/background/add/
keywords: "Aspose.Cells, добавить фоновое изображение, Excel API, REST, облачный SDK, cURL, фон рабочей книги"
description: "Узнайте, как добавить фоновое изображение в рабочую книгу Excel с помощью Aspose.Cells Cloud REST API. Включает необходимые параметры, данные по аутентификации, полный пример на cURL и информацию об обработке ошибок."
weight: 160
---

## REST API

Этот REST API добавляет **фоновое изображение** в рабочую книгу Excel.

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/background
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud являются защищёнными и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.


### Параметры запроса

| Имя параметра | Тип   | Описание                                               |
| ------------- | ----- | ------------------------------------------------------ |
| `picPath`     | string | Путь к файлу изображения, используемому в качестве фона. |
| `folder`      | string | Папка, содержащая исходную рабочую книгу.              |
| `storageName` | string | Имя хранилища, в котором находится файл.                |

### Параметр тела запроса

| Имя параметра | Тип  | Описание                                             |
| ------------- | ---- | ---------------------------------------------------- |
| `datafile`    | file | Файл рабочей книги, к которой будет применено фоновое изображение. |

**Параметр пути** – `{name}` в URL-адресе представляет **имя файла рабочей книги** (например, `Book1.xlsx`).


### **Ответ**

```json
{
    "Status" : "OK",
    "Code" : 200
}
```

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                                                 |
|-----|-----------------------------|--------------------------------------------------------------------------|
| 200 | OK                          | Фильтр успешно применён; ответ содержит детали операции.                 |
| 400 | Bad Request                 | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized                | Недопустимый или отсутствующий JWT-токен.                               |
| 413 | Payload Too Large           | Загруженный файл превышает лимит размера.                                |
| 500 | Internal Server Error       | Непредвиденная ошибка сервера.                                           |

## Как использовать API PutWorkbookBackground с SDK

### Спецификация API PutWorkbookBackground

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookBackground) определяет публично доступное программное интерфейсное описание, позволяющее выполнять взаимодействие по REST напрямую из веб-браузера.

Вы можете использовать инструмент командной строки **cURL** для простого доступа к веб-сервисам Aspose.Cells. Приведённый ниже пример демонстрирует полный запрос, включая флаг загрузки multipart-файла и обязательный заголовок аутентификации.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/background?picPath=DotnetFiles%2FWaterMark.png&folder=DotnetFiles" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -F "datafile=@/path/to/Book1.xlsx"
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


### Использование SDK Aspose.Cells Cloud

Использование SDK — самый быстрый способ разработки. SDK абстрагирует низкоуровневые детали, позволяя сосредоточиться на бизнес-логике. Полный список SDK Aspose.Cells Cloud см. в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}