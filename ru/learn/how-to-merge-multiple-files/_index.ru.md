---
title: "Как объединить несколько файлов электронных таблиц с Aspose.Cells Cloud"
linktitle: "Как объединить несколько файлов электронных таблиц"
type: docs
url: /ru/how-to-merge-multiple-files
description: "Как объединить несколько файлов электронных таблиц с помощью Aspose.Cells Cloud."
weight: 10
kwords: Excel, Office Cloud, REST API, Электронная таблица, PDF, CSV, JSON, Markdown, Как объединить несколько файлов через Aspose.Cells Cloud
---

## Введение

Aspose.Cells Cloud API — мощное облачное решение, предназначенное для создания, редактирования и преобразования файлов электронных таблиц. В этой статье мы проведём вас через процесс использования Aspose.Cells Cloud API для объединения файлов различных форматов, включая типичные сценарии использования и примеры кода.

## Обзор

Aspose.Cells Cloud API предоставляет надёжные API для объединения нескольких файлов электронных таблиц в один файл одного из поддерживаемых форматов. Поддерживаемые форматы включают **Excel** (XLS, XLSX), **CSV**, **HTML**, **PDF** и другие. Благодаря Aspose.Cells Cloud API вы можете без труда объединять несколько файлов электронных таблиц в файл одного из широко используемых форматов, что позволяет удовлетворить разнообразные требования.

Доступны различные API для объединения файлов, совместимые, как правило, с различными онлайн-средами. Ниже приведено подробное описание этих API:

