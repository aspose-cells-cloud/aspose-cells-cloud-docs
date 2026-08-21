---
title: "Travail avec le filtre automatique Excel"
second_title: "Document"
linktitle: "Filtre automatique"
type: docs
url: /fr/autofilter/
aliases: [  /fr/working-with-autofilter/ ]
keywords: "Filtre automatique, Aspose.Cells Cloud, Filtre Excel, filtre couleur, filtre date, filtre dynamique, filtre nombre, filtre texte, filtre blanc, filtre personnalisé"
description: "Découvrez comment ajouter, modifier et supprimer des filtres automatiques Excel (couleur, date, dynamique, nombre, texte, blanc) à l'aide des API Aspose.Cells Cloud. Exemples de code dans plusieurs langages."
weight: 100
ArticleTitle: "Travail avec le filtre automatique Excel – Documentation Aspose.Cells Cloud"
---

Le filtre automatique est la méthode la plus rapide pour n’afficher que les éléments nécessaires à partir d’une feuille de calcul. Cette fonctionnalité permet aux utilisateurs de filtrer une liste selon des critères spécifiés — par texte, nombres ou dates.

**Différents types de filtres**

Aspose.Cells Cloud propose plusieurs API permettant d’appliquer divers types de filtres, tels que le filtre couleur, le filtre date, le filtre nombre, le filtre texte, le filtre blanc et le filtre non-blanc.

<table class="table table-striped">
  <tr>
    <td class="col-md-2"><strong>Couleur de remplissage</strong></td>
    <td class="col-md-10">
      <p>Aspose.Cells Cloud propose <a href="/cells/autofilter/add-color-filter/">l’API Add Fill Color Filter</a> pour filtrer les données selon la propriété de couleur de remplissage des cellules.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Date</strong></td>
    <td class="col-md-10">
      <p>Plusieurs filtres de date peuvent être appliqués, par exemple filtrer les lignes dont les dates correspondent à janvier 2018. Utilisez <a href="/cells/autofilter/add-date-filter/">l’API Add Date Filter</a> pour ajouter un filtre de date.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Date dynamique</strong></td>
    <td class="col-md-10">
      <p>Les filtres de date dynamique permettent de filtrer les cellules appartenant à un mois spécifique, indépendamment de l’année (par exemple, toutes les dates de janvier). Voir <a href="/cells/autofilter/add-dynamic-filter/">l’API Dynamic Filter</a>.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Nombre</strong></td>
    <td class="col-md-10">
      <p>L’<a href="/cells/autofilter/add-filter/">API Custom Filters</a> permet de filtrer les cellules dont les valeurs numériques se situent dans une plage donnée.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Texte</strong></td>
    <td class="col-md-10">
      <p>Si une colonne contient du texte, vous pouvez sélectionner les cellules contenant une chaîne spécifique à l’aide de <a href="/cells/autofilter/add-filter/">l’API Add Filter</a>.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Blancs</strong></td>
    <td class="col-md-10">
      <p>Pour récupérer les lignes où une colonne est vide, utilisez <a href="/cells/autofilter/match-all-blank/">l’API Match All Blank Cells</a>.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Non-blancs</strong></td>
    <td class="col-md-10">
      <p>Pour filtrer les lignes où une colonne contient une valeur non vide, utilisez <a href="/cells/autofilter/match-all-non-blank/">l’API Match All Non-Blank Cells</a>.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Filtre personnalisé</strong></td>
    <td class="col-md-10">
      <p>Aspose.Cells Cloud fournit <a href="/cells/autofilter/add-custom-filter/">l’API Custom Filters</a> pour des scénarios avancés, tels que le filtrage des lignes contenant une sous-chaîne spécifique ou commençant/se terminant par une chaîne donnée.</p>
    </td>
  </tr>
</table>

**Opérations sur le filtre automatique**

- [Comment ajouter un filtre couleur dans une feuille de calcul Excel](/cells/autofilter/add-color-filter/) – **Méthode :** POST, **Point de terminaison :** `/cells/autofilter/add-color-filter/`
- [Comment ajouter un filtre personnalisé dans une feuille de calcul Excel](/cells/autofilter/add-custom-filter/) – **Méthode :** POST, **Point de terminaison :** `/cells/autofilter/add-custom-filter/`
- [Comment ajouter un filtre date dans une feuille de calcul Excel](/cells/autofilter/add-date-filter/) – **Méthode :** POST, **Point de terminaison :** `/cells/autofilter/add-date-filter/`
- [Comment ajouter un filtre dynamique dans une feuille de calcul Excel](/cells/autofilter/add-dynamic-filter/) – **Méthode :** POST, **Point de terminaison :** `/cells/autofilter/add-dynamic-filter/`
- [Comment ajouter un filtre dans une feuille de calcul Excel](/cells/autofilter/add-filter/) – **Méthode :** POST, **Point de terminaison :** `/cells/autofilter/add-filter/`
- [Comment ajouter un filtre par icône dans une feuille de calcul Excel](/cells/autofilter/add-icon-filter/) – **Méthode :** POST, **Point de terminaison :** `/cells/autofilter/add-icon-filter/`
- [Comment supprimer un filtre date dans une feuille de calcul Excel](/cells/autofilter/delete-a-date-filter/) – **Méthode :** DELETE, **Point de terminaison :** `/cells/autofilter/delete-a-date-filter/`
- [Comment supprimer un filtre dans une feuille de calcul Excel](/cells/delete-filter/) – **Méthode :** DELETE, **Point de terminaison :** `/cells/delete-filter/`
- [Comment obtenir la description d’un filtre automatique dans une feuille de calcul Excel](/cells/autofilter/get/) – **Méthode :** GET, **Point de terminaison :** `/cells/autofilter/get/`
- [Comment faire correspondre toutes les cellules blanches dans une feuille de calcul Excel](/cells/autofilter/match-all-blank/) – **Méthode :** POST, **Point de terminaison :** `/cells/autofilter/match-all-blank/`
- [Comment faire correspondre toutes les cellules non vides dans une feuille de calcul Excel](/cells/autofilter/match-all-non-blank/) – **Méthode :** POST, **Point de terminaison :** `/cells/autofilter/match-all-non-blank/`
- [Comment actualiser un filtre automatique dans une feuille de calcul Excel](/cells/autofilter/refresh/) – **Méthode :** POST, **Point de terminaison :** `/cells/autofilter/refresh/`
---