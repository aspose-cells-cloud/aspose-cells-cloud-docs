---
title: "Guide de développement Aspose.Cells Cloud 3.0"
ArticleTitle: "Guide du développeur Aspose.Cells Cloud 3.0 REST API – Création, conversion et mise en forme des classeurs Excel"
second_title: "Document"
type: docs
url: /developer-guide-3.0/
aliases: [/developer-guide/v3.0/, /developer-guide-v3.0/]
keywords: "Aspose.Cells Cloud, API REST Excel, conversion de classeur, API graphique, importation de données, exportation, PDF, CSV, JSON, guide de développement"
description: "Découvrez comment utiliser les API REST Aspose.Cells Cloud 3.0 pour la création, la conversion, la mise en forme, les graphiques, les tableaux et bien plus encore. Inclut des exemples de code et des conseils de bonnes pratiques."
weight: 150
---

## Travailler avec les API REST Aspose.Cells Cloud

Le **Guide de développement Aspose.Cells Cloud 3.0** propose une vue d’ensemble concise et consultable des opérations les plus utilisées de l’API REST pour les classeurs et les feuilles de calcul Excel. Ce guide s’adresse aux développeurs souhaitant créer, modifier, convertir et manipuler des fichiers Excel par programmation. Utilisez les sections ci-dessous pour localiser l’opération souhaitée ; chaque lien pointe vers une page détaillée contenant la syntaxe des requêtes, les paramètres et des exemples. Cette page centrale regroupe la documentation de référence de l’**API REST Aspose.Cells Cloud**, facilitant ainsi la recherche des points de terminaison liés aux classeurs, la gestion des graphiques, l’importation et l’exportation de données.

**Prérequis :** Avant d’utiliser les API, assurez-vous d’avoir un compte Aspose Cloud valide, une clé API et un secret, ainsi que les SDK appropriés installés dans votre environnement de développement.

### Table des matières

