---
title: "Удаление строки в рабочем листе Excel"
second_title: "Документ"
linktitle: "Строка"
type: docs
url: /ru/rows/delete/row/
aliases: [/ru/delete-row-from-a-worksheet/]
description: "Используйте конечную точку DELETE /worksheets/{sheetName}/cells/rows/{rowIndex} для удаления конкретной строки из рабочего листа Excel через REST API Aspose.Cells Cloud. Приведены команды cURL, примеры SDK и полная справка по параметрам."
keywords: "Aspose.Cells, удаление строки, Excel, API, REST, облако, SDK"
weight: 80
ArticleTitle: "Удаление строки в рабочем листе Excel – Руководство по API Aspose.Cells Cloud"
---

Этот REST API удаляет строку из рабочего листа Excel.

**Необходимые условия**  
- Действующий JWT-токен **Authorization**.  
- Рабочая книга должна быть сохранена в поддерживаемом облачном хранилище Aspose (по умолчанию или пользовательском).  
- Целевая папка (если указана) должна существовать в выбранном хранилище.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **Параметры запроса**

| Имя параметра      | Тип     | Путь / Запрос | Обязательный | Описание                                                                            |
|--------------------|---------|---------------|-------------|-------------------------------------------------------------------------------------|
| **name**           | string  | path          | Да          | Имя рабочей книги.                                                                  |
| **sheetName**      | string  | path          | Да          | Имя рабочего листа.                                                                 |
| **rowIndex**       | integer | path          | Да          | Индекс удаляемой строки (начинается с нуля).                                        |
| **startrow**       | integer | query         | Нет         | Индекс первой удаляемой строки (обычно совпадает с `rowIndex`).                    |
| **totalRows**      | integer | query         | Нет         | Количество последовательно удаляемых строк.                                         |
| **updateReference**| boolean | query         | Нет         | Если `true` (по умолчанию), формулы, именованные диапазоны и другие ссылки обновляются после удаления. |
| **folder**         | string  | query         | Нет         | Папка, содержащая рабочую книгу.                                                    |
| **storageName**    | string  | query         | Нет         | Имя сервиса хранилища.                                                              |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetRow) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Пример ниже демонстрирует полный, готовый к выполнению вызов.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=1&updateReference=true" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

**Возможные коды HTTP-ответов**

| Код  | Значение                             | Описание                                                                        |
|------|--------------------------------------|---------------------------------------------------------------------------------|
| 200  | OK (OK)                              | Строка успешно удалена.                                                         |
| 400  | Bad Request (Неверный запрос)        | Отсутствующие или некорректные параметры (например, нечисловой `rowIndex`).    |
| 401  | Unauthorized (Неавторизован)         | Неверный или отсутствующий JWT-токен.                                           |
| 404  | Not Found (Не найдено)               | Указанная рабочая книга, рабочий лист или строка не существуют.                |
| 500  | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера; подробности — в ответе об ошибке. |

**Пример ответа об ошибке**

```json
{
  "Code": 400,
  "Message": "Указан недопустимый индекс строки."
}
```

## Семейство облачных SDK

Использование SDK — лучший способ ускорить разработку. SDK абстрагирует низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже демонстрируют, как выполнять вызовы веб-сервисов Aspose.Cells с помощью различных SDK:

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=1&updateReference=true" \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

**См. также**  
- [Добавление строки](/ru/cells/rows/add/row/)  
- [Удаление нескольких строк](/ru/cells/rows/delete/rows/)  
- [Получение данных о строке](/ru/cells/rows/get/row/)  
---