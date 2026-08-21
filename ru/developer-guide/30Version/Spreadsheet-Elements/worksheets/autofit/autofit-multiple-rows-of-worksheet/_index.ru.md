---
title: "Автоподбор высоты нескольких строк в рабочей книге Excel"
second_title: "Документ"
linktitle: "Строки"
type: docs
url: /ru/worksheets/autofit/rows/
aliases: [  /ru/autofit-multiple-rows-of-worksheet/ ]
keywords: "автоподбор строк, Excel, Aspose.Cells Cloud, REST API, рабочая тетрадь, электронная таблица"
description: "Узнайте, как использовать REST API Aspose.Cells Cloud для автоподбора высоты нескольких строк в рабочей книге Excel. Включает синтаксис запроса, параметры, пример cURL, фрагменты кода SDK и обработку ошибок."
weight: 40
ArticleTitle: "Автоподбор высоты нескольких строк в рабочей книге Excel – Документация API Aspose.Cells Cloud"
---

Этот REST API автоматически регулирует высоту строк в рабочей книге Excel.

## Безопасность и аутентификация
API Aspose.Cells Cloud защищены и требуют [аутентификации на основе токена JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitrows
```

### **Параметры запроса**

| Имя параметра         | Тип     | Местоположение | Описание                                                                                                                             | Обязательный |
| --------------------- | ------- | -------------- | ------------------------------------------------------------------------------------------------------------------------------------ | ------------ |
| **name**              | string  | path           | Имя файла Excel.                                                                                                                     | ✔            |
| **sheetName**         | string  | path           | Имя рабочего листа.                                                                                                                  | ✔            |
| **autoFitterOptions** | object  | body           | Параметры, управляющие тем, как выполняется автоподбор строк (например, игнорировать скрытые строки). См. краткое описание полей ниже. | ✖            |
| **startRow**          | integer | query          | Номер первой строки для автоподбора (индексация с 1).                                                                                | ✔            |
| **endRow**            | integer | query          | Номер последней строки для автоподбора (включительно).                                                                              | ✔            |
| **onlyAuto**          | boolean | query          | Если `true`, API изменяет только те строки, высота которых автоматически вычисляется в Excel. Если `false`, выполняется полный автоподбор. | ✖            |
| **folder**            | string  | query          | Папка, содержащая документ.                                                                                                          | ✖            |
| **storageName**       | string  | query          | Имя сервиса хранилища.                                                                                                               | ✖            |

Поля **autoFitterOptions** (все необязательны):

- `AutoFitMergedCells` _(boolean)_ – Если `true`, объединённые ячейки учитываются при расчёте высоты строки.
- `IgnoreHidden` _(boolean)_ – Если `true`, скрытые строки игнорируются в процессе автоподбора.
- `OnlyAuto` _(boolean)_ – Отражает значение параметра запроса `onlyAuto`; при установке переопределяет значение параметра запроса.

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetRows) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Следующий пример демонстрирует вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitrows?startRow=1&endRow=7" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells": true, "IgnoreHidden": true, "OnlyAuto": false}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Типичные ответы об ошибках:

- **400 Bad Request** – Некорректные значения параметров или повреждённое тело JSON.
- **401 Unauthorized** – Отсутствует или недействителен токен JWT.
- **404 Not Found** – Указанный файл или рабочий лист не существует.
- **500 Internal Server Error** – Возникла непредвиденная ошибка сервера.

**Коды HTTP-статуса**

| Код  | Значение                    | Описание                                                             |
|------|-----------------------------|----------------------------------------------------------------------|
| 200  | OK                          | Фильтр успешно применён; ответ содержит детали выполнения операции. |
| 400  | Bad Request                 | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized                | Недействителен или отсутствует токен JWT.                            |
| 413  | Payload Too Large           | Загружаемый файл превышает допустимый размер.                        |
| 500  | Internal Server Error       | Непредвиденная ошибка сервера.                                       |

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

Использование SDK — это самый быстрый способ разработки. SDK берёт на себя работу с низкоуровневыми деталями, позволяя вам сосредоточиться на вашем проекте. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}