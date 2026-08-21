---
title: "Преобразование рабочего листа — Документация API Aspose.Cells Cloud"
second_title: "Документ"
ArticleTitle: "Как преобразовать данные локальной электронной таблицы рабочего листа в файл изображения: пошаговое руководство"
linktype: "Преобразование рабочего листа в изображение"
type: docs
url: /convert-worksheet-to-image/
keywords: "Aspose.Cells Cloud, преобразование рабочего листа в изображение, конвертация рабочего листа в изображение, Excel в PNG, Excel в SVG, Excel в TIFF, Excel в JPEG, Excel в BMP, API для преобразования изображений, REST API, экспорт изображений из электронных таблиц, примеры SDK"
description: "Пошаговое руководство по преобразованию электронной таблицы Excel в форматы изображений (PNG, SVG, TIFF, JPEG, BMP и др.) с использованием API Aspose.Cells Cloud, включая параметры запроса, данные ответа, коды ошибок, сценарии использования и примеры кода SDK."
weight: 100
---

Экспортируйте данные рабочего листа из локального файла Excel в файл [изображения](https://docs.fileformat.com/image/) с помощью API Aspose.Cells Cloud. Эта операция поддерживает множество форматов изображений и идеально подходит для создания визуальных снимков данных электронной таблицы.

**Поддерживаемые ФОРМАТЫ ИЗОБРАЖЕНИЙ**

- [PNG](https://docs.fileformat.com/image/png/)
- [SVG](https://docs.fileformat.com/page-description-language/svg/)
- [TIFF](https://docs.fileformat.com/image/tiff/)
- [JPEG](https://docs.fileformat.com/image/jpeg/)
- [BMP](https://docs.fileformat.com/image/bmp/)

## **API преобразования рабочего листа в изображение**

### Web API

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/worksheet/image
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### **Параметры запроса**

| Имя параметра | Тип   | Путь/Строка запроса/HTTPBody | Описание                                                                 |
| :------------ | :---- | :-------------------------- | :----------------------------------------------------------------------- |
| Spreadsheet   | File  | FormData                    | Загрузка файла электронной таблицы.                                      |
| worksheet     | String| Query                       | Имя рабочего листа, подлежащего преобразованию.                          |
| format        | String| Query                       | Желаемый формат изображения (`svg`, `png`, `tiff`, `jpeg`, `bmp` и др.).|
| outPath       | String| Query                       | _(Необязательный)_ Путь к папке, где будет сохранено выходное изображение; по умолчанию `null`. |
| outStorageName| String| Query                       | Имя хранилища для выходного файла.                                       |
| fontsLocation | String| Query                       | Путь к пользовательской папке со шрифтами, если требуются шрифты, недоступные на сервере. |
| region        | String| Query                       | Настройка региона электронной таблицы (например, `en-US`).               |
| password      | String| Query                       | Пароль, необходимый для открытия защищенного файла электронной таблицы.  |

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

| Код | Значение               | Описание                                                       |
| --- | ---------------------- | -------------------------------------------------------------- |
| 200 | OK (Успех)            | Фильтр успешно применен; ответ содержит данные об операции.    |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизовано) | Неверный или отсутствующий JWT-токен.                         |
| 413 | Payload Too Large (Слишком большой полезный нагрузочный пакет) | Загруженный файл превышает лимит размера.                     |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                               |

## **Где следует использовать API преобразования рабочего листа в изображение?**

- **Статические снимки отчетов** – Преобразуйте финансовые таблицы, расчеты или другие данные в изображения для включения в PDF-отчеты, презентации PowerPoint или печатные документы, где редактирование не требуется.
- **Визуализация данных в презентациях** – Преобразуйте сложные таблицы электронных таблиц (включая условное форматирование или простые диаграммы) в изображения, которые можно встраивать в презентации (PPTX, Google Slides).
- **Документация и обучающие материалы** – Фиксируйте примеры электронных таблиц, шаблоны или формы ввода данных в виде изображений для руководств пользователей, учебных пособий или статей в базе знаний.
- **Миниатюры предпросмотра** – Генерируйте небольшие изображения-предпросмотры ключевых разделов электронных таблиц для файловых браузеров, библиотек документов или результатов поиска.

## **Почему стоит использовать API преобразования рабочего листа в изображение?**

- **Удобен для разработчиков** – Aspose.Cells Cloud предоставляет SDK-библиотеки на множестве языков, что обеспечивает быструю разработку и сопровождается подробной документацией. По сравнению с созданием собственного решения для отрисовки диаграмм, это значительно сокращает трудозатраты.
- **Экономически эффективно** – Вы можете преобразовывать данные таблиц без предварительного постоянного хранения книги, что экономит место хранения и снижает затраты.
- **Точное воспроизведение пикселей** – В выходном изображении точно воспроизводится внешний вид Excel — включая форматирование ячеек, формулы (в виде отображаемых значений), границы, цвета и условное форматирование.
- **Универсальная совместимость** – Форматы изображений (PNG, JPEG, TIFF, BMP, SVG и др.) доступны для просмотра на любом устройстве или платформе без специального программного обеспечения, обеспечивая максимальную доступность.

## **Как использовать API преобразования рабочего листа в изображение с помощью SDK?**

### Спецификация API преобразования рабочего листа в изображение

[Спецификация API преобразования рабочего листа в изображение](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToImage) определяет публично доступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells Cloud. В следующем примере показано, как делать вызовы в Cloud API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/image?format=png&worksheet=Sheet1" \
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

Использование SDK — это самый быстрый способ разработки, поскольку он абстрагирует низкоуровневые детали и позволяет преобразовывать данные рабочего листа в изображение с минимальным объемом кода. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют, как вызывать веб-сервисы Aspose.Cells Cloud с использованием различных SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorksheetToSvg.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorksheetToSvg.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorksheetToSvg.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorksheetToSvg.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorksheetToSvg.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorksheetToSvg.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorksheetToSvg.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorksheetToSvg.go" >}}
{{</tab>}}
{{< /tabs >}}