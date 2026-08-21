---
title: "Удаление всех свойств документа"
second_title: "Документ"
linktype: "Очистка"
type: docs
url: /ru/document-properties/clear/
aliases: [  /ru/remove-all-document-properties/ ]
keywords: "Aspose.Cells, удаление свойств документа, очистка свойств Excel, REST API, облачный SDK, электронная таблица, справка по API"
description: "Пошаговое руководство по удалению всех пользовательских и встроенных свойств из рабочей книги Excel с использованием облачного REST API Aspose.Cells."
weight: 58
---

Этот REST API удаляет все пользовательские свойства документа и очищает встроенные свойства.

## REST API

```bash
DELETE http://api.aspose.cloud/v3.0/cells/{name}/documentproperties
```

### Параметры запроса

| Имя параметра | Тип   | Расположение | Описание               |
| ------------- | ----- | ------------ | ---------------------- |
| name          | string | path        | Имя документа.         |
| folder        | string | query       | Папка документа.       |
| storageName   | string | query       | Имя хранилища.         |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Properties/DeleteDocumentProperties) определяет публично доступное программное интерфейсное решение и позволяет выполнять взаимодействие по протоколу REST непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Приведённый ниже пример демонстрирует, как выполнять вызовы облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties" \
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

Использование SDK — это лучший способ ускорить разработку. SDK берёт на себя обработку низкоуровневых деталей, позволяя вам сосредоточиться на задачах вашего проекта. Полный список облачных SDK Aspose.Cells представлен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Приведённые ниже примеры кода демонстрируют, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDocumentProperties.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDocumentProperties.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDocumentProperties.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDocumentProperties.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteDocumentProperties.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDocumentProperties.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDocumentProperties.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDocumentProperties.go" >}}
{{< /tab >}}

{{< /tabs >}}