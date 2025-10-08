---
title: Копировать файл - Excel AP
second_title: Documen
linktitle: Копировать файл
type: docs
url: /ru/copy-file/
keywords: Excel API, Office Cloud, REST API, Spreadsheet Copy, PDF Conversion, CSV Export, JSON Handling, Markdown Support, Copy Excel File, Match Blank Cell
description: Узнайте, как использовать CopyFile API для Excel для эффективного копирования электронных таблиц и обработки различных форматов файлов.
weight: 100
kwords: Excel API, Office Облако, REST API, Копирование электронных таблиц, PDF Преобразование, Экспорт CSV, Обработка JSON, Поддержка Markdown, Копирование файла Excel, Сопоставление пустых ячеек
---
## **Excel API: Копировать файл**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/file/copy/{srcPath}
```

### **Описание функции**

 The**copyFile** API позволяет пользователям дублировать файл Excel из указанного исходного пути в целевой путь, поддерживая различные варианты хранения.

###  Параметры запроса**copyFile** API есть

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody|Описание|
|-------------- ||--------------------- |-------------------------------------- |
| srcPath| Нить| Путь| Исходный путь файла, который необходимо скопировать.|
| destPath| Нить| Запрос| Путь назначения, по которому будет сохранён файл.|
| srcStorageName| Нить| Запрос| Имя исходного хранилища.|
| destStorageName| Нить| Запрос| Имя целевого хранилища.|
| versionId| Нить| Запрос| Необязательный идентификатор версии файла для копирования.|

### **Описание ответа**

```json
{
Void
}
```

## Спецификация OpenAPI

 The[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/FileController/CopyFile) определяет общедоступный программный интерфейс и позволяет осуществлять REST-взаимодействие непосредственно из веб-браузера.

## Excel API SDK

 Использование SDK — лучший способ ускорить разработку. SDK управляет низкоуровневыми деталями, позволяя вам сосредоточиться на задачах проекта. Ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как совершать вызовы веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CopyFile.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CopyFile.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CopyFile.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CopyFile.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CopyFile.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CopyFile.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CopyFile.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CopyFile.go" >}}
{{< /tab >}}
{{< /tabs >}}
