---
title: Aspose.Cells Cloud SDK за руб.
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ru/available-sdks/aspose-cells-cloud-ruby/
description: Aspose.Cells Облако поддерживает Excel для создания, преобразования, объединения, разделения, защиты, операций с внутренними объектами и т. д.
weight: 30
kwords: Excel, Office Облако, REST API, электронная таблица, PDF, CSV, Json, Markdwon, Ruby
---
 SDK имеет открытый исходный код и лицензируется по лицензии MIT. Вы можете получить доступ к исходному коду библиотеки Ruby по адресу Aspose.Cells Cloud.[здесь](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby).

# **Как использовать Aspose.Cells Cloud SDK для Ruby**

Aspose.Cells Cloud SDK для Ruby — это мощная библиотека, которая позволяет разработчикам манипулировать и обрабатывать файлы Microsoft Excel с помощью языка программирования Ruby. С помощью этого SDK вы можете создавать, редактировать и конвертировать документы Excel в облаке без установки дополнительного программного обеспечения или зависимостей на локальном компьютере.

В этой статье мы рассмотрим, как использовать Cloud SDK Aspose.Cells для Ruby для выполнения некоторых распространенных задач, таких как создание новой книги Excel, вставка данных в ячейки и сохранение измененной книги в облаке.

## Начиная

 Прежде чем вы сможете начать использовать Cloud SDK для Go Aspose.Cells, вам необходимо настроить среду разработки и установить необходимые зависимости. Ссылаться на[статья](https://docs.aspose.cloud/cells/quickstart/) на веб-сайте Aspose, чтобы получить идентификатор клиента и секрет клиента.

## Как установить пакет Ruby для облака Aspose.Cells

Вы можете установить Aspose.Cells Cloud SDK для Ruby с помощью следующей команды:

```bash

    gem install aspose_cells_cloud
  
 ```

## Как использовать пакет Ruby для преобразования Xlsx в PDF

- Импортировать облачную библиотеку Aspose.Cells
 Начните с импорта необходимого пакета из Aspose.Cells Cloud Python SDK в свой проект.
- Настройте клиент API с учетными данными
 Аутентифицируйте своего клиента API с помощью уникального идентификатора клиента и секретного кода клиента.
- Подготовьте параметры преобразования
 Определите параметры задачи преобразования, включая имя исходного файла, желаемый выходной формат и путь к папке хранения.
- Выполнить преобразование книги
 Вызовите процесс преобразования с помощью метода PostConvertWorkbook и обработайте ответ.

```Ruby
require 'openssl'
require 'bundler'
require 'aspose_cells_cloud'

@instance = AsposeCellsCloud::CellsApi.new(ENV['CellsCloudClientId'], ENV['CellsCloudClientSecret'],'v3.0',ENV['CellsCloudApiBaseUrl'])

remote_folder = 'TestData/In'

local_name = 'Book1.xlsx'
remote_name = 'Book1.xlsx'

format = "csv"

    
mapFiles = { }   
mapFiles = { }               
mapFiles[local_name] = ::File.open(File.expand_path("TestData/"+local_name),"r")  
 
uploadrequest = AsposeCellsCloud::UploadFileRequest.new( { :UploadFiles=>mapFiles,:path=>remote_folder })
@instance.upload_file(uploadrequest)
mapFiles[local_name]= ::File.open(File.expand_path("TestData/"+local_name),"r")
request =   AsposeCellsCloud::PutConvertWorkbookRequest.new(:File=>mapFiles,:format=>format);
@instance.put_convert_workbook(request);


```
