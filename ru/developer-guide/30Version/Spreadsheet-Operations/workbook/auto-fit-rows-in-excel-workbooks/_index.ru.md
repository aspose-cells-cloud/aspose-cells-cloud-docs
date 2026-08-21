---
title: "Автоматическая подстройка строк в рабочей тетради Excel"
second_title: "Документ"
linktitle: "Строки"
type: docs
url: /ru/autofit-rows-on-an-excel-file/
aliases: [  /ru/auto-fit-rows-in-excel-workbooks/ , /ru/workbook/autofit/rows/ ]
keywords: "автоматическая подстройка строк, рабочая тетрадь Excel, Aspose.Cells Cloud, REST API, параметры автофиттера"
description: "Узнайте, как автоматически изменять высоту строк в рабочей тетради Excel с помощью REST API Aspose.Cells Cloud. Включает endpoint, параметры, пример cURL и фрагменты кода SDK для C#, Java, Python и других языков."
weight: 90
ArticleTitle: "Автоматическая подстройка строк в рабочей тетради Excel – Aspose.Cells Cloud API"
---

**Необходимые условия**  
Перед вызовом API получите действительный токен Bearer JWT из сервиса аутентификации Aspose и убедитесь, что целевая рабочая тетрадь хранится в поддерживаемом хранилище (по умолчанию — в облачном хранилище Aspose или в настроенном вами пользовательском хранилище).

Этот REST API позволяет вам **автоматически подстраивать строки** в рабочей тетради Excel, автоматически изменяя высоту строк после вставки или изменения данных.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/autofitrows
```

Параметры запроса:

| Имя параметра     | Тип               | Расположение | Описание                                                                 |
| ----------------- | ----------------- | ------------ | ------------------------------------------------------------------------ |
| name              | string            | path         | Имя файла рабочей тетради.                                               |
| autoFitterOptions | AutoFitterOptions | body         | Параметры, управляющие поведением автофиттера.                          |
| startRow          | integer           | query        | Индекс первой строки для подстройки.                                     |
| endRow            | integer           | query        | Индекс последней строки для подстройки.                                  |
| firstColumn       | integer           | query        | Индекс первого столбца, учитываемого при подстройке.                     |
| lastColumn        | integer           | query        | Индекс последнего столбца, учитываемого при подстройке.                  |
| onlyAuto          | boolean           | query        | Если **true**, обрабатываются только строки с флагом AutoFit (по умолчанию **false**). |
| folder            | string            | query        | Путь к папке, где хранится рабочая тетрадь.                             |
| storageName       | string            | query        | Имя сервиса хранилища.                                                   |

**AutoFitterOptions** — объект, определяющий поведение операции автофиттирования (например, `AutoFitMergedCells`, `IgnoreHidden`).

**Коды HTTP-статуса**

| Код  | Значение                    | Описание                                                       |
|------|-----------------------------|----------------------------------------------------------------|
| 200  | OK                          | Фильтр применён успешно; ответ содержит детали операции.      |
| 400  | Bad Request                 | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized                | Неверный или отсутствующий JWT-токен.                          |
| 413  | Payload Too Large           | Загруженный файл превышает допустимый размер.                  |
| 500  | Internal Server Error       | Непредвиденная ошибка сервера.                                 |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostAutofitWorkbookRows) предоставляет общедоступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для вызова веб-сервисов Aspose.Cells. Замените `<jwt token>` на действительный токен Bearer JWT, полученный из сервиса аутентификации Aspose.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/autofitrows" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells":true, "IgnoreHidden":true}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*Пример ответа об ошибке (например, отсутствующая рабочая тетрадь):*

```json
{
  "Code": 404,
  "Status": "Not Found",
  "Message": "Указанная рабочая тетрадь 'myWorkbook.xlsx' не существует."
}
```

{{< /tab >}}

{{< /tabs >}}

**Примечания**  
- Если `AutoFitMergedCells` установлено в **true**, объединённые ячейки обрабатываются как единое целое при операции автофиттирования.  
- При установке `IgnoreHidden` в **true** скрытые строки и столбцы пропускаются, сохраняя их текущие размеры.

## Семейство облачных SDK

Использование SDK — самый быстрый способ разработки. SDK скрывает низкоуровневые детали, позволяя сосредоточиться на проекте. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorkbookRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorkbookRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorkbookRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorkbookRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorkbookRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorkbookRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorkbookRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorkbookRows.go" >}}

{{< /tab >}}

{{< /tabs >}}