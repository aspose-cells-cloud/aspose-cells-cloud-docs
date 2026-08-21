---
title: "ConvertRangeToPdf"
ArticleTitle: "Преобразование диапазона в PDF – Aspose.Cells Cloud API"
second_title: "Документ"
linktype: "ConvertRangeToPdf"
type: docs
url: /cells/convert/range/pdf
aliases: []
keywords: "Aspose.Cells, преобразование диапазона в PDF, API"
description: "Преобразует заданный диапазон электронной таблицы в PDF с использованием Aspose.Cells Cloud."
weight: 1
---

## ConvertRangeToPdf веб-служб Aspose.Cells Cloud

Преобразует диапазон электронной таблицы, расположенный на локальном диске, в PDF-файл.

### Конечная точка веб-API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/pdf
```

### **Безопасность и аутентификация**

Веб-API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе токена JWT</a>.

### Параметры запроса

| Имя параметра   | Тип   | Путь/Строка запроса/HTTP-тело | Описание                                                                                                                                    |
|------------------|--------|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | File   | FormData                    | Загрузить файл электронной таблицы.                                                                                                                       |
| worksheet        | String | Query                       | Имя листа электронной таблицы.                                                                                                                |
| range            | String | Query                       | Ячейочный диапазон. Например, A1:C10                                                                                                                         |
| outPath          | String | Query                       | (Необязательно) Путь к папке, где хранится рабочая книга. По умолчанию — null.                                                                 |
| outStorageName   | String | Query                       | Имя хранилища для выходного файла.                                                                                                                      |
| fontsLocation    | String | Query                       | Использовать пользовательские шрифты.                                                                                                                              |
| AutoRowsFit      | Boolean| Query                       | (Необязательно) Автоматически подогнать все строки на листах.                                                                                                   |
| AutoColumnsFit   | Boolean| Query                       | (Необязательно) Автоматически подогнать все столбцы на листах.                                                                                                |
| region           | String | Query                       | Региональные/языковые настройки электронной таблицы (например, `en-US`, `fr-FR`). Влияют на форматирование чисел, разбор дат и поведение, зависящее от региона.       |
| password         | String | Query                       | Пароль для открытия файла электронной таблицы.                                                                                                     |

### Параметр тела запроса

| Имя параметра | Тип | Описание |
|----------------|------|-------------|
| Spreadsheet    | File | Загрузить файл электронной таблицы. |

### **Ответ**

```json
{
  "file": "<двоичное содержимое PDF>"
}
```

**Коды статуса ответа**

| Код | Значение | Описание |
|------|---------|-------------|
| 200 | OK | Успешное преобразование; возвращает поток сгенерированного PDF-файла. |
| 400 | Bad Request | Неверный URL. |
| 401 | Unauthorized | Аутентификация не удалась или не были предоставлены учётные данные. |
| 413 | Payload Too Large | Размер загруженного файла превышает допустимый лимит. |
| 500 | Internal Server Error | В электронной таблице возникла ошибка при получении данных для преобразования. |

## Как использовать ConvertRangeToPdf с SDK

### Спецификация ConvertRangeToPdf

[Спецификация API ConvertRangeToPdf](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToPdf) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для удобного доступа к веб-службам Aspose.Cells Cloud. В следующем примере показано, как выполнять вызовы в облачный API с помощью cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# Используйте HTTPS для защищённого соединения
curl -v "https://api.aspose.cloud/v4.0/cells/convert/range/pdf?worksheet=Sheet1&range=A1:C10" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/pdf" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<двоичное содержимое PDF>"
}
```

{< /tab >}

{< /tabs >}

### Использование SDK Aspose Cells Cloud

Использование SDK — самый быстрый способ ускорить разработку. SDK скрывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. С полным списком SDK Aspose.Cells Cloud можно ознакомиться в <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">репозитории на GitHub</a>.

Следующие примеры кода демонстрируют, как вызывать веб-службы Aspose Cells Cloud с использованием различных SDK:

```csharp
// Пример кода SDK для C#
var apiInstance = new ConversionApi();
var file = File.OpenRead("sample.xlsx");
var result = apiInstance.ConvertRangeToPdf(file, "Sheet1", "A1:C10", outPath: null, outStorageName: null, fontsLocation: null, autoRowsFit: null, autoColumnsFit: null, region: null, password: null);
File.WriteAllBytes("output.pdf", result);
```

```java
// Пример кода SDK для Java
ConversionApi api = new ConversionApi();
File file = new File("sample.xlsx");
byte[] result = api.convertRangeToPdf(file, "Sheet1", "A1:C10", null, null, null, null, null, null, null);
Files.write(Paths.get("output.pdf"), result);
```

```python
# Пример кода SDK для Python
api_instance = conversion_api.ConversionApi()
with open("sample.xlsx", "rb") as f:
    result = api_instance.convert_range_to_pdf(f, worksheet="Sheet1", range="A1:C10")
    with open("output.pdf", "wb") as out_file:
        out_file.write(result)
```

```javascript
// Пример кода SDK для JavaScript/Node.js
const fs = require('fs');
const { ConversionApi } = require('asposecellscloud');
const apiInstance = new ConversionApi();

let file = fs.createReadStream('sample.xlsx');
apiInstance.convertRangeToPdf(file, { worksheet: 'Sheet1', range: 'A1:C10' })
    .then((result) => {
        fs.writeFileSync('output.pdf', result);
    })
    .catch((error) => console.error(error));
```

`[TBD]`
---