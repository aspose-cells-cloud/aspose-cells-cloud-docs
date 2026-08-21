---
title: "Создание папки – Aspose.Cells Cloud API | Управление хранилищем Excel"
second_title: "Документ"
ArticleTitle: "Создание папки – Aspose.Cells Cloud API"
linktitle: "Создание папки"
type: docs
url: /ru/create-folder/
keywords: "Aspose.Cells, облачный API, создание папки, управление хранилищем, Excel"
description: "Создайте новую папку в облачном хранилище Aspose.Cells Cloud с помощью простого PUT-запроса. Ознакомьтесь с форматом запроса, параметрами, ответом и обработкой ошибок."
weight: 100
---

Операция **createFolder** создает новую папку в указанном месте облачного хранилища, используемого Excel API. Это важно для организации файлов и поддержания структурированной иерархии каталогов.

## **Excel API: Создание папки**

### Web API

```
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **Безопасность и аутентификация**

Облачные API Aspose.Cells защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе токена JWT</a>.

### Параметры запроса API **createFolder**

| Имя параметра | Тип   | Расположение | Обязательный | По умолчанию | Описание                                                                 |
| ------------- | ----- | ------------ | ------------ | ------------ | ------------------------------------------------------------------------ |
| `path`        | String | Путь         | Да           | –            | Путь к создаваемой папке (например, `myFolder/subFolder`).              |
| `storageName` | String | Параметр запроса | Нет          | –            | Имя используемого хранилища. Если не указано, применяется хранилище по умолчанию. |

### Описание ответа

```json
{}
```

При успешном выполнении операция не возвращает содержимое. Типичные HTTP-коды статуса:

**HTTP-коды статуса**

| HTTP-код | HTTP-статус           | Описание                                                                 |
| -------- | --------------------- | ------------------------------------------------------------------------ |
| 200      | OK (ОК)               | Web API вызван успешно; ответ содержит детали операции.                 |
| 400      | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401      | Unauthorized (Неавторизовано) | Недействительный или отсутствующий JWT-токен.                           |
| 413      | Payload Too Large (Слишком большой payload) | Загруженный файл превышает лимит размера.                               |
| 500      | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                                          |

## Спецификация OpenAPI

[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/FolderController/CreateFolder) определяет общедоступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать инструмент командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как выполнять вызовы в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/myFolder/subFolder" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — это лучший способ ускорить разработку. SDK управляет низкоуровневыми деталями, позволяя сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">репозитории GitHub</a>.

Приведенные ниже примеры кода демонстрируют, как выполнять вызовы веб-сервисов Aspose.Cells с использованием различных SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateFolder.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateFolder.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateFolder.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateFolder.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateFolder.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateFolder.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateFolder.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateFolder.go" >}}
{{</tab>}}
{{< /tabs >}}