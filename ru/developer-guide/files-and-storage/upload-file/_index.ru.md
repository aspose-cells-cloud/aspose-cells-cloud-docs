---
title: Загрузить файл на номер Aspose
second_title: Developer Guide for File Uploa
linktitle: Загрузить файл
type: docs
url: /ru/upload-file/
keywords: Aspose, file upload, Excel API, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, upload Excel files, match blank cell
description: Подробное руководство по загрузке файлов с помощью Aspose Cells API, включая параметры и структуру ответа
weight: 100
kwords: Excel, Office Cloud, REST API, Электронная таблица, PDF, CSV, JSON, Markdown, сопоставление всех пустых ячеек на листе Excel, загрузка файлов
---
## **Aspose Cells API: Загрузить файл**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **Описание функции**

 The**загрузитьФайл** API позволяет разработчикам загружать файлы напрямую в облачное хранилище для обработки с помощью Aspose Cells.

###  Параметры запроса**загрузитьФайл** API есть

| Имя параметра| Тип| Путь/Строка запроса/Тело HTTP| Описание|
|:- |:- |:- |:- |
| ЗагрузитьФайлы| Файл| FormData|Загрузите файлы в облачное хранилище.|
| путь| Нить| Путь| Путь к месту назначения в облачном хранилище. Укажите путь, куда следует загрузить файл.|
| имя_хранилища| Нить| Запрос| Имя хранилища, куда будет загружен файл.|

### **Описание ответа**

```json
{
  "Name": "FilesUploadResult",
  "Description": [
    "File upload result"
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Uploaded",
      "Description": [
        "List of uploaded file names"
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "String",
        "ElementDataType": {
          "Identifier": "String",
          "Name": "string"
        },
        "Name": "container"
      }
    },
    {
      "Name": "Errors",
      "Description": [
        "List of errors."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "Error",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "Error",
          "Name": "class:error"
        },
        "Name": "container"
      }
    }
  ]
}
```

## Спецификация OpenAPI

 The[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/FileController/UploadFile) содержит подробное описание API, позволяющее разработчикам выполнять REST-взаимодействия непосредственно из веб-браузера.

## Aspose Cells API SDK

 Использование SDK повышает эффективность разработки за счёт управления деталями низкого уровня, позволяя разработчикам сосредоточиться на задачах проекта. Посетите[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

Следующие примеры кода иллюстрируют, как вызывать веб-службы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UploadFile.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UploadFile.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UploadFile.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UploadFile.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UploadFile.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UploadFile.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UploadFile.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UploadFile.go" >}}
{{< /tab >}}
{{< /tabs >}}
