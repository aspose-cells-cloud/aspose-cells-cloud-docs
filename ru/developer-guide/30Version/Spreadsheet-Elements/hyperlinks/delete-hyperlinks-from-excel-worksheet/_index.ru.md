---
title: "Очистка гиперссылок"
type: docs
url: /ru/hyperlinks/clear/
aliases: [  /ru/add-hyperlinks-to-excel-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel, удаление гиперссылок, очистка гиперссылок, REST API, рабочий лист, SDK"
description: "Узнайте, как удалить все гиперссылки из рабочего листа Excel с помощью Aspose.Cells Cloud REST API или любого поддерживаемого SDK (C#, Java, Python, Node.js, Go, PHP, Ruby, Perl и др.)."
weight: 40
ArticleTitle: "Очистка гиперссылок – документация Aspose.Cells Cloud API"
---

Этот REST API удаляет **все гиперссылки** с рабочего листа Excel.

## Безопасность и аутентификация
Aspose.Cells Cloud API защищены и требуют [аутентификации на основе JWT-токена](https://docs.aspose.cloud/total/ru/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
```

### Параметры запроса

| Имя параметра | Тип    | Местоположение | Описание                                     |
| ------------- | ------ | -------------- | -------------------------------------------- |
| name          | string | path           | Имя файла Excel.                             |
| sheetName     | string | path           | Имя рабочего листа.                          |
| folder        | string | query          | Папка, содержащая документ.                  |
| storageName   | string | query          | Имя сервиса облачного хранилища.             |

### Коды ошибок

| HTTP-код | Причина                                          | Пример тела ответа                                                    |
| -------- | ------------------------------------------------ | --------------------------------------------------------------------- |
| **400**  | Неверный запрос — отсутствуют или некорректны параметры. | `{ "Code":"400", "Message":"Некорректное значение параметра." }`      |
| **401**  | Неавторизован — отсутствует или некорректен JWT-токен.   | `{ "Code":"401", "Message":"Токен доступа отсутствует или некорректен." }` |
| **404**  | Не найдено — книга или рабочий лист не существуют.        | `{ "Code":"404", "Message":"Файл не найден." }`                       |
| **500**  | Внутренняя ошибка сервера — непредвиденный сбой сервера. | `{ "Code":"500", "Message":"Произошла непредвиденная ошибка." }`      |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Hyperlinks/DeleteWorksheetHyperlinks) определяет общедоступное программное интерфейсное описание, позволяющее выполнять взаимодействие с REST API непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки **cURL** для вызова веб-сервисов Aspose.Cells. В приведённом ниже примере показано, как удалить все гиперссылки с рабочего листа.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test1.xlsx/worksheets/Sheet1/hyperlinks" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

Использование SDK ускоряет разработку, поскольку обрабатывает низкоуровневые детали за вас. Полный список SDK Aspose.Cells Cloud доступен на [GitHub-репозитории](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют, как удалить гиперссылки с рабочего листа с помощью различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetHyperlinks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetHyperlinks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetHyperlinks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetHyperlinks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetHyperlinks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetHyperlinks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetHyperlinks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetHyperlinks.go" >}}

{{< /tab >}}

{{< /tabs >}}