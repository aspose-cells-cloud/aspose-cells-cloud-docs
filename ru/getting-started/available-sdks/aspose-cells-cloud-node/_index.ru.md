---
title: Aspose.Cells Cloud SDK для Nod
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ru/available-sdks/aspose-cells-cloud-node/
description: Aspose.Cells Облако поддерживает Excel для создания, преобразования, объединения, разделения, защиты, операций с внутренними объектами и т. д.
weight: 30
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdwon, Node
---
 SDK имеет открытый исходный код и лицензируется по лицензии MIT. Вы можете получить доступ к исходному коду библиотеки Node для Aspose.Cells Cloud.[здесь](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node).


# **Как использовать библиотеку Node Aspose.Cells Cloud**

Aspose.Cells Cloud SDK для Node — это мощная библиотека, которая позволяет разработчикам манипулировать и обрабатывать файлы Microsoft Excel с помощью языка программирования Node. С помощью этого SDK вы можете создавать, редактировать и конвертировать документы Excel в облаке без установки дополнительного программного обеспечения или зависимостей на локальном компьютере.


В этой статье мы рассмотрим, как использовать Aspose.Cells Cloud SDK для Node для выполнения некоторых распространенных задач, таких как создание новой книги Excel, вставка данных в ячейки и сохранение измененной книги в облаке.

## Начиная

 Прежде чем вы сможете начать использовать Cloud SDK для Go Aspose.Cells, вам необходимо настроить среду разработки и установить необходимые зависимости. Ссылаться на[статья](https://docs.aspose.cloud/cells/quickstart/) на веб-сайте Aspose, чтобы получить идентификатор клиента и секрет клиента.

## Как установить пакет Node для облака Aspose.Cells

Вы можете установить Aspose.Cells Cloud SDK для Node с помощью npm. Ниже приведены шаги для npm:


```Powershell

npm install asposecellscloud

```

## Как добавить зависимости в конфигурацию пакета для Aspose.Cells Cloud

файл конфигурации узла: package.json

```Node

{
    "requires": true,
    "lockfileVersion": 1,
    "dependencies": {
        "@types/jest": "^26.0.24",
        "@types/request": "^2.48.7",
        "asposecellscloud": "24.4",
        "axios": "^1.5.1",
        "JSON": "^1.0.0",
        "mocha": "^10.2.0",
        "request": "^2.88.2",
        "request-debug": "^0.2.0"
    }
}

```

## Как использовать пакет Node для преобразования Xlsx в PDF

- Импортировать облачную библиотеку Aspose.Cells
 Начните с импорта необходимого пакета из Cloud NodeJS SDK Aspose.Cells в свой проект.
- Настройте клиент API с учетными данными
 Аутентифицируйте своего клиента API с помощью уникального идентификатора клиента и секретного кода клиента.
- Подготовьте параметры преобразования
 Определите параметры задачи преобразования, включая имя исходного файла, желаемый выходной формат и путь к папке хранения.
- Выполнить преобразование книги
 Вызовите процесс преобразования с помощью метода PostConvertWorkbook и обработайте ответ.

```javascript
var fs = require('fs');
var path = require('path');
const _ = require('asposecellscloud');

const cellsApi = new CellsApi(process.env.CellsCloudClientId, process.env.CellsCloudClientSecret,"v3.0",process.env.CellsCloudApiBaseUrl);

var remoteFolder = "TestData/In"
  
var localName = "Book1.xlsx"
var remoteName = "Book1.xlsx"

var localNameRequest = new  model.UploadFileRequest();
localNameRequest.uploadFiles ={localName:fs.createReadStream(localPath  + localName)};
localNameRequest.path = remoteFolder + "/" + remoteName ;
localNameRequest.storageName ="";
cellsApi.uploadFile(localNameRequest );
 
var format = "csv"

var mapFiles = {};           

 mapFiles[localName]= fs.createReadStream(localPath  +localName) ;

var request = new model.PutConvertWorkbookRequest();
request.file =  mapFiles;
request.format =  format;
return cellsApi.putConvertWorkbook(request).then((result) => {
    expect(result.response.statusCode).to.equal(200);
});
```
