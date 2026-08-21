---
title: "Обновление стиля сводной таблицы"
second_title: "Документ"
linktype: "Форматировать все"
type: docs
url: /ru/pivot-tables/format-all/
aliases: [  /ru/update-style-for-pivot-table/ ]
keywords: "сводная таблица, обновление стиля, Aspose.Cells Cloud, REST API, Excel, электронная таблица, API, стиль сводной таблицы, форматировать все"
description: "Узнайте, как обновить стиль всей сводной таблицы с помощью REST API Aspose.Cells Cloud. Включает подробности запроса, пример cURL и фрагменты кода SDK для множества языков программирования."
weight: 100
ArticleTitle: "Обновление стиля сводной таблицы — Aspose.Cells Cloud API"
---

Этот REST API обновляет стиль сводной таблицы.

## API PostPivotTableStyle

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/FormatAll
```

**Требования / Аутентификация**  
Для заголовка `Authorization` необходимо предоставить действительный JWT-токен доступа (например, `Bearer <jwt token>`). Убедитесь, что токен имеет права доступа к указанной рабочей книге и рабочему листу.

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### **Параметры запроса**

| Имя параметра  | Тип    | Расположение | Описание                                                                            |
| --------------- | ------- | -------- | -------------------------------------------------------------------------------------- |
| name            | string  | путь     | Имя файла рабочей книги.                                                              |
| sheetName       | string  | путь     | Рабочий лист, содержащий сводную таблицу.                                             |
| pivotTableIndex | integer | путь     | Индекс сводной таблицы (начиная с нуля), стиль которой необходимо изменить.          |
| style           | object  | тело     | Объект DTO стиля, определяющий форматирование, которое необходимо применить.         |
| needReCalculate | boolean | запрос   | Установите значение **true**, чтобы пересчитать сводную таблицу после форматирования; по умолчанию — **false**. |
| folder          | string  | запрос   | Папка, в которой хранится рабочая книга.                                             |
| storageName     | string  | запрос   | Имя сервиса хранения.                                                                 |

<a href="https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableStyle" rel="noopener noreferrer">Спецификация OpenAPI</a> определяет публично доступный программный интерфейс и позволяет выполнять REST-взаимодействия напрямую из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Пример ниже демонстрирует, как выполнить вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/FormatAll" \
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

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                                      |
|------|-----------------------------|---------------------------------------------------------------|
| 200  | OK (ОК)                     | Фильтр успешно применён; в ответе содержатся детали операции. |
| 400  | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized (Неавторизован) | Недействительный или отсутствующий JWT-токен.                |
| 413  | Payload Too Large (Слишком большой запрос) | Загруженный файл превышает лимит размера.                    |
| 500  | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                               |

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

Использование SDK — самый быстрый способ разработки под API. SDK абстрагирует низкоуровневые детали, позволяя сосредоточиться на бизнес-логике. Полный список облачных SDK Aspose.Cells Cloud см. в <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">репозитории на GitHub</a>.

Пример кода ниже демонстрирует вызов API с использованием SDK для Go:

{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "0b2caae7acfa3e947b856c07b6e8633a" >}}

{{< /tab >}}

{{< /tabs >}}