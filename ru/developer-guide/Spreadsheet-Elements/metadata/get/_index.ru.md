---
title: Получить метаданные из файла Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Получить без использования хранилища
type: docs
url: /ru/metadata/get/
keywords: Get properties from Excel files
description: Aspose.Cells Cloud REST API поддерживает получение свойств из файлов Excel. SDK поддерживает различные языки разработки. Они включают Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и Swift
weight: 23
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdown, Получение метаданных из файлов Excel
---
Этот REST API указывает на получение `metadata` из нескольких файлов Excel.

```bash

POST https://api.aspose.cloud/v3.0/cells/metadata/get

```

- **Параметр запроса**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
| тип| нить| ВСЕ/Встроенные/Пользовательские|

- **Параметр тела запроса**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
|файл Excel| файл данных|Файл данных сохраняется в первой части многокомпонентного контента.|

- **Ответ**

```bash
{
    [
        { 
            "Name":"test1",
            "Value":"test1",
            ...
        },
        { 
            "Name":"test2",
            "Value":"test3",
            ...
        }
    ]
}
```

- **Семейство облачных SDK**

 Использование SDK — лучший способ ускорить разработку. SDK заботится о низкоуровневых деталях и позволяет вам сосредоточиться на задачах вашего проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как выполнять вызовы веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}
