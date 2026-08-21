---
title: "Работа с диаграммами в Excel"
second_title: "Документ"
linktype: "Диаграммы"
type: docs
url: /ru/charts/
aliases: [  /ru/working-with-charts/ ]
keywords: "Aspose, Cells, Excel, диаграмма, API, REST, облачные технологии, электронная таблица"
description: "Узнайте, как управлять диаграммами в Excel с помощью API Aspose.Cells Cloud. Пошаговые руководства, примеры кода и обработка ошибок при извлечении, добавлении, обновлении, удалении и преобразовании диаграмм в графические форматы."
weight: 100
ArticleTitle: "Работа с диаграммами в Excel – Документация Aspose.Cells Cloud"
---

## Работа с диаграммами в файле Excel

**Последнее обновление:** Июль 2026 г.

Диаграммы в Excel — это визуальное представление данных, позволяющее пользователям быстро понять тренды и закономерности.  
API Aspose.Cells Cloud позволяет разработчикам программно работать с такими диаграммами, содержащимися в файлах Excel, хранящихся в облаке. С помощью этого API можно извлекать существующие диаграммы, добавлять новые, изменять их свойства (такие как заголовки, оси и легенды), удалять ненужные диаграммы, а также преобразовывать диаграммы в графические форматы для отчетности или последующей обработки. Следующие ссылки ведут к подробным страницам операций для каждой поддерживаемой действия, связанной с диаграммами.

### Краткая справка

| Операция | HTTP-метод | Конечная точка (шаблон) | Документация |
|----------|------------|-------------------------|--------------|
| Получить диаграмму | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}` | [Получить диаграмму из рабочего листа](/ru/cells/get-chart-from-a-worksheet/) |
| Добавить диаграмму | POST | `/cells/{file}/worksheets/{sheet}/charts` | [Добавить диаграмму в рабочий лист](/ru/cells/add-a-chart-in-a-worksheet/) |
| Удалить все диаграммы | DELETE | `/cells/{file}/worksheets/{sheet}/charts` | [Удалить все диаграммы из рабочего листа](/ru/cells/delete-all-charts-from-a-worksheet/) |
| Удалить диаграмму | DELETE | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}` | [Удалить диаграмму из рабочего листа](/ru/cells/delete-a-chart-from-a-worksheet/) |
| Преобразовать диаграмму в изображение | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/image` | [Преобразовать диаграмму в изображение](/ru/cells/convert-chart-to-image/) |
| Получить область диаграммы | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/area` | [Получить область диаграммы из рабочего листа](/ru/cells/get-chart-area-from-a-worksheet/) |
| Получить формат заливки | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/area/fillformat` | [Получить формат заливки области диаграммы из рабочего листа](/ru/cells/get-fill-format-of-a-chart-area-from-a-worksheet/) |
| Получить легенду | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend` | [Получить легенду диаграммы из рабочего листа](/ru/cells/get-chart-legend-from-a-worksheet/) |
| Обновить легенду | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend` | [Обновить легенду диаграммы в рабочем листе](/ru/cells/update-chart-legend-in-a-worksheet/) |
| Показать легенду | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend/show` | [Показать легенду диаграммы в рабочем листе](/ru/cells/show-chart-legend-in-a-worksheet/) |
| Скрыть легенду | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend/hide` | [Скрыть легенду диаграммы в рабочем листе](/ru/cells/hide-chart-legend-in-a-worksheet/) |
| Получить заголовок | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [Получить заголовок диаграммы из рабочего листа](/ru/cells/get-chart-title-from-a-worksheet/) |
| Задать заголовок | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [Установить заголовок диаграммы в рабочем листе Excel](/ru/cells/set-chart-title-in-excel-worksheet/) |
| Обновить заголовок | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [Обновить заголовок диаграммы в рабочем листе Excel](/ru/cells/update-chart-title-in-excel-worksheet/) |
| Удалить заголовок | DELETE | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [Удалить заголовок диаграммы в рабочем листе](/ru/cells/delete-chart-title-in-a-worksheet/) |
| Обновить свойства диаграммы | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}` | [Обновить свойства диаграммы](/ru/cells/charts/properties/update/) |
| Получить ось категорий | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/categoryaxis` | [Получить ось категорий диаграммы](/ru/cells/charts/category-axis/get/) |
| Получить ось значений | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/valueaxis` | [Получить ось значений диаграммы](/ru/cells/charts/value-axis/get/) |
| Получить вторую ось категорий | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondcategoryaxis` | [Получить вторую ось категорий диаграммы](/ru/cells/charts/second-category-axis/get/) |
| Получить вторую ось значений | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondvalueaxis` | [Получить вторую ось значений диаграммы](/ru/cells/charts/second-value-axis/get/) |
| Обновить ось категорий | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/categoryaxis` | [Обновить ось категорий диаграммы](/ru/cells/charts/category-axis/update/) |
| Обновить ось значений | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/valueaxis` | [Обновить ось значений диаграммы](/ru/cells/charts/value-axis/update/) |
| Обновить вторую ось категорий | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondcategoryaxis` | [Обновить вторую ось категорий диаграммы](/ru/cells/charts/second-category-axis/update/) |
| Обновить вторую ось значений | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondvalueaxis` | [Обновить вторую ось значений диаграммы](/ru/cells/charts/second-value-axis/update/) |

