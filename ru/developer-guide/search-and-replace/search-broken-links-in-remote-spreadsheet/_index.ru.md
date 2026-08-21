---
title: "Aspose.Cells Cloud – API обнаружения битых ссылок в Excel – сканирование и проверка ссылок в удалённых книгах"
second_title: "Документ"
ArticleTitle: "Поиск и исправление битых ссылок в удалённых файлах Excel – облачный проверщик ссылок"
linktype: "Search Remote Spreadsheets Broken Links"
type: docs
url: /ru/search-broken-links-in-remote-spreadsheet/
keywords: "Excel, битые ссылки, API, облачные технологии, электронная таблица, валидация, Aspose.Cells"
description: "Используйте API Aspose.Cells Cloud для сканирования удалённых книг Excel на наличие битых внешних ссылок, некорректных формул и отсутствующих источников данных."
weight: 100
---

## **Поиск битых ссылок в удалённой электронной таблице через API**

Автоматически обнаруживайте битые ссылки в файлах Excel, хранящихся в облачном хранилище. Наш API сканирует указанные диапазоны на наличие битых внешних ссылок, некорректных формул и отсутствующих источников данных. Поддерживает аудит удалённых электронных таблиц, автоматическую проверку качества и интеграцию с поставщиками облачных хранилищ. Используйте RESTful API для автоматизации корпоративных рабочих процессов.

### **Веб-API**

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/search/broken-links
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Параметры запроса:**

| Имя параметра | Тип    | Путь / Строка запроса / HTTPBody | Описание                                                                                                                                               |
| :------------ | :----- | :----------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------- |
| name          | String | Path                           | **Обязательный.** Имя файла книги Excel, подлежащего сканированию на битые ссылки (например, `Quarterly_Report.xlsx`).                                |
| worksheet     | String | Query                          | **Обязательный.** Имя листа, в котором будет выполняться операция поиска. Укажите точное имя листа, как оно отображается в книге.                      |
| cellArea      | String | Query                          | **Обязательный.** Диапазон ячеек, подлежащий анализу на битые ссылки, в нотации A1 (например, `C5:J50`). API ищет только в пределах этого диапазона.  |
| folder        | String | Query                          | **Необязательный.** Путь к каталогу, содержащему книгу в вашем облачном хранилище. Если не указан, считается корневой каталог.                         |
| storageName   | String | Query                          | **Необязательный.** Имя пользовательской конфигурации облачного хранилища. Если не указано, используется хранилище по умолчанию.                      |
| region        | String | Query                          | **Необязательный.** Языковой стандарт, применяемый при обработке (например, `ru-RU`). Может повлиять на интерпретацию синтаксиса формул или ссылок.  |
| password      | String | Query                          | **Необязательный.** Пароль, необходимый для открытия зашифрованной электронной таблицы. Пропустите, если файл не защищён паролем.                      |

**Пример запроса cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/Quarterly_Report.xlsx/search/broken-links?worksheet=Sheet1&cellArea=C5:J50" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

### **Ответ**

```json
{
  "Name": "BrokenLinksResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "Properties": [
    {
      "Name": "BrokenLinks",
      "DataType": {
        "Identifier": "Container",
        "Reference": "BrokenLink",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "BrokenLink"
        }
      }
    },
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer"
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String"
      }
    }
  ]
}
```

**Пример JSON-ответа**

```json
{
  "BrokenLinks": [
    {
      "Worksheet": "Sheet1",
      "CellName": "D12",
      "Link": "https://example.com/data/source.xlsx",
      "IsValid": false,
      "ErrorMessage": "Файл не найден"
    },
    {
      "Worksheet": "Sheet1",
      "CellName": "F30",
      "Link": "C:\\LocalFolder\\data.xlsx",
      "IsValid": false,
      "ErrorMessage": "Внешняя ссылка не поддерживается в облачном режиме"
    }
  ],
  "Code": 200,
  "Status": "OK"
}
```

### Коды ошибок

- **400 Bad Request** – Неверный URI API Aspose.Cells Cloud.  
- **401 Unauthorized** – Неверный токен доступа, client ID или client secret.  
- **404 Not Found** – Файл электронной таблицы недоступен.  
- **500 Server Error** – Возникла ошибка при получении данных для расчёта.

## Где следует использовать поиск битых ссылок в API электронной таблицы?

- **Регулярный аудит крупных финансовых моделей** – Перед публикацией ежемесячных или квартальных отчётов автоматически сканируйте ключевые расчётные области (например, `Dashboard!B5:K50`), содержащие множество внешних ссылок на данные, чтобы убедиться, что все ссылки указывают на существующие файлы-источники.  
- **Интеграция данных при слияниях и поглощениях** – После объединения нескольких электронных таблиц, представляющих бизнес-подразделения, проверьте лист «Обзор» на наличие ссылок, ставших недействительными из-за изменения путей к файлам или проблем с правами доступа.  
- **Подготовка пакетов данных для инвесторов** – Перед финализацией презентационных материалов, содержащих диаграммы и таблицы, связанные с внешними базами данных или источниками рыночных данных, проверьте корректность всех ссылок.

## Почему стоит использовать поиск битых ссылок в API электронной таблицы?

- **Разработческая простота** – Aspose.Cells Cloud предоставляет SDK на множестве языков программирования, что позволяет быстро разрабатывать решения при полной документации. По сравнению с созданием собственного решения это значительно сокращает трудозатраты.  
- **Снижение трудозатрат** – Автоматизирует проверку ссылок, исключая необходимость в выделенных сотрудниках для ручной сверки документов.  
- **Оплата по факту использования** – Нет необходимости в стартовых инвестициях; вы платите только за фактически выполненные вызовы API.  
- **Отсутствие затрат на обслуживание** – Нет серверов для поддержки, обновлений ПО и проблем совместимости.

## Как использовать поиск битых ссылок в API электронной таблицы с SDK

### Спецификация OpenAPI

[Спецификация OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchBrokenLinksInRemoteSpreadsheet) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

### Использование SDK Aspose.Cells Cloud

Использование SDK — самый эффективный способ ускорить разработку. SDK абстрагирует детали HTTP-взаимодействия, позволяя реализовать обнаружение битых ссылок с минимальным объёмом кода. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют взаимодействие с веб-сервисами Aspose.Cells Cloud с использованием различных SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteSpreadsheet.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteSpreadsheet.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteSpreadsheet.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteSpreadsheet.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteSpreadsheet.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteSpreadsheet.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteSpreadsheet.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteSpreadsheet.go" >}}  
{{</tab>}}  
{{< /tabs >}}