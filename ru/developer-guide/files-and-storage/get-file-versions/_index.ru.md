---
title: Получить версию файла
second_title: Documen
linktitle: Получить версию файла
type: docs
url: /ru/get-file-versions/
keywords: file versions, Excel API, Office Cloud, REST API, spreadsheet management, document histor
description: Извлекайте и управляйте версиями файлов, хранящихся в облаке Aspose.Cells, улучшая управление документами и совместную работу.
weight: 100
kwords: Получить версии файлов, Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, JSON, Markdown, управление документами
---
## **Excel API: Получить версии файлов**

```
GET http://api.aspose.cloud/v4.0/cells/storage/version/{path}
```

### **Описание функции**

 The**GetFileVersions** API позволяет пользователям получать различные версии указанного файла, хранящегося в облаке Aspose.Cells. Эта функция критически важна для поддержания целостности документа и отслеживания изменений с течением времени.

###  Параметры запроса**GetFileVersions** API есть

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody| Описание|
|:- |:- |:- |:- |
| путь| Нить| Путь| Путь к файлу, для которого необходимо получить версии.|
| имя_хранилища| Нить| Запрос| Имя хранилища, где находится файл.|

### **Описание ответа**

```json
{
  "Name": "FileVersions",
  "Description": [
    "Contains a list of file versions for the specified document."
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Value",
      "Description": [
        "A collection of file version details."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "FileVersion",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "FileVersion",
          "Name": "class:fileversion"
        },
        "Name": "container"
      }
    }
  ]
}
```

## Спецификация OpenAPI

 The[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/StorageController/GetFileVersions)предоставляет комплексный программный интерфейс для выполнения REST-взаимодействий непосредственно из веб-браузера.

## Excel API SDK

 Использование SDK оптимизирует разработку, абстрагируя низкоуровневые сложности и позволяя разработчикам сосредоточиться на основных функциях.[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

Следующие примеры кода иллюстрируют, как взаимодействовать с веб-сервисами Aspose.Cells на различных языках программирования:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetFileVersions.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetFileVersions.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetFileVersions.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetFileVersions.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetFileVersions.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetFileVersions.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetFileVersions.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetFileVersions.go" >}}
{{< /tab >}}
{{< /tabs >}}
