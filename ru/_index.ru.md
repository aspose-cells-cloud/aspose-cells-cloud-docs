---
title: "Aspose.Cells Cloud API – Конвертирование, объединение, разбиение и защита файлов Excel"
second_title: "Документ"
ArticleTitle: "Aspose.Cells Cloud API – Конвертирование, объединение, разбиение и защита файлов Excel"
linktitle: "Центр разработчика"
type: docs
url: /ru/
description: "Aspose.Cells Cloud REST API позволяет конвертировать, объединять, разбивать, защищать и выполнять комплексную обработку электронных таблиц Excel. Бесплатный тариф — до 150 вызовов API в месяц, SDK для 8 языков."
weight: 10
keywords: "Aspose.Cells Cloud, Excel API, конвертация электронных таблиц, объединение Excel, разбиение Excel, защита Excel, облачный SDK для электронных таблиц, REST API, обработка Excel"
---

## Что такое Aspose.Cells Cloud API?

Aspose.Cells Cloud API — это набор облачных сервисов для работы с электронными таблицами/Excel. Установка Office или настройка сервера не требуются — достаточно отправить HTTP-запрос, и вы сможете создавать, редактировать, конвертировать, очищать данные, генерировать диаграммы, строить сводные таблицы, шифровать, разбивать, объединять, добавлять водяные знаки, применять цифровые подписи и многое другое — с любого языка программирования.

## Почему использовать Aspose.Cells Cloud API?

- Создание, редактирование, конвертирование и анализ электронных таблиц в облачном хранилище с использованием веб-API Aspose.Cells Cloud.  
- Создание, редактирование, конвертирование и анализ локальных файлов электронных таблиц с использованием веб-API Aspose.Cells Cloud.  
- Поддерживаемые форматы файлов — 30 форматов, включая **xlsx**, **csv**, **ods**, **xlsb** и др.  
- Работа с электронными таблицами напрямую через веб-API Aspose.Cells Cloud без зависимости от Microsoft Excel.  
- Бесплатный тариф — до 150 вызовов API в месяц.  
- Платежи по принципу «плати за потребление» — оплата основывается на фактическом использовании.  
- **Короткие сценарии (short-codes)**: операции, выполняемые в одну строку.  
  - **Конвертировать XLSX в PDF** → ConvertSpreadsheetToPdf  
  - **Удалить лишние пробелы во всём файле** → TrimSpreadsheetContent  
  - **Объединить 10+ файлов в один отчёт** → MergeSpreadsheets  

## **Как использовать Aspose.Cells Cloud API?**

### Шаг 1: **Получите учётные данные API**  

