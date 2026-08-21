---
title: "Преобразование диаграммы Excel в изображение – REST API Aspose.Cells Cloud"
type: docs
url: /ru/charts/to-image/
aliases: [  /ru/convert-charts-to-image/ ]
weight: 50
keywords: "Aspose.Cells Cloud, диаграмма в изображение, преобразование диаграммы Excel, REST API, формат изображения, PNG, JPEG, BMP, TIFF, GIF"
description: "Узнайте, как преобразовать объекты диаграмм Excel в изображения форматов PNG, JPEG, BMP, TIFF или GIF с помощью REST API Aspose.Cells Cloud. Включает подробности эндпоинта, параметры, пример cURL, фрагменты SDK, пример ответа и обработку ошибок."
ArticleTitle: "Преобразование диаграммы Excel в изображение – REST API Aspose.Cells Cloud"
---

Этот REST API демонстрирует, как преобразовать **диаграмму Excel** в изображение с помощью **Aspose.Cells Cloud**.

## API PutWorksheetAddChart

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartNumber}?format={format}
```

Поддерживаемые форматы изображений: `png`, `jpeg`, `bmp`, `tiff` и `gif`.

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификацию по токену JWT</a>.

### Параметры запроса

| Имя параметра | Тип    | Расположение | Описание                   |
|---------------|--------|-------------|----------------------------|
| name          | string | path        | Имя документа.             |
| sheetName     | string | path        | Имя рабочего листа.        |
| chartNumber   | integer| path        | Номер диаграммы.           |
| format        | string | query       | Формат экспортируемого файла. |
| folder        | string | query       | Папка документа.           |
| storageName   | string | query       | Имя хранилища.             |

### **Ответ**

Эндпоинт возвращает файл изображения в запрошенном формате в виде бинарного потока (например, `byte[]`). Заголовок `Content-Type` ответа соответствует выбранному формату изображения: `image/png`, `image/jpeg` и т.д.

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                               |
|-----|-----------------------------|--------------------------------------------------------|
| 200 | OK (ОК)                     | Фильтр применён успешно; ответ содержит детали операции. |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизован) | Недействительный или отсутствующий токен JWT.          |
| 413 | Payload Too Large (Слишком большой payload) | Загруженный файл превышает лимит размера. |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера. |

## Как использовать API PutWorksheetAddChart с SDK

### Спецификация API PutWorksheetAddChart

<a href="https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChart" rel="noopener noreferrer">Спецификация OpenAPI</a> определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Приведённый ниже пример показывает, как выполнять вызовы в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0?format=jpg" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <ваш_jwt_токен>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```text
byte[]
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — лучший способ ускорить разработку. SDK берёт на себя обработку низкоуровневых деталей, позволяя сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">репозитории GitHub</a>.

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Node.js" tabName5="Python" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-ConvertChartToImage-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetWorksheetChartWithFormat-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_chart_in_specified_format-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-ConvertChartToImage-1.js" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ConvertChartToImage.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-ConvertChartToImage-convert-chart-to-image.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

Пример появится в ближайшее время.

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-ConvertChartToImage-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "d22256010a610e1351ab15969a7adeef" >}}

{{< /tab >}}

{{< /tabs >}}
---