---
title: "Пакетная блокировка файлов Excel"
second_title: "Документ"
type: docs
url: /batch/lock
keywords: "пакетная блокировка, Excel, Aspose.Cells, облачный API, электронная таблица, защита файла"
description: "Aspose.Cells Cloud API позволяет выполнять пакетную блокировку нескольких файлов Excel. Используйте REST-конечную точку или любой из поддерживаемых SDK (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go и др.) для массовой блокировки файлов."
weight: 100
---

Этот REST API позволяет выполнять **пакетную блокировку** подходящих файлов Excel.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/lock
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.


### Параметры запроса

| Имя параметра   | Тип                 | Расположение | Описание                                     |
|------------------|---------------------|--------------|----------------------------------------------|
| BatchLockRequest | BatchLockRequest    | body         | JSON-тело, содержащее параметры блокировки. |

#### Свойства **BatchLockRequest**

| Имя              | Тип                      | Описание                                              | Примечания |
|------------------|--------------------------|-------------------------------------------------------|------------|
| SourceFolder     | string                   | Папка, содержащая исходные файлы Excel.              | необязательно |
| MatchCondition   | MatchConditionRequest    | Условия для выбора файлов, подлежащих блокировке.     | необязательно |
| Password         | string                   | Пароль, применяемый к заблокированным файлам.         | необязательно |
| OutFolder        | string                   | Папка назначения для заблокированных файлов.          | необязательно |

#### Свойства **MatchConditionRequest**

| Имя                | Тип       | Описание                                               | Примечания |
|--------------------|-----------|--------------------------------------------------------|------------|
| RegexPattern       | string    | Шаблон регулярного выражения для сопоставления имен файлов. | необязательно |
| FullMatchConditions| string[]  | Точные совпадения по имени файла для блокировки.      | необязательно |

### Параметр тела запроса

| Имя параметра | Тип  | Описание                                   |
| ------------- | ---- | ------------------------------------------ |
| data          | file | Двоичное содержимое файла рабочей книги.   |
  
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

| Код | Значение                    | Когда возвращается                      |
|-----|-----------------------------|-----------------------------------------|
| 200 OK | Рабочая книга успешно создана | При нормальном ходе выполнения          |
| 201 Created | Рабочая книга создана (альтернативный ответ) | Когда API возвращает статус «создано» |
| 400 Bad Request | Некорректные параметры | Ошибка на стороне клиента               |
| 401 Unauthorized | Отсутствует или недействителен токен | Ошибка аутентификации                 |
| 409 Conflict | Файл уже существует и `isWriteOver=false` | Конфликт с существующим файлом         |

## Как использовать API PostBatchLock с SDK

### Спецификация API PostBatchLock

[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/Batch/PostBatchLock) определяет общедоступный программный интерфейс, позволяющий выполнять взаимодействие с REST напрямую из веб-браузера.

Вы можете использовать утилиту командной строки **cURL** для простого доступа к веб-сервисам Aspose.Cells. В приведенном ниже примере показано, как вызвать облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/lock" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Password\":\"123456\"}"
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

Использование SDK — самый быстрый способ разработки. SDK скрывает низкоуровневые детали, позволяя сосредоточиться на задачах блокировки. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchLock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchLock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchLock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchLock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchLock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchLock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchLock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchLock.go" >}}

{{< /tab >}}

{{< /tabs >}}