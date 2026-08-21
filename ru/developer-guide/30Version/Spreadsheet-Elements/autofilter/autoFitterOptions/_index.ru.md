---
title: "AutoFitterOptions — Свойства и руководство по использованию | Aspose.Cells Cloud API"
second_title: "Документ"
linktitle: "AutoFitterOptions"
type: docs
url: /auto-fitter-options/
keywords: "AutoFitterOptions, Aspose.Cells, Автоподбор высоты строк в Excel, высота строк, объединённые ячейки, API"
description: "Узнайте, как управлять автоподбором высоты строк, обработкой объединённых ячеек, скрытыми строками/столбцами, настройками языка и параметрами отображения с помощью объекта AutoFitterOptions в API Aspose.Cells Cloud."
weight: 79
ArticleTitle: "AutoFitterOptions — Руководство по свойствам и использованию для Aspose.Cells Cloud"
---

# Свойства AutoFitterOptions

Объект `AutoFitterOptions` позволяет тонко настраивать автоматический подбор высоты строк, выполняемый сервисом Aspose.Cells Cloud. Это особенно полезно, когда требуется точный контроль над обработкой объединённых ячеек, скрытыми строками/столбцами, форматированием, зависящим от языка, или поведением, специфичным для отображения (рендеринга).

**Необходимые условия** — Для использования этих параметров вы должны быть аутентифицированы с помощью действующего токена доступа OAuth 2.0, включающего область **Cells.ReadWrite**. Запрос будет работать с любой версией SDK, поддерживающей API версии 3.0.

| Имя                        | Тип         | Описание                                                                                              | Примечания                                                                                                          |
| -------------------------- | ----------- | ----------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| **AutoFitMergedCellsType** | **string**  | Определяет, как объединённые ячейки подстраиваются под высоту строки.                                 | Допустимые значения: `All`, `First`, `None`. По умолчанию: `All`. Пример JSON: `"AutoFitMergedCellsType":"All"`      |
| **IgnoreHidden**           | **boolean** | Если **true**, скрытые строки и столбцы игнорируются при автоподборе.                                  | По умолчанию: `false`. Пример JSON: `"IgnoreHidden":false`                                                         |
| **OnlyAuto**               | **boolean** | Указывает, следует ли применять автоподбор только к строкам, высота которых не задана вручную.        | По умолчанию: `false`. Пример JSON: `"OnlyAuto":false`                                                             |
| **DefaultEditLanguage**    | **string**  | Устанавливает язык редактирования по умолчанию для рабочей книги.                                     | По умолчанию: язык системы (например, `"ru-RU"` или `"en-US"`). Пример JSON: `"DefaultEditLanguage":"ru-RU"`        |
| **MaxRowHeight**           | **double**  | Максимальная высота строки (в пунктах), применяемая при автоподборе. Значение **0** означает отсутствие ограничения. | По умолчанию: `0`. Пример JSON: `"MaxRowHeight":0`                                                                  |
| **AutoFitWrappedTextType** | **string**  | Управляет автоподбором перенесённого текста внутри ячеек.                                             | Допустимые значения: `All`, `OnlyWrapped`, `None`. По умолчанию: `All`. Пример JSON: `"AutoFitWrappedTextType":"All"` |
| **FormatStrategy**         | **string**  | Определяет стратегию форматирования, используемую во время операции автоподбора.                     | Типичные значения: `AutoFit`, `PreserveExisting`. По умолчанию: `AutoFit`. Пример JSON: `"FormatStrategy":"AutoFit"` |
| **ForRendering**           | **string**  | Указывает, должен ли выполняться автоподбор с учётом отображения (например, для PDF или изображений). | Допустимые значения: `True`, `False`. По умолчанию: `False`. Пример JSON: `"ForRendering":"False"`                   |

Ниже приведён типичный JSON- payload, который можно отправить в API при настройке `AutoFitterOptions`.

```json
{
  "AutoFitMergedCellsType": "All",
  "IgnoreHidden": false,
  "OnlyAuto": false,
  "DefaultEditLanguage": "ru-RU",
  "MaxRowHeight": 0,
  "AutoFitWrappedTextType": "All",
  "FormatStrategy": "AutoFit",
  "ForRendering": "False"
}
```

Пример запроса `cURL`, применяющего эти параметры к рабочей книге:

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/workbook/autoFitter" \
  -H "Authorization: Bearer {access_token}" \
  -H "Content-Type: application/json" \
  -d @autoFitterOptions.json
```

**Справочник по конечным точкам**

| Метод | URL | Обязательные параметры | Описание |
|-------|-----|------------------------|----------|
| PUT   | `/cells/workbook/autoFitter` | `autoFitterOptions` (JSON-тело) | Применяет указанные `AutoFitterOptions` к целевой рабочей книге. |
| GET   | `/cells/workbook/autoFitter` | *нет* | Получает текущие настройки `AutoFitterOptions` для рабочей книги. |

**Параметры запроса для конечной точки PUT**

| Параметр                 | Тип     | Обязательный | Описание |
|--------------------------|---------|--------------|----------|
| AutoFitMergedCellsType   | string  | Да           | Как объединённые ячейки подстраиваются под высоту строки (`All`, `First`, `None`). |
| IgnoreHidden             | boolean | Нет          | Следует ли игнорировать скрытые строки/столбцы. |
| OnlyAuto                 | boolean | Нет          | Подстраивать только строки без ручной настройки высоты. |
| DefaultEditLanguage      | string  | Нет          | Язык редактирования (например, `ru-RU`). |
| MaxRowHeight             | double  | Нет          | Максимальная высота строки в пунктах; `0` = без ограничений. |
| AutoFitWrappedTextType   | string  | Нет          | Как обрабатывается перенесённый текст (`All`, `OnlyWrapped`, `None`). |
| FormatStrategy           | string  | Нет          | Стратегия форматирования (`AutoFit`, `PreserveExisting`). |
| ForRendering             | string  | Нет          | Применять автоподбор для отображения (`True`, `False`). |

Типичные коды ответов:

- **200 OK** — Операция завершена успешно.  
- **400 Bad Request** — Некорректный JSON-payload или недопустимое значение.  
- **401 Unauthorized** — Отсутствует или недействителен токен аутентификации.  
- **500 Internal Server Error** — Непредвиденная ошибка сервера.

**Пример ответа GET**

```json
{
  "AutoFitMergedCellsType": "All",
  "IgnoreHidden": false,
  "OnlyAuto": false,
  "DefaultEditLanguage": "ru-RU",
  "MaxRowHeight": 0,
  "AutoFitWrappedTextType": "All",
  "FormatStrategy": "AutoFit",
  "ForRendering": "False"
}
```

Эти примеры демонстрируют, как настроить и вызвать модель `AutoFitterOptions` в API Aspose.Cells Cloud.