- **[Зарегистрируйте аккаунт Aspose Cloud](https://dashboard.aspose.cloud/signup)**  
- **[Получите клиентские учётные данные](https://dashboard.aspose.cloud/#/applications)**  

### Шаг 2: **Вызов веб-API электронных таблиц с использованием SDK (рекомендуется)**  

Рекомендуется использовать официальный SDK для упрощения аутентификации и обработки запросов. SDK автоматически получает и обновляет токены доступа.

#### **[Установка SDK для .NET (NuGet)](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab)**

```powershell
dotnet add package Aspose.Cells-Cloud --version 26.6.0
```

#### Пример: **Конвертирование Excel в PDF с использованием SDK**

```csharp
CellsApi cellsApi = new CellsApi(
    Environment.GetEnvironmentVariable("ProductClientId"),
    Environment.GetEnvironmentVariable("ProductClientSecret"));
cellsApi.ConvertSpreadsheet(
    new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" },
    "EmployeeSalesSummary.pdf");
```

#### Описание параметров

- **Spreadsheet**: Имя файла Excel, расположенного в локальном хранилище.  
- **Format**: Целевой формат (например, pdf, png, csv, json).  
- **Output file**: Полученный файл будет сохранён локально под указанным именем.  

## **Основные функции**

Aspose.Cells Cloud предоставляет следующие ключевые возможности для автоматизации обработки электронных таблиц на уровне корпоративных решений:

### **Конвертирование электронных таблиц**

- **[Конвертировать электронную таблицу в PDF-файл](https://docs.aspose.cloud/cells/convert-excel-file-to-pdf-file/)**  
- **[Конвертировать диаграмму электронной таблицы в изображение](https://docs.aspose.cloud/cells/convert-chart-to-image/)**  
- **[Сохранить электронную таблицу как](https://docs.aspose.cloud/cells/save-an-excel-file-as-other-formats-files/)**  

### **Обработка данных**

- **[Объединить электронные таблицы](https://docs.aspose.cloud/cells/merge-spreadsheets/)**  
- **[Разбить электронную таблицу](https://docs.aspose.cloud/cells/split-spreadsheet/)**  
- **[Удалить пустые строки из электронной таблицы](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-rows/)**  
- **[Удалить пустые столбцы из электронной таблицы](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-columns/)**  
- **[Заменить содержимое электронной таблицы](https://docs.aspose.cloud/cells/replace-spreadsheet-content/)**  

> **Примечание:** Подробные схемы запросов и ответов, HTTP-методы, параметры запроса и примеры ответов для каждой конечной точки доступны в **Справочнике по веб-API Aspose.Cells Cloud для электронных таблиц**, указанном ниже.

**Быстрый справочник по конечным точкам**

| Операция | HTTP-метод | Путь | Обязательные параметры | Пример ответа |
|-----------|-------------|------|---------------------|-----------------|
| Конвертировать электронную таблицу | POST | `/cells/convert` | `Spreadsheet` (файл), `format` (строка) | Двоичный файл (например, PDF) |
| Объединить электронные таблицы | POST | `/cells/worksheets/merge` | `files` (список файлов) | Объединённая рабочая книга |
| Разбить электронную таблицу | POST | `/cells/worksheets/split` | `Spreadsheet` (файл), `format` (строка) | Архив с разбитыми файлами |
| Удалить пустые строки | POST | `/cells/worksheets/blankrows/delete` | `Spreadsheet` (файл) | Обновлённая рабочая книга |
| Заменить содержимое | POST | `/cells/replace` | `Spreadsheet` (файл), `oldValue`, `newValue` | Обновлённая рабочая книга |

## Поддерживаемые SDK (**Доступные SDK**)

- Aspose.Cells Cloud предоставляет готовые к использованию [SDK](https://github.com/aspose-cells-cloud) на всех основных языках программирования — клонируйте, пишите код и развертывайте:

| Язык | Метод установки | Репозиторий на GitHub |
|------|----------|-------------|
| [Java](https://www.oracle.com/java/) | [Maven](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/blob/master/Aspose.Cells.Cloud.pom.xml) | [Репозиторий SDK для Java на GitHub](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java) |
| [.NET](https://dotnet.microsoft.com/) | [NuGet](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab) | [Репозиторий SDK для .NET на GitHub](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet) |
| [Python](https://www.python.org/) | [pip](https://pypi.org/project/asposecellscloud/) | [Репозиторий SDK для Python на GitHub](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python) |
| [Node.js](https://nodejs.org/en) | [npm](https://www.npmjs.com/package/asposecellscloud) | [Репозиторий SDK для Node.js на GitHub](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node) |
| [PHP](https://www.php.net/) | [Composer](https://packagist.org/packages/aspose/cells-sdk-php) | [Репозиторий SDK для PHP на GitHub](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php) |
| [GoLang](https://go.dev/) | [Go Modules](https://pkg.go.dev/github.com/aspose-cells-cloud/aspose-cells-cloud-go/v25) | [Репозиторий SDK для GoLang на GitHub](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go) |
| [Ruby](https://www.ruby-lang.org/) | [RubyGems](https://rubygems.org/gems/aspose_cells_cloud) | [Репозиторий SDK для Ruby на GitHub](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby) |
| [Perl](https://www.perl.org/) | [CPAN](https://metacpan.org/dist/AsposeCellsCloud-CellsApi) | [Репозиторий SDK для Perl на GitHub](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl) |
| **Конечная точка API** | [Справочник по веб-API Aspose.Cells Cloud для электронных таблиц](https://reference.aspose.cloud/cells/) |  |

## **Примеры кода и проекты с открытым исходным кодом**

Все SDK имеют открытый исходный код и включают богатые примеры:

- [Примеры SDK для Java на GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/tree/master/Examples)  
- [Примеры SDK для .NET на GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet/tree/master/examples)  
- [Примеры SDK для Python на GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python/tree/master/examples)  
- [Примеры SDK для Node.js на GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node/tree/master/Examples)  
- [Примеры SDK для PHP на GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php/tree/master/examples)  
- [Примеры SDK для Go на GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go/tree/master/examples)  
- [Примеры SDK для Ruby на GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby/tree/master/examples)  
- [Примеры SDK для Perl на GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl/tree/master/examples)  
---