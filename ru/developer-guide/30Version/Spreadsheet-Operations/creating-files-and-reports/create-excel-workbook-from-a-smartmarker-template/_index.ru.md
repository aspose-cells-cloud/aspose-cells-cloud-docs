---
title: "Создание отчетов Excel с шаблонами Smart Marker"
second_title: "Документ"
linktype: "SmartMarker"
type: docs
url: /ru/build-report-with-smart-marker/
aliases:
  - /create-excel-workbook-from-a-smartmarker-template/
  - /workbook/smartmarker/
  - /workbook/create/smartmarker/
keywords: "Excel, Smart Marker, Aspose.Cells Cloud, REST API, рабочая книга, SDK, API, генерация отчетов"
description: "Узнайте, как создавать рабочие книги Excel на основе шаблонов Smart Marker с использованием Aspose.Cells Cloud REST API. Включает подробную информацию о запросах и ответах, пример cURL, предварительные требования, примечания и примеры кода SDK."
weight: 40
ArticleTitle: "Создание отчетов Excel с шаблонами Smart Marker – Руководство по API Aspose.Cells Cloud"
---

Этот REST API создает рабочую книгу на основе шаблона Smart Marker.

## API Smart Marker для рабочей книги

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/smartmarker
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

### **Что такое Smart Marker?**

Smart Marker — это синтаксис заполнителя, который связывает поля данных в XML- (или JSON-) файле с ячейками в шаблоне Excel. Во время выполнения Aspose.Cells заменяет маркеры соответствующими данными, что позволяет программно создавать полностью заполненные отчеты.

### **Параметры запроса**

| Имя параметра | Тип   | Описание                                                     |
| ------------- | ----- | ------------------------------------------------------------ |
| outPath       | string | Путь назначения, куда будет сохранена созданная рабочая книга. |
| folder        | string | Папка, содержащая исходную рабочую книгу.                    |
| storageName   | string | Имя используемого сервиса хранилища.                          |

### **Параметр тела запроса**

| Имя параметра | Тип | Описание                                         |
| ------------- | --- | ------------------------------------------------ |
| xmlFile       | file | XML-файл данных Smart Marker, загруженный с запросом. |

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

**Примечания / Ограничения:**  
- API поддерживает файлы Excel размером до **50 МБ**.  
- Поддерживаемые форматы: только **.xlsx**, **.xlsm** и **.xlsb**.  
- Ограничение скорости: **20 запросов в секунду** на аккаунт.

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                                      |
|-----|-----------------------------|---------------------------------------------------------------|
| 200 | OK (ОК)                     | Фильтр применён успешно; ответ содержит детали операции.     |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизовано) | Недействительный или отсутствующий токен JWT.                |
| 413 | Payload Too Large (Слишком большой запрос) | Загруженный файл превышает допустимый размер.                |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                               |

## Как использовать API Smart Marker для рабочей книги

### Спецификация API Smart Marker для рабочей книги

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookGetSmartMarkerResult) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

### Использование SDK Aspose.Cells Cloud

Вы можете использовать утилиту командной строки **cURL** для простого доступа к веб-сервисам Aspose.Cells. Следующий пример демонстрирует, как делать запросы к облачному API с помощью cURL.

**Краткий пример (одна строка)**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/{name}/smartmarker?outPath={outPath}" -H "Authorization: Bearer {access_token}" -F "xmlFile=@Sample_SmartMarker_Data.xml"
```

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/newworkbook_14.xlsx/smartmarker?outPath=GeneratedReport.xlsx" \
    -H "accept: multipart/form-data" \
    -H "x-aspose-client: Containerize.Swagger" \
    -F "xmlFile=@Sample_SmartMarker_Data.xml"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```text
HTTP/1.1 200 OK
Content-Type: application/json

{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### **Обработка ошибок**

| HTTP-статус | Описание              | Типичная причина                                            |
|-------------|-----------------------|-------------------------------------------------------------|
| 400         | Bad Request (Неверный запрос) | Отсутствует шаблон, некорректный XML или недопустимые параметры. |
| 401         | Unauthorized (Неавторизовано) | Недействительный или отсутствующий токен аутентификации.     |
| 404         | Not Found (Не найдено) | Указанная рабочая книга или место хранилища не существует.   |
| 500         | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка на стороне сервера.                   |

**Пример ответа об ошибке (400)**

```json
{
  "Code": 400,
  "Message": "XML-файл данных отсутствует или повреждён."
}
```

## Семейство облачных SDK

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookCreate.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookCreate.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookCreate.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookCreate.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookCreate.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookCreate.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookCreate.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookCreate.go" >}}

{{< /tab >}}

{{< /tabs >}}