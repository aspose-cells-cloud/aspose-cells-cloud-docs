---
title: Копировать Folde
second_title: Documen
linktitle: Копировать Folde
type: docs
url: /ru/copy-folder/
keywords: Excel API, Copy Folder, Office Cloud, REST API, Spreadsheet Management, File Operation
description: Узнайте, как использовать CopyFolder API для эффективного копирования папок в облачной среде Aspose.Cells.
weight: 100
kwords: Excel, Office Cloud, REST API, Копировать папку, Управление файлами, PDF, CSV, JSON, Markdown, Сопоставление всех пустых ячеек на листе Excel
---
## **Excel API: Копировать папку**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/folder/copy/{srcPath}
```

### **Описание функции**

 The**КопироватьПапку**API позволяет пользователям создавать копии существующей папки в облачном хранилище Aspose.Cells. Эта функция необходима для эффективного управления файлами, позволяя пользователям создавать резервные копии или организовывать свою работу без ручного переноса содержимого.

###  Параметры запроса**КопироватьПапку** API есть

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody| Описание|
|----------------|--|-----------------------|-------------------------------------|
| srcPath| Нить| Путь| Путь к исходной папке для копирования.|
| destPath| Нить| Запрос| Путь, по которому будет создана новая папка.|
| srcStorageName| Нить| Запрос| Имя хранилища, содержащего исходную папку.|
| destStorageName| Нить| Запрос| Имя целевого хранилища, куда следует скопировать папку.|

### **Описание ответа**

```json
{
Void
}
```

## Спецификация OpenAPI

 The[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/FolderController/CopyFolder) определяет общедоступный программный интерфейс и позволяет осуществлять REST-взаимодействие непосредственно из веб-браузера.

## Excel API SDK

 Использование SDK — лучший способ ускорить разработку. SDK берёт на себя решение низкоуровневых задач и позволяет вам сосредоточиться на задачах проекта. Ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как совершать вызовы веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CopyFolder.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CopyFolder.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CopyFolder.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CopyFolder.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CopyFolder.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CopyFolder.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CopyFolder.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CopyFolder.go" >}}
{{< /tab >}}
{{< /tabs >}}
