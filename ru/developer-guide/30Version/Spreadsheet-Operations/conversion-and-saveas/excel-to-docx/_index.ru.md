---
title: "Excel в DOCX"
second_title: "Документ"
linktitle: "Excel в DOCX"
type: docs
url: /ru/ruconvert-excel-file-to-docx-file/
keywords: "конвертация Excel в DOCX, Aspose.Cells Cloud, REST API, конвертация электронных таблиц, генерация документов"
description: "Конвертируйте электронные таблицы Excel в документы DOCX с помощью REST API Aspose.Cells Cloud. Поддерживает множество SDK и языков программирования для бесшовной интеграции."
weight: 90
---

Этот REST API конвертирует файл электронной таблицы в формат DOCX.

## REST API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/docx
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе токена JWT</a>.



**Параметры запроса**

| Имя параметра         | Тип    | Описание                                                                                     |
| --------------------- | ------ | -------------------------------------------------------------------------------------------- |
| password              | string | Пароль, необходимый для открытия файла Excel.                                               |
| storageName           | string | Имя хранилища, в котором расположен файл.                                                   |
| checkExcelRestriction | bool   | Указывает, следует ли проверять ограничения файла Excel при изменении пользователем объектов, связанных с ячейками. |

**Параметр тела запроса**

| Имя параметра | Тип       | Описание                                                      |
| -------------- | --------- | ------------------------------------------------------------- |
| datafile       | data file | Файл данных, сохранённый в первой части тела запроса multipart. |

**Ответ**

API возвращает объект **FileInfo**, содержащий созданный Word-файл.

| Поле            | Тип    | Описание                                    |
| --------------- | ------ | ------------------------------------------- |
| **Filename**    | string | Имя Word-файла (например, `example.docx`). |
| **FileSize**    | int    | Размер файла в байтах.                      |
| **FileContent** | string | Содержимое Word-файла в формате Base64.     |


[FileInfo](/cells/file-info/)

**Коды HTTP-статусов**

| Код  | Значение                    | Описание                                                     |
|------|-----------------------------|--------------------------------------------------------------|
| 200  | OK (ОК)                     | Фильтр применён успешно; ответ содержит детали операции.    |
| 400  | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized (Неавторизован) | Недопустимый или отсутствующий токен JWT.                    |
| 413  | Payload Too Large (Слишком большой полезный груз) | Загруженный файл превышает предельный размер. |
| 500  | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера. |

## Как использовать API PostConvertWorkbookToDocx с SDK

### Спецификация API PostConvertWorkbookToDocx

[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToDocx) определяет публично доступное программное интерфейсное описание и позволяет выполнять взаимодействие по REST непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки **cURL** для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как делать вызовы в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/docx" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d '{"File":{}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.docx",
  "FileSize": 12345,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — это лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя вам сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToDocx.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToDocx.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToDocx.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToDocx.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToDocx.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToDocx.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToDocx.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToDocx.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Другие API, реализующие эту функцию

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Сохраняет файл Excel как DOCX с дополнительными настройками и сохраняет результат в указанном хранилище.

- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Конвертирует файл Excel в DOCX с необязательными настройками и возвращает результат в ответе.

- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Получает рабочую книгу Excel и конвертирует её в DOCX с необязательными параметрами.

---