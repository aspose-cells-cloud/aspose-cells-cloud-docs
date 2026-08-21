---
title: "Arbeta med Excel AutoFilter"
second_title: "Dokument"
linktitle: "AutoFilter"
type: docs
url: /sv/autofilter/
aliases: [  /sv/working-with-autofilter/ ]
keywords: "AutoFilter, Aspose.Cells Cloud, Excel-filter, färgfilter, datumfilter, dynamiskt filter, nummerfilter, textfilter, tomfilter, anpassat filter"
description: "Lär dig lägga till, redigera och ta bort Excel AutoFilter (färg, datum, dynamiskt, nummer, text, tom) med Aspose.Cells Cloud API:er. Kodexempel i flera språk."
weight: 100
ArticleTitle: "Arbeta med Excel AutoFilter – Aspose.Cells Cloud-dokumentation"
---

AutoFilter är den snabbaste sättet att endast visa de objekt du behöver från ett kalkylblad. Funktionen AutoFilter låter användare filtrera en lista baserat på angivna kriterier – efter text, nummer eller datum.

**Olika filtertyper**

Aspose.Cells Cloud tillhandahåller flera API:er för att tillämpa olika filtertyper, såsom färgfilter, datumfilter, nummerfilter, textfilter, tomfilter och icke-tomfilter.

<table class="table table-striped">
  <tr>
    <td class="col-md-2"><strong>Fyllningsfärg</strong></td>
    <td class="col-md-10">
      <p>Aspose.Cells Cloud erbjuder <a href="/sv/cells/autofilter/add-color-filter/">API:et för att lägga till fyllningsfärgfilter</a> för att filtrera data baserat på cellernas fyllningsfärgsegenskap.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Datum</strong></td>
    <td class="col-md-10">
      <p>Olika datumfilter kan tillämpas, till exempel att filtrera rader med datum i januari 2018. Använd <a href="/sv/cells/autofilter/add-date-filter/">API:et för att lägga till datumfilter</a> för att lägga till ett datumfilter.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Dynamiskt datum</strong></td>
    <td class="col-md-10">
      <p>Dynamiska datumfilter låter dig filtrera celler som tillhör en viss månad oavsett år (t.ex. alla januaridatum). Se <a href="/sv/cells/autofilter/add-dynamic-filter/">API:et för dynamiska filter</a>.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Nummer</strong></td>
    <td class="col-md-10">
      <p><a href="/sv/cells/autofilter/add-filter/">API:et för anpassade filter</a> möjliggör filtrering av celler vars numeriska värden ligger inom ett givet intervall.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Text</strong></td>
    <td class="col-md-10">
      <p>Om en kolumn innehåller text kan du välja celler som innehåller en specifik sträng med <a href="/sv/cells/autofilter/add-filter/">API:et för att lägga till filter</a>.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Tomma</strong></td>
    <td class="col-md-10">
      <p>För att hämta rader där en kolumn är tom, använd <a href="/sv/cells/autofilter/match-all-blank/">API:et för att matcha alla tomma celler</a>.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Icke-tomma</strong></td>
    <td class="col-md-10">
      <p>För att filtrera rader där en kolumn innehåller något värde utom tomt, använd <a href="/sv/cells/autofilter/match-all-non-blank/">API:et för att matcha alla icke-tomma celler</a>.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Anpassat filter</strong></td>
    <td class="col-md-10">
      <p>Aspose.Cells Cloud erbjuder <a href="/sv/cells/autofilter/add-custom-filter/">API:et för anpassade filter</a> för avancerade scenarier, till exempel att filtrera rader som innehåller en specifik delsträng eller som börjar/slutar med en viss sträng.</p>
    </td>
  </tr>
</table>

**Åtgärder för AutoFilter**

- [Hur man lägger till ett färgfilter i ett Excel-kalkylblad](/sv/cells/autofilter/add-color-filter/) – **Metod:** POST, **Slutpunkt:** `/cells/autofilter/add-color-filter/`
- [Hur man lägger till ett anpassat filter i ett Excel-kalkylblad](/sv/cells/autofilter/add-custom-filter/) – **Metod:** POST, **Slutpunkt:** `/cells/autofilter/add-custom-filter/`
- [Hur man lägger till ett datumfilter i ett Excel-kalkylblad](/sv/cells/autofilter/add-date-filter/) – **Metod:** POST, **Slutpunkt:** `/cells/autofilter/add-date-filter/`
- [Hur man lägger till ett dynamiskt filter i ett Excel-kalkylblad](/sv/cells/autofilter/add-dynamic-filter/) – **Metod:** POST, **Slutpunkt:** `/cells/autofilter/add-dynamic-filter/`
- [Hur man lägger till ett filter i ett Excel-kalkylblad](/sv/cells/autofilter/add-filter/) – **Metod:** POST, **Slutpunkt:** `/cells/autofilter/add-filter/`
- [Hur man lägger till ett ikonfilter i ett Excel-kalkylblad](/sv/cells/autofilter/add-icon-filter/) – **Metod:** POST, **Slutpunkt:** `/cells/autofilter/add-icon-filter/`
- [Hur man tar bort ett datumfilter i ett Excel-kalkylblad](/sv/cells/autofilter/delete-a-date-filter/) – **Metod:** DELETE, **Slutpunkt:** `/cells/autofilter/delete-a-date-filter/`
- [Hur man tar bort ett filter i ett Excel-kalkylblad](/sv/cells/delete-filter/) – **Metod:** DELETE, **Slutpunkt:** `/cells/delete-filter/`
- [Hur man hämtar en AutoFilter-beskrivning från ett Excel-kalkylblad](/sv/cells/autofilter/get/) – **Metod:** GET, **Slutpunkt:** `/cells/autofilter/get/`
- [Hur man matchar alla tomma celler i ett Excel-kalkylblad](/sv/cells/autofilter/match-all-blank/) – **Metod:** POST, **Slutpunkt:** `/cells/autofilter/match-all-blank/`
- [Hur man matchar alla icke-tomma celler i ett Excel-kalkylblad](/sv/cells/autofilter/match-all-non-blank/) – **Metod:** POST, **Slutpunkt:** `/cells/autofilter/match-all-non-blank/`
- [Hur man uppdaterar en AutoFilter i ett Excel-kalkylblad](/sv/cells/autofilter/refresh/) – **Metod:** POST, **Slutpunkt:** `/cells/autofilter/refresh/`
---