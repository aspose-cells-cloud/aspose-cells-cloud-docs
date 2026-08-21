---
title: "Пакетная разблокировка"
second_title: "Документ"
type: docs
url: /batch/unlock
keywords: "пакетная разблокировка, Aspose.Cells Cloud, Excel, REST API, электронная таблица, облачный SDK"
description: "Разблокируйте несколько файлов Excel пакетно с использованием REST API Aspose.Cells Cloud. Поддерживаются SDK для C#, Java, Python и других языков."
weight: 100
---

Этот REST API позволяет пакетно разблокировать подходящие файлы Excel.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/unlock
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

### Параметры запроса

| Имя параметра | Тип | Расположение | Описание |
|----------------|------|----------|-------------|
| **BatchLockRequest** |  | body | Тело запроса, содержащее настройки разблокировки. |

### Свойства **BatchLockRequest**

| Имя             | Тип                     | Описание                                      | Примечания |
|-----------------|--------------------------|-----------------------------------------------|------------|
| SourceFolder    | string                   | Папка, содержащая исходные файлы Excel.       | [необязательно] |
| MatchCondition  | MatchConditionRequest    | Критерии выбора файлов для разблокировки.      | [необязательно] |
| Password        | string                   | Пароль, применённый к защищённым рабочим книгам. | [необязательно] |
| OutFolder       | string                   | Папка назначения для разблокированных файлов.  | [необязательно] |

### Свойства **MatchConditionRequest**

| Имя                | Тип       | Описание                                     | Примечания |
|--------------------|-----------|----------------------------------------------|------------|
| RegexPattern       | string    | Регулярное выражение для сопоставления имён файлов. | [необязательно] |
| FullMatchConditions| string[]  | Точные условия имён файлов для сопоставления. | [необязательно] |

### Параметр тела запроса

| Имя параметра | Тип | Описание                                     |
| -------------- | ---- | -------------------------------------------- |
| data           | file | Двоичное содержимое файла рабочей книги для создания. |

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

| Код | Значение                      | Когда возвращается                        |
|-----|-------------------------------|-------------------------------------------|
| 200 OK | Рабочая книга успешно создана | Нормальный ход выполнения                  |
| 201 Created | Рабочая книга создана (альтернативный ответ) | Если API возвращает статус «создано» |
| 400 Bad Request | Недопустимые параметры | Ошибка на стороне клиента                 |
| 401 Unauthorized | Отсутствует или недействителен токен | Ошибка аутентификации                    |
| 409 Conflict | Файл существует, а `isWriteOver=false` | Конфликт с существующим файлом            |

## Как использовать API PostBatchLock с SDK

### Спецификация API PostBatchLock

[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/Batch/PostBatchUnlock) определяет общедоступное программное интерфейсное решение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать инструмент командной строки cURL для лёгкого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как выполнять вызовы облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/unlock" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"SourceFolder":"CellsTests","OutFolder":"Output","MatchCondition":{"RegexPattern":"(^Book)(.+)(xlsx$)"},"Password":"123456"}'
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

Использование SDK — самый быстрый способ разработки функциональности разблокировки. SDK абстрагирует низкоуровневые детали, позволяя сосредоточиться на бизнес-логике. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchUnlock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchUnlock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchUnlock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchUnlock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchUnlock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchUnlock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchUnlock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchUnlock.go" >}}

{{< /tab >}}

{{< /tabs >}}