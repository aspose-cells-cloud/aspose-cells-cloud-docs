﻿---
title: АннотацияРасчетEngin
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ru/specification/model/abstractcalculationengine/
description: "Aspose.Cells Спецификация облачной модели: AbstractCalculationEngine. Легко обрабатывайте Excel и другие документы электронных таблиц с помощью таких функций, как открытие, создание, редактирование, разделение, слияние, сравнение и преобразование."
kwords: Excel, Office, электронная таблица, Cloud REST API, AbstractCalculationEngine
weight: 50
---
## **АннотацияРасчетДвигатель**

Представляет пользовательский механизм вычислений, расширяющий механизм вычислений по умолчанию Aspose.Cells.

| Имя свойства| Тип недвижимости| Обнуляемый| Только чтение| Значение по умолчанию| Описание|
|:- |:- |:- |:- |:- |:- |
| IsParamLiteralRequired| логическое значение| Истинный| ЛОЖЬ|| Указывает, нужен ли этому механизму буквальный текст параметра при выполнении вычислений. Значение по умолчанию — ложь.|
| IsParamArrayModeRequired| логическое значение| Истинный| ЛОЖЬ|| Указывает, нужен ли этому механизму параметр для вычисления в режиме массива. Значение по умолчанию — ложь. Если это требуется при вычислении пользовательских функций, для этого свойства необходимо установить значение true.|
| Процессбуилтинфункции| логическое значение| Истинный| ЛОЖЬ|| Должны ли встроенные функции, поддерживаемые встроенным механизмом, проверяться и обрабатываться этой реализацией. По умолчанию — ложь. Если пользователю необходимо изменить логику вычислений некоторых встроенных функций, это свойство должно быть установлено как true. В противном случае, пожалуйста, оставьте это свойство как ложное из соображений производительности.|

