﻿---
title: Как защитить файл через Aspose.Cells Clou
type: docs
url: /ru/how-to-protect-file
description: Как защитить файл через облако Aspose.Cells
weight: 10
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdwon, Как защитить файл через Aspose.Cells Облако
---
## Введение

Aspose.Cells Cloud API — это мощное облачное решение, созданное для создания, редактирования и преобразования файлов электронных таблиц. В этой статье мы познакомим вас с процессом использования облака Aspose.Cells API для защиты файлов, включая типичные случаи использования и примеры кода.

## Обзор

Облако Aspose.Cells API предоставляет множество надежных API для защиты файлов Excel или электронных таблиц. Используя облако Aspose.Cells API, вы можете легко защитить Excel или другие файлы электронных таблиц, отвечающие широкому спектру требований.


Для защиты файлов доступны многочисленные API-интерфейсы, обычно совместимые с различными онлайн-средами. Ниже приведено подробное описание этих API:

- **[Защитите MS Excel и электронную таблицу OpenDocument, применив защиту паролем.] (https://reference.aspose.cloud/cells/#/Workbook/PostEncryptWorkbook)** . Инструкции о том, как позвонить на номер API, см.[руководство по разработке](https://docs.aspose.cloud/cells/workbook/encrypt/).
- **[Защитите MS Excel и электронную таблицу OpenDocument.](https://reference.aspose.cloud/cells/#/Workbook/PostProtectWorkbook)** . Инструкции о том, как позвонить на номер API, см.[руководство по разработке](https://docs.aspose.cloud/cells/workbook/protect/).
- **[Защитите MS Excel и электронную таблицу OpenDocument без использования облачного хранилища.] (https://reference.aspose.cloud/cells/#/LightCells/PostProtect)** . Инструкции о том, как позвонить на номер API, см.[руководство по разработке](https://docs.aspose.cloud/cells/protect/without-using-storage/).
- **[MS Excel и цифровая подпись электронной таблицы OpenDocument.] (https://reference.aspose.cloud/cells/#/Workbook/PostDigitalSignature)** . Инструкции о том, как позвонить на номер API, см.[руководство по разработке](https://docs.aspose.cloud/cells/workbook/digital-signature/).
- **[Пакетная защита файлов](https://reference.aspose.cloud/cells/#/Batch/PostBatchProtect)** . Инструкции о том, как позвонить на номер API, см.[руководство по разработке](https://docs.aspose.cloud/cells/batch/protect/).


# Как защитить файл Excel или другую таблицу с помощью облака Aspose.Cells

 Облако Aspose.Cells API обеспечивает[несколько SDK](https://github.com/aspose-cells-cloud) для разных языков программирования. Выберите SDK, соответствующий предпочитаемому вами языку программирования, и следуйте сопроводительной документации для установки и инициализации. Кроме того, вы можете создать свой собственный SDK в соответствии с[API ссылка](https://reference.aspose.cloud/cells/). В этом разделе мы будем использовать C# в качестве примера, чтобы подробно описать процесс объединения файлов.


## Регистрация и получение ключа API

 Прежде чем приступить к работе, вам необходимо[зарегистрировать облачный аккаунт Aspose](https://id.containerize.com/signup) и[получить ключ API для аутентификации](https://dashboard.aspose.cloud/applications). Зайдя на официальный сайт Aspose Cloud, вы можете создать бесплатную учетную запись и получить ключ API для целей аутентификации.

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

При этом создается новый экземпляр PostProtectRequest, инициализирующий его нужными файлами и запросом защитной книги. Затем он вызывает защиту API с этим запросом на защиту. Функция защиты также поддерживает расширенные параметры запроса. Ниже приведены подробности вышеупомянутого фрагмента кода:


```CSharp

using System.Collections.Generic;

PostProtectRequest request = new PostProtectRequest();

IDictionary<string, System.IO.Stream> mapFiles =new Dictionary<string, System.IO.Stream>(); 
mapFiles.Add("Book1.xlsx", File.OpenRead(@"c:\testdata\Book1.xlsx"));
mapFiles.Add("Book2.xlsx", File.OpenRead(@"c:\testdata\Book2.xlsx"));
request.Files = mapFiles;

request.protectWorkbookRequst = new ProtectWorkbookRequst {
    AwaysOpenReadOnly = true ,
    EncryptWithPassword = "123456",
    ProtectCurrentSheet = new Protection { 
        AllowDeletingColumn =true
    }
};


cellsInstance.PostProtect(request);

```


## Случаи использования

**защищать** Excel или другая функция электронной таблицы облака Aspose.Cells API полезна в различных практических случаях. Вот некоторые распространенные сценарии:

-  Добавлять**несколько файлов цифровой подписи** для локальных файлов Excel или других файлов электронных таблиц.
-  Добавлять**защита паролем** для локальных файлов Excel или других файлов электронных таблиц.
-  Набор**Всегда Открыто Только для чтения** для удобства обмена.
- **Объединить несколько файлов в html-файл** для отображения и встраивания в веб-страницы.

## Заключение

С помощью Aspose.Cells Cloud API вы можете легко создавать защищенные файлы Excel или другие файлы электронных таблиц. Выполняя простые вызовы API и устанавливая соответствующие параметры защиты, вы можете эффективно выполнить различные требования к объединению файлов. Интегрируйте Aspose.Cells Cloud API в свои приложения, чтобы повысить производительность и сэкономить время на разработку.

 Обратите внимание, что приведенный выше пример кода предназначен только для демонстрационных целей, и при его практическом использовании вам потребуется заменить его действительными учетными данными для аутентификации и путями к файлам. Кроме того, Aspose.Cells Cloud API предлагает множество других функций, таких как создание, редактирование, манипулирование и обработка электронных таблиц. Подробную документацию API и пример кода можно найти на странице[руководство разработчика официального сайта Aspose](/developer-guide/).

Мы надеемся, что эта статья поможет вам понять, как использовать Aspose.Cells Cloud API для слияния файлов. Удачи в реализации!

