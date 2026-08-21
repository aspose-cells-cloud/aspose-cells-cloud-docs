---
title: "Снять защиту с книги Excel — Aspose.Cells Cloud API"
second_title: "Документ"
linktitle: "Снять защиту с файла Excel"
type: docs
url: /ru/excel-file-unprotect/
aliases:
  - /unprotect-excel-workbooks/
  - /workbook/unprotect/
keywords: "Aspose Cells, API снятия защиты Excel, удаление защиты книги, REST API, облачная электронная таблица"
description: "Узнайте, как снять защиту с книги Excel с помощью Aspose.Cells Cloud REST API. Включает синтаксис запроса, параметры, пример cURL и код SDK на нескольких языках."
weight: 60
ArticleTitle: "Снять защиту с книги Excel — Aspose.Cells Cloud API"
---

Используйте этот REST API для снятия защиты с книги Excel.

## API DeleteUnProtectWorkbook

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/protection
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### Параметры пути

| Параметр | Тип    | Описание                                                | Обязательный |
| -------- | ------ | ------------------------------------------------------- | ------------ |
| **name** | string | Имя файла книги (включая расширение).                   | Да           |

### Параметры запроса

| Имя параметра | Тип    | Описание                                           |
| ------------- | ------ | -------------------------------------------------- |
| folder        | string | Путь к папке, содержащей исходную книгу.          |
| storageName   | string | Имя службы хранилища, где находится книга.        |

### Параметры тела запроса

| Имя параметра | Тип                     | Описание                                          |
| ------------- | ----------------------- | ------------------------------------------------- |
| protection    | WorkbookProtectionRequest | Объект, определяющий параметры защиты для удаления. |

#### WorkbookProtectionRequest

| Имя параметра | Тип    | Описание                                                                                  |
| ------------- | ------ | ----------------------------------------------------------------------------------------- |
| ProtectionType | string | Тип удаляемой защиты (`ALL`, `CONTENTS`, `NONE`, `OBJECTS`, `SCENARIOS`, `STRUCTURE`, `WINDOWS`). |
| Password       | string | Пароль, необходимый для снятия защиты (опционально).                                      |

#### Пример cURL

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/protection?folder=MyFolder&storageName=MyStorage" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -d '{ "ProtectionType": "ALL", "Password": "aspose"}'
```

#### Ответ (успех)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Коды ошибок HTTP

| HTTP-статус | Код ошибки          | Описание                                                       |
| ----------- | ------------------- | -------------------------------------------------------------- |
| 400         | BadRequest          | Отсутствуют или недопустимы параметры.                         |
| 401         | Unauthorized        | Недействительный или отсутствующий токен доступа.             |
| 404         | NotFound            | Указанная книга не найдена в указанной папке/хранилище.        |
| 500         | InternalServerError | Непредвиденная ошибка сервера.                                 |

## Как использовать API DeleteUnProtectWorkbook с SDK

### Спецификация API DeleteUnProtectWorkbook

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Protection/DeleteUnProtectWorkbook) определяет общедоступное программное интерфейсное определение и позволяет выполнять REST-взаимодействия прямо из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Приведённый ниже пример демонстрирует, как выполнять вызовы облачного API с помощью cURL.

### Использование SDK Aspose.Cells Cloud

Использование SDK упрощает интеграцию и снижает объём шаблонного кода. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Приведённые ниже примеры кода показывают, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteUnProtectWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteUnProtectWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteUnProtectWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteUnProtectWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteUnProtectWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteUnProtectWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteUnProtectWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteUnProtectWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
---