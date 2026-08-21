---
title: "Оценка Aspose.Cells Cloud"
second_title: "Документ"
ArticleTitle: "Оценка Aspose.Cells Cloud"
LinkTitle: "Оценка"
type: docs
url: /evaluate-aspose-cells/
description: "Изучите Aspose.Cells Cloud — REST API для создания, преобразования, объединения, разделения, защиты и обработки файлов Excel и других форматов электронных таблиц."
weight: 60
keywords:
  - Aspose.Cells Cloud
  - Excel API
  - REST API
  - обработка электронных таблиц
  - бесплатная пробная версия
  - оценка
---

Вы можете оценить REST API **Aspose.Cells Cloud**, создав бесплатную пробную учетную запись на панели управления Aspose Cloud. После регистрации вы получите **Client Id** и **Client Secret**, которые позволяют выполнять до 150 вызовов API в месяц.

**Необходимые условия**  
Прежде чем начать, убедитесь, что у вас есть активное интернет-соединение и поддерживаемая среда разработки. API можно вызывать напрямую через HTTP или использовать один из SDK Aspose.Cells (например, для .NET, Java, Python, PHP) для упрощения интеграции.

**Быстрый старт**

1. **Создайте бесплатную пробную учетную запись** — перейдите на [панель управления Aspose Cloud](https://dashboard.aspose.cloud), зарегистрируйтесь и подтвердите свой адрес электронной почты.  
2. **Получите учетные данные** — найдите *Client Id* и *Client Secret* в разделе **Authentication** (Аутентификация) на панели управления.  
3. **Сгенерируйте токен доступа** — отправьте `POST`-запрос на `https://api.aspose.cloud/connect/token` со своими учетными данными (точный формат запроса см. в справочнике по API).  
4. **Выполните первый вызов API** — включите токен в заголовке `Authorization: Bearer <token>` и вызовите простой endpoint, например, `GET https://api.aspose.cloud/v3.0/cells/{file}/worksheets`.  

Бесплатная пробная версия дает практическое представление о возможностх сервиса и позволяет начать разработку и тестирование без каких-либо затрат.

**Краткое описание API**

| Операция | Метод | URL | Обязательные параметры | Пример ответа |
|----------|-------|-----|------------------------|---------------|
| Получить токен доступа | POST | `https://api.aspose.cloud/connect/token` | `grant_type=client_credentials`, `client_id`, `client_secret` (в формате form-urlencoded) | `{ "access_token": "eyJ0eXAi...", "expires_in": 3600 }` |
| Список листов | GET | `https://api.aspose.cloud/v3.0/cells/{file}/worksheets` | Путь: `{file}` — имя загруженной рабочей книги; Заголовок: `Authorization: Bearer <token>` | `{ "Worksheets": { "WorksheetList": [ { "Name": "Sheet1" }, { "Name": "Sheet2" } ] } }` |

Для получения подробной информации о тарифах, ограничениях использования и дополнительных планах см. страницу [Trial Plan](https://purchase.aspose.cloud/trial).