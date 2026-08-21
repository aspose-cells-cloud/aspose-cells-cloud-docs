---
title: "Обновление проверки данных на листе Excel"
second_title: "Документ"
linktitle: "Обновление"
type: docs
url: /validations/update/
keywords: "Aspose.Cells Cloud, обновление проверки данных Excel, REST API, проверка данных на листе, Excel API"
description: "Как обновить проверку данных на листе Excel с помощью REST API Aspose.Cells Cloud, включая примеры cURL и фрагменты кода SDK для различных языков программирования."
weight: 10
ArticleTitle: "Обновление проверки данных на листе с помощью API Aspose.Cells Cloud"
---

Этот REST API обновляет проверку данных на листе Excel по её индексу.

Перед вызовом этой конечной точки получите JWT-токен доступа с соответствующими областями действия (например, `Cells.ReadWrite`). Включите токен в заголовок `Authorization`, как показано в примерах.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
```

### **Параметры запроса**

| Имя параметра   | Тип     | Расположение | Описание                                                   |
| ---------------- | ------- | ------------ | ---------------------------------------------------------- |
| name             | string  | path         | Имя файла рабочей книги.                                   |
| sheetName        | string  | path         | Имя листа, содержащего проверку данных.                   |
| validationIndex  | integer | path         | Индекс обновляемой проверки данных (начинается с 0).      |
| validation       | object  | body         | JSON-объект, определяющий новые параметры проверки данных. |
| folder           | string  | query        | Папка в облачном хранилище, где расположена рабочая книга. |
| storageName      | string  | query        | Имя службы хранилища (если используется пользовательская служба). |

<a href="https://apireference.aspose.cloud/cells/#/WorksheetValidations/PostWorksheetValidation" target="_blank" rel="noopener noreferrer">Спецификация OpenAPI</a> определяет общедоступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого вызова веб-сервисов Aspose.Cells. Пример ниже показывает, как выполнить вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations/0" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{ "AlertStyle":"Warning" }'
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

**Возможные HTTP-коды состояния**

| Код | Значение                               | Описание |
|-----|----------------------------------------|----------|
| 200 | OK (ОК)                                | Проверка данных успешно обновлена. |
| 400 | Bad Request (Неверный запрос)          | Запрос синтаксически некорректен или отсутствуют обязательные параметры. |
| 401 | Unauthorized (Неавторизован)           | Неверный или отсутствующий JWT-токен. |
| 403 | Forbidden (Запрещено)                  | Токен не содержит необходимых областей действия. |
| 404 | Not Found (Не найдено)                 | Указанная рабочая книга, лист или индекс проверки не существует. |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | На сервере произошла непредвиденная ошибка. |

Дополнительные сведения об обработке ошибок см. в <a href="https://apireference.aspose.cloud/cells/#/Errors" target="_blank" rel="noopener noreferrer">документации Aspose.Cells Cloud по ошибкам</a>.

Также вы можете ознакомиться с родственными операциями, такими как добавление новой проверки или удаление существующей:

- [Добавление проверки данных на листе](https://docs.aspose.cloud/cells/validations/add/)
- [Удаление проверки данных на листе](https://docs.aspose.cloud/cells/validations/delete/)

## Семейство облачных SDK

Использование SDK — самый быстрый способ разработки. SDK скрывает детали низкого уровня, позволяя сосредоточиться на бизнес-логике. Ознакомьтесь с <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">репозиторием на GitHub</a>, чтобы увидеть полный список SDK Aspose.Cells Cloud.

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}