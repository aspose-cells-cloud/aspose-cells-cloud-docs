---
title: "Excel в PNG"
second_title: "Документ"
linktitle: "Excel в PNG"
type: docs
url: /ruconvert-excel-file-to-png-file/
keywords: "Excel в PNG, Aspose.Cells Cloud, REST API, конвертация электронных таблиц, формат PNG"
description: "Конвертируйте файлы электронных таблиц Excel в изображения PNG с помощью REST API Aspose.Cells Cloud. Поддерживает множество SDK и предоставляет подробные примеры для различных языков программирования."
weight: 90
---

Этот REST API преобразует файл электронной таблицы в формат PNG.

## Спецификация REST API

```
POST https://api.aspose.cloud/v3.0/cells/convert/png
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе токена JWT</a>.

### **Параметр запроса (query parameter)**

| Имя параметра        | Тип    | Описание                                                                                     |
| --------------------- | ------ | -------------------------------------------------------------------------------------------- |
| password              | string | Пароль, необходимый для открытия файла Excel.                                               |
| storageName           | string | Имя хранилища, в котором расположен файл.                                                   |
| checkExcelRestriction | bool   | Определяет, следует ли проверять ограничения файла Excel при изменении ячеек или связанных объектов. |

### **Параметр тела запроса (request body parameter)**

| Имя параметра | Тип       | Описание                                                              |
| -------------- | --------- | --------------------------------------------------------------------- |
| datafile       | data file | Файл электронной таблицы, включённый в первую часть multipart-запроса. |

### **Ответ**

API возвращает объект **FileInfo**, содержащий созданное изображение PNG.

| Поле            | Тип    | Описание                                    |
| --------------- | ------ | ------------------------------------------- |
| **Filename**    | string | Имя PNG-файла (например, `example.png`).   |
| **FileSize**    | int    | Размер файла в байтах.                      |
| **FileContent** | string | Содержимое PNG-файла в кодировке Base64.    |

[FileInfo](/cells/file-info/)


**Коды HTTP-статуса**

| Код  | Значение                    | Описание                                                  |
|------|-----------------------------|-----------------------------------------------------------|
| 200  | OK                          | Фильтр успешно применён; ответ содержит сведения об операции. |
| 400  | Bad Request                 | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized                | Недопустимый или отсутствующий токен JWT.                 |
| 413  | Payload Too Large           | Загруженный файл превышает предельный размер.             |
| 500  | Internal Server Error       | Непредвиденная ошибка сервера.                            |

## Как использовать API PostConvertWorkbookToPNG с SDK

### Спецификация API PostConvertWorkbookToPNG

[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPNG) определяет публично доступное программное интерфейсное API и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать инструмент командной строки **cURL** для лёгкого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как отправлять запросы к Cloud API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/png" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d {"File":{}}
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "xxxxxx.png",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — это лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах вашего проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPNG.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPNG.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPNG.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPNG.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPNG.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPNG.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPNG.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPNG.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Другие API, реализующие аналогичные функции

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Сохраняет файл Excel в формате CSV (или другом формате) с дополнительными настройками и сохраняет результат.
- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Преобразует файл Excel в CSV (или другой формат) с необязательными параметрами и возвращает результат в ответе.
- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Получает файл Excel и может конвертировать его в CSV (или другой формат) на лету.

---