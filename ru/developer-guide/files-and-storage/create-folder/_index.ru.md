---
title: Создать папку в Excel AP
second_title: Developer Guide for Aspose.Cell
linktitle: Создать папку
type: docs
url: /ru/create-folder/
keywords: Excel API, Create Folder, Office Cloud, REST API, Cloud Storage, Folder Management, Excel, Spreadsheet, PDF, CSV, JSON, Markdow
description: Узнайте, как создать папку в Excel API с помощью REST
weight: 100
kwords: Создание папки, Excel API, Office Облако, REST API, Облачное хранилище, Управление папками, Сопоставление всех пустых ячеек на листе Excel
---
## **Excel API: Создать папку**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **Описание функции**

 The**создатьПапку** API позволяет пользователям создавать новую папку по указанному пути в облачном хранилище Excel API. Эта функция необходима для организации файлов и поддержания структурированного каталога.

###  Параметры запроса**создатьПапку** API есть

| Имя параметра| Тип| Путь/Строка запроса/Тело HTTP| Описание|
|----------|--|------------------------|---------------------------------|
| путь| Нить| Путь| Путь, по которому будет создана папка.|
| имя_хранилища| Нить| Запрос| Имя используемого хранилища.|

### **Описание ответа**

```json
{
Void
}
```

## Спецификация OpenAPI

 The[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/FolderController/CreateFolder) определяет общедоступный программный интерфейс и позволяет осуществлять REST-взаимодействие непосредственно из веб-браузера.

## Excel API SDK

 Использование SDK — лучший способ ускорить разработку. SDK управляет низкоуровневыми деталями и позволяет вам сосредоточиться на задачах проекта. Ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как совершать вызовы веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateFolder.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateFolder.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateFolder.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateFolder.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateFolder.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateFolder.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateFolder.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateFolder.go" >}}
{{< /tab >}}
{{< /tabs >}}
