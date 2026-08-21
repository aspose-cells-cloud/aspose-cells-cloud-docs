---
title: "Экспорт диаграммы Excel — Aspose.Cells Cloud API"
second_title: "Документ"
description: "Преобразуйте диаграмму из рабочей книги Excel, хранимой в облаке, в форматы PDF, PNG, SVG и другие с помощью одного REST-вызова."
ArticleTitle: "Как преобразовать локальный лист электронной таблицы в PDF-файл: пошаговое руководство"
linktitle: "Преобразование листа в PDF"
type: docs
url: /ru/export-chart-as-format/
keywords: "Aspose.Cells Cloud, экспорт диаграммы, API, PDF, PNG, SVG, Excel, REST, облачное преобразование"
weight: 100
---

Экспортируйте диаграмму, расположенную в рабочей книге, хранимой в Aspose Cloud Storage, в другой файловый формат (PDF, PNG, SVG и т.д.), не скачивая исходный файл.

## API ExportChartAsFormat

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/charts/{chartIndex}
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

### 📦 Параметры запроса

| Имя                | Тип     | Местоположение | Обязательный | Описание                                                       |
| ------------------ | ------- | -------------- | ------------ | -------------------------------------------------------------- |
| **name**           | string  | Path           | Да           | Имя файла рабочей книги.                                       |
| **worksheet**      | string  | Path           | Да           | Имя листа, содержащего диаграмму.                             |
| **chartIndex**     | integer | Path           | Да           | Индекс экспортируемой диаграммы (начиная с нуля).             |
| **format**         | string  | Query          | Да           | Желаемый выходной формат (например, `png`, `pdf`, `svg`).     |
| **folder**         | string  | Query          | Нет          | Путь к папке, где хранится рабочая книга (по умолчанию: корень). |
| **storageName**    | string  | Query          | Нет          | Имя пользовательского хранилища; опустите, чтобы использовать хранилище по умолчанию. |
| **outPath**        | string  | Query          | Нет          | Путь к папке, куда будет сохранён преобразованный файл.       |
| **outStorageName** | string  | Query          | Нет          | Имя хранилища для выходного файла.                            |
| **fontsLocation**  | string  | Query          | Нет          | Путь к папке, содержащей пользовательские шрифты.             |
| **region**         | string  | Query          | Нет          | Языковой стандарт (например, `en-US`, `fr-FR`).                |
| **password**       | string  | Query          | Нет          | Пароль для открытия защищённой рабочей книги.                 |

### **Ответ**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

**Коды HTTP-статуса**

| Код | Значение                | Описание                                                           |
| --- | ----------------------- | ------------------------------------------------------------------ |
| 200 | OK                      | Фильтр применён успешно; в ответе содержатся данные операции.     |
| 400 | Bad Request             | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized            | Недействительный или отсутствующий JWT-токен.                    |
| 413 | Payload Too Large       | Загруженный файл превышает допустимый размер.                     |
| 500 | Internal Server Error   | Непредвиденная ошибка сервера.                                    |

## Как использовать API экспорта диаграммы в формат с помощью SDK?

### Спецификация API экспорта диаграммы в формат

[Спецификация API экспорта диаграммы в формат](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportChartAsFormat) предоставляет публично доступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как выполнить вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/charts/{chartIndex}?format={format}" \
  -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 закодировано)",
  "contentType": "MIME-тип",
  "fileDownloadName": "необязательное имя файла"
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — самый быстрый способ разработки, так как он абстрагирует низкоуровневые детали, позволяя преобразовывать табличные данные электронной таблицы в PDF-файл с минимальным количеством кода. Посетите [репозиторий на GitHub](https://github.com/aspose-cells-cloud), чтобы ознакомиться с полным списком SDK Aspose.Cells Cloud.

Следующие примеры кода иллюстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK: