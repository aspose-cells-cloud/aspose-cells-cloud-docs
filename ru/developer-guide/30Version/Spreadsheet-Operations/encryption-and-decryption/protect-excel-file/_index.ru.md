---
title: "Защита рабочей книги Excel с помощью API Aspose.Cells Cloud"
second_title: "Документ"
linktitle: "Защита файла Excel"
type: docs
url: /ru/protect-excel-file/
aliases: [/ru/protect-excel-workbooks/, /ru/workbook/protect/]
keywords: "Aspose.Cells, защита Excel, API, REST, SDK"
description: "Узнайте, как защитить рабочую книгу Excel с помощью REST API Aspose.Cells Cloud. Включает шаги аутентификации, параметры запроса и тела запроса, cURL-запрос и примеры кода SDK для C#, Java, PHP, Ruby, Node.js, Python, Perl и Go."
weight: 30
ArticleTitle: "Защита рабочей книги Excel с помощью API Aspose.Cells Cloud"
---

Этот REST API **защищает** рабочую книгу Excel, позволяя вам надежно защитить её с помощью пароля и параметров защиты с использованием Aspose.Cells Cloud.

## API PostProtectDocument

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/protection
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud являются защищенными и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### Параметры запроса

| Имя параметра | Тип   | Описание                                                     |
| -------------- | ------ | --------------------------------------------------------------- |
| folder         | string | Папка, содержащая исходную рабочую книгу. _(необязательно)_          |
| storageName    | string | Имя хранилища. _(необязательно; по умолчанию = "Default")_ |

### Параметры тела запроса

| Имя параметра | Тип                      | Описание                                                   |
| -------------- | ------------------------- | ------------------------------------------------------------- |
| protection     | WorkbookProtectionRequest | Объект, определяющий параметры защиты для рабочей книги. |

#### WorkbookProtectionRequest

| Имя параметра | Тип   | Описание                                                                                                                                              |
| -------------- | ------ | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ProtectionType | string | Тип применяемой защиты. Допустимые значения (без учета регистра): **ALL**, **CONTENTS**, **NONE**, **OBJECTS**, **SCENARIOS**, **STRUCTURE**, **WINDOWS**. |
| Password       | string | Необязательный пароль для установки защиты.                                                                                                             |

### Ответ

```json
{
  "Status":"OK",
  "Code":200
}
```

**Коды HTTP-статусов**

| Код | Значение                     | Описание                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK (Успешно)                          | Фильтр применён успешно; ответ содержит сведения о выполненной операции. |
| 400  | Bad Request (Неверный запрос)                 | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized (Неавторизовано)                | Недействительный или отсутствующий JWT-токен. |
| 413  | Payload Too Large (Слишком большой полезный груз)           | Загруженный файл превышает лимит размера. |
| 500  | Internal Server Error (Внутренняя ошибка сервера)       | Непредвиденная ошибка сервера. |

## Как использовать API PostProtectDocument с SDK

### Необходимые условия

Перед вызовом API убедитесь, что вы выполнили следующие шаги:

- **Получите JWT-токен доступа**, следуя описанному в разделе «Безопасность и аутентификация» процессу аутентификации.  
- **Загрузите рабочую книгу** в хранилище Aspose Cloud или подтвердите, что она уже существует в целевой папке.  
- **Знайте имя хранилища** (по умолчанию — `"Default"`, если не указано иное) и точное имя файла, который необходимо защитить.

### Спецификация API PostProtectDocument

Спецификация <a href="https://apireference.aspose.cloud/cells/#/Workbook/PostProtectDocument" target="_blank" rel="noopener noreferrer">OpenAPI</a> определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

### Пример: Защита рабочей книги с помощью cURL

1. Получите токен доступа, как описано в разделе **Необходимые условия / Аутентификация**.  
2. Выполните запрос:

   ```bash
   curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/protection?folder=MyFolder&storageName=MyStorage" \
        -H "accept: application/json" \
        -H "Content-Type: application/json" \
        -H "Authorization: Bearer <access_token>" \
        -d '{ "ProtectionType": "ALL", "Password": "aspose" }'
   ```

   В ответе будет возвращён объект со статусом, подтверждающим успешное применение защиты.

### Использование SDK Aspose.Cells Cloud

Использование SDK — самый быстрый способ разработки приложений для Aspose.Cells Cloud. SDK скрывает низкоуровневые детали, позволяя сосредоточиться на бизнес-логике. Полный список SDK Aspose.Cells Cloud доступен в <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">репозитории GitHub</a>.

Следующие примеры кода демонстрируют вызов веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostProtectWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostProtectWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostProtectWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostProtectWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostProtectWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostProtectWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostProtectWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostProtectWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

### Пример полного ответа

```json
{
  "Status": "OK",
  "Code": 200,
  "Workbook": {
    "Name": "test.xlsx",
    "Path": "/MyFolder/test.xlsx",
    "Protection": {
      "ProtectionType": "ALL",
      "Password": true
    }
  }
}
```