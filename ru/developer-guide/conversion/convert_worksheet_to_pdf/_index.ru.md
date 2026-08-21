---
title: "ConvertWorksheetToPdf"
ArticleTitle: "Преобразование листа в PDF – Aspose.Cells Cloud API"
second_title: "Документ"
linktitle: "ConvertWorksheetToPdf"
type: docs
url: /cells/convert/worksheet/pdf
aliases: []
keywords: "Aspose.Cells, преобразование листа в PDF, API"
description: "Преобразует лист файла электронной таблицы в PDF с использованием Aspose.Cells Cloud."
weight: 10
---

## Метод ConvertWorksheetToPdf в веб-сервисах Aspose.Cells Cloud

Этот метод считывает файл электронной таблицы из локальной файловой системы, преобразует его лист в PDF-файл и возвращает результат преобразования. Необходимо корректно указать путь к исходному файлу и целевой формат. Убедитесь, что имеются необходимые разрешения на чтение исходного файла и запись преобразованного файла (если применимо). Процесс преобразования происходит полностью на облачном сервере, что исключает необходимость использования облачного хранилища или внешних загрузок.

Основные возможности включают облачную нативную конвертацию, снижение нагрузки на облачные ресурсы и упрощённый рабочий процесс.

### Конечная точка веб-API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf
```

### **Безопасность и аутентификация**

Веб-API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе токена JWT</a>.

### Параметры запроса

| Имя параметра   | Тип    | Путь/Строка запроса/HTTP-тело | Описание                                                                                                                            |
|------------------|---------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | File    | FormData                    | Загрузка файла электронной таблицы.                                                                                                               |
| worksheet        | String  | Query                       | Имя листа электронной таблицы.                                                                                                         |
| outPath          | String  | Query                       | (Необязательно) Путь к папке, в которой сохраняется рабочая книга. По умолчанию — null.                                                          |
| outStorageName   | String  | Query                       | Имя хранилища для выходного файла.                                                                                                              |
| fontsLocation    | String  | Query                       | Использование пользовательских шрифтов.                                                                                                                      |
| AutoRowsFit      | Boolean | Query                       | (Необязательно) Автоподбор высоты всех строк в листах.                                                                                           |
| AutoColumnsFit   | Boolean | Query                       | (Необязательно) Автоподбор ширины всех столбцов в листах.                                                                                        |
| region           | String  | Query                       | Региональные/языковые настройки электронной таблицы (например, `en-US`, `fr-FR`). Влияет на форматирование чисел, разбор дат и поведение, зависящее от локали. |
| password         | String  | Query                       | Пароль для открытия файла электронной таблицы.                                                                                             |

### Параметр тела запроса

| Имя параметра | Тип | Описание |
| -------------- | ---- | ----------- |
| [TBD]          |      |             |

### **Ответ**

```json
{
  "file": "<двоичный поток сгенерированного PDF>"
}
```

**Коды статуса ответа**

| Код | Значение | Описание |
|------|---------|-------------|
| 200 | OK | Лист успешно преобразован в PDF и возвращён как поток файла. |
| 400 | Bad Request | Недопустимые параметры запроса или некорректный URL. |
| 401 | Unauthorized | Аутентификация не удалась или учётные данные не предоставлены. |
| 404 | Not Found | Исходный файл недоступен. |
| 413 | Payload Too Large | Загруженный файл превышает допустимый размер. |
| 500 | Internal Server Error | Во время преобразования произошёл сбой в обработке электронной таблицы. |

## Использование ConvertWorksheetToPdf с SDK

### Спецификация ConvertWorksheetToPdf

[Спецификация API ConvertWorksheetToPdf](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#Conversion/ConvertWorksheetToPdf) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Для простого доступа к веб-сервисам Aspose.Cells Cloud можно использовать утилиту командной строки cURL. В следующем примере показано, как выполнить вызов облачного API с помощью cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}

{< tab tabNum="1" >}

```bash
# Используйте HTTPS для безопасного соединения
curl -v "https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf?worksheet=Sheet1&outPath=output%2Ffolder&outStorageName=MyStorage&fontsLocation=%2Fcustom%2Ffonts&AutoRowsFit=true&AutoColumnsFit=true&region=en-US&password=SecretPwd" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<двоичный поток сгенерированного PDF>"
}
```

{< /tab >}

{< /tabs >}

### Использование SDK Aspose.Cells Cloud

Использование SDK — это самый быстрый способ ускорить разработку. SDK абстрагирует низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">репозитории на GitHub</a>.

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells Cloud с использованием различных SDK:
`[TBD]`
---