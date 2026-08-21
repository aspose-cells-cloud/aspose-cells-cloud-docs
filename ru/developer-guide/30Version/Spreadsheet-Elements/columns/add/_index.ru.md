---
title: "Добавление пустого столбца в рабочий лист Excel с помощью API Aspose.Cells Cloud"
second_title: "Документ"
linktype: "Добавить"
type: docs
url: /ru/columns/add/
aliases:
  - /add-an-empty-column-in-an-excel-worksheet/
  - /add-an-empty-column-in-a-worksheet/
keywords: "добавить, столбец, Excel, API, Aspose.Cells, облако, REST, вставить"
description: "Узнайте, как вставить новый столбец в таблицу Excel с помощью REST API Aspose.Cells Cloud. Приведены синтаксис запроса, пример cURL и примеры кода SDK."
weight: 20
ArticleTitle: "Добавление пустого столбца в рабочий лист Excel с помощью API Aspose.Cells Cloud"
---

Этот REST API вставляет один или несколько столбцов в рабочий лист.

**Необходимые условия**  
Перед вызовом этого endpoint убедитесь, что вы выполнили следующие действия:

- Получите действительный токен доступа OAuth 2.0 и включите его в заголовок `Authorization`.  
- Сохраните целевую рабочую книгу в выбранном хранилище (по умолчанию — «Default») либо укажите соответствующие параметры `folder` и `storageName`.  
- Убедитесь, что имя рабочего листа, указанное в `sheetName`, существует в рабочей книге.

## API PutInsertWorksheetColumns

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}?totalColumns=1
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### Параметры запроса

| Имя параметра       | Тип     | Расположение | Описание                                                     |
| ------------------- | ------- | ------------ | ------------------------------------------------------------ |
| **name**            | string  | path         | Имя файла рабочей книги.                                     |
| **sheetName**       | string  | path         | Имя рабочего листа.                                           |
| **columnIndex**     | integer | path         | Индекс столбца (начиная с 0), с которого начинается вставка. |
| **totalColumns**    | integer | query        | Количество вставляемых столбцов.                             |
| **updateReference** | boolean | query        | Если **true**, ссылки на ячейки обновляются с учетом вставки. |
| **folder**          | string  | query        | Путь к папке, содержащей рабочую книгу.                      |
| **storageName**     | string  | query        | Имя службы хранилища.                                         |

**Примечания**

- Значение `columnIndex` должно находиться в диапазоне от 0 до текущего количества столбцов в рабочем листе. Вставка за пределами существующего диапазона автоматически расширит лист.  
- Вставка нескольких столбцов (`totalColumns` > 1) сдвигает существующие столбцы вправо.  
- Параметр `updateReference` по умолчанию равен `false`; установите его в `true`, чтобы обновить формулы и именованные диапазоны.

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PutInsertWorksheetColumns) определяет публично доступное программное интерфейсное определение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для вызова веб-сервисов Aspose.Cells. Приведенный ниже пример показывает полный запрос, включая аутентификацию и правильные параметры пути.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/1?totalColumns=1&updateReference=true" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: application/json"
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

**Коды ответов**

| Код  | Описание                                     |
|------|----------------------------------------------|
| 200  | Столбец(ы) успешно вставлены.                |
| 400  | Неверный запрос — отсутствующие или некорректные параметры. |
| 401  | Неавторизовано — недействительный или отсутствующий токен. |
| 404  | Рабочая книга или рабочий лист не найдены.    |
| 500  | Внутренняя ошибка сервера.                    |

**Примеры ошибочных ответов**

```json
// 400 Bad Request – отсутствующие или некорректные параметры
{
  "Code": 400,
  "Message": "Неверный параметр: totalColumns должно быть положительным целым числом."
}

// 401 Unauthorized – недействительный или отсутствующий токен
{
  "Code": 401,
  "Message": "Ошибка аутентификации. Токен доступа отсутствует или недействителен."
}

// 404 Not Found – рабочая книга или рабочий лист не существует
{
  "Code": 404,
  "Message": "Рабочая книга 'test.xlsx' не найдена."
}

// 500 Internal Server Error
{
  "Code": 500,
  "Message": "На сервере произошла непредвиденная ошибка."
}
```

## Семейство облачных SDK

Использование SDK — самый быстрый способ разработки. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на логике вашего проекта. Полный список облачных SDK Aspose.Cells Cloud доступен в <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">репозитории на GitHub</a>.

Приведенные ниже примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutInsertWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutInsertWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutInsertWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutInsertWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutInsertWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutInsertWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutInsertWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutInsertWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}