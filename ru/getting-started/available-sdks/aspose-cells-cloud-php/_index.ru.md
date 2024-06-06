---
title: Aspose.Cells Cloud SDK для PH
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ru/available-sdks/aspose-cells-cloud-php/
description: Aspose.Cells Облако поддерживает Excel для создания, преобразования, объединения, разделения, защиты, операций с внутренними объектами и т. д.
weight: 30
kwords: Excel, Office Облако, REST API, электронная таблица, PDF, CSV, Json, Markdwon, PHP
---
 SDK имеет открытый исходный код и лицензируется по лицензии MIT. Вы можете получить доступ к исходному коду библиотеки PHP для Aspose.Cells Cloud.[здесь](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php).

# **Как использовать Cloud SDK Aspose.Cells для PHP**

Aspose.Cells Cloud SDK для PHP — это мощная библиотека, которая позволяет разработчикам манипулировать и обрабатывать файлы Microsoft Excel с помощью языка программирования Go. С помощью этого SDK вы можете создавать, редактировать и конвертировать документы Excel в облаке без установки дополнительного программного обеспечения или зависимостей на локальном компьютере.

В этой статье мы рассмотрим, как использовать Cloud SDK Aspose.Cells для PHP для выполнения некоторых распространенных задач, таких как создание новой книги Excel, вставка данных в ячейки и сохранение измененной книги в облаке.

## Начиная

 Прежде чем вы сможете начать использовать Cloud SDK для Go Aspose.Cells, вам необходимо настроить среду разработки и установить необходимые зависимости. Ссылаться на[статья](https://docs.aspose.cloud/cells/quickstart/) на веб-сайте Aspose, чтобы получить идентификатор клиента и секрет клиента.

## Как установить пакет PHP для облака Aspose.Cells

Вы можете установить Aspose.Cells Cloud SDK для PHP. Ниже приведены шаги:

- Добавьте Aspose.Cells Cloud в качестве зависимости к вашему файлу `composer.json`:

   ```json
   {
       "require": {
           "aspose/cells-cloud": "^24.3"
       }
   }
   ```

- Запустите обновление Composer, чтобы установить SDK:

   ```bash

   composer install

   ```

- Включите автозагрузчик Composer в свой код PHP:

   ```php

   require 'vendor/autoload.php';

   ```

## Как использовать пакет PHP для преобразования Xlsx в PDF

- Импортировать облачную библиотеку Aspose.Cells
 Начните с импорта необходимого пакета из Aspose.Cells Cloud PHP SDK в свой проект.
- Настройте клиент API с учетными данными
 Аутентифицируйте своего клиента API с помощью уникального идентификатора клиента и секретного кода клиента.
- Подготовьте параметры преобразования
 Определите параметры задачи преобразования, включая имя исходного файла, желаемый выходной формат и путь к папке хранения.
- Выполнить преобразование книги
 Вызовите процесс преобразования с помощью метода PostConvertWorkbook и обработайте ответ.

```PHP
<?php
require_once('vendor\autoload.php');
use \Aspose\Cells\Cloud\Api\CellsApi;
use \Aspose\Cells\Cloud\Request\PutConvertWorkbookRequest;

$cellsApi = new CellsApi(getenv("CellsCloudClientId"),getenv("CellsCloudClientSecret"),"v3.0",getenv("CellsCloudApiBaseUrl"));

$remoteFolder = "TestData/In";

$localName = "Book1.xlsx";
$remoteName = "Book1.xlsx";

$format = "csv";

$mapFiles = array ();
$mapFiles[$localName] = CellsApiTestBase::getfullfilename($localName);
CellsApiTestBase::ready(  $this->instance,$localName ,$remoteFolder . "/" . $remoteName ,  "");
 
$request = new PutConvertWorkbookRequest();
$request->setFile( $mapFiles);
$request->setFormat( $format);
$$cellsApi->putConvertWorkbook($request);
```
