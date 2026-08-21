---
title: "Преобразование объекта списка в диапазон — Aspose.Cells Cloud API"
ArticleTitle: "Преобразование объекта списка (таблицы) в диапазон с использованием Aspose.Cells Cloud API"
second_title: "Документ"
linktitle: "Преобразование"
type: docs
url: /ru/list-objects/to-range/
aliases:
  - /convert-list-object-or-table-to-range/
  - /tables/to-range/
keywords: "Aspose Cells API, преобразование объекта списка в диапазон, Excel REST API"
description: "Узнайте, как преобразовать объект списка (таблицу) Excel в диапазон с использованием Aspose.Cells Cloud REST API. Включает синтаксис запроса, параметры, пример cURL, схему ответа, данные об аутентификации, коды ошибок и примеры SDK."
weight: 30
---

Этот REST API преобразует **объект списка (таблицу)** в **диапазон** в пределах рабочего листа Excel.

**Необходимые условия:**  
Перед вызовом конечной точки убедитесь, что рабочая книга загружена в облачное хранилище Aspose Cloud, на рабочем листе присутствует целевой объект списка, и используется поддерживаемый формат файла (например, .xlsx, .xlsm).

## REST API

**Аутентификация**  
Для вызова этой операции необходимо включить действительный JWT-токен в заголовке `Authorization`. Получите токен, отправив POST-запрос на конечную точку OAuth 2.0 с вашим идентификатором клиента и секретом клиента. Токен должен включать область `Cells.ReadWrite` и действителен в течение периода, возвращаемого сервисом токенов.

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/ConvertToRange
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

### Параметры запроса

| Название            | Тип     | Расположение | Обязательный | По умолчанию | Описание                                                |
| ------------------- | ------- | ------------ | ----------- | ------------ | ------------------------------------------------------- |
| **name**            | string  | путь         | Да          | –            | Имя файла Excel.                                        |
| **sheetName**       | string  | путь         | Да          | –            | Имя рабочего листа, содержащего объект списка.         |
| **listObjectIndex** | integer | путь         | Да          | –            | Индекс объекта списка (таблицы) для преобразования (начиная с 0). |
| **folder**          | string  | запрос       | Нет         | –            | Путь к папке, в которой хранится файл.                 |
| **storageName**     | string  | запрос       | Нет         | –            | Имя сервиса хранилища.                                  |

> **Примечание:** Эта операция работает только с современными форматами Excel, такими как **.xlsx** и **.xlsm**. Объект списка не должен быть защищён. Дополнительные сведения об объектах списка см. в [обзоре объектов списка](/list-objects/). Сведения о работе с диапазонами см. в [документации по диапазонам](/ranges/).

### Пример cURL (запрос)

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/0/ConvertToRange" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your-jwt-token>"
```

{{< /tab >}}

#### Схема ответа

API возвращает ответ **200 OK** с данными о новом созданном диапазоне.

```json
{
  "Code": 200,
  "Status": "OK",
  "RangeName": "A1:C10",
  "Address": "Sheet1!A1:C10",
  "FirstRow": 0,
  "FirstColumn": 0,
  "RowCount": 10,
  "ColumnCount": 3
}
```

| Поле            | Тип     | Описание                                           |
| --------------- | ------- | -------------------------------------------------- |
| **Code**        | integer | Код HTTP-подобного статуса (200 означает успех).   |
| **Status**      | string  | Текстовое сообщение статуса.                       |
| **RangeName**   | string  | Имя, присвоенное созданному диапазону.             |
| **Address**     | string  | Полный адрес диапазона, включая имя листа.         |
| **FirstRow**    | integer | Индекс первой строки диапазона (начиная с 0).      |
| **FirstColumn** | integer | Индекс первого столбца диапазона (начиная с 0).    |
| **RowCount**    | integer | Количество строк в диапазоне.                      |
| **ColumnCount** | integer | Количество столбцов в диапазоне.                   |

**Коды HTTP-статусов**

| Код | Значение                    | Описание                                                 |
|-----|-----------------------------|----------------------------------------------------------|
| 200 | OK                          | Фильтр успешно применён; ответ содержит данные операции. |
| 400 | Bad Request                 | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized                | Недопустимый или отсутствующий JWT-токен.               |
| 413 | Payload Too Large           | Загруженный файл превышает ограничение по размеру.       |
| 500 | Internal Server Error       | Непредвиденная ошибка сервера.                           |

**Схема ответа об ошибке (пример):**

```json
{
  "Code": 400,
  "Message": "Invalid listObjectIndex. Index must be between 0 and 5."
}
```

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "RangeName": "A1:C10",
  "Address": "Sheet1!A1:C10",
  "FirstRow": 0,
  "FirstColumn": 0,
  "RowCount": 10,
  "ColumnCount": 3
}
```

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Ознакомьтесь с [репозиторием GitHub](https://github.com/aspose-cells-cloud), чтобы увидеть полный список SDK Aspose.Cells Cloud.

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectConvertToRange.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectConvertToRange.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectConvertToRange.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectConvertToRange.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectConvertToRange.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectConvertToRange.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectConvertToRange.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectConvertToRange.go" >}}

{{< /tab >}}

{{< /tabs >}}