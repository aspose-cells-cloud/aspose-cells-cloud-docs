---
title: "Вычисление формулы ячейки – Aspose.Cells Cloud API"
type: docs
url: /calculate-cells-formula/
weight: 90
keywords: "Aspose.Cells Cloud, вычисление формулы ячейки, Excel API, REST API, SDK"
description: "Вычислите формулу ячейки Excel через REST API Aspose.Cells Cloud (v3.0). Включает endpoint, параметры, пример cURL и фрагменты SDK."
ArticleTitle: "Вычисление формулы ячейки – Документация Aspose.Cells Cloud API"
---

## REST API

Этот REST API вычисляет **формулу ячейки** в книге Excel.

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/calculate
```

## Безопасность и аутентификация

API Aspose.Cells Cloud являются безопасными и требуют [аутентификацию на основе токена JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Параметры запроса

| Имя параметра | Тип    | Расположение параметра (path/query/body) | Описание                                                           |
|---------------|--------|------------------------------------------|--------------------------------------------------------------------|
| name          | string | path                                     | Имя файла Excel (например, `Book1.xlsx`).                          |
| sheetName     | string | path                                     | Имя рабочего листа, содержащего ячейку.                            |
| cellName      | string | path                                     | Адрес ячейки, подлежащей вычислению (например, `A1`).              |
| options       | object | body                                     | JSON-объект с параметрами вычисления (см. таблицу **Объект options**). |
| folder        | string | query                                    | Папка в хранилище, где расположен файл.                            |
| storageName   | string | query                                    | Имя хранилища Aspose Cloud.                                        |

#### Объект options

| Поле            | Тип     | Описание                                                                              | Значение по умолчанию |
|-----------------|---------|---------------------------------------------------------------------------------------|-----------------------|
| CalcStackSize   | string  | Максимальный размер стека вычислений.                                                 | `"1"`                 |
| IgnoreError     | boolean | Если `true`, ошибки вычислений игнорируются, а значение ячейки устанавливается в `#N/A`. | `false`               |
| Recursive       | boolean | Включает рекурсивное вычисление зависимых ячеек.                                      | `false`               |
| Precision       | string  | Количество десятичных знаков для числовых результатов.                                | `"15"`                |
| UseThreading    | boolean | Включает многопоточное вычисление.                                                    | `false`               |

### **Ответ**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Коды HTTP-статуса**

| Код | Значение                      | Описание                                                                 |
|-----|-------------------------------|--------------------------------------------------------------------------|
| 200 | OK                            | Фильтр применён успешно; ответ содержит детали операции.                 |
| 400 | Bad Request                   | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized                  | Недействительный или отсутствующий токен JWT.                            |
| 413 | Payload Too Large             | Загруженный файл превышает лимит размера.                                |
| 500 | Internal Server Error         | Непредвиденная ошибка сервера.                                           |

## Как использовать API PostCellCalculate с SDK

### Спецификация API PostCellCalculate

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostCellCalculate) определяет публично доступное программное интерфейсное решение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Следующий пример показывает, как вызвать облачный API с помощью cURL. **Сначала получите токен JWT**, пройдя аутентификацию через endpoint `/connect/token`, и замените `<jwt token>` на значение полученного токена.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/A1/calculate" \
  -d '{"CalcStackSize":"1"}' \
  -X POST \
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

### Использование SDK Aspose.Cells Cloud

Использование SDK — это лучший способ ускорить разработку. SDK абстрагирует низкоуровневые детали и позволяет сосредоточиться на задачах вашего проекта. Пожалуйста, ознакомьтесь с <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">репозиторием на GitHub</a> для получения полного списка SDK Aspose.Cells Cloud.

Приведённые ниже примеры кода демонстрируют, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCellCalculate.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCellCalculate.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCellCalculate.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCellCalculate.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCellCalculate.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCellCalculate.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCellCalculate.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCellCalculate.go" >}}

{{< /tab >}}

{{< /tabs >}}
---