---
title: "Aspose.Cells Cloud API для загрузки файлов — Интерфейс для быстрой загрузки файлов в облако"
second_title: "Документ"
ArticleTitle: "Aspose.Cells Cloud API для загрузки файлов — Интерфейс для быстрой загрузки файлов в облако"
linktitle: "Загрузить файл"
type: docs
url: /ru/upload-file/
keywords: "Aspose.Cells, загрузка файлов, Excel API, облачное хранилище, REST API"
description: "Руководство по загрузке файлов с помощью API Aspose.Cells Cloud, включающее параметры запроса, коды HTTP-статусов, обработку ошибок и примеры кода."
weight: 100
---

API **uploadFile** позволяет разработчикам напрямую загружать файлы в облачное хранилище для последующей обработки с помощью Aspose Cells.

## **Aspose Cells API: Загрузка файлов**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Параметры запроса API **uploadFile**

| Имя параметра | Тип   | Путь/Строка запроса/Тело HTTP-запроса | Описание                                                                                      |
| :------------ | :---- | :------------------------------------- | :-------------------------------------------------------------------------------------------- |
| UploadFiles   | Файл  | FormData                               | Загрузка файлов в облачное хранилище.                                                         |
| path          | Строка | Путь                                   | Путь назначения в облачном хранилище. Укажите путь, куда следует загрузить файл.              |
| storageName   | Строка | Параметр запроса                       | Имя хранилища, в которое будет загружен файл.                                                 |

### **Ответ**

```json
{
  "Name": "FilesUploadResult",
  "Description": ["Результат загрузки файла"],
  "Type": "Класс",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Uploaded",
      "Description": ["Список имён загруженных файлов"],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Контейнер",
        "Reference": "String",
        "ElementDataType": {
          "Identifier": "String",
          "Name": "строка"
        },
        "Name": "контейнер"
      }
    },
    {
      "Name": "Errors",
      "Description": ["Список ошибок."],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Контейнер",
        "Reference": "Error",
        "ElementDataType": {
          "Identifier": "Класс",
          "Reference": "Error",
          "Name": "класс:ошибка"
        },
        "Name": "контейнер"
      }
    }
  ]
}
```

API возвращает следующие HTTP-коды состояния:

| Код состояния                 | Описание                                              |
| ----------------------------- | ----------------------------------------------------- |
| **200 OK**                    | Файл успешно загружен.                                |
| **400 Bad Request**           | Неверные параметры или некорректный запрос.           |
| **401 Unauthorized**          | Отсутствует или недействителен токен аутентификации.  |
| **403 Forbidden**             | Недостаточно прав для указанного хранилища.           |
| **500 Internal Server Error** | Непредвиденная ошибка сервера.                        |

## Как использовать API загрузки файлов с помощью SDK?

### Спецификация OpenAPI

[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/FileController/UploadFile) содержит подробное описание API, позволяя разработчикам взаимодействовать с ним напрямую через веб-браузер.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как выполнять вызовы в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/Folder/Book1.xlsx" \
  -H "Authorization: Bearer {access_token}" \
  -F "UploadFiles=@/path/to/Book1.xlsx" \
  -F "path=Folder/Book1.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Uploaded": ["Book1.xlsx"],
  "Errors": []
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK повышает эффективность разработки, скрывая низкоуровневые детали, позволяя разработчикам сосредоточиться на задачах проекта. Посетите [репозиторий GitHub](https://github.com/aspose-cells-cloud), чтобы получить полный список SDK Aspose.Cells Cloud.

Следующие примеры кода демонстрируют, как вызывать веб-сервисы Aspose.Cells с помощью различных SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UploadFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UploadFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UploadFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UploadFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UploadFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UploadFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UploadFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UploadFile.go" >}}
{{</tab>}}
{{< /tabs >}}

**См. также**

- [API загрузки файлов](/download-file/) – Получить файл из облачного хранилища.
- [API копирования файлов](/copy-file/) – Скопировать файл внутри облачного хранилища.
- [API удаления файлов](/delete-file/) – Удалить файл из облачного хранилища.