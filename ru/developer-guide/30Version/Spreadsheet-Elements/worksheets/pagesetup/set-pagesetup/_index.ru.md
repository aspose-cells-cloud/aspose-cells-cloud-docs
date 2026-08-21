---
title: "Настройка параметров страницы для рабочего листа"
second_title: "Документ"
linktitle: "Настройка параметров страницы"
type: docs
url: /ru/set-page-setup/
keywords: "Aspose.Cells, Excel, настройка страницы, REST API, рабочий лист, облачный SDK"
description: "Узнайте, как настроить параметры страницы для рабочего листа Excel с помощью Aspose.Cells Cloud REST API. Приведены подробности запроса, безопасный пример вызова через cURL по HTTPS, коды состояния ответа и фрагменты кода SDK для нескольких языков программирования."
weight: 20
ArticleTitle: "Настройка параметров страницы для рабочего листа – Руководство по API Aspose.Cells Cloud"
---

Необходимые условия: для вызова этого API у вас должен быть действительный JWT-токен (OAuth), и книга должна находиться в хранилище Aspose Cloud, где у вас есть права на чтение и запись. Убедитесь, что токен передан в заголовке **Authorization**, и что ваша учетная запись имеет необходимый лимит API.

Этот REST API устанавливает параметры страницы для рабочего листа Excel.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pagesetup
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификацию по токену JWT</a>.

### **Параметры запроса**

| Имя параметра | Тип   | Местоположение | Описание                     |
| ------------- | ----- | -------------- | ---------------------------- |
| name          | string | path          | Имя документа.               |
| sheetName     | string | path          | Имя рабочего листа.          |
| pageSetup     | object | body          | Описание параметров страницы.|
| folder        | string | query         | Папка документа.             |
| storageName   | string | query         | Имя хранилища.               |

**Пример JSON-тела для объекта `pageSetup`**

```json
{
  "pageSetup": {
    "orientation": "Portrait",
    "paperSize": "A4",
    "fitToPagesTall": 1,
    "fitToPagesWide": 1,
    "centerHorizontally": true,
    "centerVertically": false
  }
}
```

<a href="https://reference.aspose.cloud/cells/#/PageSetup/PostPageSetup" target="_blank" rel="noopener noreferrer">Спецификация OpenAPI</a> определяет публично доступное программное интерфейсное описание и позволяет выполнять взаимодействие с REST-интерфейсом непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как делать вызовы к облачному API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Tasks/pagesetup" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{
  "pageSetup": {
    "orientation": "Portrait",
    "paperSize": "A4",
    "fitToPagesTall": 1,
    "fitToPagesWide": 1,
    "centerHorizontally": true,
    "centerVertically": false
  }
}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

API возвращает JSON-объект, указывающий результат выполнения операции:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Возможные коды состояния ответа**

| Код | Значение                    | Когда возникает                                           |
|-----|-----------------------------|-----------------------------------------------------------|
| 200 | OK (OK)                     | Успешное обновление параметров страницы                  |
| 400 | Bad Request (Неверный запрос)| Неверное JSON-тело или отсутствие обязательных полей     |
| 401 | Unauthorized (Неавторизован)| Отсутствующий или недействительный JWT-токен            |
| 404 | Not Found (Не найдено)      | Книга или рабочий лист с указанным именем не существует  |
| 500 | Internal Server Error (Внутренняя ошибка сервера)| Непредвиденный сбой сервера                    |

## Семейство облачных SDK

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали и позволяет сосредоточиться на задачах проекта. Ознакомьтесь с <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">репозиторием на GitHub</a>, чтобы получить полный список облачных SDK Aspose.Cells.

Примеры кода ниже демонстрируют, как делать вызовы к веб-сервисам Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostPageSetup.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostPageSetup.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostPageSetup.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostPageSetup.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostPageSetup.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostPageSetup.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostPageSetup.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostPageSetup.go" >}}

{{< /tab >}}

{{< /tabs >}}
---