---
title: "Получить все изображения на листе Excel"
second_title: "Документ"
linktype: "get-all"
type: docs
url: /ru/pictures/get-all/
aliases: [  /ru/get-picture-from-a-worksheet/ ]
keywords: "Aspose.Cells Cloud, лист Excel, API изображений, получить все изображения, REST API, SDK"
description: "Получить все объекты изображений с листа Excel через REST API Aspose.Cells Cloud."
ArticleTitle: "Получить все изображения на листе Excel — API Aspose.Cells Cloud"
weight: 10
---

Этот REST API извлекает всю информацию об изображениях с листа Excel.

**Необходимые условия**  
Перед вызовом этого эндпоинта убедитесь, что у вас есть:

- Действующий JWT-токен доступа Aspose Cloud.  
- Целевой файл Excel, загруженный в выбранное хранилище.  
- Правильное имя хранилища (если используется пользовательское хранилище).  
- Имя листа, содержащего изображения.

## API GetWorksheetPictures

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

**Примечание:** Используйте HTTPS (TLS 1.2 или выше) при вызове API и включайте действующий JWT-токен в заголовок `Authorization`.

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### **Параметры запроса**

| Имя параметра | Тип    | Расположение | Описание                                       |
| ------------- | ------ | ------------ | ---------------------------------------------- |
| name          | string | path         | Имя файла Excel.                               |
| sheetName     | string | path         | Имя листа, содержащего изображения.            |
| folder        | string | query        | Путь к папке, в которой хранится файл.         |
| storageName   | string | query        | Имя сервиса хранилища.                         |

### **Ответы об ошибках**

| HTTP-код | Описание                                                                      |
| -------- | ----------------------------------------------------------------------------- |
| 401      | Неавторизован — отсутствует или недействителен токен.                        |
| 404      | Не найдено — указанный файл, лист или индекс разрыва страницы не существует.  |
| 400      | Неверный запрос — некорректный синтаксис запроса или недопустимые параметры.  |
| 500      | Внутренняя ошибка сервера — возникло непредвиденное состояние.                |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Pictures/GetWorksheetPictures) определяет публично доступное программное интерфейсное описание и позволяет выполнять взаимодействие по REST непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Следующий пример показывает, как выполнять вызовы к облачному API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Pictures": {
    "PictureList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/1",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/2",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      }
    ],
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet2/pictures",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Успешный ответ** — успешный вызов возвращает HTTP 200 с JSON-полезной нагрузкой, содержащей объект `Pictures`, в котором перечислены ссылки на ресурсы каждого изображения.

## Семейство облачных SDK

Использование SDK — это лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя вам сосредоточиться на задачах вашего проекта. Посетите [репозиторий на GitHub](https://github.com/aspose-cells-cloud), чтобы ознакомиться с полным списком SDK Aspose.Cells Cloud.

Следующие примеры кода демонстрируют, как выполнять вызовы к веб-сервисам Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetPictureWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetPictureWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetPictureWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetPictureWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetPictureWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetPictureWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetPictureWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetPictureWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}

Вы можете загрузить SDK непосредственно из соответствующих менеджеров пакетов (например, NuGet для .NET, Maven Central для Java, Composer для PHP, npm для Node.js, PyPI для Python, CPAN для Perl и Go modules для Go).

*См. также:* Добавить изображение, Удалить изображение, Обновить свойства изображения.