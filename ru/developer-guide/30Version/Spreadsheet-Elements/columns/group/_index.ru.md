---
title: "Группировка столбцов — Документация Aspise.Cells Cloud API"
description: "Группировка столбцов рабочего листа в Excel-файле с использованием REST API Aspose.Cells Cloud (версия 3.0). Содержит синтаксис запроса, параметры, примеры cURL и SDK, а также детали ответа."
keywords: "Aspose.Cells, группировка столбцов, Excel API, REST, облачный SDK"
weight: 60
type: docs
aliases:
  - /group-columns-in-an-excel-worksheet/
  - /group-columns-in-excel-worksheet/
---

# Группировка столбцов в Excel-таблице

**Версия API:** v3.0  
**Операция:** `PostGroupWorksheetColumns` — группировка столбцов рабочего листа.

---

## Обзор

Этот REST API позволяет сгруппировать диапазон столбцов на рабочем листе. Группируемые столбцы можно отображать или скрывать, что позволяет создавать сворачиваемые секции, аналогичные тем, что реализованы в Microsoft Excel.

---

## Предварительные требования

- Действующий **JWT-токен доступа**, полученный из службы аутентификации Aspose Cloud.  
- Книга должна храниться в месте, доступном для Aspose.Cells Cloud (по умолчанию — в облачном хранилище, либо в пользовательском хранилище).  
- Требуемая версия SDK (если используется SDK): последняя версия, поддерживающая API **v3.0**.  

---

## Аутентификация

Все запросы требуют аутентификации с использованием **Bearer-токена**.

```http
Authorization: Bearer <access_token>
```

Сведения о получении токена см. в [руководстве по аутентификации JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

---

## HTTP-запрос

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/group
```

| Параметр | Место | Обязательный | Описание |
|----------|-------|-------------|----------|
| `name` | Path | Да | Имя файла книги (например, `test.xlsx`). |
| `sheetName` | Path | Да | Имя рабочего листа, содержащего столбцы для группировки. |
| `firstIndex` | Query | Да | Нулевой индекс первого столбца, включаемого в группу. |
| `lastIndex` | Query | Да | Нулевой индекс последнего столбца, включаемого в группу. |
| `hide` | Query | Нет | Если `true`, сгруппированные столбцы скрываются; иначе остаются видимыми. |
| `folder` | Query | Нет | Путь к папке, содержащей книгу. |
| `storageName` | Query | Нет | Имя сервиса хранилища, где расположен файл. |

---

## Пример запроса (cURL)

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/group?firstIndex=1&lastIndex=2&hide=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

> **Примечание:** Запрос использует **HTTPS** для обеспечения зашифрованной передачи данных.

---

## Ответ

### Успех (200)

| Поле | Тип | Описание |
|------|-----|----------|
| `Code` | integer | HTTP-код статуса (`200`). |
| `Status` | string | Текстовое описание состояния операции (`OK`). |

**Пример**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Ошибка (например, 400 Bad Request)

| Поле | Тип | Описание |
|------|-----|----------|
| `Code` | integer | HTTP-код статуса (`400`, `401`, `404`, `500`, …). |
| `Status` | string | Текстовое описание (`Error`). |
| `ErrorMessage` | string | Человекочитаемое описание ошибки. |
| `ErrorCode` | string | Программный идентификатор ошибки. |

**Пример — Неверный запрос**

```json
{
  "Code": 400,
  "Status": "Error",
  "ErrorMessage": "Недопустимый индекс столбца.",
  "ErrorCode": "InvalidParameter"
}
```

---

## Примеры SDK

Ниже приведены фрагменты кода, демонстрирующие вызов операции **Group Worksheet Columns** с использованием поддерживаемых SDK.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostGroupWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostGroupWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostGroupWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostGroupWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostGroupWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostGroupWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostGroupWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostGroupWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}

---

## Примечания

- **Поведение при группировке:** API создаёт группу столбцов, которую можно разворачивать и сворачивать в Excel. При установке `hide=true` группа сразу сворачивается.  
- **Нумерация с нуля:** Параметры `firstIndex` и `lastIndex` начинаются с **0**; первый столбец на листе имеет индекс 0.  
- **Работа со хранилищем:** Если книга хранится не в хранилище по умолчанию, необходимо указать оба параметра запроса: `folder` и `storageName`.  

---

## См. также

- [Аутентификация — на основе JWT-токена](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [OpenAPI-спецификация операции Group Worksheet Columns](https://apireference.aspose.cloud/cells/#/Cells/PostGroupWorksheetColumns)  
- [SDK Aspose.Cells Cloud (GitHub)](https://github.com/aspose-cells-cloud)  
- [Группировка строк в Excel-таблице](/rows/group/)  

---

> *Иллюстрация:* ![Снимок экрана сгруппированных столбцов в Excel-таблице](./images/group-columns.png){: .img-fluid alt="Снимок экрана сгруппированных столбцов в Excel-таблице" }

*Вышеприведённое заглушечное изображение следует заменить реальным скриншотом, демонстрирующим визуальный результат группировки столбцов.*