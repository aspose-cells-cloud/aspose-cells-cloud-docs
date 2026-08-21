---
title: "Aspose.Cells Cloud Web API — преобразование локальных данных таблицы Excel в PDF-файл — бесплатный онлайн-инструмент"
second_title: "Документ"
ArticleTitle: "Как преобразовать табличные данные из локальной электронной таблицы в PDF-файл: пошаговое руководство"
linktitle: "Преобразовать таблицу в PDF"
type: docs
url: /convert-table-to-pdf/
keywords: "Aspose.Cells, Excel в PDF, преобразование таблицы, облачный API"
description: "Быстро преобразуйте локальную таблицу Excel в PDF-файл с помощью облачного REST API Aspose.Cells."
weight: 100
---

Экспорт табличных данных из локального файла Excel в PDF-файл с использованием облачного API.

## **Преобразование таблицы в PDF: API**

### Веб-API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/pdf
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе токена JWT</a>.

### **Параметры запроса:**

| Имя параметра | Тип   | Путь/Строка запроса/Тело HTTP | Описание                                                                 |
| :------------ | :---- | :--------------------------- | :----------------------------------------------------------------------- |
| Spreadsheet   | Файл  | FormData                     | Загрузите файл электронной таблицы, который нужно преобразовать.        |
| worksheet     | Строка | Запрос                       | Имя рабочего листа электронной таблицы.                                  |
| tableName     | Строка | Запрос                       | Имя таблицы для преобразования.                                          |
| outPath       | Строка | Запрос                       | (Необязательно) Путь к папке, где будет сохранён преобразованный PDF. По умолчанию — null. |
| outStorageName| Строка | Запрос                       | Укажите имя хранилища выходного файла.                                   |
| fontsLocation | Строка | Запрос                       | Использовать пользовательские шрифты для PDF.                            |
| region        | Строка | Запрос                       | Указать региональные настройки для электронной таблицы.                  |
| password      | Строка | Запрос                       | Пароль для доступа к файлу электронной таблицы.                          |

### **Ответ**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**Пример заголовков ответа**

```http
HTTP/1.1 200 OK
Content-Type: application/pdf
Content-Disposition: attachment; filename="ConvertedTable.pdf"
Content-Length: 124578
```

**Коды HTTP-статуса**

| Код | Значение              | Описание                                                       |
| --- | --------------------- | -------------------------------------------------------------- |
| 200 | OK (ОК)              | Фильтр успешно применён; ответ содержит детали операции.      |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизован) | Недействительный или отсутствующий токен JWT.                 |
| 413 | Payload Too Large (Слишком большой Payload) | Загруженный файл превышает лимит размера.                    |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                              |

## **Где следует использовать API преобразования таблицы в PDF?**

- **Финансовая отчётность**: преобразуйте балансы, отчёты о прибылях и убытках (конкретные таблицы) в PDF для подготовки к аудиту.
- **Отчёты по продажам**: преобразуйте панели управления продажами или расчёты комиссионных в PDF-файлы, готовые к распространению.
- **Операционные метрики**: экспортируйте таблицы KPI и показатели эффективности в виде официальных PDF-отчётов.
- **Договорные данные**: экспортируйте ценовые таблицы и соглашения об уровне обслуживания из электронных таблиц в PDF-вложения.
- **Аудиторские следы**: сохраняйте таблицы финансовых данных в виде неизменяемых PDF-доказательств.
- **Сводки портфеля**: экспортируйте таблицы инвестиционной эффективности в PDF-отчёты, готовые для клиентов.
- **Отчёты по контролю качества**: экспортируйте таблицы данных инспекций в PDF для архивирования в системе соответствия требованиям.
- **Сводки по запасам**: преобразуйте таблицы уровней запасов в PDF для обзора руководством.

## **Почему следует использовать API преобразования таблицы в PDF?**

- **Удобен для разработчиков**: Aspose.Cells Cloud предоставляет SDK-библиотеки на множестве языков программирования, что обеспечивает быструю разработку, и сопровождается подробной документацией. По сравнению с созданием собственных решений для визуализации графиков, это существенно снижает объём работы по разработке.
- **Экономически эффективно**: вы можете преобразовывать табличные данные без предварительной загрузки всей книги, что экономит место в хранилище и снижает затраты.
- **Сохраняет сложное форматирование Excel** в универсально доступном формате PDF.

## **Как использовать API преобразования таблицы в PDF с помощью SDK?**

### Спецификация API преобразования таблицы в PDF

[Спецификация API преобразования таблицы в PDF](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToPDF) предоставляет публично доступное программное интерфейсное описание для выполнения REST-взаимодействий непосредственно из веб-браузера.
Вы можете использовать инструмент командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как выполнить вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/pdf?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.pdf
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 encoded)",
  "contentType": "MIME type",
  "fileDownloadName": "optional file name"
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — самый быстрый способ разработки, так как он абстрагирует низкоуровневые детали, позволяя преобразовывать табличные данные электронной таблицы в PDF-файл с минимальным объёмом кода. Ознакомьтесь с [репозиторием на GitHub](https://github.com/aspose-cells-cloud) для получения полного списка SDK Aspose.Cells Cloud.

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}