---
title: "Добавление сводной таблицы в рабочий лист Excel"
second_title: "Документ"
linktitle: Добавление
type: docs
url: /ru/pivot-tables/add/
aliases: [  /ru/add-a-pivot-table-in-a-worksheet/ ]
keywords: "Добавление сводной таблицы, рабочий лист Excel, Aspose.Cells Cloud, REST API, SDK, сводная таблица Excel"
description: "Используйте Aspose.Cells Cloud REST API для добавления сводной таблицы в рабочий лист Excel. Доступно через SDK для C#, Java, PHP, Python, Node.js, Android, Swift, Perl, Go."
weight: 30
ArticleTitle: "Как добавить сводную таблицу в рабочий лист Excel с помощью Aspose.Cells Cloud"
---

Этот REST API добавляет сводную таблицу в рабочий лист.

**Необходимые условия:**  
- Учётная запись Aspose.Cells Cloud с действительным JWT-токеном доступа.  
- Целевая рабочая книга должна быть сохранена в поддерживаемом хранилище (по умолчанию или указанном пользователем).  
- Рабочий лист, указанный через параметр `sheetName`, должен существовать в рабочей книге.  

## API PutWorksheetPivotTable

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### **Параметры запроса**

| Имя параметра  | Тип     | Расположение | Описание                                                                                                                          |
| -------------- | ------- | ------------ | ---------------------------------------------------------------------------------------------------------------------------------- |
| name           | string  | путь         | Имя документа Excel.                                                                                                              |
| sheetName      | string  | путь         | Имя рабочего листа, в котором будет создана сводная таблица.                                                                     |
| request        | object  | тело         | Объект `CreatePivotTableRequest` — DTO, содержащий определение сводной таблицы.                                                  |
| folder         | string  | запрос       | Папка, содержащая документ.                                                                                                       |
| storageName    | string  | запрос       | Имя хранилища, в котором находится документ.                                                                                      |
| sourceData     | string  | запрос       | Диапазон, предоставляющий исходные данные для нового кэша сводной таблицы (например, `A5:E10`).                                  |
| destCellName   | string  | запрос       | Адрес левой верхней ячейки целевого диапазона для отчёта сводной таблицы.                                                        |
| tableName      | string  | запрос       | Имя, присваиваемое новой сводной таблице.                                                                                         |
| useSameSource  | boolean | запрос       | Если `true`, новая сводная таблица повторно использует существующий источник данных, экономя память, если другой сводная таблица уже использует этот источник. |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/PutWorksheetPivotTable) определяет общедоступное программное API-интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки **cURL** для простого доступа к веб-сервисам Aspose.Cells. Следующий пример показывает, как вызвать облачный API с помощью cURL.

**Примечание по безопасности:** Всегда используйте `https://` при вызове API и храните JWT-токен в секрете; передача его по незащищённому HTTP может привести к его перехвату.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/pivottables" \
-X PUT \
-d '{"Name":"MyPivot","SourceData":"A5:E10","DestCellName":"H20","UseSameSource":true,"PivotFieldRows":[1],"PivotFieldColumns":[1],"PivotFieldData":[1]}' \
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

**Коды HTTP-статусов**

| Код  | Значение                    | Описание                                                                 |
|------|-----------------------------|--------------------------------------------------------------------------|
| 200  | OK (ОК)                     | Фильтр успешно применён; ответ содержит детали выполнения операции.     |
| 400  | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized (Неавторизовано) | Недействительный или отсутствующий JWT-токен.                           |
| 413  | Payload Too Large (Слишком большой payload) | Загруженный файл превышает ограничение по размеру.                     |
| 500  | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                                         |

## Семейство облачных SDK

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-AddPivottableWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-AddPivottableWorksheet-add-pivot-table-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddPivotTableInw" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-AddPivottableWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-AddPivottableWorksheet-add-pivot-table-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-AddPivottableWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "980246b631d7816f257f2ad4664788ea" >}}

{{< /tab >}}

{{< /tabs >}}

Дополнительные операции доступны на соответствующих страницах API: **[Получить сводную таблицу](https://docs.aspose.cloud/cells/pivot-tables/get/)**, **[Удалить сводную таблицу](https://docs.aspose.cloud/cells/pivot-tables/delete/)** и **[Обновить сводную таблицу](https://docs.aspose.cloud/cells/pivot-tables/update/)**.