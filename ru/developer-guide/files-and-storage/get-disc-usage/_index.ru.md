---
title: "Aspose.Cells Cloud API — Получение данных об использовании диска | Метрики хранилища в реальном времени"
second_title: "Документ"
ArticleTitle: "Решение для управления файлами Excel в облаке — интерфейс для быстрого получения данных об использовании диска в облаке."
linktype: "Получение данных об использовании диска"
type: docs
url: /ru/get-disk-usage/
keywords: "Aspose Cells, Cloud API, Использование диска, Метрики хранилища, Excel, REST"
description: "Получите данные об использовании диска в реальном времени для Aspose.Cells Cloud. Ознакомьтесь с конечной точкой GET /v4.0/cells/storage/disk, необходимой аутентификацией и примером ответа."
weight: 100
---

Операция **Получение данных об использовании диска** возвращает метрики хранилища в реальном времени для вашей учетной записи Aspose.Cells Cloud. Используйте эту конечную точку для мониторинга занятого и общего объема дискового пространства.

- Получает текущие данные об использовании диска для Excel API в среде Aspose Cloud.
- Позволяет разработчикам отслеживать, сколько хранилища было использовано их приложениями.
- Обеспечивает проактивное управление лимитами хранилища и контроль затрат.

## Excel API: GetDiskUsage

### Web API

```http
GET https://api.aspose.cloud/v4.0/cells/storage/disk
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе токена JWT</a>.

### Параметры запроса

| Имя параметра | Тип   | Расположение | Описание                                                   | Обязательный |
| -------------- | ------ | ------------ | ---------------------------------------------------------- | ------------ |
| storageName    | String | Query        | Имя хранилища, для которого нужно получить данные об использовании. | Необязательный |

### **Ответ**

```json
{
  "Name": "DiskUsage",
  "Description": ["Класс для информации об использовании дискового пространства."],
  "Type": "Класс",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "UsedSize",
      "Description": ["Объем дискового пространства, занятого приложением."],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Long",
        "Name": "long"
      }
    },
    {
      "Name": "TotalSize",
      "Description": ["Общий доступный объем дискового пространства."],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Long",
        "Name": "long"
      }
    }
  ]
}
```

**Коды HTTP-статуса**

| Код | Значение               | Описание                                                                 |
| ---- | --------------------- | ------------------------------------------------------------------------ |
| 200  | OK (ОК)               | Фильтр применен успешно; ответ содержит детали операции.                |
| 400  | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized (Неавторизовано) | Недействительный или отсутствующий токен JWT.                            |
| 413  | Payload Too Large (Слишком большой полезный载荷) | Загруженный файл превышает лимит размера.                             |
| 500  | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                                          |

## Спецификация OpenAPI

[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/StorageController/GetDiskUsage) определяет публично доступное программное интерфейсное решение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как выполнять вызовы в Cloud API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/disk?storageName=MyStorage" \
     -H "Authorization: Bearer ВАШ_ТОКЕН_ДОСТУПА"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "UsedSize": 12345678,
  "TotalSize": 10737418240
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя вам сосредоточиться на задачах вашего проекта. Полный список SDK Aspose.Cells Cloud представлен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют, как выполнять вызовы в веб-сервисы Aspose.Cells с использованием различных SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetDiskUsage.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetDiskUsage.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetDiskUsage.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetDiskUsage.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetDiskUsage.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetDiskUsage.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetDiskUsage.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetDiskUsage.go" >}}
{{</tab>}}
{{< /tabs >}}