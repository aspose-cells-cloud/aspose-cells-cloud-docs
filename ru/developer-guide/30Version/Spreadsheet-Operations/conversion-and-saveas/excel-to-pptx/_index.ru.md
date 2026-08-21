---
title: "Преобразование Excel в PPTX с помощью Aspose.Cells Cloud API v3.0"
second_title: "Документ"
linktitle: "Excel в PPTX"
type: docs
url: /convert-excel-file-to-pptx-file/
keywords: "Aspose, Cells, Excel, PPTX, преобразование, REST API, облачные технологии"
description: "Узнайте, как преобразовывать рабочие книги Excel в презентации PPTX с помощью Aspose.Cells Cloud REST API v3.0. Включает примеры запросов cURL, кода SDK, аутентификацию и обработку ошибок."
weight: 90
ArticleTitle: "Преобразование Excel в PPTX с помощью Aspose.Cells Cloud API v3.0"
---

Этот REST API преобразует файл электронной таблицы в формат PPTX.

## API PostConvertWorkbookToPptx

```http
POST https://api.aspose.cloud/v3.0/cells/convert/pptx
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

### Параметры запроса

| Имя параметра         | Тип    | Описание                                                                 |
| --------------------- | ------ | ------------------------------------------------------------------------ |
| `password`            | string | Пароль, необходимый для открытия рабочей книги Excel.                   |
| `storageName`         | string | Имя хранилища, в котором находится исходный файл.                        |
| `checkExcelRestriction` | bool | Определяет, следует ли применять ограничения файлов Excel при изменении объектов, связанных с ячейками. |

### Параметр тела запроса

| Имя параметра | Тип       | Описание                                                           |
| ------------- | --------- | ------------------------------------------------------------------ |
| `datafile`    | data file | Файл Excel, включенный в первую часть многокомпонентного тела запроса. |

**Пример многокомпонентного тела запроса (упрощённо):**

```
--boundary
Content-Disposition: form-data; name="File"; filename="input.xlsx"
Content-Type: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet

<двоичное содержимое input.xlsx>
--boundary
Content-Disposition: form-data; name="password"

MyPwd
--boundary--
```

### Ответ

API возвращает объект **FileInfo**, содержащий сгенерированный файл pptx.

| Поле            | Тип    | Описание                                      |
| --------------- | ------ | --------------------------------------------- |
| **Filename**    | string | Имя файла pptx (например, `example.pptx`).   |
| **FileSize**    | int    | Размер файла в байтах.                        |
| **FileContent** | string | Содержимое файла pptx в кодировке Base64.     |

[FileInfo](/cells/file-info/)

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                                             |
|-----|-----------------------------|----------------------------------------------------------------------|
| 200 | OK (ОК)                     | Фильтр успешно применён; ответ содержит детали операции.            |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизовано) | Неверный или отсутствует токен JWT.                                 |
| 413 | Payload Too Large (Слишком большой payload) | Загруженный файл превышает лимит размера.                          |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                                    |

*Примечания:* Конечная точка поддерживает распространённые форматы Excel (`.xlsx`, `.xls`, `.xlsm`). Максимальный размер файла ограничен 50 МБ. Преобразование может быть недоступно для рабочих книг, содержащих макросы или защищённые листы, если не предоставлены соответствующие параметры.

## Как использовать API PostConvertWorkbookToPptx с помощью SDK

### Спецификация API PostConvertWorkbookToPptx

<a href="https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPptx" rel="noopener noreferrer">Спецификация OpenAPI</a> определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки **cURL** для простого доступа к веб-сервисам Aspose.Cells. В приведённом ниже примере показано, как вызвать облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/pptx?storageName=MyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@/path/to/input.xlsx" \
     -F "password=MyPwd"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.pptx",
  "FileSize": 123456,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — самый быстрый способ разработки. SDK абстрагирует низкоуровневые детали, позволяя сосредоточиться на вашем проекте. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud" rel="noopener noreferrer").

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPptx.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPptx.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPptx.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPptx.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPptx.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1c" "Example_PostConvertWorkbookToPptx.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPptx.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPptx.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Другие API, реализующие эту функцию

- **[POST /cells/convert/pdf](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPdf)** – Преобразует файл Excel в PDF.
- **[POST /cells/convert/png](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPng)** – Преобразует файл Excel в изображения PNG.
- **[POST /cells/convert/svg](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToSvg)** – Преобразует файл Excel в формат SVG.