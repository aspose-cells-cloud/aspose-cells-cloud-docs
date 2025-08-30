---
title: Как объединить несколько файлов электронных таблиц с помощью Aspose.Cells Clou
linktitle: Как объединить несколько файлов электронных таблиц
type: docs
url: /ru/how-to-merge-multiple-files
description: Как объединить несколько файлов электронных таблиц с помощью Aspose.Cells Cloud
weight: 10
kwords: Excel, Office Cloud, REST API, Электронная таблица, PDF, CSV, Json, Markdown, Как объединить несколько файлов через Aspose.Cells Cloud
---
## Введение

Облако Aspose.Cells (API) — это мощное облачное решение для создания, редактирования и преобразования файлов электронных таблиц. В этой статье мы подробно расскажем вам о процессе использования Облака Aspose.Cells (API) для объединения форматов файлов, включая типичные примеры использования и примеры кода.

## Обзор

 Облако Aspose.Cells (API) предоставляет надежные API для объединения нескольких электронных таблиц в один файл в различных форматах. Поддерживаемые форматы включают:**Excel** (XLS, XLSX),**CSV**, **HTML**, **PDF**и многое другое. Используя Cloud Aspose.Cells API, вы можете легко объединить несколько файлов электронных таблиц в один файл с использованием широко распространённых форматов, отвечающий самым разным требованиям.

Для объединения файлов доступно множество API, как правило, совместимых с различными онлайн-средами. Ниже приведено подробное описание этих API:

