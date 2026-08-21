---
title: "Удаление дублирующихся строк из ListObject – Документация API Aspose.Cells Cloud"
second_title: "Документ"
linktitle: "Удаление дубликатов"
type: docs
keywords: "удаление дубликатов, listobject, API Aspose.Cells Cloud, Excel, REST"
url: /list-objects/remove-duplicates/ru/
description: "Узнайте, как удалить дублирующиеся строки из ListObject в листе Excel с помощью REST API Aspose.Cells Cloud. Включает endpoint, параметры, аутентификацию, а также примеры запросов и ответов."
weight: 20
---

Этот REST API удаляет дублирующиеся строки из **ListObject** в листе Excel.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates
```

### **Параметры запроса**

| Имя параметра      | Тип    | Расположение | Описание                                                |
| ------------------- | ------ | ------------ | ------------------------------------------------------- |
| **name**            | String | Path         | Имя файла Excel.                                        |
| **sheetName**       | String | Path         | Имя листа, содержащего объект списка.                   |
| **listObjectIndex** | Integer| Path         | Индекс объекта списка (начинается с 0) для обработки.   |
| **folder**          | String | Query        | (Необязательно) Путь к папке, где хранится файл.        |
| **storageName**     | String | Query        | (Необязательно) Имя сервиса хранилища.                  |

### Пример запроса (cURL)

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates" \
  -X POST \
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
  "DuplicateRowsRemoved": 12,
  "Message": "Дублирующиеся строки успешно удалены."
}
```

{{< /tab >}}
{{< /tabs >}}

### Ответ

При успешном выполнении сервис возвращает JSON-объект, подобный приведённому выше. Поля:

- **Code** — HTTP-код статуса (`200` — успех).
- **Status** — Текстовое описание статуса.
- **DuplicateRowsRemoved** — Количество удалённых строк.
- **Message** — Дополнительная информация об операции.

**HTTP-коды статуса**

| Код | Значение                    | Описание                                             |
|-----|-----------------------------|------------------------------------------------------|
| 200 | OK                          | Фильтр успешно применён; ответ содержит детали операции. |
| 400 | Bad Request                 | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized                | Недопустимый или отсутствующий JWT-токен.            |
| 413 | Payload Too Large           | Загружаемый файл превышает допустимый размер.        |
| 500 | Internal Server Error       | Непредвиденная ошибка сервера.                       |

## Семейство облачных SDK

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в репозитории GitHub.

Примеры кода ниже демонстрируют, как вызывать облачные службы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectRemoveDuplicates.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectRemoveDuplicates.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectRemoveDuplicates.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectRemoveDuplicates.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectRemoveDuplicates.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectRemoveDuplicates.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectRemoveDuplicates.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectRemoveDuplicates.go" >}}

{{< /tab >}}

{{< /tabs >}}