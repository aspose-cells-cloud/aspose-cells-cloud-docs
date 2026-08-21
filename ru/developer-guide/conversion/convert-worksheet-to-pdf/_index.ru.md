---
title: "Aspose.Cells Cloud Web API – Преобразование локального листа Excel в файл PDF – Бесплатный онлайн-инструмент"
second_title: "Документ"
ArticleTitle: "Как преобразовать лист локальной электронной таблицы в файл PDF: Пошаговое руководство"
linktitle: "Преобразовать лист в PDF"
type: docs
url: /convert-worksheet-to-pdf/
keywords: "Aspose.Cells, Excel в PDF, преобразование листа, REST API, облачное преобразование, PDF для электронной таблицы, конечная точка API, генерация PDF"
description: "Используйте Aspose.Cells Cloud API для быстрого и безопасного преобразования листа из локального файла Excel в документ PDF."
weight: 100
---

Экспортируйте лист из локального файла Excel в файл [PDF](https://docs.fileformat.com/pdf/) с помощью облачного API.

## **API преобразования листа в PDF**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе токена JWT</a>.

### **Параметры запроса:**

| Имя параметра | Тип   | Путь/Строка запроса/Тело HTTP-запроса | Описание                                                               |
|---------------|-------|---------------------------------------|------------------------------------------------------------------------|
| Spreadsheet   | Файл  | FormData                              | Загрузка файла электронной таблицы.                                    |
| worksheet     | Строка | Запрос                                | Имя листа в электронной таблице.                                       |
| outPath       | Строка | Запрос                                | (Необязательно) Путь к папке для сохранения рабочей книги; по умолчанию null. |
| outStorageName| Строка | Запрос                                | Имя хранилища для выходного файла.                                     |
| fontsLocation | Строка | Запрос                                | Использование пользовательских шрифтов для PDF.                        |
| region        | Строка | Запрос                                | Определение настройки региона электронной таблицы.                     |
| password      | Строка | Запрос                                | Пароль, необходимый для открытия файла электронной таблицы.           |

### **Ответ**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

**Коды HTTP-статуса**

| Код | Значение               | Описание                                                             |
|-----|------------------------|----------------------------------------------------------------------|
| 200 | OK (ОК)               | Фильтр применён успешно; ответ содержит сведения об операции.       |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизован) | Недействительный или отсутствующий токен JWT.                       |
| 413 | Payload Too Large (Слишком большой payload) | Загруженный файл превышает предельный размер.                      |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                                    |

## **Где следует использовать API преобразования листа в PDF?**

- **Финансовая отчётность**: Преобразование балансов, отчётов о прибылях и убытках (конкретные таблицы) в PDF для подготовки документов к аудиту.
- **Отчёты о продажах**: Преобразование панелей управления продажами или расчётов комиссионных в распределяемые PDF-файлы.
- **Операционные метрики**: Экспорт таблиц ключевых показателей эффективности (KPI) и метрик производительности в виде официальных PDF-отчётов.
- **Договорные данные**: Экспорт ценовых таблиц и соглашений об уровне обслуживания из электронных таблиц в виде PDF-вложений.
- **Журналы аудита**: Сохранение финансовых листов в виде неизменяемых PDF-доказательств.
- **Сводки портфелей**: Экспорт таблиц производительности инвестиций в виде готовых к отправке клиентам PDF-выписок.
- **Отчёты по контролю качества**: Экспорт листов инспекций в PDF для хранения в архивах соответствия требованиям.
- **Сводки по запасам**: Преобразование листов склада в PDF для обзора руководством.

## **Почему следует использовать API преобразования листа в PDF?**

- **Удобен для разработчиков**: Aspose.Cells Cloud предоставляет библиотеки SDK на множестве языков программирования, что обеспечивает быструю разработку, и сопровождается подробной документацией. По сравнению с созданием собственных решений для визуализации диаграмм, это существенно снижает объём работы по разработке.
- **Экономически эффективно**: Можно преобразовывать табличные данные без предварительной загрузки рабочей книги, что экономит место в хранилище и снижает затраты.
- **Сохранение форматирования**: Сохраняет сложное форматирование Excel в универсально доступном формате PDF.

## **Как использовать API преобразования листа в PDF с SDK?**

### Спецификация API преобразования листа в PDF

[Спецификация API преобразования листа в PDF](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToPDF) предоставляет публично доступный программный интерфейс и позволяет взаимодействовать с REST API непосредственно из веб-браузера.

Вы можете использовать инструмент командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Пример ниже показывает, как делать вызовы в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/json?worksheet=Sheet1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.json
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

Использование SDK — самый быстрый способ разработки, так как он скрывает низкоуровневые детали, позволяя преобразовывать табличные данные электронной таблицы в PDF-файл с минимальным объёмом кода. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода иллюстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorksheetToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorksheetToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorksheetToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorksheetToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorksheetToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorksheetToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorksheetToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorksheetToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}