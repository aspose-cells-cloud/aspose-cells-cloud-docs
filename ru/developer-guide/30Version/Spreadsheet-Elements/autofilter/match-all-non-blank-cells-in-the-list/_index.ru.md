---
title: "Сопоставление всех непустых ячеек в рабочем листе Excel"
second_title: "Документ"
linktype: "docs"
url: /ru/autofilter/match-all-non-blank/
aliases: [  /ru/match-all-non-blank-cells-in-the-list/ ]
keywords: "Aspose.Cells Cloud, сопоставление непустых ячеек, автофильтр, Excel API"
description: "Узнайте, как использовать REST API Aspose.Cells Cloud для сопоставления всех непустых ячеек в списке автофильтра на рабочем листе Excel. Включает endpoint, параметры, аутентификацию, схему ответа, коды ошибок и примеры SDK."
ArticleTitle: "Сопоставление всех непустых ячеек в рабочем листе Excel с помощью API Aspose.Cells Cloud"
weight: 100
---

**Обзор**  
Операция *Сопоставление всех непустых ячеек* применяет автофильтр к рабочему листу и возвращает только те строки, в указанным столбце которых содержатся данные, игнорируя пустые ячейки. Это полезно для очистки наборов данных, генерации отчетов или подготовки данных к дальнейшему анализу.

**Необходимые условия**  
- Действующий JWT-токен для аутентификации в Aspose.Cells Cloud.  
- Книга должна быть загружена в облачное хранилище Aspose.  
- Требуется имя файла, имя рабочего листа и индекс столбца (с нулевым основанием — `fieldIndex`), к которому применяется фильтр.

Этот REST API сопоставляет все непустые ячейки в списке автофильтра на рабочем листе Excel.

## API PostWorksheetMatchNonBlanks

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/matchNonBlanks
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### Параметры запроса

| Имя параметра | Тип    | Расположение | Описание                                                    |
| -------------- | ------- | -------- | -------------------------------------------------------------- |
| name           | string  | path     | Имя файла Excel.                                    |
| sheetName      | string  | path     | Имя рабочего листа, содержащего автофильтр.        |
| fieldIndex     | integer | query    | Индекс столбца (с нулевым основанием), к которому применяется фильтр. |
| folder         | string  | query    | _(Опционально)_ Путь к папке, где хранится файл.             |
| storageName    | string  | query    | _(Опционально)_ Имя используемого сервиса хранилища.               |

### **Ответ**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Коды HTTP-статуса**

| Код | Значение                     | Описание                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK (ОК)                          | Фильтр успешно применён; ответ содержит детали операции. |
| 400  | Bad Request (Неверный запрос)                 | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized (Неавторизован)                | Неверный или отсутствующий JWT-токен. |
| 413  | Payload Too Large (Слишком большой полезный груз)           | Загруженный файл превышает лимит размера. |
| 500  | Internal Server Error (Внутренняя ошибка сервера)       | Непредвиденная ошибка сервера. |

*Пример ответа об ошибке (400)*  

```json
{
  "Code": 400,
  "Message": "Неверный параметр: fieldIndex должен быть неотрицательным целым числом."
}
```

## Как использовать API PostWorksheetMatchNonBlanks с SDK

### Спецификация API PostWorksheetMatchNonBlanks

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PostWorksheetMatchNonBlanks) определяет общедоступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Пример ниже демонстрирует, как выполнять вызовы в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/matchNonBlanks?fieldIndex=0" \
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

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже показывают, как выполнять вызовы в веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMatchNonBlanks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMatchNonBlanks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMatchNonBlanks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMatchNonBlanks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMatchNonBlanks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMatchNonBlanks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMatchNonBlanks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMatchNonBlanks.go" >}}

{{< /tab >}}

{{< /tabs >}}