- [Opérations sur les fichiers](#file-operations)
- [Accueil (Mise en forme des cellules et gestion des lignes/colonnes)](#home-cell-formatting--rowcolumn-management)
- [Insertion (Graphiques, tableaux et objets OLE)](#insert-charts-tables--ole-objects)
- [Mise en page (Sauts de page et configuration)](#page-layout-page-breaks--setup)
- [Formules (Calcul et noms)](#formulas-calculate--names)
- [Données (Groupe, filtre et importation)](#data-outline-filter--import)
- [Révision (Commentaires et protection)](#review-comments--protection)
- [Affichage (Contrôles de fenêtre et de zoom)](#view-window--zoom-controls)

### Résumé rapide des API

| Groupe d’API              | Exemple de point de terminaison                        | Action principale                                                 |
| ------------------------- | ------------------------------------------------------ | ----------------------------------------------------------------- |
| **Créer un classeur**     | `POST /cells/workbook`                                 | Créer un nouveau classeur Excel vide                              |
| **Converter un classeur** | `PUT /cells/workbook/convert`                          | Convertir un fichier Excel en PDF, CSV, JSON, etc.                |
| **Ajouter un graphique**  | `POST /cells/worksheets/{sheetName}/charts`            | Insérer un nouveau graphique dans une feuille de calcul           |
| **Gérer les tableaux**    | `PUT /cells/worksheets/{sheetName}/tables/{tableName}` | Mettre à jour ou supprimer un objet liste (tableau)               |
| **Importer des données**  | `POST /cells/worksheets/{sheetName}/import`            | Importer CSV, JSON, images ou tableaux dans une feuille de calcul |
| **Calculer les formules** | `POST /cells/workbook/calculate`                       | Recalculer toutes les formules d’un classeur                      |
| **Appliquer des filtres** | `POST /cells/worksheets/{sheetName}/filters`           | Ajouter ou supprimer des critères de filtre automatique           |
| **Protéger le classeur**  | `POST /cells/workbook/protect`                         | Appliquer une protection par mot de passe à un classeur           |

Ces opérations fréquentes couvrent la fonctionnalité principale de l’**API REST Aspose.Cells Cloud Excel** et pointent directement vers les pages de documentation détaillées.

Vous pouvez télécharger une version PDF du tableau Résumé rapide des API pour une consultation hors ligne.

{{< tabs tabTotal="8" tabID="1" tabName1="Fichier" tabName2="Accueil" tabName3="Insertion" tabName4="Mise en page" tabName5="Formules" tabName6="Données" tabName7="Révision" tabName8="Affichage" >}}
{{< tab tabNum="1" >}}

<div class="row">
    <div class="col-md-6">
        <p>Classeur : nouveau, convertir, enregistrer sous</p>
        <ul>
            <li><a href="/cells/create-an-empty-excel-workbook/" title="Créer un classeur Excel vide via l’API" rel="noopener">Créer un classeur Excel vide.</a></li>
            <li><a href="/cells/create-excel-workbook-from-a-template-file/" title="Créer un classeur à partir d’un fichier modèle" rel="noopener">Créer un classeur Excel à partir d’un fichier modèle.</a></li>
            <li><a href="/cells/create-excel-workbook-from-a-smartmarker-template/" title="Créer un classeur à partir d’un modèle SmartMarker" rel="noopener">Créer un classeur Excel à partir d’un modèle SmartMarker.</a></li>
            <li><a href="/cells/convert/" title="Convertir un classeur Excel dans un autre format" rel="noopener">Convertir un classeur Excel dans différents formats de fichier.</a></li>
            <li><a href="/cells/saveas-other-formats/" title="Enregistrer un classeur Excel dans un autre format" rel="noopener">Enregistrer un classeur Excel dans différents formats de fichier.</a></li>
        </ul>
        <p>Rechercher, remplacer</p>
        <ul>
            <li><a href="/cells/search/" title="Rechercher du texte dans des fichiers Excel" rel="noopener">Rechercher du texte dans des fichiers Excel.</a></li>
            <li><a href="/cells/replace/" title="Remplacer des valeurs dans des fichiers Excel" rel="noopener">Remplacer les anciennes valeurs par des nouvelles dans des fichiers Excel.</a></li>
        </ul>
        <p>Compresser</p>
        <ul>
            <li><a href="/cells/compress/" title="Compresser des fichiers Excel" rel="noopener">Compresser des fichiers Excel.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Classeur : fusionner, diviser</p>
        <ul>
            <li><a href="/cells/merge/" title="Fusionner plusieurs classeurs Excel" rel="noopener">Fusionner des classeurs Excel.</a></li>
            <li><a href="/cells/split/" title="Diviser un classeur Excel en fichiers séparés" rel="noopener">Diviser des classeurs Excel.</a></li>
        </ul>
        <p>Filigranes</p>
        <ul>
            <li><a href="/cells/add-background-in-workbook/" title="Ajouter une image de fond à un classeur" rel="noopener">Ajouter une image de fond à un classeur.</a></li>
            <li><a href="/cells/delete-background-in-workbook/" title="Supprimer une image de fond d’un classeur" rel="noopener">Supprimer une image de fond d’un classeur.</a></li>
            <li><a href="/cells/set-background-or-watermark-for-excel-worksheet/" title="Définir un fond ou un filigrane sur une feuille de calcul" rel="noopener">Définir un fond ou un filigrane sur une feuille de calcul Excel.</a></li>
            <li><a href="/cells/delete-background-or-watermark-of-excel-worksheet/" title="Supprimer le fond ou le filigrane d’une feuille de calcul" rel="noopener">Supprimer le fond ou le filigrane d’une feuille de calcul Excel.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="2" >}}
<div class="row">
    <div class="col-md-6">
        <p>Polices, styles, mise en forme conditionnelle et valeurs des cellules</p>
        <ul>
            <li><a href="/cells/get-cell-style-from-a-worksheet/" title="Récupérer le style d’une cellule dans une feuille de calcul" rel="noopener">Obtenir le style d’une cellule dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/update-multiple-cells-style/" title="Mettre à jour les styles de plusieurs cellules" rel="noopener">Mettre à jour le style de plusieurs cellules dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/change-cell-style-in-excel-worksheet/" title="Modifier le style d’une seule cellule" rel="noopener">Mettre à jour le style d’une cellule dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/apply-rich-text-formatting-to-a-cell/" title="Appliquer une mise en forme RTF à une cellule" rel="noopener">Appliquer une mise en forme texte enrichi à une cellule dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/clear-contents-and-styles-of-cells-in-excel-worksheet/" title="Effacer le contenu et les styles des cellules" rel="noopener">Effacer le contenu et les styles des cellules dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/working-with-conditional-formatting/" title="Gérer les règles de mise en forme conditionnelle" rel="noopener">Ajouter, supprimer et mettre à jour la mise en forme conditionnelle dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/set-value-of-a-cell-in-a-worksheet/" title="Définir la valeur d’une cellule" rel="noopener">Définir la valeur d’une cellule dans une feuille de calcul Excel.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Ligne/Colonne : insérer, supprimer, copier, masquer et ajuster automatiquement</p>
        <ul>
            <li><a href="/cells/add-an-empty-row-in-a-worksheet/" title="Insérer une ligne vide dans une feuille de calcul" rel="noopener">Ajouter une ligne vide dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/delete-row-from-a-worksheet/" title="Supprimer une ligne d’une feuille de calcul" rel="noopener">Supprimer une ligne d’une feuille de calcul Excel.</a></li>
            <li><a href="/cells/copy-rows-in-excel-worksheet/" title="Copier des lignes dans une feuille de calcul" rel="noopener">Copier des lignes dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/hide-rows-in-excel-worksheet/" title="Masquer des lignes dans une feuille de calcul" rel="noopener">Masquer des lignes dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/auto-fit-rows-in-excel-workbooks/" title="Ajuster automatiquement les lignes dans un classeur" rel="noopener">Ajuster automatiquement les lignes dans un classeur Excel.</a></li>
            <li><a href="/cells/columns/add/" title="Insérer une colonne vide dans une feuille de calcul" rel="noopener">Ajouter une colonne vide dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/columns/delete/" title="Supprimer une colonne d’une feuille de calcul" rel="noopener">Supprimer une colonne d’une feuille de calcul Excel.</a></li>
            <li><a href="/cells/columns/copy/" title="Copier des colonnes dans une feuille de calcul" rel="noopener">Copier des colonnes dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/columns/hide/" title="Masquer des colonnes dans une feuille de calcul" rel="noopener">Masquer des colonnes dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/columns/autofit/" title="Ajuster automatiquement les colonnes dans un classeur" rel="noopener">Ajuster automatiquement les colonnes dans un classeur Excel.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="3" >}}
<div class="row">
    <div class="col-md-6">
        <p>Graphique</p>
        <ul>
            <li><a href="/cells/add-a-chart-in-a-worksheet/" title="Ajouter un graphique dans une feuille de calcul" rel="noopener">Ajouter un graphique dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/delete-a-chart-from-a-worksheet/" title="Supprimer un graphique d’une feuille de calcul" rel="noopener">Supprimer un graphique dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/delete-all-charts-from-a-worksheet/" title="Supprimer tous les graphiques d’une feuille de calcul" rel="noopener">Supprimer tous les graphiques dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/convert-chart-to-image/" title="Convertir un graphique en fichier image" rel="noopener">Convertir un graphique en image.</a></li>
            <li><a href="/cells/hide-chart-legend-in-a-worksheet/" title="Masquer la légende d’un graphique" rel="noopener">Masquer la légende d’un graphique dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/update-chart-title-in-excel-worksheet/" title="Mettre à jour le titre d’un graphique" rel="noopener">Mettre à jour le titre d’un graphique dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/delete-chart-title-in-a-worksheet/" title="Supprimer le titre d’un graphique" rel="noopener">Supprimer le titre d’un graphique dans une feuille de calcul.</a></li>
        </ul>
        <p>Tableau</p>
        <ul>
            <li><a href="/cells/add-a-list-object-or-table-inside-the-worksheet/" title="Ajouter un tableau (objet liste) dans une feuille de calcul" rel="noopener">Ajouter un objet liste dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/update-a-list-object-or-table-inside-the-worksheet/" title="Mettre à jour un tableau dans une feuille de calcul" rel="noopener">Mettre à jour un objet liste dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/convert-list-object-or-table-to-range/" title="Convertir un tableau en plage" rel="noopener">Convertir un objet liste en plage.</a></li>
            <li><a href="/cells/sort-table-data/" title="Trier les données d’un tableau" rel="noopener">Trier les données d’un tableau.</a></li>
        </ul>
        <p>Objet OLE</p>
        <ul>
            <li><a href="/cells/add-oleobject-to-excel-worksheet/" title="Ajouter un objet OLE dans une feuille de calcul" rel="noopener">Ajouter un objet OLE dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/update-a-specific-oleobject-from-excel-worksheet/" title="Mettre à jour un objet OLE spécifique" rel="noopener">Mettre à jour un objet OLE spécifique dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/convert-oleobject-to-image/" title="Convertir un objet OLE en image" rel="noopener">Convertir un objet OLE en image.</a></li>
            <li><a href="/cells/delete-all-oleobjects-from-excel-worksheet/" title="Supprimer tous les objets OLE d’une feuille de calcul" rel="noopener">Supprimer tous les objets OLE dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/delete-a-specific-oleobject-from-excel-worksheet/" title="Supprimer un objet OLE spécifique" rel="noopener">Supprimer un objet OLE spécifique dans une feuille de calcul Excel.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Forme</p>
        <ul>
            <li><a href="/cells/add-a-shape-inside-the-worksheet/" title="Ajouter une forme dans une feuille de calcul" rel="noopener">Ajouter une forme dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/delete-all-shapes-inside-the-worksheet/" title="Supprimer toutes les formes d’une feuille de calcul" rel="noopener">Supprimer toutes les formes dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/delete-a-shape-by-index-inside-the-worksheet/" title="Supprimer une forme par son index" rel="noopener">Supprimer une forme par index dans une feuille de calcul Excel.</a></li>
        </ul>
        <p>Tableau croisé dynamique</p>
        <ul>
            <li><a href="/cells/add-a-pivot-table-in-a-worksheet/" title="Ajouter un tableau croisé dynamique dans une feuille de calcul" rel="noopener">Ajouter un tableau croisé dynamique dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/delete-worksheet-pivot-tables/" title="Supprimer tous les tableaux croisés dynamiques d’une feuille de calcul" rel="noopener">Supprimer tous les tableaux croisés dynamiques dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/delete-worksheet-pivot-table-by-index/" title="Supprimer un tableau croisé dynamique par son index" rel="noopener">Supprimer un tableau croisé dynamique par index dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/update-cell-style-for-pivot-table/" title="Mettre à jour le style des cellules d’un tableau croisé dynamique" rel="noopener">Mettre à jour le style des cellules d’un tableau croisé dynamique dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/update-style-for-pivot-table/" title="Mettre à jour le style global d’un tableau croisé dynamique" rel="noopener">Mettre à jour le style global d’un tableau croisé dynamique dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/working-with-pivot-filters/" title="Travailler avec les filtres de tableau croisé dynamique" rel="noopener">Travailler avec les filtres de tableau croisé dynamique dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/hide-pivot-field-item/" title="Masquer un élément de champ de tableau croisé dynamique" rel="noopener">Masquer les éléments de champ de tableau croisé dynamique dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/move-pivot-table/" title="Déplacer un tableau croisé dynamique dans une feuille de calcul" rel="noopener">Déplacer un tableau croisé dynamique dans une feuille de calcul Excel.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="4" >}}
<div class="row">
    <div class="col-md-6">
        <p>Saut de page</p>
        <ul>
            <li><a href="/cells/insert-horizontal-page-break-inside-worksheet/" title="Insérer un saut de page horizontal" rel="noopener">Insérer un saut de page horizontal dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/insert-vertical-page-break-inside-worksheet/" title="Insérer un saut de page vertical" rel="noopener">Insérer un saut de page vertical dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/delete-horizontal-page-break-inside-worksheet/" title="Supprimer un saut de page horizontal" rel="noopener">Supprimer un saut de page horizontal dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/delete-vertical-page-break-inside-worksheet/" title="Supprimer un saut de page vertical" rel="noopener">Supprimer un saut de page vertical dans une feuille de calcul Excel.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Configuration de la mise en page</p>
        <ul>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="5" >}}
<div class="row">
    <div class="col-md-6">
        <p>Calcul</p>
        <ul>
            <li><a href="/cells/calculate-all-formulas-in-a-workbook/" title="Calculer toutes les formules d’un classeur" rel="noopener">Calculer toutes les formules dans un classeur Excel.</a></li>
            <li><a href="/cells/calculate-cells-formula/" title="Calculer la formule d’une cellule spécifique" rel="noopener">Calculer les formules des cellules dans un classeur Excel.</a></li>
            <li><a href="/cells/calculate-formula-in-a-worksheet/" title="Calculer une formule dans une feuille de calcul" rel="noopener">Calculer une formule dans une feuille de calcul Excel.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Nom</p>
        <ul>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="6" >}}
