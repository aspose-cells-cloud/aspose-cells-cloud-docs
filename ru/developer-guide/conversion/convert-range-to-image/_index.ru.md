---
title: "Преобразование диапазона Excel в изображение — Aspose.Cells Cloud API"
description: "Преобразуйте конкретный диапазон из локального файла Excel в формат PNG, JPEG, SVG, TIFF или BMP с помощью REST API Aspose.Cells Cloud — не требуется загружать всю рабочую книгу."
keywords: "Aspose.Cells Cloud, преобразование диапазона в изображение, Excel API, форматы изображений, PNG, JPEG, SVG, TIFF, BMP"
slug: convert-range-to-image
api_version: "v4.0"
date: 2026-07-30
---

Вызов загружает локальный файл электронной таблицы, преобразует указанный диапазон и возвращает изображение в виде бинарного потока.

## Метод преобразования диапазона в изображение

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/image
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе токена JWT</a>.

## Параметры запроса

| Название           | Местоположение                     | Тип     | Обязательный | Описание                                                                 |
|--------------------|------------------------------------|---------|-------------|--------------------------------------------------------------------------|
| **Spreadsheet**    | Form‑Data (`multipart/form-data`)  | Файл    | **Да**      | Файл Excel для обработки.                                                |
| **worksheet**      | Query                              | Строка  | **Да**      | Имя листа, содержащего диапазон (например, `Sheet1`).                  |
| **range**          | Query                              | Строка  | **Да**      | Диапазон ячеек для преобразования, например, `A1:C10`.                  |
| **format**         | Query                              | Строка  | **Да**      | Формат выходного изображения (`png`, `jpeg`, `svg`, `tiff`, `bmp`).    |
| **printHeadings**  | Query                              | Логический | Нет       | `true` — включить заголовки строк и столбцов в изображение.            |
| **outPath**        | Query                              | Строка  | Нет         | Путь к папке для сохранения сгенерированного файла в облачное хранилище.|
| **outStorageName** | Query                              | Строка  | Нет         | Имя сервиса хранилища (например, `MyStorage`).                         |
| **fontsLocation**  | Query                              | Строка  | Нет         | URL или путь к пользовательским шрифтам, используемым при преобразовании.|
| **region**         | Query                              | Строка  | Нет         | Идентификатор языкового стандарта (например, `en-US`, `fr-FR`). Влияет на форматирование чисел и дат. |
| **password**       | Query                              | Строка  | Нет         | Пароль для зашифрованных рабочих книг.                                  |
| **AutoRowsFit**    | Query                              | Логический | Нет       | Автоматическая подгонка строк перед рендерингом.                        |
| **AutoColumnsFit** | Query                              | Логический | Нет       | Автоматическая подгонка столбцов перед рендерингом.                     |

## Ответ

API возвращает преобразованный HTML-файл в виде **бинарного потока** (`application/octet-stream`).

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

### Пример успешного ответа (HTTP)

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.png"
Content-Length: 8423
```

Сохраните тело ответа в файл (например, `report.png`), чтобы просмотреть отрендеренное изображение в браузере.

---

**Коды HTTP-статусов**

| Код  | Значение              | Описание                                                             |
|------|-----------------------|----------------------------------------------------------------------|
| 200  | OK (ОК)               | Фильтр применён успешно; ответ содержит детали операции.            |
| 400  | Bad Request (Неверный запрос) | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized (Неавторизован) | Неверный или отсутствующий токен JWT.                               |
| 413  | Payload Too Large (Слишком большой полезный нагрузка) | Загруженный файл превышает допустимый размер.       |
| 500  | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                              |

## Как использовать API преобразования диапазона в изображение с SDK?

### Спецификация OpenAPI

[Спецификация OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToImage) описывает публично доступный API, позволяющий выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как делать вызовы в Cloud API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/image?format=png&worksheet=Sheet1&range=A1:C10&AutoRowsFit=true&AutoColumnsFit=true" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Report.xlsx" \
     -F "outPath=output/report.png"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.png"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

## Использование SDK Aspose.Cells Cloud

Использование SDK — самый быстрый способ разработки, так как он абстрагирует низкоуровневые детали и позволяет преобразовать диапазон данных в файл изображения с минимальным количеством кода.  
Полный список SDK Aspose.Cells Cloud доступен в нашем [репозитории GitHub](https://github.com/aspose-cells-cloud).

Приведённые ниже примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK. Если загрузка из Gist заблокирована, вы можете скачать примеры напрямую из репозитория.