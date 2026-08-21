---
title: "Aspose.Cells Cloud Excel Compression Web API – Программное уменьшение размера файлов электронных таблиц"
second_title: "Документ"
ArticleTitle: "Как сжать файлы Excel – Уменьшить размер электронной таблицы и оптимизировать производительность"
linktitle: "Сжать электронную таблицу"
type: docs
url: /compress-spreadsheet/
keywords: "сжатие Excel, Aspose.Cells Cloud, уменьшение размера электронной таблицы, API, оптимизация рабочей книги"
description: "Узнайте, как сжимать рабочие книги Excel с помощью API Aspose.Cells Cloud. Получите пошаговые примеры, параметры, сведения об аутентификации и лучшие практики."
weight: 100
---

Программно сжимайте электронные таблицы Excel и уменьшайте размер файлов с помощью API Aspose.Cells Cloud. Оптимизируйте производительность рабочей книги за счёт удаления неиспользуемых данных, сжатия встроенных объектов и очистки форматирования. Этот RESTful API позволяет автоматизировать процессы сжатия и оптимизации файлов Excel.

## **API сжатия электронной таблицы**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/compress
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Параметры запроса

| Имя параметра | Тип    | Путь/Запрос/Строка/Тело HTTP | Описание                                                                                                                          |
| ------------- | ------ | ---------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet   | File   | FormData                     | **Обязательный.** Исходный файл рабочей книги Excel (`.xlsx`, `.xls` и т.д.) для сжатия.                                          |
| level         | Integer| Query                        | **Необязательный.** Уровень интенсивности сжатия (0 = максимально быстро/минимально, 9 = максимально медленно/максимально). При отсутствии используется сбалансированное значение по умолчанию (5). |
| outPath       | String | Query                        | **Необязательный.** Путь к папке назначения в вашем облачном хранилище. При отсутствии файл сохраняется в той же папке, что и исходная рабочая книга. |
| outStorageName| String | Query                        | **Обязательный.** Идентификатор настроенной облачной службы хранения (например, `CorporateDrive`).                                |
| region        | String | Query                        | **Необязательный.** Языковой стандарт (например, `de-DE`), который может влиять на обработку региональных данных.                 |
| password      | String | Query                        | **Необязательный.** Пароль для расшифровки защищённой электронной таблицы. Оставьте пустым, если файл не зашифрован.               |

### Ответ

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

| Код | Значение                | Описание                                                           |
| --- | ----------------------- | ------------------------------------------------------------------ |
| 200 | OK                      | Фильтр успешно применён; в ответе содержатся детали операции.     |
| 400 | Bad Request             | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized            | Недействительный или отсутствующий JWT-токен.                     |
| 413 | Payload Too Large       | Загружаемый файл превышает допустимый размер.                      |
| 500 | Internal Server Error   | Непредвиденная ошибка сервера.                                     |

## Где следует использовать API сжатия электронной таблицы?

- **Автоматическая рассылка отчётов** – Сжимайте ежемесячные финансовые отчёты перед отправкой по электронной почте, чтобы гарантировать успешную доставку и улучшить впечатление получателя.
- **Оптимизация загрузки файлов пользователями** – Сжимайте загружаемые файлы Excel в фоновом режиме, чтобы сэкономить место в облачном хранилище и снизить затраты на хранение.
- **Обработка и миграция в конвейере данных** – Сжимайте промежуточные файлы Excel, генерируемые в ходе ETL-процессов, для ускорения передачи по сети и снижения нагрузки на временное хранилище.

## Почему следует использовать API сжатия электронной таблицы?

- **Удобный для разработчиков** – Aspose.Cells Cloud предоставляет SDK-библиотеки на множестве языков программирования, что позволяет быстро разрабатывать решения при полной поддержке документацией.
- **Снижение трудозатрат** – Исключает необходимость в специалистах для ручного объединения документов.
- **Тарификация по факту использования** – Нет необходимости в первоначальных инвестициях; вы платите только за фактически выполненные вызовы API.
- **Отсутствие необходимости в обслуживании серверов** – Не требуется обслуживать серверы, обновлять программное обеспечение или беспокоиться о совместимости.

## Как использовать API сжатия электронной таблицы с SDK

### Спецификация API сжатия электронной таблицы

[Спецификация API сжатия электронной таблицы](https://reference.aspose.cloud/cells/#/ManagementController/CompressSpreadsheet) предоставляет общедоступный интерфейс для взаимодействия по REST, позволяя выполнять прямые вызовы API из веб-браузера.

Вы можете использовать утилиту командной строки cURL для удобного доступа к веб-сервисам Aspose.Cells Cloud. В следующем примере показано, как выполнять вызовы в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/compress?level=5&outStorageName=MyStorage" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/input.xlsx"
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

Использование SDK — самый быстрый способ разработки, поскольку оно абстрагирует низкоуровневые детали и позволяет сжать электронную таблицу всего в несколько строк кода. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют взаимодействие с веб-сервисами Aspose.Cells Cloud с использованием различных SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CompressSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CompressSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CompressSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CompressSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CompressSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CompressSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CompressSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CompressSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}