| Функция| Описание| API Ссылка|
|:------------------------- |:------------------------- |:------------------------- |
|**[MergeSpreadsheets](https://docs.aspose.cloud/cells/merge-spreadsheets/)** |Объединить локальные файлы электронных таблиц в файл указанного формата.|[MergeSpreadsheets](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeSpreadsheets) |
|**[MergeRemoteSpreadsheet](https://docs.aspose.cloud/cells/merge-remote-spreadsheet/)** | Объединить файлы электронных таблиц в папке облачного хранилища в файл указанного формата.|[Объединение удаленных электронных таблиц](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeRemoteSpreadsheet) |
|**[Объединить таблицы в удаленной папке](https://docs.aspose.cloud/cells/merge-spreadsheets-in-remote-folder/)** | Объединить файлы электронных таблиц в папке облачного хранилища в файл указанного формата.|[Объединение таблиц в удаленной папке](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeSpreadsheetsInRemoteFolder) |

# Как объединить несколько файлов в один файл через облако Aspose.Cells

 Облако Aspose.Cells API обеспечивает[несколько SDK](https://github.com/aspose-cells-cloud) для разных языков программирования. Выберите SDK, соответствующий вашему предпочитаемому языку программирования, и следуйте прилагаемой документации по установке и инициализации. Вы также можете создать свой собственный SDK в соответствии с[API ссылка](https://reference.aspose.cloud/cells/)В этом разделе мы будем использовать C# в качестве примера для подробного описания процесса объединения файлов.

## Регистрация и получение ключа API

Прежде чем начать, вам необходимо[зарегистрируйте учетную запись Cloud Aspose](https://id.containerize.com/signup) и[получить ключ API для аутентификации](https://dashboard.aspose.cloud/applications). Зайдя на официальный сайт облака Aspose, вы можете создать бесплатную учетную запись и получить ключ API для аутентификации.

 Более подробную информацию об операциях можно найти в следующих документах:[Быстрый старт с облаком Cells](https://docs.aspose.cloud/cells/quickstart/)

## Установка и инициализация Cloud SDK Aspose.Cells

Установите пакет Aspose.Cells-Cloud NuGet в свой проект .NET, вы можете использовать консоль менеджера пакетов NuGet или менеджер пакетов NuGet в Visual Studio.
Вот как можно установить пакет с помощью консоли менеджера пакетов:

```Powershell

Install-Package Aspose.Cells-Cloud

```

Создаёт новый экземпляр класса CellsApi, инициализируя его вашим идентификатором клиента и секретным ключом клиента. Ниже приведены подробности вышеупомянутого фрагмента кода:

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

Обязательно замените ВАШ_API_КЛЮЧ, ВАШ_ПРИЛОЖЕНИЕ_SID и ВАШ_ПРИЛОЖЕНИЕ_KEY с вашим реальным ключом API, SID приложения и ключом приложения.

## Создайте запрос API и позвоните по номеру API

### Используйте облачные сервисы для объединения локальных электронных таблиц и доставки консолидированных файлов — либо в виде локальных выходных данных, либо в виде потоков в памяти — в любом необходимом формате.

```CSharp

using System.Collections.Generic;

var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));

// Suild merged spreadsheet request
var request = new Aspose.Cells.Cloud.SDK.Request.MergeSpreadsheetsRequest();
// Set need merged files.
IDictionary<string, System.IO.Stream> mapFiles = new Dictionary<string, System.IO.Stream>();
mapFiles.Add("Book1.xlsx", File.OpenRead("Book1.xlsx"));
mapFiles.Add("Book2.xlsx", File.OpenRead("Book2.xlsx"));
request.Spreadsheet = mapFiles;
// Set output format
request.outFormat = "pdf";

cellsApi.MergeSpreadsheets(request, "MergedResultFile.pdf");

```

### Облачное объединение электронных таблиц, хранящихся в облаке, и отправка консолидированного файла — локально или обратно в облачное хранилище — в любом необходимом формате.

```C#
// Get your Client ID and Client Secret from https://dashboard.aspose.cloud (free registration is required).
var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));
// Build merge request parameters 
var request = new Aspose.Cells.Cloud.SDK.Request.MergeRemoteSpreadsheetRequest();
// Set cloud main file
request.name = "Book1.xlsx";
request.folder = "RemoteFolder1";
// Set cloud merged file
request.mergedSpreadsheet = "RemoteFolder2/Book2.xlsx";
request.outFormat = "pdf";
cellsApi.MergeRemoteSpreadsheet(request, "MergedResultOutPutToLocalFile.pdf");
```

### Автоматически объединяйте соответствующие файлы в облачном каталоге, экспортируйте объединенный результат в указанном формате и доставляйте его локально или обратно в облачное хранилище.

```csharp
// Get your Client ID and Client Secret from https://dashboard.aspose.cloud (free registration is required).
var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));
// Build merge request parameters 
var request = new Aspose.Cells.Cloud.SDK.Request.MergeSpreadsheetsInRemoteFolderRequest();
// Storage directory that needs to merge files
request.folder = "RemoteFolder";
request.fileMatchExpression = "*xlsx$";
request.outFormat = "pdf";
cellsApi.MergeSpreadsheetsInRemoteFolder(request, "MergedResultOutPutToLocalFile.pdf");
```

## Варианты использования

 Несколько файлов**объединены**Функция Cloud Aspose.Cells API полезна в различных практических ситуациях. Вот несколько распространённых сценариев:

- **Объединить несколько файлов Excel в файл Excel** для анализа и хранения данных.
- **Объединить файлы данных в файл Excel** для анализа данных.
- **Объединить несколько файлов изображений в файл PDF** для удобства обмена.
- **Объединить несколько файлов в HTML-файл** для отображения и встраивания в веб-страницы.

## Заключение

С помощью Aspose.Cells Cloud API вы можете легко объединить в файл несколько электронных таблиц. Выполняя простые вызовы API и устанавливая соответствующие параметры объединения, вы можете эффективно выполнять различные требования к объединению файлов. Интегрируйте Aspose.Cells Cloud API в свои приложения, чтобы повысить производительность и сократить время разработки.

Обратите внимание, что приведённый выше пример кода предназначен только для демонстрации, и при использовании на практике вам потребуется заменить его действительными учётными данными аутентификации и путями к файлам. Кроме того, Aspose.Cells Cloud API предлагает множество других функций, таких как создание, редактирование, изменение и обработка электронных таблиц. Подробную документацию и пример кода API можно найти на сайте[руководство разработчика официального сайта Aspose](/developer-guide/).

Надеемся, эта статья поможет вам разобраться, как использовать Cloud Aspose.Cells для слияния файлов. Удачи в реализации!
