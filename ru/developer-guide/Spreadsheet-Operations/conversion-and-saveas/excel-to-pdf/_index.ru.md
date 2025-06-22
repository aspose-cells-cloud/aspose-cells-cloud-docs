---
title: Excel в ПД
second_title: Aspose.Cells Cloud Documen
linktitle: Excel в ПД
type: docs
url: /ru/convert-excel-file-to-pdf-file/
aliases: [/convert-excel-file-to-pdf-in-cloud/,/convert/excel-to-pdf/]
keywords: Convert excel files to pdf files
description: Aspose.Cells Cloud REST API поддерживает преобразование файлов Excel в файлы PDF. SDK поддерживает различные языки разработки. Они включают Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и Swift
weight: 80
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdown, Excel по PDF
---
Этот REST API указывает `convert` на файл электронной таблицы в формате PDF.

**Параметр запроса**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
|пароль|нить| Пароль, необходимый для открытия файла Excel.|
|имя_хранилища|нить| Имя хранилища, где находится файл.|
|checkExcelОграничение|бул| Проверять ли ограничения файла Excel, когда пользователь изменяет объекты, связанные с ячейками.|

**Параметр тела запроса**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
|файл данных| файл данных|Файл данных сохраняется в первой части многокомпонентного контента.|

**Ответ**

[Информация о файле](/cells/ru/file-info/)

## REST API Спецификация

|**API**|**Тип**|**Описание**|**Ссылка Swagger**|
|:- |:- |:- |:- |
|/ячейки/конвертировать/pdf|ПОЧТА|Преобразуйте электронную таблицу в PDF-файл.|[PostConvertWorkbookToPDF](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPDF)|

 The[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPDF) определяет общедоступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

 Вы можете использовать**cURL** Инструмент командной строки для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как совершать вызовы в Cloud API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/pdf" 
     -H "accept: multipart/form-data" 
     -H "Content-Type: multipart/form-data" 
     -H "x-aspose-client: curl" 
     -d {"File":{}}
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```

{
  "Filename": "xxxxxx.pdf”,
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}

```

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

 Использование SDK — лучший способ ускорить разработку. SDK заботится о низкоуровневых деталях и позволяет вам сосредоточиться на задачах вашего проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как выполнять вызовы веб-служб Aspose.Cells с использованием различных SDK:
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPdf.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPdf.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPdf.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPdf.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPdf.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPdf.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPdf.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPdf.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Другие API реализуют эту функцию

|**API**|**Тип**|**Описание**|**Ссылка Swagger**|
|:- |:- |:- |:- |
|/ячейки/преобразовать|ПОМЕЩАТЬ|Конвертирует рабочую книгу из содержимого запроса в некоторый формат|[PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)|

[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) API позволяет сохранить файл MS Excel как файл PDF с дополнительными настройками и сохранить результат в хранилище.

Этот файл REST API `convert` Excel в PDF.

[РАЗМЕСТИТЬ /ячейки/конвертировать](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) API позволяет преобразовать файл MS Excel в файл PDF с дополнительными настройками и сохранить результат в ответе.

Этот файл REST API `export` Excel в PDF.

[ПОЛУЧИТЬ /cells/{имя}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook  ) API позволяет преобразовать файл MS Excel в файл PDF с дополнительными настройками и сохранить результат в ответе.

 Эти[PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook), [GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook), [PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) API определяют общедоступный программный интерфейс и позволяют выполнять REST-взаимодействия непосредственно из веб-браузера.
