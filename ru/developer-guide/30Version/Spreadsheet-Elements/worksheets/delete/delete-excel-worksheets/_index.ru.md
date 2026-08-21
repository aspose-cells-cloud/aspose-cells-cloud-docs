---
title: "Удаление нескольких рабочих листов Excel"
second_title: "Документ"
linktype: "docs"
url: /ru/worksheets/delete-multiple/
aliases: [  /ru/delete-excel-worksheets/ ]
keywords: "Aspose.Cells Cloud, удаление нескольких рабочих листов, Excel API, REST API, v3.0, удаление рабочих листов"
description: "Узнайте, как удалить несколько рабочих листов из книги Excel с помощью REST API Aspose.Cells Cloud (v3.0). Включает безопасный HTTPS-endpoint, необходимые параметры, исправленный пример cURL и фрагменты SDK для нескольких языков программирования."
weight: 20
ArticleTitle: "Удаление нескольких рабочих листов Excel с помощью REST API Aspose.Cells Cloud"
---

Этот REST API удаляет несколько рабочих листов из книги.

## Безопасность и аутентификация
API Aspose.Cells Cloud защищены и требуют [аутентификации на основе токена JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets
```

### **Параметры запроса**

| Имя параметра | Тип    | Местоположение | Описание                                                                 |
| ------------- | ------ | -------------- | ------------------------------------------------------------------------ |
| name          | string | path           | Имя файла Excel.                                                         |
| matchCondition| object | body           | Объект `MatchConditionRequest`, определяющий, какие рабочие листы удалить. |
| folder        | string | query          | Путь к папке в хранилище, где расположен файл.                           |
| storageName   | string | query          | Имя службы хранилища.                                                    |

**Свойства MatchConditionRequest**

| Имя                 | Тип      | Описание                                   | Примечания |
| ------------------- | -------- | ------------------------------------------ | ---------- |
| RegexPattern        | string   | Регулярное выражение для сопоставления имён рабочих листов. | необязательное |
| FullMatchConditions | string[] | Точные имена рабочих листов для удаления. | необязательное |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheets) определяет публично доступное программное интерфейсное решение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для удобного доступа к веб-сервисам Aspose.Cells. Следующий пример демонстрирует, как выполнять вызовы облачного API с помощью cURL. **В заголовке `Authorization` требуется действительный токен JWT.**

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets?folder=Temp" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>" \
  -d '{"FullMatchConditions":["Sheet1","Sheet2","Sheet3"]}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Запрос также может возвращать типовые ошибочные ответы, например:

| HTTP-статус | Значение                                      | Пример полезной нагрузки                                |
| ----------- | --------------------------------------------- | ------------------------------------------------------- |
| 400         | Неверный запрос — недопустимый JSON или параметры | `{"Code":400,"Message":"Invalid request payload."}`      |
| 401         | Неавторизован — отсутствующий или недействительный токен JWT | `{"Code":401,"Message":"Authentication failed."}`        |
| 403         | Доступ запрещён — недостаточно прав           | `{"Code":403,"Message":"Access denied."}`                |
| 404         | Не найдено — файл или рабочий лист не существуют | `{"Code":404,"Message":"Resource not found."}`           |
| 500         | Внутренняя ошибка сервера                     | `{"Code":500,"Message":"An unexpected error occurred."}` |

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя вам сосредоточиться на задачах вашего проекта. Полный список облачных SDK Aspose.Cells Cloud представлен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют, как выполнять вызовы веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheets.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheets.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheets.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheets.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheets.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheets.go" >}}

{{< /tab >}}

{{< /tabs >}}

**См. также:**  
- [Удаление одного рабочего листа](https://docs.aspose.cloud/cells/worksheets/delete/)  
- [Копирование рабочего листа](https://docs.aspose.cloud/cells/worksheets/copy/)  
- [Перемещение рабочего листа](https://docs.aspose.cloud/cells/worksheets/move/)  
---