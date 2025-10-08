---
title: Excel к Доку
second_title: Documen
linktitle: Excel к Доку
type: docs
url: /ruconvert-excel-file-to-docx-file/
keywords: Convert excel files to docx files
description: Aspose.Cells Cloud REST API поддерживает преобразование файлов Excel в CSV-файлы. SDK поддерживает различные языки разработки, включая Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и Swift.
weight: 90
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdown, Excel в Docx
---
Этот REST API указывает `convert` на файл электронной таблицы в формате docx.

**Параметр запроса**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
|пароль|нить| Пароль, необходимый для открытия файла Excel.|
|имя_хранилища|нить| Имя хранилища, где находится файл.|
|checkExcelRestriction|бул| Проверять ли ограничения файла Excel, когда пользователь изменяет ячейки, связанные с объектами.|

**Параметр тела запроса**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
|файл данных| файл данных|Файл данных сохраняется в первой части многочастного контента.|

**Ответ**

[FileInfo](/cells/ru/file-info/)

## REST API Спецификация

|**API**|**Тип**|**Описание**|**Swagger Link**|
|:- |:- |:- |:- |
|/cells/convert/docx|ПОЧТА|Конвертировать электронную таблицу в файл docx.|[PostConvertWorkbookToDocx](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToDocx)|

 The[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToDocx) определяет общедоступный программный интерфейс и позволяет осуществлять REST-взаимодействие непосредственно из веб-браузера.

 Вы можете использовать**cURL** Инструмент командной строки для лёгкого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как совершать вызовы в облако API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/docx" 
     -H "accept: multipart/form-data" 
     -H "Content-Type: multipart/form-data" 
     -H "x-aspose-client: curl" 
     -d {"File":{}}
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```

{
  "Filename": "xxxxxx.docx",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}

```

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

 Использование SDK — лучший способ ускорить разработку. SDK берёт на себя решение низкоуровневых задач и позволяет вам сосредоточиться на задачах проекта. Ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как совершать вызовы веб-служб Aspose.Cells с использованием различных SDK:
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

## Другие API реализуют эту функцию

[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)API позволяет сохранить файл MS Excel как CSV-файл с дополнительными настройками и сохранить результат в хранилище.

Этот файл REST API `convert` Excel в CSV.

[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) API позволяет преобразовать файл MS Excel в файл CSV с дополнительными настройками и сохранить результат в ответе.

Этот файл REST API `export` Excel в CSV.

[ПОЛУЧИТЬ /cells/{имя}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook  ) API позволяет преобразовать файл MS Excel в файл CSV с дополнительными настройками и сохранить результат в ответе.