<div class="row">
    <div class="col-md-6">
        <p>Groupe</p>
        <ul>
            <li><a href="/cells/group-rows-in-excel-worksheet/" title="Grouper des lignes dans une feuille de calcul" rel="noopener">Grouper des lignes dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/ungroup-rows-in-excel-worksheet/" title="Dégrouper des lignes dans une feuille de calcul" rel="noopener">Dégrouper des lignes dans une feuille de calcul Excel.</a></li>
        </ul>
        <p>Filtre</p>
        <ul>
            <li><a href="/cells/add-a-filter-for-a-filter-column/" title="Ajouter un filtre à une colonne" rel="noopener">Ajouter un filtre à une colonne dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/delete-a-filter-for-a-filter-column/" title="Supprimer un filtre de colonne" rel="noopener">Supprimer un filtre à une colonne dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/remove-a-date-filter/" title="Supprimer un filtre de date" rel="noopener">Supprimer un filtre de date dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/add-an-icon-filter/" title="Ajouter un filtre par icône" rel="noopener">Ajouter un filtre par icône dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/add-date-filter-in-a-worksheet/" title="Ajouter un filtre de date" rel="noopener">Ajouter un filtre de date dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/filter-data-by-using-an-autofilter/" title="Filtrer les données à l’aide du filtre automatique" rel="noopener">Filtrer les données à l’aide du filtre automatique dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/filter-the-top-10-items-in-the-list/" title="Filtrer les 10 premiers éléments" rel="noopener">Filtrer les 10 premiers éléments de la liste dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/match-all-blank-cells-in-the-list/" title="Cibler toutes les cellules vides" rel="noopener">Cibler toutes les cellules vides de la liste dans une feuille de calcul Excel.</a></li>
        </ul>
        <p>Trier</p>
        <ul>
            <li><a href="/cells/sort-worksheet-data/" title="Trier les données d’une feuille de calcul" rel="noopener">Trier les données dans une feuille de calcul Excel.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Importer des données</p>
        <ul>
            <li><a href="/cells/import/" title="Importer des données dans des fichiers Excel" rel="noopener">Importer des données dans des fichiers Excel.</a></li>
            <li><a href="/cells/import-CSV-data-into-worksheet/" title="Importer des données CSV dans une feuille de calcul" rel="noopener">Importer des données CSV dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/import/picture/" title="Importer une image dans une feuille de calcul" rel="noopener">Importer une image dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/import/double-array/" title="Importer un tableau de doubles dans une feuille de calcul" rel="noopener">Importer un tableau de doubles dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/import/integer-array/" title="Importer un tableau d’entiers dans une feuille de calcul" rel="noopener">Importer un tableau d’entiers dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/import/string-array/" title="Importer un tableau de chaînes dans une feuille de calcul" rel="noopener">Importer un tableau de chaînes dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/import/with-using-storage/" title="Importer des données à l’aide du stockage" rel="noopener">Importer des données dans une feuille de calcul Excel à l’aide du stockage.</a></li>
            <li><a href="/cells/import/without-using-storage/" title="Importer des données sans utiliser le stockage" rel="noopener">Importer des données dans une feuille de calcul Excel sans utiliser le stockage.</a></li>
        </ul>
        <p>Assemblage</p>
        <ul>
            <li><a href="/cells/assembly/" title="Assembler des données dans des fichiers Excel" rel="noopener">Assembler des données dans des fichiers Excel.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="7" >}}
