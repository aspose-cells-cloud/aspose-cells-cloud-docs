---
title: Получить список файлов - Aspose.Cells AP
second_title: Developer Guide for Aspose.Cell
linktitle: Получить список файлов
type: docs
url: /ru/get-files-list/
keywords: Aspose.Cells API, Get Files List, REST API, Excel File Management, Cloud Storage, File Retrieval, Programming Interfac
description: Узнайте, как получить список файлов из указанной папки с помощью Aspose.Cells API. В этом руководстве приведены подробные сведения о параметрах запроса, структуре ответа и примеры кода на различных языках программирования.
weight: 100
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, JSON, Markdown, Управление файлами в облаке, Получение списка файлов
---
## **Excel API: Получить список файлов**

```
GET http://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **Описание функции**

 The**получитьСписокФайлов**API позволяет пользователям получать полный список файлов и папок, содержащихся в указанном каталоге в облачном хранилище Aspose.Cells. Эта конечная точка критически важна для эффективного управления файлами и поддерживает различные форматы файлов.

###  Параметры запроса**получитьСписокФайлов** API есть

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody| Описание|
|:- |:- |:- |:- |
| путь| Нить| Путь| Путь к папке в облачном хранилище, из которой следует извлечь список файлов.|
| имя_хранилища| Нить| Запрос| Имя хранилища, к которому необходимо получить доступ.|

### **Описание ответа**

```json
{
  "Name": "FilesList",
  "Description": [
    "Files list"
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Value",
      "Description": [
        "Files and folders contained by the specified StorageFile."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "StorageFile",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "StorageFile",
          "Name": "class:storagefile"
        },
        "Name": "container"
      }
    }
  ]
}
```

## Спецификация OpenAPI

 The[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/FolderController/GetFilesList) определяет общедоступный программный интерфейс, который позволяет взаимодействовать с REST непосредственно из веб-браузера, что упрощает интеграцию и тестирование.

## Excel API SDK

 Использование SDK — оптимальный подход к ускорению процесса разработки. SDK управляет низкоуровневыми деталями, позволяя вам сосредоточиться на задачах проекта. Полный список облачных SDK Aspose.Cells можно найти на сайте[Репозиторий GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода иллюстрируют, как вызывать веб-службы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetFilesList.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetFilesList.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetFilesList.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetFilesList.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetFilesList.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetFilesList.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetFilesList.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetFilesList.go" >}}
{{< /tab >}}
{{< /tabs >}}
