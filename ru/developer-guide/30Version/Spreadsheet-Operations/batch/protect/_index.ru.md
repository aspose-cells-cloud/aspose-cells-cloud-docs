---
title: "Пакетная защита файлов Excel"
second_title: "Документ"
type: docs
url: /batch/protect
keywords: "Пакетная защита файлов Excel, Aspose Cells Cloud, REST API, защита Excel, пакетная защита"
description: "Узнайте, как использовать REST API Aspose.Cells Cloud для пакетной защиты нескольких файлов Excel. Включает подробную информацию о запросе, пример cURL и примеры кода SDK для различных языков."
weight: 100
---

Это REST API позволяет выполнять **пакетную защиту** подходящих файлов Excel.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/protect
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе токена JWT</a>.

### Параметры запроса

| Имя параметра        | Тип                 | Местоположение | Описание                                                                                              |
|----------------------|---------------------|----------------|----------------------------------------------------------------------------------------------------------|
| batchProtectRequest  | BatchProtectRequest | body           | JSON-полезная нагрузка, определяющая исходную папку, условия отбора, тип защиты, пароль и выходную папку. |

### Свойства BatchProtectRequest

| Имя               | Тип                     | Описание                                                                                 | Примечания |
|-------------------|--------------------------|---------------------------------------------------------------------------------------------|------------|
| SourceFolder      | string                   | Папка, содержащая исходные файлы Excel.                                                   | необязательно |
| MatchCondition    | MatchConditionRequest   | Критерии, используемые для отбора файлов для защиты.                                      | необязательно |
| ProtectionType    | string                   | Тип применяемой защиты (например, `All`, `ReadOnly`).                                    | необязательно |
| Password          | string                   | Пароль, устанавливаемый для защищённых файлов.                                            | необязательно |
| OutFolder         | string                   | Папка назначения для защищённых файлов.                                                   | необязательно |

### Свойства MatchConditionRequest

| Имя                 | Тип        | Описание                                    | Примечания |
|---------------------|------------|---------------------------------------------|------------|
| RegexPattern        | string     | Регулярное выражение, используемое для сопоставления имён файлов. | необязательно |
| FullMatchConditions | string[]   | Список точных условий по имени файла.       | необязательно |

### Параметр тела запроса

| Имя параметра | Тип  | Описание                                    |
|---------------|------|---------------------------------------------|
| data          | file | Бинарное содержимое файла рабочей книги для создания. |

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

| Код  | Значение                     | Когда возвращается                           |
|------|------------------------------|----------------------------------------------|
| 200 OK | Рабочая книга успешно создана | Нормальный сценарий выполнения               |
| 201 Created | Рабочая книга создана (альтернативный ответ) | Когда API возвращает статус «создано» |
| 400 Bad Request | Недопустимые параметры | Ошибка со стороны клиента                   |
| 401 Unauthorized | Отсутствующий или недействительный токен | Ошибка аутентификации              |
| 409 Conflict | Файл существует, а `isWriteOver=false` | Конфликт с существующим файлом |

## Как использовать API PostProtectConvert с SDK

### Спецификация API PostProtectConvert

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/PostProtectConvert) определяет общедоступное программное интерфейсное определение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать инструмент командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Пример ниже показывает, как выполнить вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/protect" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Password\":\"123456\",\"ProtectionType\":\"All\"}"
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

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали и позволяет сосредоточиться на задачах вашего проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже показывают, как выполнять вызовы веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchProtect.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchProtect.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchProtect.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchProtect.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchProtect.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchProtect.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchProtect.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchProtect.go" >}}

{{< /tab >}}

{{< /tabs >}}