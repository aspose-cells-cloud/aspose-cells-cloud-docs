---
title: "Обновление стиля ячейки сводной таблицы"
second_title: "Документ"
linktype: "Форматирование"
type: docs
url: /pivot-tables/format/
aliases: [/update-cell-style-for-pivot-table/]
keywords: "Aspose.Cells Cloud, стиль сводной таблицы, API обновления стиля ячейки, REST API, Excel API, форматирование электронных таблиц, облачный SDK, стиль ячейки, сводная таблица"
description: "Узнайте, как обновить стиль конкретной ячейки сводной таблицы в Aspose.Cells Cloud через REST API. Включает адрес endpoints, параметры, аутентификацию, пример cURL, фрагмент кода Go SDK и SEO‑оптимизированное руководство."
weight: 90
ArticleTitle: "Обновление стиля ячейки сводной таблицы — документация API Aspose.Cells Cloud"
---

Этот REST API обновляет **стиль** ячейки в сводной таблице.

**Предварительные требования / Аутентификация**  
Для вызова этого endpoints необходимо иметь действующий JWT-токен доступа Aspose Cloud. Получите токен с помощью потока OAuth 2.0, описанного в [Руководстве по аутентификации](/authentication/). Включите токен в заголовок запроса:

```http
Authorization: Bearer <jwt token>
```

JWT-токен требуется для всех вызовов API Aspose.Cells Cloud.

## API PostPivotTableCellStyle

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/Format
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### **Параметры запроса**

| Имя параметра   | Тип     | Расположение | Описание                                                                                               |
|-----------------|---------|-------------|--------------------------------------------------------------------------------------------------------|
| name            | string  | path        | Имя документа (обязательно).                                                                           |
| sheetName       | string  | path        | Имя рабочего листа (обязательно).                                                                      |
| pivotTableIndex | integer | path        | Индекс сводной таблицы (обязательно).                                                                  |
| column          | integer | query       | Нулевой индекс столбца ячейки для форматирования (обязательно).                                        |
| row             | integer | query       | Нулевой индекс строки ячейки для форматирования (обязательно).                                         |
| style           | object  | body        | DTO стиля (объект передачи данных), определяющий новый стиль ячейки.                                  |
| needReCalculate | boolean | query       | Указывает, следует ли пересчитать сводную таблицу после форматирования. Значение по умолчанию — **false**. |
| folder          | string  | query       | Папка, в которой хранится документ (необязательно).                                                    |
| storageName     | string  | query       | Имя хранилища (необязательно).                                                                         |
| Method          | string  | N/A         | Используемый HTTP-метод запроса (**POST**).                                                            |

<a href="https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableCellStyle" target="_blank" rel="noopener noreferrer">Спецификация OpenAPI</a> определяет общедоступное программное интерфейсное решение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать инструмент командной строки **cURL** для простого доступа к веб-сервисам Aspose.Cells. Пример ниже показывает, как сделать вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/Format?column=1&row=1" \
  -X POST \
  -d '{"Font":{"Name":"Arial","Size":10}}' \
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

**Ответ**  
При успешном выполнении сервис возвращает HTTP 200 с пустым телом, что означает применение стиля. В случае ошибки возвращается JSON-полезная нагрузка с кодом и сообщением об ошибке.

| HTTP-статус | Описание                                                                 |
|------------|--------------------------------------------------------------------------|
| 200        | Стиль успешно применён.                                                  |
| 400        | Неверный запрос — например, недопустимый индекс столбца/строки.          |
| 401        | Неавторизованный доступ — отсутствует или недействителен JWT-токен.     |
| 404        | Не найдено — указанный документ, рабочий лист или сводная таблица не существует. |
| 500        | Внутренняя ошибка сервера — непредвиденное состояние.                    |

Тело ответа при успешном выполнении пусто.

Дополнительные сведения см. в документации API **Get Pivot Table**.

## Семейство облачных SDK

Использование SDK — самый быстрый способ разработки. SDK скрывает низкоуровневые детали, позволяя сосредоточиться на бизнес-логике. Посетите <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">репозиторий GitHub</a>, чтобы ознакомиться с полным списком облачных SDK Aspose.Cells Cloud.

Пример кода ниже демонстрирует вызов веб-сервисов Aspose.Cells с использованием **Go SDK**:

{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "3236805d26482f06f4656b14f2d00d79" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Обновление стиля ячейки сводной таблицы",
  "description": "Руководство по обновлению стиля конкретной ячейки сводной таблицы Aspose.Cells Cloud через REST API.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2026-07-30",
  "keywords": "Aspose.Cells Cloud, сводная таблица, стиль ячейки, REST API, Go SDK",
  "url": "https://docs.aspose.cloud/cells/pivot-tables/format/",
  "publisher": {
    "@type": "Organization",
    "name": "Aspose"
  }
}
</script>
---