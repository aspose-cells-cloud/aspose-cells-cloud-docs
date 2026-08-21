---
title: "Пакетное разделение"
second: "Документ"
type: docs
url: /ru/batch/split
keywords: "Пакетное разделение, Aspose.Cells Cloud, REST API, Excel, PDF, CSV, JSON, Электронная таблица, облачный SDK"
description: "Документация по API Aspose.Cells Cloud для пакетного разделения, который разделяет файлы электронных таблиц на несколько форматов, таких как PDF, CSV или JSON. Включает детали запроса, примеры команд cURL и использование SDK для различных языков программирования."
weight: 100
---

Этот REST API выполняет **пакетное разделение** подходящих файлов.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/split
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификацию на основе токена JWT</a>.

### Параметры запроса

| Имя параметра   | Тип                | Путь/Запрос/Строка/Тело HTTP | Описание                                     |
|------------------|--------------------|------------------------------|----------------------------------------------|
| BatchSplitRequest| BatchSplitRequest  | body                         | Полезная нагрузка запроса, содержащая параметры разделения. |

### **Свойства BatchSplitRequest**

| Имя               | Тип                 | Описание                                        | Примечания      |
|-------------------|---------------------|-------------------------------------------------|-----------------|
| SourceFolder      | string              | Папка, содержащая исходный файл.               | [необязательно] |
| SourceStorage     | string              | Имя хранилища, где находится исходный файл.    | [необязательно] |
| MatchCondition    | MatchConditionRequest| Условия, используемые для выбора файлов для разделения.| [необязательно] |
| Format            | string              | Желаемый выходной формат (например, pdf, csv). | [необязательно] |
| FromIndex         | integer             | Начальный индекс страниц для разделения.        | [необязательно] |
| ToIndex           | integer             | Конечный индекс страниц для разделения.         | [необязательно] |
| OutFolder         | string              | Папка назначения для разделённых файлов.        | [необязательно] |
| SaveOptions       | SaveOptions         | Дополнительные параметры сохранения выходных данных.| [необязательно] |

### **Свойства MatchConditionRequest**

| Имя                | Тип       | Описание                                      | Примечания      |
|--------------------|-----------|-----------------------------------------------|-----------------|
| RegexPattern       | string    | Регулярное выражение для сопоставления имён файлов.| [необязательно] |
| FullMatchConditions| string[]  | Список условий полного совпадения.            | [необязательно] |

### Параметр тела запроса

| Имя параметра | Тип | Описание                                      |
| -------------- | ---- | --------------------------------------------- |
| data           | file | Бинарное содержимое файла рабочей книги для создания. |

### **Ответ**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**Коды HTTP-статуса**

| Код | Значение                      | Когда возвращается                              |
|-----|-------------------------------|-------------------------------------------------|
| 200 OK | Рабочая книга успешно создана | Нормальный поток выполнения                      |
| 201 Created | Рабочая книга создана (альтернативный ответ) | Если API возвращает статус «создано»         |
| 400 Bad Request | Некорректные параметры | Ошибка на стороне клиента                        |
| 401 Unauthorized | Отсутствует или недействителен токен | Ошибка аутентификации                          |
| 409 Conflict | Файл существует, а `isWriteOver=false` | Конфликт с существующим файлом                 |


## Как использовать API PostBatchSplit с SDK

### Спецификация API PostBatchSplit

[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/Batch/PostBatchSplit) определяет общедоступное программное интерфейсное определение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для удобного доступа к веб-службам Aspose.Cells. В следующем примере показано, как выполнять вызовы в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/split" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Format\":\"pdf\"}"
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

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали и позволяет сосредоточиться на задачах разделения. Ознакомьтесь с [репозиторием GitHub](https://github.com/aspose-cells-cloud) для получения полного списка SDK Aspose.Cells Cloud.

Приведённые ниже примеры кода демонстрируют вызовы веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js"  tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

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