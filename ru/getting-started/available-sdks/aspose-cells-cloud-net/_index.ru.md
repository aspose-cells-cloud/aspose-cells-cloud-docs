---
title: Aspose.Cells Cloud SDK для Ne
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ru/available-sdks/aspose-cells-cloud-net/
description: Aspose.Cells Облако поддерживает Excel для создания, преобразования, объединения, разделения, защиты, операций с внутренними объектами и т. д.
weight: 30
kwords: Excel, Office Облако, REST API, электронная таблица, PDF, CSV, Json, Markdwon, Net
---
 SDK имеет открытый исходный код и лицензируется по лицензии MIT. Вы можете получить доступ к исходному коду библиотеки Net для Aspose.Cells Cloud.[здесь](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet).


# **Как использовать сетевую библиотеку Aspose.Cells Cloud**

Aspose.Cells Cloud SDK для Net — это мощная библиотека, которая позволяет разработчикам манипулировать и обрабатывать файлы Microsoft Excel с помощью языка программирования Net. С помощью этого SDK вы можете создавать, редактировать и конвертировать документы Excel в облаке без установки дополнительного программного обеспечения или зависимостей на локальном компьютере.

В этой статье мы рассмотрим, как использовать Aspose.Cells Cloud SDK для Net для выполнения некоторых распространенных задач, таких как создание новой книги Excel, вставка данных в ячейки и сохранение измененной книги в облаке.

## Начиная

 Прежде чем вы сможете начать использовать Cloud SDK для Go Aspose.Cells, вам необходимо настроить среду разработки и установить необходимые зависимости. Ссылаться на[статья](https://docs.aspose.cloud/cells/quickstart/) на веб-сайте Aspose, чтобы получить идентификатор клиента и секрет клиента.

## Как установить сетевой пакет для облака Aspose.Cells

Вы можете установить Aspose.Cells Cloud SDK for Net, используя nuget. Ниже приведены шаги для nuget:

```nuget

Install-Package Aspose.Cells-Cloud

```

Вы также можете установить Aspose.Cells Cloud SDK for Net с помощью dotnet. Ниже приведены шаги для dotnet:

```powershell

dotnet add package Aspose.Cells-Cloud 

```

## Как использовать пакет Net для преобразования Xlsx в PDF

- Импортировать облачную библиотеку Aspose.Cells
 Начните с импорта необходимого пакета из Cloud DotNet SDK Aspose.Cells в свой проект.
- Настройте клиент API с учетными данными
 Аутентифицируйте своего клиента API с помощью уникального идентификатора клиента и секретного кода клиента.
- Подготовьте параметры преобразования
 Определите параметры задачи преобразования, включая имя исходного файла, желаемый выходной формат и путь к папке хранения.
- Выполнить преобразование книги
 Вызовите процесс преобразования с помощью метода PostConvertWorkbook и обработайте ответ.

### **Образец кода**

```CSharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using Aspose.Cells.Cloud.SDK.Request;
using System;
using System.IO;
using System.Collections.Generic;

CellsApi cellsApi = new CellsApi("xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx");
string remoteFolder = "TestData/In";

string localName = "Book1.xlsx";
string remoteName = "Book1.xlsx";

this.UploadFile( localName, remoteFolder + "/" + remoteName, "");

IDictionary<string, Stream> mapFiles =new Dictionary<string,Stream>(); 
AddFileParameter(localName,mapFiles);       
var request = new PutConvertWorkbookRequest(
    file: mapFiles,
    format: format
);
this.CellsApi.PutConvertWorkbook(request);
```
