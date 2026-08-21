---
title: "Скрытие строк в рабочей книге Excel"
second_title: "Документ"
linktype: "Скрыть"
type: docs
url: /ru/rows/hide/
aliases: [/hide-rows-in-excel-worksheet/]
keywords: "скрыть строки, Aspose.Cells Cloud, Excel API, REST, SDK"
description: "Узнайте, как скрыть одну или несколько строк в рабочей книге Excel с помощью REST API Aspose.Cells Cloud. Включает пример cURL, фрагменты SDK, параметры, аутентификацию, детали ответа и обработку ошибок."
weight: 40
ArticleTitle: "Скрытие строк в рабочей книге Excel с помощью API Aspose.Cells Cloud"
---

Этот REST API скрывает строки в рабочей книге Excel.

**Требования:** Действующий JWT-токен, полученный из OAuth-эндпоинта Aspose Cloud, рабочая книга, сохранённая в облачном хранилище Aspose, и имя рабочего листа, содержащего строки, которые нужно скрыть. API работает с файлами Excel в форматах XLS, XLSX и других поддерживаемых форматах.

## API PostHideWorksheetRows

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/hide
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### Параметры запроса

| Параметр        | Тип     | Расположение | Описание                                                         |
| --------------- | ------- | ------------ | ---------------------------------------------------------------- |
| **name**        | string  | path         | Имя файла рабочей книги.                                         |
| **sheetName**   | string  | path         | Имя рабочего листа, содержащего строки, которые нужно скрыть.   |
| **startrow**    | integer | query        | Индекс первой скрываемой строки (отсчёт с нуля).                 |
| **totalRows**   | integer | query        | Количество последовательных строк для скрытия, начиная с **startrow**. |
| **folder**      | string  | query        | Папка в хранилище, где расположена рабочая книга.               |
| **storageName** | string  | query        | Имя службы хранилища.                                            |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/PostHideWorksheetRows) предоставляет общедоступное программное интерфейсное описание, позволяющее выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки **cURL** для вызова веб-сервисов Aspose.Cells. API требует JWT-токена, полученного из OAuth-эндпоинта Aspose Cloud; его необходимо указать в заголовке `Authorization`. Ниже приведён пример скрытия строки с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/hide?startrow=1&totalRows=1" \
  -X POST \
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

**Коды состояния ответа**

| Код | Описание |
|-----|----------|
| 200 | Успех — строки скрыты |
| 400 | Неверный запрос — недопустимые параметры |
| 401 | Неавторизован — отсутствует или недействителен JWT-токен |
| 404 | Не найдено — рабочая книга или рабочий лист не существуют |
| 500 | Ошибка сервера — внутренняя ошибка обработки |

При успешном вызове возвращается JSON-объект, содержащий поля `Code` и `Status`. В случае ошибки в ответе также присутствуют дополнительные поля, например `Message`, и соответствующие HTTP-коды состояния (например, 400, 401, 404, 500).

**Примечания:** Убедитесь, что значение `startrow` находится в пределах допустимого диапазона строк рабочего листа; в противном случае API вернёт ошибку 400. Индексы строк начинаются с нуля, т.е. `startrow=0` соответствует первой строке.

## Семейство облачных SDK

Использование SDK — самый быстрый способ интеграции этой функциональности в ваше приложение. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на бизнес-логике. Полный список облачных SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют скрытие строк с помощью различных SDK. (Имена файлов примеров содержат «Unhide» из-за устаревшего именования; однако внутри каждого примера выполняется операция **Hide**.)

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}