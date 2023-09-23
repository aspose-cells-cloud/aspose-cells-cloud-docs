---
title: Как конвертировать форматы файлов через Aspose.Cells Clou
type: docs
url: /ru/how-to-convert-file-formats
description: Как конвертировать форматы файлов через Облако Aspose.Cells
weight: 10
---
## Введение
Aspose.Cells Cloud API — это мощное облачное решение, созданное для создания, редактирования и преобразования файлов электронных таблиц. В этой статье мы познакомим вас с процессом использования облака Aspose.Cells API для преобразования форматов файлов, включая типичные варианты использования и примеры кода.

## Обзор

 Облако Aspose.Cells API предоставляет надежный набор API для преобразования файлов электронных таблиц в различные форматы. Поддерживаемые форматы включают в себя**Excel** (XLS, XLSX),**CSV-файл**, **HTML**, **PDF**, и более. Используя облако Aspose.Cells API, вы можете легко конвертировать файлы электронных таблиц в другие широко используемые форматы, отвечающие самым разнообразным требованиям.

Для преобразования файлов доступны многочисленные API-интерфейсы, обычно совместимые с различными онлайн-средами. Ниже приведено подробное описание этих API:

- **[Получите файл Excel указанного формата](https://reference.aspose.cloud/cells/#/Conversion/GetWorkbook)** . Инструкции о том, как позвонить на номер API, см.[руководство по разработке](https://docs.aspose.cloud/cells/export-different-formats/).
- **[Преобразовать файл Excel в файл другого формата] (https://reference.aspose.cloud/cells/#/Conversion/PutConvertWorkbook)** . Инструкции о том, как позвонить на номер API, см.[руководство по разработке](https://docs.aspose.cloud/cells/convert/excel-to-different-formats/).
- **[Сохранить файл Excel как файл другого формата] (https://reference.aspose.cloud/cells/#/Conversion/PostWorkbookSaveAs)** . Инструкции о том, как позвонить на номер API, см.[руководство по разработке](https://docs.aspose.cloud/cells/saveas-other-formats/).
- **[Экспорт файлов Excel](https://reference.aspose.cloud/cells/#/LightCells/PostExport)** . Инструкции о том, как позвонить на номер API, см.[руководство по разработке](https://docs.aspose.cloud/cells/export/excel-to-different-formats/).


# Как конвертировать форматы файлов через Облако Aspose.Cells

 Облако Aspose.Cells API обеспечивает[несколько SDK](https://github.com/aspose-cells-cloud)для разных языков программирования. Выберите SDK, соответствующий предпочитаемому вами языку программирования, и следуйте сопроводительной документации для установки и инициализации. Кроме того, вы можете создать свой собственный SDK в соответствии с[API ссылка](https://reference.aspose.cloud/cells/). В этом разделе мы будем использовать C# в качестве примера, чтобы подробно описать процесс преобразования файлов.


## Регистрация и получение ключа API

 Прежде чем приступить к работе, вам необходимо[зарегистрировать облачный аккаунт Aspose](https://id.containerize.com/signup) и[получить ключ API для аутентификации](https://dashboard.aspose.cloud/applications). Зайдя на официальный веб-сайт Aspose Cloud, вы можете создать бесплатную учетную запись и получить ключ API для целей аутентификации.

 Более подробную информацию о операциях можно найти в следующих документах:[Быстрый старт с облаком Cells](https://docs.aspose.cloud/cells/quickstart/)


## Установка и инициализация Cloud SDK Aspose.Cells

Установите пакет Aspose.Cells-Cloud NuGet в свой проект .NET. Вы можете использовать консоль диспетчера пакетов NuGet или диспетчер пакетов NuGet в Visual Studio.
Вот как вы можете установить пакет с помощью консоли диспетчера пакетов:

```Powershell

Install-Package Aspose.Cells-Cloud

```
Создает новый экземпляр класса CellsApi, инициализируя его вашим идентификатором клиента и секретным ключом клиента. Ниже приведены подробности вышеупомянутого фрагмента кода:

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

Обязательно замените СВОЙ_API_КЛЮЧ, ВАШ_ПРИЛОЖЕНИЕ_Сид и ВАШ_ПРИЛОЖЕНИЕ_KEY с вашим фактическим ключом API, SID приложения и ключом приложения.

## Создайте запрос API и позвоните на номер API.

При этом создается новый экземпляр PutConvertWorkbookRequest, инициализирующий его нужным форматом и файлами. Затем он вызывает преобразование API с этим запросом преобразования. Ниже приведены подробности вышеупомянутого фрагмента кода:


```CSharp

using System.Collections.Generic;

PutConvertWorkbookRequest request = new PutConvertWorkbookRequest();

request.Format = "pdf";
IDictionary<string, System.IO.Stream> mapFiles =new Dictionary<string, System.IO.Stream>(); 
mapFiles.Add("Book1.xlsx", File.OpenRead(@"c:\testdata\Book1.xlsx"));
mapFiles.Add("Book2.xlsx", File.OpenRead(@"c:\testdata\Book2.xlsx"));
request.Files = mapFiles;

cellsInstance.PutConvertWorkbook(request);

```

Функция Convert включает в себя менее известную функцию: расширенные параметры запроса. Эта функция в первую очередь служит для настройки дополнительных параметров экономии для удовлетворения разнообразных потребностей клиентов. Конкретные параметры можно сохранить в соответствующем формате согласно ссылке Aspose.Cells API, например PDFSaveOptions.

Итак, как установить эти расширенные параметры запроса? Давайте рассмотрим следующий фрагмент кода:

```CSharp

using System.Collections.Generic;

PutConvertWorkbookRequest request = new PutConvertWorkbookRequest();

request.Format = "pdf";
IDictionary<string, System.IO.Stream> mapFiles =new Dictionary<string, System.IO.Stream>(); 
mapFiles.Add("Book1.xlsx", File.OpenRead(@"c:\testdata\Book1.xlsx"));
mapFiles.Add("Book2.xlsx", File.OpenRead(@"c:\testdata\Book2.xlsx"));
request.Files = mapFiles;
request.extendQueryParameterMap = new  Dictionary<string, string>();
request.extendQueryParameterMap.Add("OnePagePerSheet","false");
request.extendQueryParameterMap.Add("CalculateFormula","true");
cellsInstance.PutConvertWorkbook(request);

```

## Случаи использования

 Файл**преобразование формата** Функция облака Aspose.Cells API полезна в различных практических случаях. Вот некоторые распространенные сценарии:

- **Конвертировать файлы Excel в формат PDF.** для совместного использования и печати на разных устройствах.
- **Преобразование файлов электронных таблиц в формат HTML** для отображения и встраивания в веб-страницы.
- **Конвертируйте CSV-файлы в формат Excel.** для дальнейшего редактирования и анализа в приложениях для работы с электронными таблицами.
- **Преобразование файлов электронных таблиц в другие форматы**для удовлетворения конкретных бизнес-требований или потребностей обмена данными.

## Заключение

 С помощью Aspose.Cells Cloud API вы можете легко выполнять преобразования форматов файлов электронных таблиц, независимо от того, конвертируете ли вы файлы электронных таблиц.**Excel** файлы в**PDF**, **HTML** или конвертация**CSV-файл** файлы в**Excel** формат. Выполняя простые вызовы API и устанавливая соответствующие параметры преобразования, вы можете эффективно выполнить различные требования к преобразованию форматов файлов. Интегрируйте Aspose.Cells Cloud API в свои приложения, чтобы повысить производительность и сэкономить время на разработку.

 Обратите внимание, что приведенный выше пример кода предназначен только для демонстрационных целей, и при его практическом использовании вам потребуется заменить его действительными учетными данными для аутентификации и путями к файлам. Кроме того, Aspose.Cells Облако API предлагает множество других функций, таких как создание, редактирование, манипулирование и обработка электронных таблиц. Подробную документацию API и пример кода можно найти на странице[руководство разработчика официального сайта Aspose](/developer-guide/).

Мы надеемся, что эта статья поможет вам понять, как использовать Aspose.Cells Cloud API для преобразования форматов файлов. Удачи в реализации!

