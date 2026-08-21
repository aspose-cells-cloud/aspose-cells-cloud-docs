---
title: "Объединение нескольких файлов Excel в одну рабочую книгу"
second_title: "Документ"
linktitle: "Объединение нескольких файлов Excel"
type: docs
url: /merge-multi-files-into-excel/
aliases: [/merge/multi-files/]
keywords: "Aspose.Cells Cloud, объединение нескольких файлов Excel, REST API, объединение электронных таблиц, облачный SDK"
description: "Узнайте, как объединить несколько рабочих книг Excel в один файл с помощью REST API Aspose.Cells Cloud (версия 3.0). Включает HTTPS-адрес, команду cURL, примеры SDK, необходимые параметры и детали обработки ошибок."
weight: 32
---

## REST API

Этот REST API объединяет несколько файлов Excel в одну рабочую книгу Excel.

```bash
POST https://api.aspose.cloud/v3.0/cells/merge
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе токена JWT</a>.


### Параметры запроса

| Имя параметра | Тип    | Расположение | Описание                                                                                     | Обязательный |
|---------------|--------|--------------|----------------------------------------------------------------------------------------------|-------------|
| files[]       | file   | formData     | Одна или несколько рабочих книг Excel для объединения. Используйте `file1`, `file2`, … в запросе. | Да          |
| format        | string | query        | Желаемый выходной формат (например, `xlsx`).                                                | Да          |
| mergeToOneSheet | boolean | query     | Установите значение `true`, чтобы объединить все рабочие листы в один лист; по умолчанию — `false`. | Нет         |

### **Ответ**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[имя объединённого файла]",
    "Filesize" : [размер файла],
    "FileContent" : "[Base64String]"
}
```

**Коды HTTP-статусов**

| Код | Значение                    | Описание                                                  |
|-----|-----------------------------|-----------------------------------------------------------|
| 200 | OK (OK)                     | Фильтр успешно применён; ответ содержит детали операции. |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизовано) | Неверный или отсутствующий токен JWT.                     |
| 413 | Payload Too Large (Слишком большой полезный груз) | Загруженный файл превышает предельный размер.             |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                            |
## Как использовать API PostMerge с SDK

### Спецификация API PostMerge

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostMerge) определяет общедоступное программное интерфейсное определение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Пример ниже показывает, как делать вызовы в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/merge?format=xlsx" \
  -X POST \
  -H "Authorization: Bearer <jwt token>" \
  -F "file1=@file1.xlsx" \
  -F "file2=@file2.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  {
    "Filename": "file1.xlsx",
    "FileSize": 274022,
    "FileContent": "-----Base64String--------"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — это лучший способ ускорить разработку. SDK обрабатывает детали низкого уровня, позволяя сосредоточиться на задачах вашего проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Merge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-Merge.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LightCells-Merge.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "LightCellsMerge.py" >}}
{{< /tab >}}

{{< /tabs >}}

---