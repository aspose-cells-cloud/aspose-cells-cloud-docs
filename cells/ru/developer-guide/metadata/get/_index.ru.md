---
title: Получить метаданные из файла Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Получить без использования хранилища
type: docs
url: /ru/metadata/get/
keywords: Get properties from Excel files
description: Aspose.Cells Cloud REST API поддерживает получение свойств из файлов Excel. SDK поддерживает различные языки разработки. К ним относятся Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и swift.
weight: 23
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
|файл Excel| файл данных|Файл данных сохраняется в первой части составного содержимого.|

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

 Использование SDK — лучший способ ускорить разработку. SDK позаботится о низкоуровневых деталях и позволит вам сосредоточиться на задачах вашего проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) полный список Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как выполнять вызовы веб-служб Aspose.Cells с помощью различных SDK.


{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Metadata-Get.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-MetaData-Get.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LiteCells-Metadata-Get.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}


{{< /tab >}}

{{< tab tabNum="5" >}}


{{< /tab >}}

{{< tab tabNum="6" >}}


{{< /tab >}}

{{< tab tabNum="7" >}}


{{< /tab >}}

{{< tab tabNum="8" >}}


{{< /tab >}}
{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "LiteCellsMetadata-Get.py" >}}
{{< /tab >}}
{{< /tabs >}}
