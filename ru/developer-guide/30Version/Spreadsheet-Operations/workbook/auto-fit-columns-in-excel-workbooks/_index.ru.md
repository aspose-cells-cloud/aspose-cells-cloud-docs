---
title: "Автоматическая подгонка столбцов в файле Excel"
second_title: "Документ"
linktype: "Столбцы"
type: docs
url: /ru/autofit-columns-on-an-excel-file/
aliases:
  [
    /auto-fit-columns-in-excel-workbooks,
    /autofit-columns-in-excel-workbooks/,
    /columns/autofit/,
    /workbook/autofit/columns/,
  ]
keywords: "автоматическая подгонка столбцов, Excel, Aspose.Cells Cloud, REST API, SDK, cURL, API"
description: "Узнайте, как использовать REST API Aspose.Cells Cloud для автоматической подгонки столбцов в книге Excel. Приведены детали запроса, пример cURL и примеры кода SDK для различных языков."
weight: 90
---

Этот REST API поддерживает автоматическую подгонку столбцов в книге Excel.

## API PostAutofitWorkbookColumns

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/autofitcolumns
```

Параметры запроса:

| Имя параметра        | Тип    | Расположение | Описание                                                |
| --------------------- | ------- | ------------ | ------------------------------------------------------- |
| **name**              | string  | путь         | Имя файла книги.                                        |
| **autoFitterOptions** | object  | тело         | Параметры, управляющие поведением автоматической подгонки. |
| **startColumn**       | integer | запрос       | Индекс первого столбца для подгонки (начинается с 0).   |
| **endColumn**         | integer | запрос       | Индекс последнего столбца для подгонки (начинается с 0). |
| **folder**            | string  | запрос       | Папка, содержащая книгу.                                |
| **storageName**       | string  | запрос       | Имя службы хранилища.                                   |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostAutofitWorkbookColumns){:rel="noopener noreferrer"} определяет публично доступное программное интерфейсное решение и позволяет выполнять взаимодействие по REST напрямую из веб-браузера.

Для простого доступа к веб-сервисам Aspose.Cells можно использовать утилиту командной строки cURL. В следующем примере показано, как вызвать облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/autofitcolumns" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{"AutoFitMergedCells":true, "IgnoreHidden":true}'
```

> **Примечание.** В рабочей среде всегда используйте HTTPS-endpoint и храните JWT-токен в секрете.

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

### Необходимые условия
Перед вызовом этой операции убедитесь, что у вас есть действующий API-ключ Aspose Cloud, сгенерированный JWT-токен и что целевая книга уже существует в указанном местоположении хранилища.

**Коды HTTP-статуса**

| Код | Значение                     | Описание                                                                 |
|-----|-----------------------------|--------------------------------------------------------------------------|
| 200 | OK                          | Фильтр применён успешно; в ответе содержатся детали операции.           |
| 400 | Bad Request                 | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized                | Недействительный или отсутствующий JWT-токен.                           |
| 413 | Payload Too Large           | Загружаемый файл превышает ограничение по размеру.                      |
| 500 | Internal Server Error       | Непредвиденная ошибка сервера.                                           |

API может возвращать следующие HTTP-статусы:

| Код | Описание                                            |
|-----|-----------------------------------------------------|
| 200 | Успех — столбцы автоматически подогнаны             |
| 400 | Неверный запрос — отсутствующие или некорректные параметры |
| 401 | Неавторизован — недействительный или просроченный JWT |
| 500 | Ошибка сервера — внутренняя ошибка обработки        |

## Семейство облачных SDK

Использование SDK — наиболее эффективный способ ускорить разработку. SDK берёт на себя низкоуровневые детали, позволяя вам сосредоточиться на логике вашего проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud){:rel="noopener noreferrer"}.

Примеры кода ниже демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorkbookColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorkbookColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorkbookColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorkbookColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorkbookColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorkbookColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorkbookColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorkbookColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}