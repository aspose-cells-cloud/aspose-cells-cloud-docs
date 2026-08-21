---
title: "Как объединить ячейки в рабочем листе Excel — Aspose.Cells Cloud API (v3.0)"
type: docs
url: /ru/merge-cells-in-excel-worksheet/
weight: 110
keywords: "объединение ячеек, Aspose.Cells, облачный API, Excel"
description: "Руководство по объединению ячеек в рабочем листе Excel с использованием облачного REST API Aspose.Cells и примеров на cURL и SDK."
ArticleTitle: "Как объединить ячейки в рабочем листе Excel — Aspose.Cells Cloud API (v3.0)"
---

Aspose.Cells Cloud REST API объединяет прямоугольный блок ячеек в одну ячейку, охватывающую указанные строки и столбцы.

**Необходимые условия**  
— Действующий JWT-токен для аутентификации.  
— Рабочая книга уже должна существовать в указанной папке хранилища.  
— Настройки хранилища (имя папки и хранилища) должны быть заданы в вашей учетной записи Aspose.Cloud.

## API PostWorksheetMerge

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/merge
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

### Параметры запроса

| Имя параметра | Тип    | Расположение | Описание                                         |
|---------------|--------|-------------|--------------------------------------------------|
| name          | string | path        | Имя рабочей книги.                               |
| sheetName     | string | path        | Имя рабочего листа.                              |
| startRow      | integer | query      | Индекс первой строки (начинается с 0; 0 = первая строка). |
| startColumn   | integer | query      | Индекс первого столбца (начинается с 0; 0 = первый столбец). |
| totalRows     | integer | query      | Количество объединяемых строк.                   |
| totalColumns  | integer | query      | Количество объединяемых столбцов.                |
| folder        | string | query       | Папка, содержащая рабочую книгу.                 |
| storageName   | string | query       | Имя хранилища.                                   |

*Тело запроса для этой операции не требуется.*

## **Ответ**

Возвращает объект CellsCloudResponse.

```json
{
  "Status":"OK",
  "Code":200
}
```

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                         |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK (OK)                     | Фильтр успешно применён; ответ содержит детали операции. |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизовано) | Неверный или отсутствующий JWT-токен.           |
| 413 | Payload Too Large (Слишком большой полезный объект) | Загруженный файл превышает лимит размера. |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                  |

## Как использовать API PostWorksheetMerge с SDK

### Спецификация API PostWorksheetMerge

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetMerge) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки **cURL** для простого доступа к веб-сервисам Aspose.Cells. Пример ниже показывает, как отправлять запросы к облачному API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/merge?startRow=10&startColumn=10&totalRows=10&totalColumns=10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — это лучший способ ускорить разработку. SDK берёт на себя обработку низкоуровневых деталей, позволяя вам сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют, как отправлять запросы к веб-сервисам Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMerge.go" >}}

{{< /tab >}}

{{< /tabs >}}