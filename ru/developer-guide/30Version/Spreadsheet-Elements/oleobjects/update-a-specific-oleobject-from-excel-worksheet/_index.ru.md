---
title: "Обновление OLE-объекта в листе Excel"
second_title: "Документ"
linktitle: "Обновление"
type: docs
url: /ru/oleobjects/update/
aliases: [/ru/update-a-specific-oleobject-from-excel-worksheet/]
keywords: "обновление OLE-объекта, Excel, Aspose.Cells Cloud, REST API, SDK"
description: "Узнайте, как обновить OLE-объект (изображение, диаграмму и т.д.) в листе Excel с помощью REST API Aspose.Cells Cloud. Примеры cURL и SDK, шаги аутентификации, обработка ошибок."
weight: 30
author: "Команда документации Aspose Cloud"
lastmod: "2024-03-01"
ArticleTitle: "Обновление OLE-объекта в листе Excel — руководство по API Aspose.Cells Cloud"
---

Этот REST API обновляет **OLE-объект** в листе Excel.

### **Безопасность и аутентификация**

API Aspose.Cells Cloud являются защищёнными и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

## API PostUpdateWorksheetOleObject

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}
```

Параметры запроса:

| Имя параметра | Тип    | Местоположение параметра | Описание                                           |
|---------------|--------|--------------------------|----------------------------------------------------|
| name          | string | path                     | Имя рабочей книги.                                 |
| sheetName     | string | path                     | Имя листа.                                         |
| oleObjectIndex| integer| path                     | Индекс OLE-объекта в листе.                        |
| ole           | object | body                     | JSON-представление обновляемого OLE-объекта.      |
| folder        | string | query                    | Папка, содержащая рабочую книгу.                   |
| storageName   | string | query                    | Имя сервиса хранения.                              |

### Поля тела запроса

| Поле                | Тип     | Обязательное | Описание                                           |
|---------------------|---------|--------------|----------------------------------------------------|
| ImageSourceFullName | string  | нет          | Путь к файлу изображения, используемому для OLE-объекта. |
| IsAutoSize          | boolean | нет          | Автоматическое изменение размера OLE-объекта.     |
| SourceFullName      | string  | да           | Исходный файл (например, изображение или диаграмма) для OLE-объекта. |
| UpperLeftRow        | integer | да           | Индекс строки (начиная с 0) верхнего левого угла. |
| UpperLeftColumn     | integer | да           | Индекс столбца (начиная с 0) верхнего левого угла. |
| Left                | integer | нет          | Горизонтальное смещение в точках от верхнего левого угла. |
| Top                 | integer | нет          | Вертикальное смещение в точках от верхнего левого угла. |
| Width               | integer | да           | Ширина OLE-объекта в точках.                       |
| Height              | integer | да           | Высота OLE-объекта в точках.                       |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/OleObjects/PostUpdateWorksheetOleObject) определяет общедоступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать командную утилиту **cURL** для простого доступа к веб-сервисам Aspose.Cells. Пример ниже демонстрирует вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/" \
  -X POST \
  -d '{"ImageSourceFullName":"aspose-logo.png","IsAutoSize":true,"SourceFullName":"Sample_Book2.xls","UpperLeftRow":15,"Top":10,"UpperLeftColumn":5,"Left":10,"Width":400,"Height":400}' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "OLEObject": {
    "Index": 0,
    "ImageSourceFullName": "aspose-logo.png",
    "IsAutoSize": true,
    "SourceFullName": "Sample_Book2.xls",
    "UpperLeftRow": 15,
    "UpperLeftColumn": 5,
    "Left": 10,
    "Top": 10,
    "Width": 400,
    "Height": 400
  }
}
```

{{< /tab >}}

{{< /tabs >}}

## Ответы об ошибках

| HTTP-статус | Код  | Сообщение                                                   |
|-------------|------|-------------------------------------------------------------|
| 400         | 4000 | Неверный запрос — отсутствующие или некорректные параметры. |
| 401         | 4010 | Неавторизованный доступ — некорректный или отсутствующий токен JWT. |
| 404         | 4040 | Не найдено — рабочая книга, лист или OLE-объект не существует. |
| 500         | 5000 | Внутренняя ошибка сервера — непредвиденная ошибка на стороне сервера. |

API также возвращает пользовательское поле **Code** в теле ответа, сопоставленное с HTTP-статусом (например, 200 → 2000, 400 → 4000 и т.д.).

## Когда использовать этот API?

Используйте этот конечный пункт, если вам нужно изменить существующий OLE-объект — например, встроенное изображение, диаграмму или документ — без повторной загрузки всего листа. Типичные сценарии включают обновление источника изображения, изменение размера объекта или изменение его позиции после генерации рабочей книги. См. также: [Добавление OLE-объекта](/ru/oleobjects/add/) и [Удаление OLE-объекта](/ru/oleobjects/delete/).

## Семейство облачных SDK

Использование SDK — самый быстрый способ разработки. SDK абстрагирует низкоуровневые детали, позволяя сосредоточиться на проекте. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Ниже приведён краткий пример на C#, демонстрирующий обновление OLE-объекта с помощью SDK Aspose.Cells Cloud:

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var config = new Configuration
{
    AppSid = "<your-app-sid>",
    AppKey = "<your-app-key>"
};
var oleApi = new OleObjectsApi(config);
var request = new OleObjectUpdateRequest
{
    ImageSourceFullName = "aspose-logo.png",
    IsAutoSize = true,
    SourceFullName = "Sample_Book2.xls",
    UpperLeftRow = 15,
    UpperLeftColumn = 5,
    Left = 10,
    Top = 10,
    Width = 400,
    Height = 400
};

var response = oleApi.UpdateWorksheetOleObject("SampleBook.xlsx", "Sheet1", 0, request, folder: "myFolder");
Console.WriteLine($"Status: {response.Status}");
```

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUpdateWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUpdateWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUpdateWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUpdateWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUpdateWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUpdateWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUpdateWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUpdateWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}