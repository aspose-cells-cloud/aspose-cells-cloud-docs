---
title: "Проверка существования хранилища — Aspose.Cells Cloud API (v4.0)"
second_title: "Документ"
ArticleTitle: "Управление файлами Excel в облаке — Проверка существования хранилища"
linktitle: "Существует ли хранилище"
type: docs
url: /storage-exists/
keywords: "Aspose.Cells, существует ли хранилище, API облачного хранилища, REST, Excel"
description: "Проверьте наличие контейнера хранилища в Aspose.Cells Cloud. Изучите конечную точку GET /v4.0/cells/storage/{storageName}/exist, необходимые параметры, формат ответа и примеры SDK на C#, Java, Python и других языках."
weight: 100
---

API `storageExists` проверяет, существует ли указанное хранилище в облачной службе Aspose.Cells Cloud. Эта функция критически важна для обеспечения корректного выполнения всех операций, зависящих от хранилища.
**Краткое описание** — Конечная точка `storageExists` позволяет убедиться, что конкретный контейнер хранилища доступен в Aspose.Cells Cloud. Используйте её перед выполнением операций, связанных с файлами, чтобы избежать ошибок во время выполнения.

## Проверка существования хранилища (storageExists)

### Веб-API

```
GET https://api.aspose.cloud/v4.0/cells/storage/{storageName}/exist
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### Параметры запроса

| Имя параметра | Тип   | Расположение | Описание                                              |
| ------------- | ----- | ------------ | ----------------------------------------------------- |
| storageName   | String | Путь         | Имя хранилища, существование которого требуется проверить. |

### **Ответ**

```json
{
  "Name": "StorageExist",
  "Description": ["Указывает, существует ли указанное хранилище."],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Exists",
      "Description": [
        "Указывает, существует ли хранилище.",
        "Свойство возвращает true, если хранилище присутствует; в противном случае возвращает false."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Boolean",
        "Name": "boolean"
      }
    }
  ]
}
```

**Коды HTTP-статуса**

| Код | Значение              | Описание                                                     |
| --- | --------------------- | ------------------------------------------------------------ |
| 200 | OK (ОК)               | Фильтр применён успешно; ответ содержит сведения об операции. |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизован) | Недействительный или отсутствующий JWT-токен.               |
| 413 | Payload Too Large (Слишком большой полезный груз) | Загруженный файл превышает предельный размер.                |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                               |

## Как использовать API существования хранилища с SDK?

### Спецификация OpenAPI

<a href="https://reference.aspose.cloud/cells/#/StorageController/StorageExists" rel="nofollow noopener noreferrer">Спецификация OpenAPI</a> определяет публично доступный программный интерфейс, позволяя разработчикам напрямую взаимодействовать с REST API из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells Cloud. В следующем примере показано, как выполнять вызовы в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/{storageName}/exist" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Exists": true
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — наиболее эффективный способ ускорить разработку. SDK абстрагирует детали низкоуровневой реализации, позволяя разработчикам сосредоточиться на задачах проекта. Полный список доступных SDK Aspose.Cells Cloud см. в <a href="https://github.com/aspose-cells-cloud" rel="nofollow noopener noreferrer">репозитории на GitHub</a>.

Приведённые ниже примеры кода демонстрируют, как выполнять вызовы API в веб-сервисы Aspose.Cells Cloud с использованием различных SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_StorageExists.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_StorageExists.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_StorageExists.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_StorageExists.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_StorageExists.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_StorageExists.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_StorageExists.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_StorageExists.go" >}}
{{</tab>}}
{{< /tabs >}}