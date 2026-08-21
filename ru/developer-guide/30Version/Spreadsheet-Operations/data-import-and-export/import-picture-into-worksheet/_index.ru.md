---
title: "Импорт изображения в рабочий лист Excel"
ArticleTitle: "Импорт изображения в рабочий лист Excel — руководство по Aspose.Cells Cloud API"
second_title: "Документ"
linktype: "docs"
url: /ru/import-picture-into-excel-worksheet/
aliases:
  - /import-picture-into-worksheet/
  - /import-data/picture/
  - /import/picture/
keywords: "импорт изображения, Excel, Aspose.Cells Cloud, REST API, v3.0"
description: "Узнайте, как импортировать изображения в рабочие листы Excel с помощью Aspose.Cells Cloud REST API v3.0. Включены примеры multipart-запросов, образцы кода SDK и рекомендации по обработке ошибок. Начните работу быстро, следуя четким шагам."
weight: 19
---

Импорт изображения в рабочий лист Excel позволяет обогатить электронные таблицы визуальным содержимым — например, логотипами, диаграммами или схемами. В этом руководстве описано, как использовать операцию Aspose.Cells Cloud **ImportPicture**, необходимый формат запроса и способы обработки ответов.

**Необходимые условия:** Перед вызовом операции импорта убедитесь, что у вас есть действительный JWT-токен аутентификации и уже сохраненная в хранилище Aspose Cloud электронная таблица.

## API PostImportData

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

### **Параметры запроса**

Запрос представляет собой HTTP **POST** с содержимым типа **multipart/related** (см. [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) или [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).

- **Первая часть** содержит JSON-объект с именем **ImportPictureOption**, описывающий, куда и как следует разместить изображение.
- **Вторая часть** передает файл изображения (или его Base64-кодированные данные).

### ImportPictureOption — определение

```json
{
  "UpperLeftRow": 0,
  "UpperLeftColumn": 0,
  "LowerRightRow": 10,
  "LowerRightColumn": 5,
  "Filename": "logo.png",
  "Data": "iVBORw0KGgoAAAANSUhEUgAA...",
  "DestinationWorksheet": "Sheet1",
  "IsInsert": true,
  "ImportDataType": "Picture",
  "Source": { "FileSource": "Storage" }
}
```

_`IsInsert` — **логическое** значение: `true` означает вставку нового изображения, `false` — замену существующего._

### Важные параметры

**ImportPictureOption**

| Имя параметра       | Тип         | Описание                                                                                                                                                                     |
|---------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UpperLeftRow        | int         | Индекс строки верхнего левого угла, в котором будет размещено изображение.                                                                                                   |
| UpperLeftColumn     | int         | Индекс столбца верхнего левого угла, в котором будет размещено изображение.                                                                                                  |
| LowerRightRow       | int         | Индекс строки нижнего правого угла, определяющего границы изображения.                                                                                                       |
| LowerRightColumn    | int         | Индекс столбца нижнего правого угла, определяющего границы изображения.                                                                                                      |
| Filename            | string      | Имя файла изображения.                                                                                                                                                       |
| Data                | string      | Base64-кодированные двоичные данные изображения (необязательно, если файл передается во второй части запроса).                                                              |
| DestinationWorksheet| string      | Имя рабочего листа, в который будет вставлено изображение.                                                                                                                  |
| **IsInsert**        | **boolean** | `true` — вставить новое изображение; `false` — заменить существующее.                                                                                                        |
| ImportDataType      | string      | Тип импортируемых данных (например, `Picture`, `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`). |
| Source              | FileSource  | Указывает местоположение файла данных, когда параметр `BatchData` равен `null`.                                                                                             |

### Ответ

Успешный запрос возвращает **HTTP 200** с JSON-полезной нагрузкой следующего вида:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Возможные коды состояния:

| Код | Значение                                      |
|-----|-----------------------------------------------|
| 200 | Импорт успешно завершен                        |
| 400 | Неверный запрос — отсутствуют или некорректны данные |
| 401 | Неавторизованный доступ — недействительный или отсутствующий токен |
| 500 | Внутренняя ошибка сервера                      |

## Как использовать API PostImportData с SDK

### Спецификация API PostImportData

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) определяет публично доступное программное интерфейсное описание и позволяет выполнять взаимодействие с REST напрямую из веб-браузера.

### Использование SDK Aspose.Cells Cloud

Использование SDK — лучший способ ускорить разработку. SDK берет на себя обработку низкоуровневых деталей, позволяя сосредоточиться на задачах вашего проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Приведенные ниже примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}
{{< /tab >}}

{{< /tabs >}}