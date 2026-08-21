---
title: "Работа с автофильтром Excel"
second_title: "Документ"
linktype: "AutoFilter"
type: docs
url: /autofilter/
aliases: [/working-with-autofilter/]
keywords: "Автофильтр, Aspose.Cells Cloud, фильтр Excel, цветовой фильтр, фильтр по дате, динамический фильтр, числовой фильтр, текстовый фильтр, фильтр пустых значений, пользовательский фильтр"
description: "Узнайте, как добавлять, редактировать и удалять автофильтры Excel (цветовой, по дате, динамический, числовой, текстовый, пустых значений) с помощью API Aspose.Cells Cloud. Примеры кода на множестве языков."
weight: 100
ArticleTitle: "Работа с автофильтром Excel – документация Aspose.Cells Cloud"
---

Автофильтр — это самый быстрый способ отобразить только те элементы, которые вам нужны, на листе. Функция автофильтра позволяет пользователям фильтровать список на основе заданных критериев — по тексту, числам или датам.

**Различные типы фильтров**

Aspose.Cells Cloud предоставляет множество API для применения различных типов фильтров, таких как цветовой фильтр, фильтр по дате, числовой фильтр, текстовый фильтр, фильтр пустых значений и фильтр непустых значений.

<table class="table table-striped">
  <tr>
    <td class="col-md-2"><strong>Цвет заливки</strong></td>
    <td class="col-md-10">
      <p>Aspose.Cells Cloud предоставляет <a href="/cells/autofilter/add-color-filter/">API добавления цветового фильтра по заливке</a> для фильтрации данных на основе свойства цвета заливки ячеек.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Дата</strong></td>
    <td class="col-md-10">
      <p>Можно применять различные фильтры по дате, например, фильтровать строки, содержащие даты января 2018 года. Используйте <a href="/cells/autofilter/add-date-filter/">API добавления фильтра по дате</a> для добавления фильтра по дате.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Динамическая дата</strong></td>
    <td class="col-md-10">
      <p>Динамические фильтры по дате позволяют фильтровать ячейки, относящиеся к определённому месяцу, независимо от года (например, все даты января). Подробнее см. в <a href="/cells/autofilter/add-dynamic-filter/">API динамического фильтра</a>.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Число</strong></td>
    <td class="col-md-10">
      <p><a href="/cells/autofilter/add-filter/">API пользовательских фильтров</a> позволяет фильтровать ячейки, числовые значения которых попадают в заданный диапазон.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Текст</strong></td>
    <td class="col-md-10">
      <p>Если столбец содержит текст, вы можете выбрать ячейки, содержащие определённую подстроку, с помощью <a href="/cells/autofilter/add-filter/">API добавления фильтра</a>.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Пустые значения</strong></td>
    <td class="col-md-10">
      <p>Для получения строк, в которых столбец пуст, используйте <a href="/cells/autofilter/match-all-blank/">API сопоставления всех пустых ячеек</a>.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Непустые значения</strong></td>
    <td class="col-md-10">
      <p>Для фильтрации строк, в которых столбец содержит любые непустые значения, используйте <a href="/cells/autofilter/match-all-non-blank/">API сопоставления всех непустых ячеек</a>.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Пользовательский фильтр</strong></td>
    <td class="col-md-10">
      <p>Aspose.Cells Cloud предоставляет <a href="/cells/autofilter/add-custom-filter/">API пользовательских фильтров</a> для решения сложных задач, например, фильтрации строк, содержащих определённую подстроку или начинающихся/заканчивающихся на определённую строку.</p>
    </td>
  </tr>
</table>

**Операции с автофильтром**

- [Как добавить цветовой фильтр на лист Excel](/cells/autofilter/add-color-filter/) — **Метод:** POST, **Конечная точка:** `/cells/autofilter/add-color-filter/`
- [Как добавить пользовательский фильтр на лист Excel](/cells/autofilter/add-custom-filter/) — **Метод:** POST, **Конечная точка:** `/cells/autofilter/add-custom-filter/`
- [Как добавить фильтр по дате на лист Excel](/cells/autofilter/add-date-filter/) — **Метод:** POST, **Конечная точка:** `/cells/autofilter/add-date-filter/`
- [Как добавить динамический фильтр на лист Excel](/cells/autofilter/add-dynamic-filter/) — **Метод:** POST, **Конечная точка:** `/cells/autofilter/add-dynamic-filter/`
- [Как добавить фильтр на лист Excel](/cells/autofilter/add-filter/) — **Метод:** POST, **Конечная точка:** `/cells/autofilter/add-filter/`
- [Как добавить фильтр по значку на лист Excel](/cells/autofilter/add-icon-filter/) — **Метод:** POST, **Конечная точка:** `/cells/autofilter/add-icon-filter/`
- [Как удалить фильтр по дате на листе Excel](/cells/autofilter/delete-a-date-filter/) — **Метод:** DELETE, **Конечная точка:** `/cells/autofilter/delete-a-date-filter/`
- [Как удалить фильтр на листе Excel](/cells/delete-filter/) — **Метод:** DELETE, **Конечная точка:** `/cells/delete-filter/`
- [Как получить описание автофильтра на листе Excel](/cells/autofilter/get/) — **Метод:** GET, **Конечная точка:** `/cells/autofilter/get/`
- [Как сопоставить все пустые ячейки на листе Excel](/cells/autofilter/match-all-blank/) — **Метод:** POST, **Конечная точка:** `/cells/autofilter/match-all-blank/`
- [Как сопоставить все непустые ячейки на листе Excel](/cells/autofilter/match-all-non-blank/) — **Метод:** POST, **Конечная точка:** `/cells/autofilter/match-all-non-blank/`
- [Как обновить автофильтр на листе Excel](/cells/autofilter/refresh/) — **Метод:** POST, **Конечная точка:** `/cells/autofilter/refresh/`