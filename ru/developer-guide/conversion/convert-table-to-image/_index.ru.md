---
title: "Aspose.Cells Cloud Web API — преобразование табличных данных локальной книги Excel в файл изображения — бесплатный онлайн-инструмент"
second_title: "Документ"
ArticleTitle: "Как преобразовать табличные данные локальной электронной таблицы в файл изображения: пошаговое руководство"
linktitle: "Преобразование таблицы в изображение"
type: docs
url: /ru/convert-table-to-image/
keywords: "Aspose.Cells, Cloud API, преобразование таблицы в изображение, Excel, PNG, JPEG, TIFF, BMP, SVG"
description: "Быстро преобразуйте табличные данные локальной книги Excel в файл изображения с помощью Aspose.Cells Cloud API. Поддерживаются форматы PNG, JPEG, TIFF, BMP, SVG и другие."
weight: 100
---

Экспортируйте табличные данные из локальной книги Excel в файл формата [Image](https://docs.fileformat.com/image/) с помощью Cloud API.

**Поддерживаемые ФОРМАТЫ ИЗОБРАЖЕНИЙ:**

- [PNG](https://docs.fileformat.com/image/png/)
- [SVG](https://docs.fileformat.com/page-description-language/svg/)
- [TIFF](https://docs.fileformat.com/image/tiff/)
- [JPEG](https://docs.fileformat.com/image/jpeg/)
- [BMP](https://docs.fileformat.com/image/bmp/)

## **API преобразования таблицы в изображение**

Перед использованием этого конечного узла убедитесь, что выполнены следующие предварительные требования:

- Действующий JWT-токен доступа, полученный через аутентификацию Aspose.Cells Cloud.
- Доступный аккаунт хранилища, если вы планируете использовать параметры `outPath` или `outStorageName`.
- Исходная рабочая книга (локальный файл Excel) должна быть доступна для чтения, а при наличии защиты — указан правильный пароль.

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/image
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

### **Параметры запроса:**

| Имя параметра  | Тип    | Путь/Строка запроса/HTTP-тело | Описание                                                                                                                               |
| :------------- | :----- | :-------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | File   | FormData                    | Загрузка файла электронной таблицы.                                                                                                     |
| worksheet      | String | Query                       | Имя листа электронной таблицы/Excel.                                                                                                    |
| tableName      | String | Query                       | Имя преобразуемой таблицы.                                                                                                              |
| format         | String | Query                       | Желаемый формат выходного файла изображения (например, png, svg).                                                                      |
| outPath        | String | Query                       | (Необязательно) Путь к папке, где будет сохранено преобразованное изображение. По умолчанию — null.                                   |
| outStorageName | String | Query                       | Указать имя хранилища для выходного файла.                                                                                             |
| fontsLocation  | String | Query                       | Использовать пользовательские шрифты при необходимости.                                                                                 |
| region         | String | Query                       | Параметр региона/языка электронной таблицы (например, `en-US`, `fr-FR`). Влияет на форматирование чисел, разбор дат и поведение, зависящее от локали. |
| password       | String | Query                       | Пароль, необходимый для доступа к файлу электронной таблицы.                                                                            |

### **Ответ**

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

**Коды HTTP-статуса**

| Код  | Значение                | Описание                                                             |
| ---- | ----------------------- | -------------------------------------------------------------------- |
| 200  | OK (OK)                 | Фильтр применён успешно; ответ содержит данные об операции.          |
| 400  | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized (Неавторизован) | Недействительный или отсутствующий JWT-токен.                       |
| 413  | Payload Too Large (Слишком большой payload) | Загруженный файл превышает лимит размера.                           |
| 500  | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                                      |

## **Где следует использовать API преобразования таблицы в изображение?**

- **Статические снимки отчётов**: преобразуйте финансовые таблицы, результаты расчётов или любые отформатированные данные в изображения для включения в PDF-отчёты, слайды PowerPoint или печатные документы, где редактирование не требуется.
- **Визуализация данных в презентациях**: преобразуйте сложные табличные данные электронных таблиц — включая условное форматирование или простые визуализации — в изображения для встраивания в презентации (PPTX, Google Slides).
- **Документация и обучающие материалы**: зафиксируйте примеры электронных таблиц, шаблоны или формы ввода данных в виде изображений для пользовательских руководств, учебных пособий или статей базы знаний.
- **Миниатюры-предпросмотры**: создавайте небольшие изображения-предпросмотры ключевых разделов электронных таблиц для файловых браузеров, библиотек документов или результатов поиска.

## Почему следует использовать API преобразования таблицы в изображение?

- **Удобен для разработчиков**: Aspose.Cells Cloud предлагает SDK на нескольких языках, что обеспечивает быструю разработку, и сопровождается подробной документацией. По сравнению с созданием собственных решений для рендеринга, это значительно снижает объём работ по разработке.
- **Экономически эффективно**: можно преобразовывать табличные данные без предварительной загрузки всей рабочей книги, экономя место в хранилище и снижая затраты.
- **Пиксельное воспроизведение**: точно воспроизводит внешний вид Excel — включая форматирование ячеек, формулы (как отображаемые значения), границы, цвета и условное форматирование — в выходном изображении.
- **Универсальная совместимость**: форматы изображений (PNG, JPEG, TIFF, BMP, SVG и др.) доступны для просмотра на любом устройстве или платформе без специального программного обеспечения, обеспечивая максимальную доступность.

## Как использовать API преобразования таблицы в изображение с SDK?

### Спецификация API преобразования таблицы в изображение

[Спецификация API преобразования таблицы в изображение](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToImage) предоставляет публично доступный программный интерфейс для выполнения REST-взаимодействий непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Пример ниже показывает, как выполнять вызовы в Cloud API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/image?format=png&worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.png
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 encoded)",
  "contentType": "MIME type",
  "fileDownloadName": "optional file name"
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — самый быстрый способ разработки, поскольку он абстрагирует низкоуровневые детали, позволяя преобразовывать табличные данные электронной таблицы в изображение с минимальным количеством кода. Ознакомьтесь с [репозиторием GitHub](https://github.com/aspose-cells-cloud) для получения полного списка SDK Aspose.Cells Cloud.

Следующие примеры кода иллюстрируют, как вызывать веб-сервисы Aspose.Cells с помощью различных SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToSvg.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToSvg.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToSvg.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToSvg.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToSvg.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToSvg.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToSvg.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToSvg.go" >}}
{{</tab>}}
{{< /tabs >}}