---
title: Aspose.Cells Cloud SDK для пер.
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ru/available-sdks/aspose-cells-cloud-perl/
description: Aspose.Cells Облако поддерживает Excel для создания, преобразования, объединения, разделения, защиты, операций с внутренними объектами и т. д.
weight: 30
kwords: Excel, Office Облако, REST API, электронная таблица, PDF, CSV, Json, Markdwon, Perl
---
 SDK имеет открытый исходный код и лицензируется по лицензии MIT. Вы можете получить доступ к исходному коду библиотеки Perl для Aspose.Cells Cloud.[здесь](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl).


# **Как использовать библиотеку Perl облака Aspose.Cells**

Aspose.Cells Cloud SDK для Perl — это мощная библиотека, которая позволяет разработчикам манипулировать и обрабатывать файлы Microsoft Excel с помощью языка программирования Perl. С помощью этого SDK вы можете создавать, редактировать и конвертировать документы Excel в облаке без установки дополнительного программного обеспечения или зависимостей на локальном компьютере.

В этой статье мы рассмотрим, как использовать Cloud SDK Aspose.Cells для Perl для выполнения некоторых распространенных задач, таких как создание новой книги Excel, вставка данных в ячейки и сохранение измененной книги в облаке.

## Начиная

 Прежде чем вы сможете начать использовать Cloud SDK для Go Aspose.Cells, вам необходимо настроить среду разработки и установить необходимые зависимости. Ссылаться на[статья](https://docs.aspose.cloud/cells/quickstart/) на веб-сайте Aspose, чтобы получить идентификатор клиента и секрет клиента.

## Как установить пакет Perl для облака Aspose.Cells

Вы можете установить Aspose.Cells Cloud SDK для Perl с помощью команды ниже:

```Powershell

perl -MCPAN -e shell

install AsposeCellsCloud::CellsApi

```

## Как использовать пакет Perl для преобразования Xlsx в PDF

- Импортировать облачную библиотеку Aspose.Cells
 Начните с импорта необходимого пакета из Aspose.Cells Cloud Perl SDK в свой проект.
- Настройте клиент API с учетными данными
 Аутентифицируйте своего клиента API с помощью уникального идентификатора клиента и секретного кода клиента.
- Подготовьте параметры преобразования
 Определите параметры задачи преобразования, включая имя исходного файла, желаемый выходной формат и путь к папке хранения.
- Выполнить преобразование книги
 Вызовите процесс преобразования с помощью метода PostConvertWorkbook и обработайте ответ.

```Perl
use lib 'lib';
use strict;
use warnings;
use File::Slurp;
use MIME::Base64;
use AsposeCellsCloud::CellsApi;

my $config = AsposeCellsCloud::Configuration->new( client_id => $ENV{'CellsCloudClientId'}, client_secret => $ENV{'CellsCloudClientSecret'});
my $instance = AsposeCellsCloud::CellsApi->new(AsposeCellsCloud::ApiClient->new( $config));

my $remoteFolder = 'TestData/In';
  
my $localName = 'Book1.xlsx';
my $remoteName = 'Book1.xlsx';

my $upload_file_request = AsposeCellsCloud::Request::UploadFileRequest->new( 'UploadFiles'=>{ $localName => $localName  }  ,'path'=>$remoteFolder . '/' . $remoteName );
 
my $format = 'csv';

my $mapFiles = {};           

 $mapFiles->{$localName}= "TestData/".$localName ;

my $request = AsposeCellsCloud::Request::PutConvertWorkbookRequest->new();
$request->{file} =  $mapFiles;
$request->{format} =  $format;
$instance->put_convert_workbook(request=> $request);
```
