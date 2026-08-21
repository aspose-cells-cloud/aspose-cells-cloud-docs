---
title: "Перемещение именованного диапазона в рабочей книге Excel"
second_title: "Документ"
linktitle: "Переместить"
type: docs
url: /ranges/move/
aliases: [/move-a-named-range-with-an-excel-worksheet/]
keywords: "Aspose.Cells Cloud, перемещение именованного диапазона, рабочая книга Excel, REST API, перемещение диапазона, примеры SDK"
description: "Узнайте, как переместить именованный диапазон в пределах рабочей книги Excel с помощью REST API Aspose.Cells Cloud v3.0. Приведены сведения об эндпоинте, аутентификации, примеры и код SDK."
weight: 20
ArticleTitle: "Перемещение именованного диапазона в рабочей книге Excel с помощью API Aspose.Cells Cloud"
---

Перемещение именованного диапазона — распространённая задача при необходимости программной переорганизации данных. В этом разделе описано, как переместить определённый диапазон на новую позицию в той же рабочей книге с использованием REST API Aspose.Cells Cloud.

Этот REST API перемещает указанный диапазон в целевой диапазон на рабочей книге Excel.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/moveto
```

### Аутентификация
API требует **Bearer JWT-токена**, полученного через OAuth-процедуру Aspose Cloud. Включите токен в заголовок `Authorization`:

```
Authorization: Bearer <jwt token>
```

Токен должен иметь область доступа **Cells**.

### Предварительные требования
- Рабочая книга должна храниться в облачном хранилище Aspose Cloud.  
- Укажите имя хранилища (`storageName`) и путь к папке (`folder`), если файл находится не в корневом каталоге.  
- Используйте последнюю версию SDK Aspose.Cells Cloud, поддерживающую версию API **v3.0**.

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### Параметры запроса

| Имя            | Тип    | Расположение | Описание |
|----------------|--------|-------------|----------|
| **name**       | string | path        | Имя файла рабочей книги |
| **sheetName**  | string | path        | Имя рабочей книги |
| **destRow**    | integer| query       | Индекс первой строки целевого диапазона (начиная с 0) |
| **destColumn**| integer| query       | Индекс первого столбца целевого диапазона (начиная с 0) |
| **range**      | object | body        | Описание исходного диапазона, который необходимо переместить |
| **folder**     | string | query       | Путь к папке, где хранится рабочая книга |
| **storageName**| string | query       | Имя облачного хранилища Aspose Cloud |

### Тело запроса

| Поле           | Тип    | Обязательное | Описание |
|----------------|--------|-------------|----------|
| **ColumnCount**| integer| Нет         | Количество столбцов в исходном диапазоне |
| **ColumnWidth**| integer| Нет         | Ширина каждого столбца (в пунктах) |
| **FirstColumn**| integer| Нет         | Индекс первого столбца исходного диапазона (начиная с 0) |
| **FirstRow**   | integer| Нет         | Индекс первой строки исходного диапазона (начиная с 0) |
| **Name**       | string | Нет         | Имя диапазона (если это именованный диапазон) |
| **RefersTo**   | string | Нет         | Ссылка в стиле A1, определяющая диапазон |
| **RowCount**   | integer| Нет         | Количество строк в исходном диапазоне |
| **RowHeight**  | integer| Нет         | Высота каждой строки (в пунктах) |
| **Worksheet**  | string | Нет         | Рабочая книга, содержащая исходный диапазон |

### Порядок выполнения

1. **Загрузите** рабочую книгу в облачное хранилище Aspose Cloud (если она ещё не загружена).  
2. **Создайте** JWT-токен с помощью OAuth-эндпоинта.  
3. **Сформируйте** JSON-полезную нагрузку, описывающую исходный диапазон.  
4. **Вызовите** эндпоинт `moveto`, указав необходимые параметры пути, запроса и JSON-тело.  
5. **Проверьте** ответ: при успешном вызове возвращается статус `200 OK`.

### Пример запроса / ответа

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/moveto?destRow=20&destColumn=20" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{ 
  "ColumnCount": 7,
  "ColumnWidth": 19,
  "FirstColumn": 0,
  "FirstRow": 9,
  "Name": "MyRange",
  "RefersTo": "A10:G10",
  "RowCount": 1,
  "RowHeight": 15,
  "Worksheet": "Sheet1"
}'
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

При возникновении ошибки в ответе присутствует необязательное поле `ErrorMessage`, содержащее дополнительные сведения об ошибке.

**Коды HTTP-статуса**

| Код  | Значение                    | Описание |
|------|-----------------------------|----------|
| 200  | OK (Успех)                  | Фильтр применён успешно; ответ содержит сведения об операции. |
| 400  | Bad Request (Неверный запрос) | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized (Неавторизован) | Некорректный или отсутствующий JWT-токен. |
| 413  | Payload Too Large (Слишком большой payload) | Загружаемый файл превышает ограничение по размеру. |
| 500  | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера. |

**Схема ответа**

| Поле | Тип | Описание |
|------|-----|----------|
| **Code** | integer | Код статуса HTTP-подобного ответа, возвращаемого API (например, 200) |
| **Status** | string | Текстовое описание результата (например, "OK") |
| **ErrorMessage** | string (необязательно) | Читаемые человеком сведения об ошибке при неудачном вызове |

## Семейство облачных SDK

Использование SDK — оптимальный способ ускорить разработку. SDK скрывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">репозитории на GitHub</a>.

Примеры кода ниже демонстрируют, как вызывать веб-сервисы Aspose.Cells с помощью различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeMoveTo.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeMoveTo.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeMoveTo.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeMoveTo.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeMoveTo.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeMoveTo.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeMoveTo.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeMoveTo.go" >}}

{{< /tab >}}

{{< /tabs >}}