<div class="row">
    <div class="col-md-6">
        <p>Commentaires</p>
        <ul>
            <li><a href="/cells/add-a-comment-to-a-cell-in-a-worksheet/" title="Ajouter un commentaire à une cellule" rel="noopener">Ajouter un commentaire à une cellule dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/update-a-comment-in-excel-workbook/" title="Mettre à jour un commentaire de cellule" rel="noopener">Mettre à jour un commentaire dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/delete-all-comments-in-a-worksheet/" title="Supprimer tous les commentaires d’une feuille de calcul" rel="noopener">Supprimer tous les commentaires dans une feuille de calcul Excel.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Modifications</p>
        <ul>
            <li><a href="/cells/protect-excel-workbooks/" title="Protéger un classeur Excel" rel="noopener">Protéger un classeur Excel.</a></li>
            <li><a href="/cells/unprotect-excel-workbooks/" title="Déprotéger un classeur Excel" rel="noopener">Déprotéger un classeur Excel.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="8" >}}
<div class="row">
    <div class="col-md-6">
        <p>Fenêtres</p>
        <ul>
            <li><a href="/cells/freeze-panes-in-excel-worksheet/" title="Figer des volets dans une feuille de calcul" rel="noopener">Figer des volets dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/unfreeze-panes-in-excel-worksheet/" title="Dégeler des volets dans une feuille de calcul" rel="noopener">Dégeler des volets dans une feuille de calcul Excel.</a></li>
            <li><a href="/cells/hide-excel-worksheets/" title="Masquer une feuille de calcul" rel="noopener">Masquer une feuille de calcul Excel.</a></li>
            <li><a href="/cells/unhide-excel-worksheets/" title="Afficher une feuille de calcul masquée" rel="noopener">Afficher une feuille de calcul Excel masquée.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Zoom</p>
        <ul>
            <li><a href="/cells/set-zoom-in-excel-worksheet/" title="Définir le niveau de zoom d’une feuille de calcul" rel="noopener">Définir le zoom dans une feuille de calcul Excel.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}

{{< /tabs >}}
