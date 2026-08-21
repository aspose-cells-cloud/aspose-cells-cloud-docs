---
title: "Добавление OLE-объекта в рабочий лист Excel"
second_title: "Документ"
linktitle: "Добавление OLE-объекта"
type: docs
url: /ru/oleobjects/add/
aliases: [/add-oleobject-to-excel-worksheet/]
keywords: "Добавление OLE-объекта, Excel, Aspose.Cells Cloud, REST API, SDK"
description: "Используйте Aspose.Cells Cloud REST API для добавления OLE-объектов в рабочие листы Excel. API можно вызывать напрямую или через SDK для C#, Java, PHP, Ruby, Node.js, Python, Perl и Go."
ArticleTitle: "Добавление OLE-объекта в рабочий лист Excel с помощью Aspose.Cells Cloud API"
weight: 20
---

Aspose.Cells Cloud API позволяет программно управлять книгами Excel, включая возможность встраивания OLE-объектов (например, документов Word, PDF или других двоичных файлов) непосредственно в рабочий лист.

Этот REST API добавляет **OLE-объект** в рабочий лист Excel.

**Предварительные требования**: У вас должен быть действительный JWT-токен аутентификации, а все исходные файлы, на которые ссылается `oleFile` или `imageFile`, должны быть загружены в указанное местоположение хранилища до вызова конечной точки.

## PutWorksheetOleObject API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

### Параметры запроса

| Имя параметра   | Тип    | Расположение | Описание                                           |
| --------------- | ------ | ------------ | -------------------------------------------------- |
| name            | string | path         | Имя файла книги.                                   |
| sheetName       | string | path         | Имя рабочего листа.                                |
| oleObject       | object | body         | Определение OLE-объекта.                           |
| upperLeftRow    | integer | query       | Индекс строки верхнего левого угла (по умолчанию 0). |
| upperLeftColumn | integer | query       | Индекс столбца верхнего левого угла (по умолчанию 0). |
| height          | integer | query       | Высота OLE-объекта (по умолчанию 0).               |
| width           | integer | query       | Ширина OLE-объекта (по умолчанию 0).                |
| oleFile         | string | query        | Имя исходного файла OLE.                           |
| imageFile       | string | query        | Имя файла изображения-предпросмотра.                |
| folder          | string | query        | Папка, содержащая книгу.                           |
| storageName     | string | query        | Имя используемого хранилища.                       |

**Примечания**: `upperLeftRow` и `upperLeftColumn` используют нумерацию, начинающуюся с нуля. `oleFile` (и при необходимости `imageFile`) должен уже существовать в целевом хранилище; в противном случае запрос вернёт ошибку.

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/OleObjects/PutWorksheetOleObject) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать инструмент командной строки **cURL** для вызова веб-сервисов Aspose.Cells. Пример ниже демонстрирует, как добавить OLE-объект с помощью cURL. **Для всех вызовов в рабочей среде требуется HTTPS.**

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/oleobjects" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"ImageSourceFullName":"aspose-logo.png", "IsAutoSize":true, "SourceFullName":"Sample_Book2.xls", "UpperLeftRow":15, "Top":10, "UpperLeftColumn":5, "Left":10, "Width":400, "Height":400}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

![Скриншот, показывающий OLE-объект, встроенный в рабочий лист Excel](/cells/images/ru/ole-object-example.png)

**Возможные коды HTTP-статуса**

| Код  | Описание                                           |
|------|----------------------------------------------------|
| 200  | OLE-объект успешно добавлен.                       |
| 400  | Неверный запрос — отсутствующие или недопустимые параметры. |
| 401  | Неавторизовано — недействительный или отсутствующий JWT-токен. |
| 404  | Не найдено — книга, рабочий лист или исходный файл не существуют. |
| 500  | Внутренняя ошибка сервера — непредвиденный сбой.   |

Типичный успешный ответ возвращает следующий JSON-payload:

```json
{
  "Code": 200,
  "Status": "OK",
  "Data": {
    "OleObjectId": "12345",
    "UpperLeftRow": 15,
    "UpperLeftColumn": 5,
    "Width": 400,
    "Height": 400,
    "SourceFullName": "Sample_Book2.xls",
    "ImageSourceFullName": "aspose-logo.png"
  }
}
```

## Семейство облачных SDK

Использование SDK ускоряет разработку. SDK абстрагирует низкоуровневые детали, позволяя сосредоточиться на бизнес-логике. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}