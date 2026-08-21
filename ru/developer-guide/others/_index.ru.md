---
title: "Aspose.Cells Cloud Web API – Другие функции: Проверка работоспособности, Получение открытого ключа"
linktitle: "Другие функции"
ArticleTitle: "Другие функции: Проверка работоспособности, Получение открытого ключа"
second_title: "Документ"
type: docs
url: /ru/other-features/
keywords: "Aspose.Cells, облачный API, проверка работоспособности, открытый ключ, токен доступа, Excel, REST"
description: "Изучите другие функции Aspose.Cells Cloud: конечную точку проверки работоспособности сервиса, получение открытого ключа и генерацию токенов для обеспечения безопасности интеграции с Excel API."
weight: 180
---

**Необходимые условия** — Для использования функций, перечисленных ниже, необходимо иметь действующую подписку Aspose Cloud и активную пару **Client ID** / **Client Secret** для аутентификации.

Эти «другие функции» обеспечивают вспомогательные операции для Aspose.Cells Cloud API, такие как подтверждение доступности сервиса, получение криптографических ключей и получение токенов доступа. Как правило, они вызываются перед работой с конечными точками, связанными с рабочими книгами.

- **[Проверка работоспособности сервиса Aspose.Cells Cloud](https://docs.aspose.cloud/cells/check-cloud-service-health/)**  
  Проверьте, что сервис Aspose.Cells Cloud доступен и работает корректно. При успешном вызове возвращается **HTTP 200** с JSON `{ "status": "OK" }`. Используйте эту конечную точку на раннем этапе вашего рабочего процесса, чтобы избежать ненужных ошибок.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/check-cloud-service-health/">Подробнее</a>

- **[Получение текущего состояния работы Aspose.Cells Cloud](https://docs.aspose.cloud/cells/get-aspose-cells-cloud-status/)**  
  Получите текущее состояние работы сервиса в режиме реального времени. Ответ указывает, работает ли API в полном объёме, находится ли он в режиме технического обслуживания или испытывает проблемы.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/get-aspose-cells-cloud-status/">Подробнее</a>

- **[Получение открытого ключа](https://docs.aspose.cloud/cells/get-public-key/)**  
  Получите открытый ключ RSA (в формате PEM), используемый для проверки подписи токенов JWT, выдаваемых Aspose.Cells Cloud. Этот ключ необходим при валидации токенов на стороне вашего сервера.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/get-public-key/">Подробнее</a>

- **[Получение токена доступа с использованием Client ID и Client Secret](https://docs.aspose.cloud/cells/post-access-token/)**  
  Сгенерируйте токен доступа OAuth 2.0 с использованием типа предоставления **client_credentials**. Укажите ваши **Client ID** и **Client Secret** в теле запроса; в ответе будут получены `access_token`, `token_type` и `expires_in`. Данный токен должен быть передан в заголовке `Authorization` для всех последующих вызовов API.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/post-access-token/">Подробнее</a>

---