---
title: Хранилище существует
second_title: Documen
linktitle: Хранилище существует
type: docs
url: /ru/storage-exists/
keywords: Excel API, Storage Exists, REST API, Office Cloud, Cloud Storage, Excel Worksheet, Check Storage, Data Management, API Integratio
description: Узнайте, как проверить наличие хранилища с помощью REST Aspose.Cells API. В этом руководстве представлены подробные сведения о конечной точке API, параметры запроса и описания ответов.
weight: 100
kwords: Excel, Office Cloud, REST API, Электронная таблица, PDF, CSV, JSON, Markdown, Сопоставление всех пустых ячеек на листе Excel
---
## **Excel API : Хранилище существует**

```
GET http://api.aspose.cloud/v4.0/cells/storage/{storageName}/exist
```

### **Описание функции**

 The**хранилище существует**API проверяет наличие указанного хранилища в облачном сервисе Aspose.Cells. Эта функция критически важна для обеспечения безошибочного выполнения всех операций, зависящих от хранилища.

###  Параметры запроса**хранилище существует** API есть

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody| Описание|
|:- |:- |:- |:- |
|имя_хранилища|Нить|Путь|Имя хранилища, существование которого необходимо проверить.|

### **Описание ответа**

```json
{
  "Name": "StorageExist",
  "Description": [
    "Indicates whether the specified storage exists."
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Exists",
      "Description": [
        "Indicates if the storage exists.",
        "This property returns true if the storage is present; otherwise, it returns false."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Boolean",
        "Name": "boolean"
      }
    }
  ]
}
```

## Спецификация OpenAPI

 The[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/StorageController/StorageExists) определяет общедоступный программный интерфейс, позволяющий разработчикам легко взаимодействовать с REST API непосредственно из веб-браузера.

## Excel API SDK

 Использование SDK — наиболее эффективный подход к ускорению разработки. SDK абстрагирует низкоуровневые детали реализации, позволяя разработчикам сосредоточиться на задачах проекта. Полный список доступных облачных SDK Aspose.Cells можно найти на сайте[Репозиторий GitHub](https://github.com/aspose-cells-cloud).

В следующих примерах кода показано, как совершать вызовы API к веб-сервисам Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_StorageExists.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_StorageExists.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_StorageExists.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_StorageExists.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_StorageExists.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_StorageExists.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_StorageExists.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_StorageExists.go" >}}
{{< /tab >}}
{{< /tabs >}}
