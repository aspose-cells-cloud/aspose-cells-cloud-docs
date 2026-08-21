---
title: "Обновление изображения в файле Excel"
second_title: "Документ"
linktype: "Обновление"
type: docs
url: /pictures/update/
aliases: [/update-a-specific-picture-from-excel-workshee/]
keywords: "Aspose.Cells Cloud, Excel, Обновление изображения, REST API, SDK"
description: "Узнайте, как обновить изображение в рабочем листе Excel с помощью REST API Aspose.Cells Cloud. Включает подробности запроса, пример cURL и фрагменты кода SDK для различных языков программирования."
ArticleTitle: "Обновление изображения в файле Excel с помощью REST API Aspose.Cells Cloud"
weight: 70
---

Этот REST API обновляет изображение, идентифицируемое по его индексу, на рабочем листе Excel.

**Необходимые условия:** У вас должен быть действительный JWT-токен Aspose Cloud, целевой файл Excel должен храниться в облачном хранилище Aspose Cloud, а также необходимо использовать версию API 3.0 или выше.

## API PostWorksheetPicture

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### **Параметры запроса**

| Имя параметра | Тип    | Расположение | Описание                                                  |
|---------------|--------|-------------|-----------------------------------------------------------|
| name          | string | path        | Имя документа Excel.                                      |
| sheetName     | string | path        | Имя рабочего листа, содержащего изображение.             |
| pictureIndex  | integer| path        | Нулевой индекс обновляемого изображения.                  |
| picture       | object | body        | JSON-объект, описывающий свойства изображения для обновления. |
| folder        | string | query       | Папка, в которой хранится документ.                       |
| storageName   | string | query       | Имя службы хранилища.                                     |

**Примечание:** Индекс изображения нумеруется с нуля. Поддерживаемые форматы изображений: JPEG, PNG, BMP и GIF. Максимальный размер изображения — 10 МБ.

### Ответы об ошибках

| HTTP-код | Описание                                                                 |
|----------|--------------------------------------------------------------------------|
| 401      | Неавторизован — отсутствует или недействителен токен.                   |
| 404      | Не найдено — указанный файл, рабочий лист или индекс изображения не существует. |
| 400      | Неверный запрос — неправильный синтаксис запроса или недопустимые параметры. |
| 500      | Внутренняя ошибка сервера — возникло непредвиденное состояние.           |

<a href="https://apireference.aspose.cloud/cells/#/Pictures/PostWorksheetPicture" rel="noopener noreferrer">Спецификация OpenAPI</a> определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Приведённый ниже пример демонстрирует вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures/1" \
-X POST \
-d "{ \"UpperLeftRow\": 10, \"Top\": 0, \"UpperLeftColumn\": 1, \"Left\": 0, \"LowerRightRow\": 0, \"Bottom\": 0, \"LowerRightColumn\": 3, \"ImageFormat\": \"jpg\", \"SourceFullName\": \"download.jpg\"}" \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

Использование SDK — самый быстрый способ разработки. SDK берёт на себя обработку низкоуровневых деталей, позволяя сосредоточиться на задачах вашего проекта. Ознакомьтесь с <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">репозиторием на GitHub</a> для получения полного списка SDK Aspose.Cells Cloud.

Приведённые ниже примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}

*См. также:* Добавление изображения, Удаление изображения, Получение изображения, Очистка изображений — другие операции, связанные с изображениями, в API Aspose.Cells Cloud.