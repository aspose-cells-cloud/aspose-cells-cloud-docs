---
title: "Добавление поля сводной таблицы в сводную таблицу"
second_title: "Документ"
linktype: "add-pivot-field"
type: docs
url: /ru/pivot-tables/add-pivot-field/
aliases: [  /ru/add-a-pivot-table-in-a-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel, сводная таблица, добавление поля сводной таблицы, REST API, SDK"
description: "Добавление поля сводной таблицы в существующую сводную таблицу с помощью REST API Aspose.Cells Cloud. Включает сведения о запросе, пример cURL и фрагменты кода SDK."
weight: 40
ArticleTitle: "Добавление поля сводной таблицы в сводную таблицу – Документация Aspose.Cells Cloud"
---

Этот REST API **добавляет** поле в существующую сводную таблицу.

> **Необходимое условие:** Для вызова этой конечной точки необходимо включить действующий JWT-токен аутентификации в заголовке `Authorization`, а также убедиться, что рабочая книга сохранена в указанной папке или в хранилище по умолчанию.

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotField
```

### Параметры запроса

| Имя параметра   | Тип     | Расположение | Описание                                                             |
| ----------------|---------|--------------|----------------------------------------------------------------------|
| name            | string  | path         | Имя документа.                                                       |
| sheetName       | string  | path         | Имя листа.                                                           |
| pivotTableIndex | integer | path         | Индекс сводной таблицы.                                              |
| pivotFieldType  | string  | query        | Тип области полей (например, Row, Column).                           |
| request         | object  | body         | DTO, содержащий индексы полей для добавления.                        |
| needReCalculate | boolean | query        | Установите значение **true**, чтобы пересчитать сводную таблицу после операции. |
| folder          | string  | query        | Папка, в которой сохранён документ.                                  |
| storageName     | string  | query        | Имя хранилища.                                                       |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/PutPivotTableField) определяет общедоступное программное интерфейсное описание и позволяет выполнять взаимодействие по REST напрямую из веб-браузера.

Вы можете использовать утилиту командной строки **cURL** для вызова веб-сервисов Aspose.Cells. В приведённом ниже примере показано, как добавить поле сводной таблицы с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/PivotField?pivotFieldType=Row" \
  -X PUT \
  -d '{"Data":[1,2]}' \
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

При успешном выполнении возвращается JSON-объект с полями `Code` и `Status`. Пример схемы:

```json
{
  "Code": 0,        // целое число, обозначающее код HTTP-статуса
  "Status": "OK"    // строковое сообщение
}
```

Возможные ошибочные ответы включают **400 Bad Request** (некорректные или отсутствующие параметры), **401 Unauthorized** (недействительный токен) и **500 Internal Server Error** (ошибки на стороне сервера).

## Семейство облачных SDK

Использование SDK — самый быстрый способ интеграции этой функциональности. SDK обрабатывают низкоуровневые детали, позволяя вам сосредоточиться на бизнес-логике. Полный список SDK Aspose.Cells Cloud приведён в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="Ruby" tabName4="Python" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-AddPivotFieldInPivottable-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-AddPivotFieldInPivottable-add-pivot-field.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddPivotFieldInPivotTable.py" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-AddPivotFieldInPivottable-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-AddPivotFieldInPivottable-add-pivot-field.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-AddPivotFieldInPivottable-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "8f9b66d50f7cfa2b14c24fa7ddb396e7" >}}

{{< /tab >}}

{{< /tabs >}}

**См. также:**  
- [Добавление сводной таблицы](https://docs.aspose.cloud/cells/ru/pivot-tables/add-pivot-table/)  
- [Удаление поля сводной таблицы](https://docs.aspose.cloud/cells/ru/pivot-tables/delete-pivot-field/)