- [Получить диаграмму из рабочего листа](/ru/cells/get-chart-from-a-worksheet/)
- [Добавить диаграмму в рабочий лист](/ru/cells/add-a-chart-in-a-worksheet/)
- [Удалить все диаграммы из рабочего листа](/ru/cells/delete-all-charts-from-a-worksheet/)
- [Удалить диаграмму из рабочего листа](/ru/cells/delete-a-chart-from-a-worksheet/)
- [Преобразовать диаграмму в изображение](/ru/cells/convert-chart-to-image/)
- [Получить область диаграммы из рабочего листа](/ru/cells/get-chart-area-from-a-worksheet/)
- [Получить формат заливки области диаграммы из рабочего листа](/ru/cells/get-fill-format-of-a-chart-area-from-a-worksheet/)
- [Получить легенду диаграммы из рабочего листа](/ru/cells/get-chart-legend-from-a-worksheet/)
- [Обновить легенду диаграммы в рабочем листе](/ru/cells/update-chart-legend-in-a-worksheet/)
- [Показать легенду диаграммы в рабочем листе](/ru/cells/show-chart-legend-in-a-worksheet/)
- [Скрыть легенду диаграммы в рабочем листе](/ru/cells/hide-chart-legend-in-a-worksheet/)
- [Получить заголовок диаграммы из рабочего листа](/ru/cells/get-chart-title-from-a-worksheet/)
- [Установить заголовок диаграммы в рабочем листе Excel](/ru/cells/set-chart-title-in-excel-worksheet/)
- [Обновить заголовок диаграммы в рабочем листе Excel](/ru/cells/update-chart-title-in-excel-worksheet/)
- [Удалить заголовок диаграммы в рабочем листе](/ru/cells/delete-chart-title-in-a-worksheet/)
- [Обновить свойства диаграммы](/ru/cells/charts/properties/update/)
- [Получить ось категорий диаграммы](/ru/cells/charts/category-axis/get/)
- [Получить ось значений диаграммы](/ru/cells/charts/value-axis/get/)
- [Получить вторую ось категорий диаграммы](/ru/cells/charts/second-category-axis/get/)
- [Получить вторую ось значений диаграммы](/ru/cells/charts/second-value-axis/get/)
- [Обновить ось категорий диаграммы](/ru/cells/charts/category-axis/update/)
- [Обновить ось значений диаграммы](/ru/cells/charts/value-axis/update/)
- [Обновить вторую ось категорий диаграммы](/ru/cells/charts/second-category-axis/update/)
- [Обновить вторую ось значений диаграммы](/ru/cells/charts/second-value-axis/update/)