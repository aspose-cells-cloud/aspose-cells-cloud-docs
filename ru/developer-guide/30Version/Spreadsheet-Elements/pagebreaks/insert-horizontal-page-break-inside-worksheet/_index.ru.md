---
title: "Добавление горизонтального разрыва страницы"
second_title: "Документ"
linktype: "Добавление горизонтального разрыва страницы"
type: docs
url: /ru/page-breaks/add-horizontal-page-break/
aliases: [  /ru/insert-horizontal-page-break-inside-worksheet/ ]
keywords: "горизонтальный разрыв страницы, Aspose.Cells Cloud, Excel API, REST, SDK, рабочий лист, cURL"
description: "Узнайте, как добавить горизонтальный разрыв страницы в рабочий лист Excel с помощью REST API Aspose.Cells Cloud. Включает детали запроса, пример cURL и фрагменты кода SDK для нескольких языков программирования."
weight: 30
ArticleTitle: "Добавление горизонтального разрыва страницы – API Aspose.Cells Cloud"
---

**API «Добавление горизонтального разрыва страницы»** вставляет горизонтальный разрыв страницы в рабочий лист Excel.

**Необходимые условия и аутентификация**  
Для всех вызовов API Aspose.Cells Cloud требуется действующий JWT-токен. Получите токен с помощью OAuth 2.0-процесса, описанного в руководстве по аутентификации, и включите его в заголовок запроса как `Authorization: Bearer <jwt token>`. Целевая рабочая книга должна находиться в хранилище, доступном для API (по умолчанию — основное хранилище или пользовательское хранилище с именем `storageName`, которое вы указываете).

## API PutHorizontalPageBreak

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### Параметры запроса

| Имя параметра | Тип    | Расположение | Описание                                                               |
|--------------|--------|-------------|-------------------------------------------------------------------------|
| name         | string | path        | Имя файла Excel.                                                   |
| sheetName    | string | path        | Имя рабочего листа, в который будет добавлен разрыв.                      |
| cellname     | string | query       | Ссылка на ячейку (например, **A1**), обозначающая начало разрыва страницы.    |
| row          | integer| query       | Индекс строки (начиная с 0) для разрыва страницы.                                  |
| column       | integer| query       | Индекс столбца (начиная с 0) для разрыва страницы.                               |
| startColumn  | integer| query       | Начальный столбец диапазона при вставке разрыва.                        |
| endColumn    | integer| query       | Конечный столбец диапазона при вставке разрыва.                          |
| folder       | string | query       | Путь к папке, содержащей файл Excel.                                    |
| storageName  | string | query       | Имя хранилища Aspose Cloud.                                         |

<a href="https://apireference.aspose.cloud/cells/#/PageBreaks/PutHorizontalPageBreak" target="_blank" rel="noopener noreferrer">Спецификация OpenAPI</a> определяет открытый интерфейс, позволяющий выполнять взаимодействие по REST непосредственно из веб-браузера.

Вы можете использовать инструмент командной строки **cURL** для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как вызвать API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
# Используйте HTTPS для обеспечения зашифрованной передачи данных
curl -v "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/horizontalpagebreaks?row=18" \
  -X PUT \
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

Пример ответа об ошибке при отсутствии или недействительности JWT-токена:

```json
{
  "Code": 401,
  "Status": "Unauthorized",
  "Message": "Недействительный или отсутствующий JWT-токен."
}
```

**Коды HTTP-статуса**

| Код | Значение                     | Описание                                      |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK                          | Фильтр успешно применён; в ответе содержатся детали операции. |
| 400 | Bad Request                 | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized                | Недействительный или отсутствующий JWT-токен. |
| 413 | Payload Too Large           | Загруженный файл превышает ограничение по размеру. |
| 500 | Internal Server Error       | Непредвиденная ошибка сервера. |

Дополнительные сведения о связанных операциях см. на страницах API **[Получение горизонтальных разрывов страницы](../get-horizontal-page-breaks/)** и **[Удаление горизонтального разрыва страницы](../delete-horizontal-page-break/)**.

## Семейство облачных SDK

Использование SDK — самый быстрый способ разработки. SDK скрывает детали низкоуровневой реализации, позволяя сосредоточиться на вашем проекте. Полный список SDK Aspose.Cells Cloud см. в <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">репозитории на GitHub</a>.

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutHorizontalPageBreak.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutHorizontalPageBreak.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutHorizontalPageBreak.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutHorizontalPageBreak.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutHorizontalPageBreak.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutHorizontalPageBreak.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutHorizontalPageBreak.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutHorizontalPageBreak.go" >}}
{{< /tab >}}

{{< /tabs >}}