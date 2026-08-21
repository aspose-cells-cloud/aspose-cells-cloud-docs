---
title: "Arbeiten mit Excel-AutoFilter"
second_title: "Dokument"
linktitle: "AutoFilter"
type: docs
url: /de/autofilter/
aliases: [  /de/working-with-autofilter/ ]
keywords: "AutoFilter, Aspose.Cells Cloud, Excel-Filter, Farbfilter, Datumsfilter, dynamischer Filter, Zahlenfilter, Textfilter, Leerzeichenfilter, benutzerdefinierter Filter"
description: "Erfahren Sie, wie Sie Excel-AutoFilter (Farbe, Datum, dynamisch, Zahl, Text, Leerzeichen) mithilfe der Aspose.Cells Cloud APIs hinzufügen, bearbeiten und löschen. Codebeispiele in mehreren Sprachen."
weight: 100
ArticleTitle: "Arbeiten mit Excel-AutoFilter – Aspose.Cells Cloud-Dokumentation"
---

Mit dem AutoFilter können Sie schnell nur die gewünschten Elemente aus einem Arbeitsblatt anzeigen. Mit dieser Funktion können Benutzer eine Liste anhand bestimmter Kriterien filtern – nach Text, Zahlen oder Datumsangaben.

**Verschiedene Filtertypen**

Aspose.Cells Cloud stellt mehrere APIs bereit, mit denen sich verschiedene Filtertypen anwenden lassen, darunter Farbfilter, Datumsfilter, Zahlenfilter, Textfilter, Leerzeichenfilter und Nicht-Leerzeichenfilter.

<table class="table table-striped">
  <tr>
    <td class="col-md-2"><strong>Füllfarbe</strong></td>
    <td class="col-md-10">
      <p>Aspose.Cells Cloud bietet <a href="/cells/autofilter/add-color-filter/">die API „Add Fill Color Filter“</a> an, um Daten basierend auf der Füllfarbeigenschaft von Zellen zu filtern.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Datum</strong></td>
    <td class="col-md-10">
      <p>Es können verschiedene Datumsfilter angewendet werden, z. B. das Filtern von Zeilen mit Datumsangaben im Januar 2018. Verwenden Sie <a href="/cells/autofilter/add-date-filter/">die API „Add Date Filter“</a>, um einen Datumsfilter hinzuzufügen.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Dynamisches Datum</strong></td>
    <td class="col-md-10">
      <p>Mit dynamischen Datumsfiltern können Sie Zellen filtern, die zu einem bestimmten Monat gehören, unabhängig vom Jahr (z. B. alle Januar-Datumsangaben). Weitere Informationen finden Sie unter <a href="/cells/autofilter/add-dynamic-filter/">der API für dynamische Filter</a>.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Zahl</strong></td>
    <td class="col-md-10">
      <p>Mit der <a href="/cells/autofilter/add-filter/">API „Custom Filters“</a> können Sie Zellen filtern, deren numerische Werte in einem bestimmten Bereich liegen.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Text</strong></td>
    <td class="col-md-10">
      <p>Für eine Spalte mit Textinhalten können Sie mithilfe von <a href="/cells/autofilter/add-filter/">der API „Add Filter“</a> Zellen auswählen, die einen bestimmten Zeichenfolgenwert enthalten.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Leerzeichen</strong></td>
    <td class="col-md-10">
      <p>Um Zeilen abzurufen, in denen eine Spalte leer ist, verwenden Sie <a href="/cells/autofilter/match-all-blank/">die API „Match All Blank Cells“</a>.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Nicht-Leerzeichen</strong></td>
    <td class="col-md-10">
      <p>Um Zeilen zu filtern, in denen eine Spalte einen beliebigen Nicht-Leerzeichenwert enthält, verwenden Sie <a href="/cells/autofilter/match-all-non-blank/">die API „Match All Non‑Blank Cells“</a>.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Benutzerdefinierter Filter</strong></td>
    <td class="col-md-10">
      <p>Aspose.Cells Cloud stellt <a href="/cells/autofilter/add-custom-filter/">die API „Custom Filters“</a> für erweiterte Szenarien bereit, z. B. zum Filtern von Zeilen, die einen bestimmten Teilstring enthalten oder mit einer bestimmten Zeichenfolge beginnen/enden.</p>
    </td>
  </tr>
</table>

**AutoFilter-Operationen**

- [Hinzufügen eines Farbfilters in einem Excel-Arbeitsblatt](/cells/autofilter/add-color-filter/) – **Methode:** POST, **Endpunkt:** `/cells/autofilter/add-color-filter/`
- [Hinzufügen eines benutzerdefinierten Filters in einem Excel-Arbeitsblatt](/cells/autofilter/add-custom-filter/) – **Methode:** POST, **Endpunkt:** `/cells/autofilter/add-custom-filter/`
- [Hinzufügen eines Datumsfilters in einem Excel-Arbeitsblatt](/cells/autofilter/add-date-filter/) – **Methode:** POST, **Endpunkt:** `/cells/autofilter/add-date-filter/`
- [Hinzufügen eines dynamischen Filters in einem Excel-Arbeitsblatt](/cells/autofilter/add-dynamic-filter/) – **Methode:** POST, **Endpunkt:** `/cells/autofilter/add-dynamic-filter/`
- [Hinzufügen eines Filters in einem Excel-Arbeitsblatt](/cells/autofilter/add-filter/) – **Methode:** POST, **Endpunkt:** `/cells/autofilter/add-filter/`
- [Hinzufügen eines Symbolsfilters in einem Excel-Arbeitsblatt](/cells/autofilter/add-icon-filter/) – **Methode:** POST, **Endpunkt:** `/cells/autofilter/add-icon-filter/`
- [Löschen eines Datumsfilters in einem Excel-Arbeitsblatt](/cells/autofilter/delete-a-date-filter/) – **Methode:** DELETE, **Endpunkt:** `/cells/autofilter/delete-a-date-filter/`
- [Löschen eines Filters in einem Excel-Arbeitsblatt](/cells/delete-filter/) – **Methode:** DELETE, **Endpunkt:** `/cells/delete-filter/`
- [Abrufen einer AutoFilter-Beschreibung aus einem Excel-Arbeitsblatt](/cells/autofilter/get/) – **Methode:** GET, **Endpunkt:** `/cells/autofilter/get/`
- [Übereinstimmen aller Leerzeichen in einem Excel-Arbeitsblatt](/cells/autofilter/match-all-blank/) – **Methode:** POST, **Endpunkt:** `/cells/autofilter/match-all-blank/`
- [Übereinstimmen aller Nicht-Leerzeichen in einem Excel-Arbeitsblatt](/cells/autofilter/match-all-non-blank/) – **Methode:** POST, **Endpunkt:** `/cells/autofilter/match-all-non-blank/`
- [Aktualisieren eines AutoFilters in einem Excel-Arbeitsblatt](/cells/autofilter/refresh/) – **Methode:** POST, **Endpunkt:** `/cells/autofilter/refresh/`
---