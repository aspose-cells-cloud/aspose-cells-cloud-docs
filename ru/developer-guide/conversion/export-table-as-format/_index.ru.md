---
title: "Экспорт таблицы — Aspose.Cells Cloud API | Преобразование Excel в PDF, PNG, CSV"
second_title: "Документ"
ArticleTitle: "Как экспортировать удалённую таблицу электронной таблицы в другой формат: пошаговое руководство"
linktype: "docs"
url: /ru/export-table-as-format/
keywords: "Aspose.Cells, экспорт таблицы, Excel в PDF, облачный API, REST"
description: "Экспортируйте удалённую таблицу Excel в PDF, PNG, CSV, JSON или другие форматы с помощью Aspose.Cells Cloud API. Защищённый HTTPS-endpoint с аутентификацией по JWT и примерами SDK."
weight: 100
---

Экспортируйте таблицу из облачного хранилища электронной таблицы (Excel) в файл другого формата.

## **API экспорта таблицы в определённый формат**

### Web API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/tables/{tableName}
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Параметры запроса:**

| Имя параметра | Тип   | Путь/Строка запроса/HTTPBody | Описание                                                                                                                                           |
| :------------ | :---- | :-------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------- |
| name          | String| Path                        | **Обязательный.** Имя файла рабочей книги, который нужно получить.                                                                                 |
| worksheet     | String| Path                        | Имя листа.                                                                                                                                          |
| tableName     | String| Path                        | Имя таблицы.                                                                                                                                        |
| format        | String| Query                       | **Обязательный.** Желаемый выходной формат (например, «png», «pdf», «svg»).                                                                         |
| folder        | String| Query                       | Необязательный. Путь к папке, где хранится рабочая книга. По умолчанию `null`.                                                                     |
| storageName   | String| Query                       | Необязательный. Имя хранилища при использовании пользовательского облачного хранилища. Используется хранилище по умолчанию, если не указано.        |
| outPath       | String| Query                       | Необязательный. Путь к папке для выходного файла. По умолчанию `null`.                                                                              |
| outStorageName| String| Query                       | Необязательный. Имя хранилища выходного файла.                                                                                                     |
| fontsLocation | String| Query                       | Необязательный. Путь к пользовательским шрифтам.                                                                                                    |
| region        | String| Query                       | Необязательный. Региональные/языковые настройки электронной таблицы (например, `en-US`, `fr-FR`). Влияет на форматирование чисел, разбор дат и другие региональные особенности. |
| password      | String| Query                       | Необязательный. Пароль для открытия файла электронной таблицы.                                                                                      |

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

| Код | Значение                | Описание                                                             |
| --- | ----------------------- | -------------------------------------------------------------------- |
| 200 | OK                      | Фильтр применён успешно; ответ содержит детали операции.            |
| 400 | Bad Request             | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized            | Некорректный или отсутствующий токен JWT.                           |
| 413 | Payload Too Large       | Загруженный файл превышает лимит размера.                           |
| 500 | Internal Server Error   | Непредвиденная ошибка сервера.                                       |

## **Где следует использовать API экспорта таблицы в другой формат?**

- **Миграция устаревших систем**: Преобразуйте тысячи устаревших файлов XLS в XLSX для использования в современных системах.
- **Стандартизация архивов**: Приведите различные форматы электронных таблиц (XLS, XLSM, ODS, CSV) к единому формату для архивирования.
- **Совместимость с офисными пакетами**: Преобразуйте файлы Excel в форматы, совместимые с LibreOffice, Google Таблицами или Apple Numbers.
- **Нормализация источников данных**: Преобразуйте различные форматы электронных таблиц в CSV или JSON для последующей загрузки в базы данных.
- **Публикация в вебе**: Преобразуйте финансовые модели в HTML для отображения в вебе.

## **Почему стоит использовать API экспорта таблицы в другой формат?**

- **Удобство для разработчиков**: Aspose.Cells Cloud предоставляет SDK на множестве языков программирования, что позволяет быстро начать разработку, а также сопровождается подробной документацией. По сравнению с созданием собственных решений для визуализации диаграмм, это значительно снижает объём работы.
- **Снижение трудозатрат**: Уменьшает необходимость выделять сотрудников на задачи по консолидации документов.
- **Оплата по факту использования**: Не требуется предварительных инвестиций; вы платите только за фактически выполненные вызовы API.
- **Нулевые затраты на обслуживание**: Не нужно обслуживать серверы, обновлять ПО или решать проблемы совместимости.
- **API возвращает только неформатированные данные таблицы без стилей всей рабочей книги.**

## **Как использовать API экспорта таблицы электронной таблицы в другой формат с помощью SDK?**

### Спецификация API экспорта таблицы в определённый формат

Спецификация <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportTableAsFormat" target="_blank" rel="noopener noreferrer">Export Table as Format API</a> определяет публичный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Пример ниже показывает, как выполнять вызовы облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/tables/Table1?format=pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/octet-stream"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 encoded)",
  "contentType": "MIME-тип",
  "fileDownloadName": "необязательное имя файла"
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — самый быстрый способ разработки, так как он скрывает низкоуровневые детали, позволяя экспортировать таблицу электронной таблицы в файл нужного формата с помощью короткого кода. Ознакомьтесь с <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">репозиторием на GitHub</a> для получения полного списка SDK Aspose.Cells Cloud.

Следующие примеры кода демонстрируют вызовы веб-сервисов Aspose.Cells с использованием различных SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportTableAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportTableAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportTableAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportTableAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportTableAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportTableAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportTableAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportTableAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}