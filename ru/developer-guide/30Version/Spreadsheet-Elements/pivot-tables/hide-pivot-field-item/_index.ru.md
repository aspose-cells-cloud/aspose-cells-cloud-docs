---
title: "Скрытие элемента поля сводной таблицы"
second_title: "Document"
linktype: Hide
type: docs
url: /pivot-tables/hide-pivot-field-item/
aliases: [/hide-pivot-field-item/]
keywords: "Aspose.Cells, скрыть элемент поля сводной таблицы, PivotTable API, REST API, облачный SDK"
description: "Узнайте, как скрыть элемент поля сводной таблицы с помощью Aspose.Cells Cloud REST API. Включает подробности запроса, пример cURL и фрагменты кода SDK для множества языков."
weight: 110
ArticleTitle: "Скрытие элемента поля сводной таблицы — руководство по Aspose.Cells Cloud API"
---

Перед вызовом API убедитесь, что у вас есть:

* Действительный **JWT-токен доступа** (получаемый через аутентификационный поток Aspose Cloud).  
* Целевая рабочая книга загружена в ваше облачное хранилище Aspose Cloud.  
* Рабочий лист и сводная таблица уже созданы.

Эти предварительные условия помогают избежать ошибок аутентификации и ответов «ресурс не найден». Далее приведены необходимые шаги по настройке перед вызовом API.

Этот REST API скрывает элемент поля сводной таблицы.

## API PostPivotTableFieldHideItem

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotField/Hide
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### **Параметры запроса**

| Имя параметра   | Тип     | Местоположение | Описание                                                                                         |
| --------------- | ------- | -------------- | ------------------------------------------------------------------------------------------------ |
| name            | string  | path           | Имя файла Excel.                                                                                |
| sheetName       | string  | path           | Рабочий лист, содержащий сводную таблицу.                                                       |
| pivotTableIndex | integer | path           | Индекс сводной таблицы внутри рабочего листа.                                                   |
| pivotFieldType  | string  | query          | Тип поля сводной таблицы (Строка, Столбец, Страница, Данные и т.д.).                            |
| fieldIndex      | integer | query          | Индекс поля сводной таблицы (начиная с 0), которое нужно изменить.                              |
| itemIndex       | integer | query          | Индекс конкретного элемента в поле, который нужно скрыть.                                       |
| isHide          | boolean | query          | Установите значение **true**, чтобы скрыть элемент; **false**, чтобы показать его.              |
| needReCalculate | boolean | query          | Указывает, следует ли пересчитать сводную таблицу после изменения. По умолчанию **false**.     |
| folder          | string  | query          | Путь к папке, где хранится рабочая книга.                                                       |
| storageName     | string  | query          | Имя сервиса хранилища.                                                                           |

**Краткая справка по обязательным параметрам запроса**

- **pivotFieldType** – тип поля (например, `Row`).  
- **fieldIndex** – индекс поля (начиная с 0), который нужно изменить.  
- **itemIndex** – индекс элемента (начиная с 0), который нужно скрыть/показать.  
- **isHide** – `true`, чтобы скрыть, `false`, чтобы показать.  
- **needReCalculate** – необязательный, по умолчанию `false`.

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableFieldHideItem) определяет общедоступное программное интерфейсное взаимодействие и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Ниже приведён пример вызова API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/pivottables/0/PivotField/Hide?pivotFieldType=Row&fieldIndex=0&itemIndex=1&isHide=true&needReCalculate=true" \
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

**Детали ответа**

| Код состояния | Описание                                                             |
| ------------- | -------------------------------------------------------------------- |
| 200           | Элемент успешно скрыт.                                               |
| 400           | Неверный запрос — отсутствующие или некорректные параметры.         |
| 401           | Неавторизован — недействительный или отсутствующий JWT-токен.      |
| 500           | Ошибка сервера — операция не может быть завершена.                  |

**Примечание:** Если указанные `fieldIndex` или `itemIndex` выходят за допустимые пределы, API возвращает ответ **400 Bad Request**.

## Семейство облачных SDK

Использование SDK — самый быстрый способ разработки под API. SDK берут на себя работу с низкоуровневыми деталями, позволяя сосредоточиться на бизнес-логике. Полный список облачных SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Приведённые ниже примеры кода демонстрируют, как скрыть элемент поля сводной таблицы с использованием различных SDK.

{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

```csharp
public void Run_PivotTable_NeedReCalculate()
{
    // Подготовка рабочей книги и рабочего листа
    url = @"https://api.aspose.cloud/v3.0/storage/file/Temp/V17.02.00_01.xlsx";
    using (HttpWebResponse response = _helper.CallDelete(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Загрузка рабочей книги
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Создание рабочего листа, содержащего сводную таблицу
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Создание второго рабочего листа с примерами данных
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/Sheet2?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Импорт примеров данных в Sheet2
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/importdata?folder=Temp";
    data = "{ \"BatchData\":[{...}] }"; // Сокращено для краткости
    using (HttpWebResponse response = _helper.CallPost(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Добавление сводной таблицы в PivotSheet
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables?folder=Temp";
    data = "{\"Name\":\"TestPivot\",\"SourceData\":\"=Sheet2!A1:E8\",\"DestCellName\":\"C1\",\"UseSameSource\":true,\"PivotFieldRows\":[0,1],\"PivotFieldColumns\":[2],\"PivotFieldData\":[3,4]}";
    using (HttpWebResponse response = _helper.CallPut(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Скрытие определённого элемента поля строк
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/PivotField/Hide?pivotFieldType=Row&fieldIndex=0&itemIndex=1&isHide=true&needReCalculate=true&folder=Temp";
    using (HttpWebResponse response = _helper.CallPost(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "a0bec26a8274b9f7cb514015843a214e" >}}

{{< /tab >}}

{{< /tabs >}}

**Примечание:** Примеры SDK предполагают, что аутентификация (JWT-токен) уже настроена и рабочая книга находится в указанной папке хранилища. При необходимости скорректируйте параметры `folder` и `storageName` в соответствии с вашей средой.