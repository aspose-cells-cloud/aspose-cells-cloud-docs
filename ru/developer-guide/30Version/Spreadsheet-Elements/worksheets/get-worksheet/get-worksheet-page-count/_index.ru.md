---
title: "Получить количество страниц для листа Excel"
second_title: "Документ"
linktitle: "PageCount"
type: docs
url: /worksheets/page-count/
keywords: "Aspose.Cells, Excel API, количество страниц листа, REST, облачный SDK, разбиение Excel на страницы"
description: "Получите количество печатаемых страниц в листе Excel с помощью REST API Aspose.Cells Cloud (v3.0). Включает формат HTTPS-запроса, шаги аутентификации, пример cURL, полный JSON-ответ, коды состояния и примеры кода SDK."
weight: 10
ArticleTitle: "Получить количество страниц для листа Excel – Aspose.Cells Cloud API"
---

Этот REST API возвращает **количество страниц** для листа.

**Аутентификация:** Все конечные точки Aspose.Cells Cloud требуют Bearer-токена, полученного по протоколу OAuth2. Включите токен в заголовок `Authorization`, как показано в примере cURL ниже.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pagecount
```

### Параметры запроса

| Параметр    | Тип    | Расположение | Описание                               |
| ----------- | ------ | ------------ | -------------------------------------- |
| name        | string | path         | Имя документа.                         |
| sheetName   | string | path         | Имя листа.                             |
| folder      | string | query        | Папка, содержащая документ.            |
| storageName | string | query        | Имя хранилища.                         |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetPageCount) определяет публично доступное программное интерфейсное решение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки **cURL** для простого доступа к веб-сервисам Aspose.Cells. Пример ниже демонстрирует вызов API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/worksheets/Sheet1/pagecount" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "PageCount": 3
}
```

{{< /tab >}}

{{< /tabs >}}

### Подробности ответа

| HTTP-статус | Значение                                              |
| ----------- | ----------------------------------------------------- |
| **200**     | Успех — возвращает JSON-полезную нагрузку, указанную выше. |
| **401**     | Неавторизован — отсутствует или недействителен токен. |
| **404**     | Не найдено — файл или лист не существуют.             |
| **500**     | Внутренняя ошибка сервера — неожиданное состояние сервера. |

### История версий

Версия API **v3.0** (выпущена в 2025 г.). Если вы используете более новую версию, обратитесь к обновлённой документации по конечной точке.

## Семейство облачных SDK

Использование SDK — самый быстрый способ разработки. SDK скрывает детали низкоуровневой реализации, позволяя сосредоточиться на бизнес-логике. Полный список облачных SDK Aspose.Cells Cloud приведён в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetPageCount.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetPageCount.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetPageCount.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetPageCount.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetPageCount.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetPageCount.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetPageCount.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetPageCount.go" >}}

{{< /tab >}}

{{< /tabs >}}

### Примечания

- Количество страниц отражает макет, пригодный для печати, и учитывает разрывы страниц, поля и масштабирование. Скрытые строки или столбцы могут повлиять на результат.
- Перед отправкой запроса убедитесь, что целевой лист существует, а файл сохранён в указанной папке (`folder`) и хранилище (`storageName`).