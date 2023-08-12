---
title: Как конвертировать форматы файлов через Aspose.Cells Clou
type: docs
url: /ru/how-to-convert-file-formats
description: Как конвертировать форматы файлов через Облако Aspose.Cells
weight: 10
---
## Введение
Aspose.Cells Cloud API — это мощное облачное решение, предназначенное для создания, редактирования и преобразования файлов электронных таблиц. В этой статье мы познакомим вас с процессом использования Aspose.Cells Cloud API для преобразования формата файла, включая типичные варианты использования и пример кода.

## Обзор

 Облако Aspose.Cells API предоставляет надежный набор API для преобразования файлов электронных таблиц между различными форматами. Поддерживаемые форматы включают**Excel** (XLS, XLSX),**CSV**, **HTML**, **PDF**, и более. Используя Aspose.Cells Cloud API, вы можете легко преобразовывать файлы электронных таблиц в другие широко используемые форматы, удовлетворяя самые разные требования.

Для преобразования файлов доступны многочисленные API, обычно совместимые с различными онлайн-средами. Ниже приведено подробное описание этих API:

- **[Получить файл Excel в указанном формате](https://reference.aspose.cloud/cells/#/Conversion/GetWorkbook)** . Инструкции о том, как позвонить по номеру API, см.[руководство по развитию](https://docs.aspose.cloud/cells/export-different-formats/).
- **[Преобразовать файл Excel в файл другого формата] (https://reference.aspose.cloud/cells/#/Conversion/PutConvertWorkbook)** . Инструкции о том, как позвонить по номеру API, см.[руководство по развитию](https://docs.aspose.cloud/cells/convert/excel-to-different-formats/).
- **[Сохранить файл Excel как файл другого формата] (https://reference.aspose.cloud/cells/#/Conversion/PostWorkbookSaveAs)** . Инструкции о том, как позвонить по номеру API, см.[руководство по развитию](https://docs.aspose.cloud/cells/saveas-other-formats/).
- **[Экспорт файлов Excel](https://reference.aspose.cloud/cells/#/LightCells/PostExport)** . Инструкции о том, как позвонить по номеру API, см.[руководство по развитию](https://docs.aspose.cloud/cells/export/excel-to-different-formats/).


# Как конвертировать форматы файлов через Облако Aspose.Cells

 Облако Aspose.Cells API обеспечивает[несколько SDK](https://github.com/aspose-cells-cloud)для разных языков программирования. Выберите SDK, соответствующий предпочитаемому вами языку программирования, и следуйте сопроводительной документации по установке и инициализации. Кроме того, вы можете создать свой собственный SDK в соответствии с[API ссылка](https://reference.aspose.cloud/cells/). В этом разделе мы будем использовать C# в качестве примера, чтобы подробно описать процесс преобразования файлов.


## Регистрация и получение ключа API

 Прежде чем приступить к работе, вам необходимо[зарегистрировать облачный аккаунт Aspose](https://id.containerize.com/signup) и[получить ключ API для аутентификации](https://dashboard.aspose.cloud/applications). Зайдя на официальный веб-сайт Aspose Cloud, вы можете создать бесплатную учетную запись и получить ключ API для аутентификации.

 Более подробные сведения об операциях см. в следующих документах:[Быстрый старт с Cells Cloud](https://docs.aspose.cloud/cells/quickstart/)


## Установка и инициализация Aspose.Cells Cloud SDK

Установите пакет Aspose.Cells-Cloud NuGet в свой проект .NET, вы можете использовать консоль диспетчера пакетов NuGet или диспетчер пакетов NuGet в Visual Studio.
Вот как вы можете установить пакет с помощью консоли диспетчера пакетов:

```Powershell

Install-Package Aspose.Cells-Cloud

```
Создает новый экземпляр класса CellsApi, инициализируя его вашим идентификатором клиента и секретом клиента. Ниже приведены детали вышеупомянутого фрагмента кода:

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

Обязательно замените ВАШ_API_КЛЮЧ, ВАШ_ПРИЛОЖЕНИЕ_SID и ВАШ_ПРИЛОЖЕНИЕ_KEY с вашим фактическим ключом API, SID приложения и ключом приложения.

## Создайте запрос API и позвоните по номеру API.

Это создает новый экземпляр PutConvertWorkbookRequest, инициализируя его нужным форматом файла и файлами. Затем он вызывает преобразование API с этим запросом на преобразование. Ниже приведены детали вышеупомянутого фрагмента кода:


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

Функция Convert включает в себя менее известную функцию: расширенные параметры запроса. Эта функция в первую очередь служит для настройки дополнительных параметров сохранения для удовлетворения разнообразных потребностей клиентов. Конкретные параметры можно сохранить в соответствующем формате в соответствии со ссылкой Aspose.Cells API, например PDFSaveOptions.

Итак, как же установить эти расширенные параметры запроса? Давайте изучим следующий фрагмент кода:

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

 Файл**преобразование формата** функция Aspose.Cells Cloud API полезна в различных практических случаях использования. Вот несколько распространенных сценариев:

- **Конвертировать файлы Excel в формат PDF** для совместного использования и печати на разных устройствах.
- **Преобразование файлов электронных таблиц в формат HTML** для отображения и встраивания в веб-страницы.
- **Преобразование файлов CSV в формат Excel** для дальнейшего редактирования и анализа в приложениях для работы с электронными таблицами.
- **Преобразование файлов электронных таблиц в другие форматы**для удовлетворения конкретных бизнес-требований или потребностей обмена данными.

## Заключение

 С Aspose.Cells Cloud API вы можете легко выполнять преобразования формата файлов для файлов электронных таблиц, будь то преобразование**Excel** файлы в**PDF**, **HTML** , или преобразование**CSV** файлы в**Excel** формат. Делая простые звонки API и устанавливая соответствующие параметры преобразования, вы можете эффективно выполнить различные требования преобразования формата файла. Интегрируйте Aspose.Cells Cloud API в свои приложения, чтобы повысить производительность и сократить время разработки.

 Обратите внимание, что приведенный выше пример кода предназначен только для демонстрационных целей, и вам потребуется заменить его действительными учетными данными для аутентификации и путями к файлам при использовании на практике. Кроме того, Aspose.Cells Cloud API предлагает множество других функций, таких как создание электронных таблиц, редактирование, обработка и обработка данных. Подробную документацию API и пример кода можно найти на[руководство разработчика официального сайта Aspose](/developer-guide/).

Мы надеемся, что эта статья поможет вам понять, как использовать Aspose.Cells Cloud API для преобразования формата файла. Удачи вам в реализации!

