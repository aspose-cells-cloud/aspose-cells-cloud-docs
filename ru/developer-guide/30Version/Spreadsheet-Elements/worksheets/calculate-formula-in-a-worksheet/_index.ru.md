---
title: "Вычисление формулы на листе Excel"
second_title: "Документ"
linktype: "Вычисление"
type: docs
url: /worksheets/calculate-formula/
aliases: [/calculate-formula-in-a-worksheet/]
keywords: "Aspose.Cells Cloud, Excel, вычисление формулы, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, Swift"
description: "Вычисление формул на листе Excel с использованием REST API Aspose.Cells Cloud. Поддержка множества SDK (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, Swift) с готовыми примерами."
weight: 20
ArticleTitle: "Вычисление формулы на листе Excel – Документация Aspose.Cells Cloud"
---

Этот REST API возвращает **вычисленное значение формулы** на листе. Его можно использовать для **оценки формулы Excel** непосредственно из вашего приложения.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/formulaResult
```

### **Параметры запроса**

| Имя параметра | Тип   | Расположение | Описание                                          |
|---------------|-------|--------------|---------------------------------------------------|
| name          | string | path         | Имя файла Excel.                                  |
| sheetName     | string | path         | Имя листа, содержащего формулу.                   |
| formula       | string | query        | Формула для вычисления (например, `SUM(A5:A10)`). |
| folder        | string | query        | Папка, в которой хранится документ.               |
| storageName   | string | query        | Имя сервиса хранения (если применимо).             |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetCalculateFormula) определяет публично доступное программное интерфейсное решение и позволяет выполнять взаимодействие REST непосредственно из веб-браузера.

### Аутентификация

Все запросы должны содержать действительный **Bearer JWT-токен** в заголовке `Authorization`:

```
Authorization: Bearer <your_jwt_token>
```

Получить токен можно, следуя описанному в руководстве по аутентификации Aspose.Cells Cloud процессу OAuth 2.0.

### Возможные коды ответа

| Код | Описание                                                     |
|-----|--------------------------------------------------------------|
| 200 | Запрос выполнен успешно; возвращено значение формулы.        |
| 400 | Неверный запрос — отсутствуют или некорректны параметры.     |
| 401 | Ошибка авторизации — недействительный или отсутствующий JWT. |
| 404 | Не найдено — указанный файл или лист не существуют.          |
| 500 | Внутренняя ошибка сервера — неожиданное состояние сервера.   |

Для удобного вызова веб-сервисов Aspose.Cells Cloud можно использовать утилиту командной строки **cURL**. Пример ниже демонстрирует запрос на получение результата формулы с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet2/formulaResult?formula=SUM(A5:A10)" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Value": {
    "Value": "0"
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

Использование SDK — самый быстрый способ интеграции API. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на бизнес-логике. Полный список SDK Aspose.Cells Cloud см. в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Приведённые ниже примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "d1a2b3c4e5f67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "a1b2c3d4e5f67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "b1c2d3e4f5g67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "c1d2e3f4g5h67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "d1e2f3g4h5i67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e1f2g3h4i5j67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f1g2h3i4j5k67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "g1h2i3j4k5l67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.go" >}}

{{< /tab >}}

{{< /tabs >}}

---

**См. также:**  
- [Получение листа](https://docs.aspose.cloud/cells/worksheets/get-worksheet/)  
- [Обновление листа](https://docs.aspose.cloud/cells/worksheets/update-worksheet/)  
- [Вычисление всех формул](https://docs.aspose.cloud/cells/worksheets/calculate-all-formulas/)  
---