| Функция | Описание | Ссылка на API |
| :------------------------- | :------------------------- | :------------------------- |
| **[MergeSpreadsheets](https://docs.aspose.cloud/cells/merge-spreadsheets/)** | Объединяет локальные файлы электронных таблиц в файл заданного формата. | [MergeSpreadsheets](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeSpreadsheets) |
| **[MergeRemoteSpreadsheet](https://docs.aspose.cloud/cells/merge-remote-spreadsheet/)** | Объединяет файлы электронных таблиц, хранящиеся в папке облачного хранилища, в файл заданного формата. | [Merge Remote Spreadsheet](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeRemoteSpreadsheet) |
| **[Merge Spreadsheets In Remote Folder](https://docs.aspose.cloud/cells/merge-spreadsheets-in-remote-folder/)** | Объединяет файлы электронных таблиц, хранящиеся в папке облачного хранилища, в файл заданного формата. | [Merge Spreadsheets In Remote Folder](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeSpreadsheetsInRemoteFolder) |

# Как объединить несколько файлов в один с помощью Aspose.Cells Cloud

Aspose.Cells Cloud API предоставляет [несколько SDK](https://github.com/aspose-cells-cloud) для различных языков программирования. Выберите SDK, соответствующий вашему предпочитаемому языку, и следуйте инструкциям в документации по его установке и инициализации. Альтернативно, вы можете создать собственное SDK на основе [справочника по API](https://reference.aspose.cloud/cells/). В этом разделе мы рассмотрим процесс объединения файлов на примере C#.

## Регистрация и получение API-ключа

Прежде чем приступить к работе, вам необходимо [зарегистрировать учётную запись Aspose Cloud](https://id.containerize.com/signup) и [получить API-ключ для аутентификации](https://dashboard.aspose.cloud/applications). Войдя на официальный сайт Aspose Cloud, вы можете создать бесплатную учётную запись и получить API-ключ для целей аутентификации.

Для более глубокого погружения обратитесь к следующим документам: [Быстрый старт с Cells Cloud](https://docs.aspose.cloud/cells/quickstart/)

## Установка и инициализация SDK Aspose.Cells Cloud

Установите пакет Aspose.Cells-Cloud NuGet в вашем .NET-проекте. Вы можете воспользоваться консолью менеджера пакетов NuGet или менеджером пакетов NuGet в Visual Studio.  
Пример установки через консоль менеджера пакетов:

```Powershell

Install-Package Aspose.Cells-Cloud

```

Создайте новый экземпляр класса `CellsApi`, инициализировав его вашим Client ID и Client Secret. Ниже приведены детали вышеупомянутого фрагмента кода:

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

Не забудьте заменить `YOUR_API_KEY`, `YOUR_APP_SID` и `YOUR_APP_KEY` на ваши реальные API-ключ, SID приложения и ключ приложения.

## Формирование запроса к API и его вызов

### Использование облачных сервисов для объединения локальных электронных таблиц и получения объединённых файлов — либо в виде локальных выходных данных, либо в виде потоков в памяти — в любом требуемом формате

```CSharp

using System.Collections.Generic;

var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));

// Формируем запрос на объединение электронных таблиц
var request = new Aspose.Cells.Cloud.SDK.Request.MergeSpreadsheetsRequest();
// Задаём файлы, подлежащие объединению.
IDictionary<string, System.IO.Stream> mapFiles = new Dictionary<string, System.IO.Stream>();
mapFiles.Add("Book1.xlsx", File.OpenRead("Book1.xlsx"));
mapFiles.Add("Book2.xlsx", File.OpenRead("Book2.xlsx"));
request.Spreadsheet = mapFiles;
// Задаём выходной формат
request.outFormat = "pdf";

cellsApi.MergeSpreadsheets(request, "MergedResultFile.pdf");

```

### Объединение в облаке таблиц, хранящихся в облаке, с получением объединённого файла — локально или обратно в облачное хранилище — в любом требуемом формате

```C#
// Получите ваш Client ID и Client Secret на https://dashboard.aspose.cloud (требуется бесплатная регистрация).
var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));
// Формируем параметры запроса на объединение
var request = new Aspose.Cells.Cloud.SDK.Request.MergeRemoteSpreadsheetRequest();
// Задаём основной файл в облаке
request.name = "Book1.xlsx";
request.folder = "RemoteFolder1";
// Задаём файл для объединения в облаке
request.mergedSpreadsheet = "RemoteFolder2/Book2.xlsx";
request.outFormat = "pdf";
cellsApi.MergeRemoteSpreadsheet(request, "MergedResultOutPutToLocalFile.pdf");
```

### Автоматическое объединение подходящих файлов в облачной директории, экспорт результата объединения в указанном формате и его доставка локально или обратно в облачное хранилище

```csharp
// Получите ваш Client ID и Client Secret на https://dashboard.aspose.cloud (требуется бесплатная регистрация).
var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));
// Формируем параметры запроса на объединение
var request = new Aspose.Cells.Cloud.SDK.Request.MergeSpreadsheetsInRemoteFolderRequest();
// Директория хранилища, в которой необходимо объединить файлы
request.folder = "RemoteFolder";
request.fileMatchExpression = "*xlsx$";
request.outFormat = "pdf";
cellsApi.MergeSpreadsheetsInRemoteFolder(request, "MergedResultOutPutToLocalFile.pdf");
```

## Применение

Функция **объединения нескольких файлов** API Aspose.Cells Cloud полезна в различных практических сценариях. Вот некоторые распространённые случаи использования:

- **Объединение нескольких файлов Excel в один файл Excel** для последующего анализа и хранения данных.
- **Объединение файлов данных в один файл Excel** для анализа.
- **Объединение нескольких файлов изображений в один файл PDF** для удобного обмена.
- **Объединение нескольких файлов в один файл HTML** для отображения и встраивания на веб-страницы.

## Заключение

С помощью Aspose.Cells Cloud API вы можете легко объединять несколько файлов электронных таблиц в один файл. Совершая простые вызовы API и задавая подходящие параметры объединения, вы можете эффективно удовлетворить разнообразные потребности в объединении файлов. Интегрируйте Aspose.Cells Cloud API в свои приложения, чтобы повысить производительность и сэкономить время разработки.

Обратите внимание, что приведённый выше пример кода служит лишь демонстрационной целью, и при практическом использовании вам потребуется заменить его на действующие учётные данные для аутентификации и действительные пути к файлам. Кроме того, Aspose.Cells Cloud API предлагает множество других функций, таких как создание, редактирование, обработка и анализ данных в электронных таблицах. Подробную документацию по API и примеры кода можно найти на [руководстве разработчика на официальном сайте Aspose](/developer-guide/).

Надеемся, что эта статья помогла вам понять, как использовать Aspose.Cells Cloud API для объединения файлов. Удачи в реализации!