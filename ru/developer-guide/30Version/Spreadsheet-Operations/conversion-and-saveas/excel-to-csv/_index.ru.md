---
title: "Excel в CSV"
second_title: "Документ"
linktitle: "Excel в CSV"
type: docs
url: /ru/ruconvert-excel-file-to-CSV-file/
aliases:
  - /convert-excel-file-to-CSV-in-cloud/
  - /convert/excel-to-csv/
  - /convert-excel-file-to-CSV-file/
keywords: "Excel в CSV, Aspose.Cells Cloud, REST API, конвертация электронных таблиц, CSV-файл, конвертация файлов"
description: "Конвертируйте электронные таблицы Excel в CSV с помощью REST API Aspose.Cells Cloud. Поддерживает множество SDK и языков программирования для простой интеграции."
weight: 90
---

Этот REST API конвертирует файл электронной таблицы в файл формата CSV.

## REST API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/csv
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе токена JWT</a>.


### Параметры запроса

| Имя параметра          | Тип   | Описание                                                                           |
| ----------------------- | ------ | ------------------------------------------------------------------------------------- |
| `password`              | string | Пароль, необходимый для открытия файла Excel.                                         |
| `storageName`           | string | Имя хранилища, в котором находится файл.                                    |
| `checkExcelRestriction` | bool   | Следует ли проверять ограничения файла Excel при изменении пользователем объектов, связанных с ячейками. |

### Параметр тела запроса

| Имя параметра | Тип      | Описание                                                             |
| -------------- | --------- | ----------------------------------------------------------------------- |
| `datafile`     | data file | Файл данных, включённый в первую часть multipart-тела запроса. |

### Ответ

API возвращает объект **FileInfo**, содержащий сгенерированный CSV-файл.

| Поле           | Тип   | Описание                                   |
| --------------- | ------ | --------------------------------------------- |
| **Filename**    | string | Имя CSV-файла (например, `example.csv`). |
| **FileSize**    | int    | Размер файла в байтах.                    |
| **FileContent** | string | Содержимое CSV-файла в кодировке Base64.      |

[FileInfo](/cells/file-info/)


**Коды HTTP-статусов**

| Код | Значение                     | Описание                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Фильтр успешно применён; ответ содержит детали операции. |
| 400  | Bad Request                 | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized                | Недопустимый или отсутствующий токен JWT. |
| 413  | Payload Too Large           | Загружаемый файл превышает предельный размер. |
| 500  | Internal Server Error       | Непредвиденная ошибка сервера. |
## Как использовать API PostConvertWorkbookToCSV с SDK

### Спецификация API PostConvertWorkbookToCSV

[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToCSV) определяет общедоступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия прямо из веб-браузера.

Вы можете использовать утилиту командной строки **cURL** для доступа к веб-сервисам Aspose.Cells. В приведённом ниже примере показано, как вызвать облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/csv" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d '{"File":{}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.CSV",
  "FileSize": 12345,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — самый быстрый способ разработки. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на вашем проекте. Полный список SDK Aspose.Cells Cloud см. в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Приведённые ниже примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPDF.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPDF.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPDF.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPDF.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPDF.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPDF.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPDF.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPDF.go" >}}

{{< /tab >}}

{{< /tabs >}}