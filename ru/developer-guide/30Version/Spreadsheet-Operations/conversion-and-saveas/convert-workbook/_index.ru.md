---
title: Конвертировать файл Excel в другой формат
second_title: Documen
linktitle: Преобразовать электронную таблицу
type: docs
url: /ru/convert-a-spread-file-to-different-formats/
keywords: Convert excel files to kinds of format files
description: Aspose.Cells Cloud REST API поддерживает преобразование файлов Excel в различные форматы. SDK поддерживает различные языки разработки, включая Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и Swift.
weight: 10
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdown, Конвертация Excel
---
Этот REST API указывает `convert` на файл Excel в другом формате. Он поддерживает различные форматы. Он также может задать параметры страницы и сохранить параметры перед конвертацией.

**Параметр тела запроса**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
|[ConvertWorkbookOptions](/cells/ru/convert-workbook-options/)| объект| Параметры преобразования рабочей книги.|

**Ответ**

[FileInfo](/cells/ru/file-info/)

## ОТДЫХ API

|**API**|**Тип**|**Описание**|**Swagger Link**|
|:- |:- |:- |:- |
|/клетки/конвертировать|ПОЧТА|Преобразует рабочую книгу из содержимого запроса в определенный формат|[PostConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PostConvertWorkBook)|

 The[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostConvertWorkBook) определяет общедоступный программный интерфейс и позволяет осуществлять REST-взаимодействие непосредственно из веб-браузера.

 Вы можете использовать**cURL** Инструмент командной строки для лёгкого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как совершать вызовы в облако API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/convert" 
     -H "accept: multipart/form-data" 
     -H "Content-Type: multipart/form-data" 
     -H "x-aspose-client: curl" 
     -d {}
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```

{
  "Filename": "filename",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}

```

## Семейство облачных SDK

 Использование SDK — лучший способ ускорить разработку. SDK берёт на себя решение низкоуровневых задач и позволяет вам сосредоточиться на задачах проекта. Ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как совершать вызовы веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
