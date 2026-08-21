---
title: "Aspose.Cells Cloud Excel Unprotect Web API — программное удаление паролей на открытие и изменение"
second_title: "Документ"
ArticleTitle: "Удаление защиты паролем от Excel — разблокировка паролей на открытие и изменение мгновенно"
linktitle: "Снять защиту с электронной таблицы"
type: docs
url: /ru/unprotect-spreadsheet/
keywords: "снять защиту, электронная таблица, Aspose.Cells, API, Excel, удаление пароля"
description: "Программно удаляйте пароли на открытие и изменение из файлов Excel с помощью API Aspose.Cells Cloud Unprotect Spreadsheet. Поддерживает форматы .xlsx/.xls, аутентификацию OAuth2 и пакетную обработку."
weight: 100
---

API Unprotect Spreadsheet удаляет защиту паролями на открытие и изменение из файлов Excel за один вызов. Это идеальное решение для конвейеров данных, систем управления документами и рабочих процессов миграции.

## **API Unprotect Spreadsheet**

### **Веб-API**

```http
PUT https://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Параметры запроса**

| Имя параметра | Тип   | Расположение | Описание                                                                                     |
|---------------|-------|--------------|----------------------------------------------------------------------------------------------|
| Spreadsheet   | File  | FormData     | Файл Excel, для которого требуется снять защиту.                                            |
| password      | String| Query        | Пароль, защищающий файл от открытия.                                                         |
| modifyPassword| String| Query        | Пароль, необходимый для изменения файла (необязательный, если задан только пароль открытия). |
| outPath       | String| Query        | (Необязательный) Путь к папке, куда будет сохранена расшифрованная рабочая книга.           |
| outStorageName| String| Query        | (Необязательный) Имя хранилища, в которое будет записан выходной файл.                      |
| region        | String| Query        | (Необязательный) Настройки региона электронной таблицы.                                      |

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

Успешный ответ возвращает расшифрованный файл в виде потока. Файл может быть сохранен в местоположение, указанное в `outPath`/`outStorageName`, или получен непосредственно из полезной нагрузки ответа.

**Коды HTTP-статуса**

| Код | Значение                   | Описание                                                        |
|-----|----------------------------|-----------------------------------------------------------------|
| 200 | OK (ОК)                    | Фильтр успешно применён; ответ содержит детали операции.       |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизован) | Неверный или отсутствующий JWT-токен.                           |
| 413 | Payload Too Large (Слишком большой запрос) | Загруженный файл превышает лимит размера.                      |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                                  |

## Когда следует использовать API Unprotect Spreadsheet?

- **Восстановление доступа к заблокированным рабочим книгам** — быстро удаляйте забытые пароли на открытие или изменение без ручного вмешательства.
- **Автоматизация массовой разблокировки** — обрабатывайте большое количество файлов в проектах миграции данных или архивирования.
- **Интеграция с существующими рабочими процессами** — объединяйте с API хранилищ или преобразования для создания сквозных конвейеров (например, загрузка → снятие защиты → преобразование в PDF).
- **Обеспечение безопасности данных** — операция выполняется на стороне сервера, что сохраняет оригинальные файлы в безопасности, а расшифрованная версия сохраняется в вашем облачном хранилище.

## Как использовать API Unprotect Spreadsheet с SDK

### Спецификация OpenAPI

[Спецификация API UnProtect Spreadsheet](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Protection/ProtectSpreadsheet) предоставляет общедоступный программный интерфейс, позволяющий выполнять прямые REST-вызовы из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как сделать вызовы в Cloud API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet?password=OldPass&modifyPassword=ModPass" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@myfile.xlsx"
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

Использование SDK упрощает вызов, обрабатывая аутентификацию, формирование запроса и разбор ответа. SDK доступны для множества языков и включают готовые методы для снятия защиты с электронных таблиц.

Следующие примеры кода иллюстрируют, как вызывать API Unprotect Spreadsheet с использованием различных SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UnprotectSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UnprotectSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UnprotectSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UnprotectSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UnprotectSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UnprotectSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UnprotectSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UnprotectSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}