---
title: "Добавление изображения в файл Excel"
second_title: "Документ"
linktitle: "Добавить"
type: docs
url: /ru/pictures/add/
aliases: [  /ru/add-pictures-to-excel-worksheet/ ]
keywords: "Aspose.Cells, Excel, добавление изображения, REST API"
description: "Используйте Aspose.Cells Cloud REST API для добавления изображения в лист Excel. SDK для Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby и Swift упрощают интеграцию на различных платформах."
weight: 20
ArticleTitle: "Добавление изображения в лист Excel — API Aspose.Cells Cloud"
---

Этот REST API добавляет новое изображение в лист Excel.  
**Необходимые условия:** У вас должен быть действительный токен аутентификации Aspose Cloud, существующая рабочая книга, сохранённая в поддерживаемом хранилище, и соответствующие права на изменение листа.

## API PutWorksheetAddPicture

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### Параметры запроса

| Имя параметра | Тип    | Расположение | Описание                                                                                   |
| ------------- | ------ | ----------- | ------------------------------------------------------------------------------------------ |
| name          | string | path        | Имя рабочей книги.                                                                         |
| sheetName     | string | path        | Имя листа.                                                                                |
| picture       | object | body        | Объект изображения (бинарные данные).                                                     |
| upperLeftRow  | integer | query      | Нулевой индекс верхней левой строки, в которую будет помещено изображение.               |
| upperLeftColumn | integer | query    | Нулевой индекс верхнего левого столбца, в который будет помещено изображение.            |
| lowerRightRow | integer | query      | Нулевой индекс нижней правой строки области изображения.                                 |
| lowerRightColumn | integer | query   | Нулевой индекс нижнего правого столбца области изображения.                              |
| picturePath   | string | query       | Путь к файлу изображения; если опущен, данные изображения должны быть переданы в теле запроса. |
| folder        | string | query       | Папка, содержащая рабочую книгу.                                                          |
| storageName   | string | query       | Имя службы хранилища.                                                                     |

**Примечание к телу запроса:** При отсутствии параметра `picturePath` передавайте бинарные данные изображения в теле запроса, используя `multipart/form-data`.

### Коды HTTP-статуса

| Код | Значение                     | Описание                                                                 |
|-----|-----------------------------|--------------------------------------------------------------------------|
| 200 | OK                          | Фильтр применён успешно; ответ содержит информацию о выполнении операции. |
| 400 | Bad Request                 | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized                | Недействительный или отсутствующий JWT-токен.                           |
| 413 | Payload Too Large           | Загруженный файл превышает лимит размера.                               |
| 500 | Internal Server Error       | Непредвиденная ошибка сервера.                                           |

**Пример схемы ответа 200**

```json
{
  "Code": 200,
  "Status": "OK",
  "PictureUrl": "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/1"
}
```

**Примечание:** Максимальный размер изображения — 10 МБ; файлы большего размера будут отклонены с ответом `400 Bad Request`.

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Pictures/PutWorksheetAddPicture) определяет общедоступное программное интерфейсное решение и позволяет выполнять взаимодействие с REST непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Следующий пример демонстрирует, как выполнять вызовы в Cloud API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.com/v1.1/cells/Sample_Test_Book.xls/worksheets/Sheet6/pictures?picturePath=aspose-cloud.png" \
  -X PUT \
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

## Семейство облачных SDK

Использование SDK — это лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Ознакомьтесь с [репозиторием на GitHub](https://github.com/aspose-cells-cloud), чтобы увидеть полный список SDK Aspose.Cells Cloud.

Следующие примеры кода демонстрируют, как выполнять вызовы в веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetAddPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetAddPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetAddPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetAddPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82deb4189bc27ae92abf73c36b4df0" "Example_PutWorksheetAddPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetAddPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetAddPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetAddPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Примечание:** Поддерживаемые форматы изображений включают PNG, JPEG, BMP и GIF. Максимальный размер изображения — 10 МБ; файлы большего размера будут отклонены с ответом `400 Bad Request`.