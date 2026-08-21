---
title: "Удаление сводной таблицы в рабочем листе Excel"
second_title: "Документ"
linktype: Удалить
type: docs
url: /ru/pivot-tables/delete/
aliases: [  /ru/delete-worksheet-pivot-table-by-index/ ]
keywords: "Aspose.Cells, сводная таблица, удаление, Excel, REST API"
description: "Удаление сводной таблицы из рабочего листа Excel с использованием Aspose.Cells Cloud REST API (v3.0). Включает формат запроса, пример cURL, коды ошибок и фрагменты кода SDK для C#, Java, Python, Node.js."
weight: 70
ArticleTitle: "Как удалить сводную таблицу в рабочем листе Excel с помощью Aspose.Cells Cloud"
---

Этот REST API удаляет сводную таблицу из рабочего листа по её индексу.

**Необходимые условия** – У вас должен быть действительный JWT-токен доступа к Aspose.Cells Cloud и целевой файл Excel должен храниться в поддерживаемом месте хранения. Перед вызовом API убедитесь, что имя файла, имя рабочего листа и данные о хранилище указаны корректно.

Сводные таблицы — мощный способ сводки данных в **рабочем листе Excel**. С помощью Aspose.Cells Cloud вы можете программно удалить ненужную сводную таблицу одним HTTP-запросом DELETE. Эта операция идеально подходит для очистки рабочих листов, автоматизации генерации отчётов или интеграции обработки Excel в ваши приложения.

## API DeleteWorksheetPivotTable

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

### **Параметры запроса**

| Имя параметра    | Тип     | Расположение | Описание                                                   |
| ---------------- | ------- | ------------ | ---------------------------------------------------------- |
| name             | string  | path         | Имя документа Excel.                                       |
| sheetName        | string  | path         | Имя рабочего листа, содержащего сводную таблицу.          |
| pivotTableIndex  | integer | path         | Индекс удаляемой сводной таблицы (начинается с нуля).      |
| folder           | string  | query        | Путь к папке, в которой хранится документ.                |
| storageName      | string  | query        | Имя службы хранилища.                                      |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/DeleteWorksheetPivotTable) определяет общедоступное программное интерфейсное описание и позволяет выполнять взаимодействие с REST напрямую из веб-браузера.

Вы можете использовать утилиту командной строки **cURL** для удобного доступа к веб-сервисам Aspose.Cells Cloud. Пример ниже показывает, как делать вызовы в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

**Пример ответа**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Ответ следует простой схеме JSON:

```json
{
  "Code": integer,   // HTTP-подобный код состояния операции
  "Status": string   // Текстовое описание, например, "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Обработка ошибок

Ниже перечислены распространённые коды состояния ответа:

| Код HTTP | Описание                                                         |
| -------- | ---------------------------------------------------------------- |
| 400      | Неверный запрос — отсутствуют или некорректны параметры.        |
| 401      | Неавторизовано — недействительный или отсутствующий JWT-токен. |
| 404      | Не найдено — файл, рабочий лист или сводная таблица не найдены. |
| 500      | Внутренняя ошибка сервера — возникло непредвиденное условие.    |

## Семейство облачных SDK

Использование SDK — лучший способ ускорить разработку. SDK берёт на себя низкоуровневые детали и позволяет сосредоточиться на задачах проекта. Полный список облачных SDK Aspose.Cells Cloud представлен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют, как делать вызовы в веб-сервисы Aspose.Cells Cloud с использованием различных SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-DeleteWorksheetPivotTableIndex-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-DeleteWorksheetPivotTableIndex-delete-worksheet-pivot-table-index.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteWorksheetPivotTablesByIndex.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-DeleteWorksheetPivotTableIndex-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-DeleteWorksheetPivotTableIndex-delete-worksheet-pivot-table-index.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-DeleteWorksheetPivotTableIndex-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "8798eca5f30bf41a4675b83583a72ec3" >}}

{{< /tab >}}

{{< /tabs >}}