---
title: "Работа с сводными таблицами с помощью задачи CellsObjectOperate"
type: docs
url: /tasks/cells-object-operate/pivottable/
aliases: [/working-with-pivot-table-using-cellsobjectoperate-task/]
keywords: "Aspose Cells API для сводных таблиц, CellsObjectOperate, REST API для Excel"
description: "Узнайте, как создавать сводные таблицы в Excel с помощью задачи CellsObjectOperate в Aspose.Cells Cloud. Приведён пример cURL, описание параметров и ссылки на SDK."
weight: 10
---

Этот REST API **создаёт** сводную таблицу с использованием задачи **CellsObjectOperate**.

**Параметры операции со сводной таблицей (PivotTableOperateParameter)**

| Имя параметра       | Тип           | Описание                                                                 |
|---------------------|---------------|--------------------------------------------------------------------------|
| DestCellName        | string        | Верхняя левая ячейка сводной таблицы (например, `C1`).                   |
| SourceData          | string        | Диапазон, содержащий исходные данные (например, `Sheet2!A1:E8`).         |
| TableName           | string        | Имя, присваиваемое новой сводной таблице.                                |
| UseSameSource       | string        | `true` / `false` — указывает, использует ли сводная таблица тот же рабочий файл. |
| PivotTableIndex     | integer       | Индекс сводной таблицы при наличии нескольких таблиц на листе.           |
| PivotFieldRows      | integer[]     | Индексы полей (начиная с 0), размещаемых в строковой области.             |
| PivotFieldColumns   | integer[]     | Индексы полей (начиная с 0), размещаемых в столбцовой области.            |
| PivotFieldData      | integer[]     | Индексы полей (начиная с 0), используемых в качестве данных для агрегирования. |

## REST API

| **API**               | **Тип** | **Описание**           | **Ссылка на ресурс** |
|-----------------------|---------|------------------------|----------------------|
| /cells/task/runtask   | POST    | Выполнить задачу       | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

[OpenAPI-спецификация](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) определяет публично доступное программное интерфейсное решение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

### Необходимые условия
Перед вызовом API необходимо:

1. Зарегистрировать учётную запись Aspose.Cloud и создать приложение для получения **client ID** и **client secret**.  
2. Получить **JWT-токен** от эндпоинта `/connect/token`, используя клиентские учётные данные.  
3. Включать токен в заголовок каждого запроса как `Authorization: Bearer <jwt token>`.  

Теперь вы можете использовать утилиту командной строки **cURL** для доступа к веб-сервисам Aspose.Cells.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
# Пример cURL — импорт данных (шаг 1)
curl -v "https://api.aspose.cloud/v3.0/cells/task/runtask" \
  -X POST \
  -H "accept: application/xml" \
  -H "Content-Type: application/xml" \
  -H "Authorization: Bearer <jwt token>" \
  -d '
<TaskData>
  <Tasks>
    <TaskDescription>
      <TaskType>ImportData</TaskType>
      <ImportDataTaskParameter>
        <Workbook>
          <FileSourceType>CloudFileSystem</FileSourceType>
          <FilePath>Book1.xlsx</FilePath>
        </Workbook>
        <ImportBatchDataOption>
          <DestinationWorksheet>Sheet2</DestinationWorksheet>
          <IsInsert>true</IsInsert>
          <BatchData>
            <!-- Примеры строк — приведены лишь несколько для краткости -->
            <CellValue><rowIndex>0</rowIndex><columnIndex>0</columnIndex><type>String</type><value>Вид спорта</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>1</columnIndex><type>String</type><value>Год</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>2</columnIndex><type>String</type><value>Квартал</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>3</columnIndex><type>String</type><value>Продажи</value></CellValue>
            <!-- …дополнительные строки опущены для краткости… -->
          </BatchData>
        </ImportBatchDataOption>
      </ImportDataTaskParameter>
    </TaskDescription>

    <TaskDescription>
      <TaskType>CellsObjectOperate</TaskType>
      <CellsObjectOperateTaskParameter>
        <OperateObject>
          <OperateObjectType>ListObject</OperateObjectType>
          <Position>
            <Workbook>
              <FileSourceType>InMemoryFiles</FileSourceType>
              <FilePath>Book1.xlsx</FilePath>
            </Workbook>
            <SheetName>Sheet1</SheetName>
            <ListObjectIndex>0</ListObjectIndex>
          </Position>
        </OperateObject>

        <PivotTableOperateParameter>
          <OperateType>Add</OperateType>
          <SourceData>=Sheet2!A1:E8</SourceData>
          <DestCellName>C1</DestCellName>
          <TableName>TestPivot</TableName>
          <UseSameSource>true</UseSameSource>
          <PivotTableIndex>0</PivotTableIndex>
          <PivotFieldRows><int>0</int><int>1</int></PivotFieldRows>
          <PivotFieldColumns><int>2</int></PivotFieldColumns>
          <PivotFieldData><int>3</int><int>4</int></PivotFieldData>
        </PivotTableOperateParameter>

        <DestinationWorkbook>
          <FileSourceType>InMemoryFiles</FileSourceType>
          <FilePath>Book001.xlsx</FilePath>
        </DestinationWorkbook>
      </CellsObjectOperateTaskParameter>
    </TaskDescription>

    <TaskDescription>
      <TaskType>SaveResult</TaskType>
      <SaveResultTaskParameter>
        <ResultSource>InMemoryFiles</ResultSource>
        <ResultDestination>
          <DestinationType>OutputStream</DestinationType>
          <InputFile>Book001.xlsx</InputFile>
          <OutputFile>Output/ReportS004.xlsx</OutputFile>
        </ResultDestination>
      </SaveResultTaskParameter>
    </TaskDescription>
  </Tasks>
</TaskData>'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```text
Возможные HTTP-коды состояния:
- **200 OK** — сводная таблица успешно создана. Тело ответа содержит `TaskId`, по которому можно запросить статус операции.
- **400 Bad Request** — неверный XML-пакет или отсутствуют обязательные параметры.
- **401 Unauthorized** — отсутствует или недействителен JWT-токен.
- **500 Internal Server Error** — непредвиденная ошибка на стороне сервера.

Пример успешного ответа (XML):

<?xml version="1.0" encoding="UTF-8"?>
<TaskResponse>
  <TaskId>12345</TaskId>
  <Status>Completed</Status>
  <Result>
    <ResultSource>InMemoryFiles</ResultSource>
    <ResultDestination>Output/ReportS004.xlsx</ResultDestination>
  </Result>
</TaskResponse>
```

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

Использование SDK — это лучший способ ускорить разработку. SDK берёт на себя работу с низкоуровневыми деталями и позволяет сосредоточиться на задачах проекта. Полный список облачных SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызовы веб-сервисов Aspose.Cells с использованием различных SDK: