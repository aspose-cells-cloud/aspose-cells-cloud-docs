---
title: "Установка стиля диапазона – Aspose.Cells Cloud API"
second_title: "Документация"
linktitle: "Установка стиля диапазона"
type: docs
url: /ranges/update/style/
aliases: [/set-the-style-of-the-range/]
keywords: "Aspose.Cells, стиль диапазона, API, Excel, облако"
description: "Узнайте, как установить стиль диапазона ячеек в листе Excel с помощью REST API Aspose.Cells Cloud. Включает шаги аутентификации, формат запроса, детали ответа и примеры SDK для .NET, Java, Python, Go и других языков."
weight: 70
---  

## **Введение**  
В этом примере показано, как установить стиль диапазона с помощью API Aspose.Cells Cloud. Вы можете вызывать API из множества языков программирования, таких как .NET, Java, PHP, Ruby, Python, JavaScript (jQuery) и других.  

## **Сведения об API**  

| API                                                   | Тип | Описание                                     | Ссылка на ресурс                                                                                                                                 |
| ----------------------------------------------------- | --- | -------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| /cells/{name}/worksheets/{sheetName}/ranges/style     | POST | Установка стиля ячеек именованного диапазона | [PostWorksheetCellsRangeStyle](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeStyle) |

### **Пример на cURL**  

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

**Необходимые условия**  
1. Получите токен доступа с помощью потока клиентских учетных данных OAuth2 (`POST https://api.aspose.cloud/connect/token`).  
2. Включайте заголовок `Authorization: Bearer <access_token>` в каждый запрос.  

**Запрос**  

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/style" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{
           "Range": {
               "FirstRow": 1,
               "FirstColumn": 1,
               "RowCount": 2,
               "ColumnCount": 2,
               "Worksheet": "Sheet1"
           },
           "Style": {
               "Font": {
                   "IsBold": true,
                   "IsItalic": true,
                   "IsStrikeout": true,
                   "IsSubscript": true,
                   "IsSuperscript": true,
                   "DoubleSize": 1
               }
           }
         }'
```

*Объект `Range` задаёт левую верхнюю ячейку и размер диапазона. Объект `Style` содержит параметры форматирования, которые необходимо применить.*  

{{< /tab >}}

{{< tab tabNum="2" >}}

**Ответ**  

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Обработка ошибок** – В случае неуспешных вызовов API возвращает соответствующий HTTP-статус (например, 400, 401, 500) и JSON-тело, содержащее поля `Error` и `Message`. Проверяйте значение поля `Code`; любой результат, отличный от 200, следует записывать в лог и обрабатывать в соответствии с вашей политикой обработки ошибок.  

{{< /tab >}}

{{< /tabs >}}

## **Исходный код SDK**  
SDK для Aspose.Cells Cloud можно загрузить со следующей страницы: [Доступные SDK](/cells/available-sdks/)

### **Примеры SDK**  
{{< tabs tabTotal="4" tabID="4" tabName1="PHP" tabName2="Ruby" tabName3="Objective C" tabName4="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "81d7e60eaf43ae7192df00993997afde" >}}

{{< /tab >}}

{{< /tabs >}}