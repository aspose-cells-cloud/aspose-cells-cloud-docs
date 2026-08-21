---
title: "Aspose.Cells Cloud API для получения версий файлов — быстрое извлечение истории версий файлов"
second_title: "Документ"
ArticleTitle: "Управление Excel в облаке — быстрое получение истории версий файлов в Aspose.Cells Cloud"
linktitle: "Получение версий файлов"
type: docs
url: /ru/get-file-versions/
keywords: "Aspose Cells API, версии файлов, управление версиями электронных таблиц, API облачного хранилища, REST, история файлов Excel"
description: "Получите полный список истории версий любого файла Excel, хранимого в Aspose.Cells Cloud. Поддерживается выбор хранилища, аутентификация и подробные коды ошибок."
weight: 100
---

Получите полный список записей версий для конкретной электронной таблицы, хранящейся в Aspose.Cells Cloud. Этот endpoint позволяет разработчикам отслеживать изменения, проводить аудит модификаций и внедрять рабочие процессы управления версиями непосредственно из облачного хранилища.

API **GetFileVersions** возвращает все записи версий для указанной электронной таблицы, хранящейся в Aspose.Cells Cloud. Это помогает поддерживать полную историю изменений для каждого файла.

## **Excel API: получение версий файлов**

### Web API

```
GET https://api.aspose.cloud/v4.0/cells/storage/version/{path}
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### Параметры запроса API **GetFileVersions**:

| Имя параметра | Тип   | Расположение | Описание                                                                                     |
| ------------- | ----- | ------------ | -------------------------------------------------------------------------------------------- |
| `path`        | String | Путь         | **Обязательный.** Полный путь к файлу, версии которого извлекаются.                          |
| `storageName` | String | Query        | Необязательный. Имя хранилища, содержащего файл. Если не указано, используется хранилище по умолчанию. |

### **Ответ**

```json
{
  "Name": "FileVersions",
  "Description": [
    "Содержит список версий файла для указанного документа."
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Value",
      "Description": ["Коллекция с подробной информацией о версиях файлов."],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "FileVersion",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "FileVersion",
          "Name": "class:fileversion"
        },
        "Name": "container"
      }
    }
  ]
}
```

При успешном выполнении API возвращает **HTTP 200 OK** с JSON-полезной нагрузкой, содержащей массив `Value` из объектов версий файлов, как показано выше.

**Коды HTTP-статуса**

| Код | Значение               | Описание                                                           |
| --- | ---------------------- | ------------------------------------------------------------------ |
| 200 | OK (OK)               | Фильтр применён успешно; ответ содержит детали операции.          |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизовано) | Неверный или отсутствующий JWT-токен.                             |
| 413 | Payload Too Large (Слишком большой полезный нагрузочный объект) | Загруженный файл превышает лимит размера.                         |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                                    |

## Спецификация OpenAPI

[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/StorageController/GetFileVersions) предоставляет исчерпывающее программное интерфейсное описание для выполнения REST-взаимодействий непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Пример ниже показывает, как выполнять вызовы к облачному API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/version/MyFolder/MyFile.xlsx" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Value": [
    {
      "VersionId": "1",
      "IsLatest": false,
      "ModifiedDate": "2024-01-15T12:34:56Z",
      "Size": 10240
    },
    {
      "VersionId": "2",
      "IsLatest": true,
      "ModifiedDate": "2024-03-01T08:22:10Z",
      "Size": 10300
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK упрощает разработку, абстрагируя низкоуровневую сложность, позволяя разработчикам сосредоточиться на ключевых функциях. Ознакомьтесь с [репозиторием на GitHub](https://github.com/aspose-cells-cloud), чтобы получить полный список SDK Aspose.Cells Cloud.

Примеры кода ниже иллюстрируют, как взаимодействовать с веб-сервисами Aspose.Cells на различных языках программирования:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetFileVersions.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetFileVersions.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetFileVersions.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetFileVersions.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetFileVersions.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetFileVersions.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetFileVersions.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetFileVersions.go" >}}
{{</tab>}}
{{< /tabs >}}