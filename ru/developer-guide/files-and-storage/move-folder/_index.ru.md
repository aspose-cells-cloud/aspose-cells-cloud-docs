---
title: Переместить Складку
second_title: Documen
linktitle: Переместить Складку
type: docs
url: /ru/move-folder/
keywords: Move folder API, Excel API, Folder management, REST API, Aspose.Cells, Cloud storag
description: В этой документации представлено подробное руководство по использованию Move Folder API для управления папками в облачном хранилище Aspose.Cells.
weight: 100
kwords: Excel API, Перемещение папки API, Office Облако, REST API, Управление электронными таблицами, PDF, CSV, JSON, Markdown, Сопоставление всех пустых ячеек на листе Excel
---
## **Excel API: Переместить папку**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/folder/move/{srcPath}
```

### **Описание функции**

Этот код API позволяет пользователям перемещать папки из одного места в другое в пределах облачного хранилища Aspose.Cells. Он необходим для эффективной организации файлов и управления облачным хранилищем.

###  Параметры запроса**переместить папку** API есть

| Имя параметра| Тип| Путь/Строка запроса/Тело HTTP| Описание|
|----------------|--|------------------------|--------------------------------------------------------|
| srcPath| Нить| Путь| Исходный путь к папке, которую необходимо переместить.|
| destPath| Нить| Запрос| Путь назначения, куда следует переместить папку.|
| srcStorageName| Нить| Запрос| Имя исходного хранилища.|
| destStorageName| Нить| Запрос| Имя целевого хранилища.|

### **Описание ответа**

```json
{
Void
}
```

## Спецификация OpenAPI

 The[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/FolderController/MoveFolder) определяет общедоступный программный интерфейс и позволяет осуществлять REST-взаимодействие непосредственно из веб-браузера.

## Excel API SDK

 Использование SDK — лучший способ ускорить разработку. SDK берёт на себя решение низкоуровневых задач и позволяет вам сосредоточиться на задачах проекта. Ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как совершать вызовы веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MoveFolder.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MoveFolder.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MoveFolder.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MoveFolder.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MoveFolder.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MoveFolder.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MoveFolder.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MoveFolder.go" >}}
{{< /tab >}}
{{< /tabs >}}
