---
title: "Configuration de la page de feuille de calcul"
second_title: "Document"
linktitle: "Configuration de la page"
type: docs
url: /fr/page-setup/
keywords: "Aspose.Cells, pageSetup, feuille de calcul, paramètres d’impression, marges, orientation, format du papier, en-tête, pied de page, mise à l’échelle"
description: "Découvrez comment configurer la mise en page d’impression d’une feuille de calcul Excel à l’aide de l’objet PageSetup d’Aspose.Cells Cloud. Inclut la liste des propriétés, leurs valeurs par défaut, les plages et des exemples de code pour C#, Java et Python."
weight: 20
ArticleTitle: "Configuration de la page de feuille de calcul – Configurer la mise en page d’impression avec Aspose.Cells Cloud"
---

# **PageSetup**

Paramètres d’impression de page Excel

## Vue d’ensemble

L’objet **PageSetup** définit les options de mise en page d’impression pour une feuille de calcul Excel, telles que les marges, l’orientation, la mise à l’échelle, les en-têtes, les pieds de page et d’autres paramètres liés à l’impression. La configuration de ces propriétés permet aux développeurs de produire des classeurs imprimables correspondant à l’apparence et à la pagination souhaitées.

Voici un court exemple en C# qui illustre comment définir des propriétés courantes de configuration de page à l’aide du SDK Aspose.Cells Cloud :

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// Initialiser le client API (remplacez par vos identifiants)
var apiInstance = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");

// Définir les paramètres PageSetup
var pageSetup = new PageSetup()
{
    Orientation = "Landscape",
    PaperSize = "A4",
    CenterHorizontally = true,
    CenterVertically = true,
    Zoom = 100
};

// Appliquer les paramètres à la première feuille du classeur
apiInstance.PutWorksheetPageSetup("Sample.xlsx", "Sheet1", pageSetup);
```

Ce fragment définit l’orientation de la feuille en paysage, utilise le format de papier A4, centre le contenu horizontalement et verticalement, et applique un facteur de mise à l’échelle de 100 %.

## Propriétés

| Nom de la propriété   | Type de propriété | Nullable | En lecture seule | Valeur par défaut | Description                                                                  |
| --------------------- | ----------------- | -------- | ---------------- | ----------------- | ---------------------------------------------------------------------------- |
| BlackAndWhite         | bool              | false    | false            | false             | Imprime la feuille de calcul en mode noir et blanc.                          |
| BottomMargin          | float             | true     | false            | 2,54 cm           | Taille de la marge inférieure en centimètres.                                |
| CenterHorizontally    | bool              | false    | false            | false             | Centre la feuille horizontalement lors de l’impression.                      |
| CenterVertically      | bool              | false    | false            | false             | Centre la feuille verticalement lors de l’impression.                        |
| FirstPageNumber       | int               | true     | false            | 1                 | Numéro de la première page utilisé lors de l’impression de la feuille.       |
| FitToPagesTall        | int               | false    | false            | 1                 | Nombre de pages de hauteur sur lesquelles la feuille de calcul sera mise à l’échelle. |
| FitToPagesWide        | int               | false    | false            | 1                 | Nombre de pages de largeur sur lesquelles la feuille de calcul sera mise à l’échelle. |
| FooterMargin          | float             | true     | false            | 2,54 cm           | Distance entre le bas de la page et le pied de page, en centimètres.         |
| HeaderMargin          | float             | true     | false            | 2,54 cm           | Distance entre le haut de la page et l’en-tête, en centimètres.              |
| IsAutoFirstPageNumber | bool              | false    | false            | false             | Attribue automatiquement le numéro de la première page.                      |
| IsHFAlignMargins      | bool              | false    | false            | true              | Si true, les marges de l’en-tête/pied de page sont alignées avec les marges de la page. |
| IsHFDiffFirst         | bool              | false    | false            | false             | Indique que l’en-tête/pied de page de la première page diffère des autres pages. |
| IsHFDiffOddEven       | bool              | false    | false            | false             | Indique que l’en-tête/pied de page des pages impaires diffère de celui des pages paires. |
| IsHFScaleWithDoc      | bool              | false    | false            | false             | Met à l’échelle l’en-tête et le pied de page avec le document (Excel 2007+). |
| IsPercentScale        | bool              | false    | false            | true              | Si false, `FitToPagesWide` et `FitToPagesTall` contrôlent la mise à l’échelle. |
| LeftMargin            | float             | true     | false            | 2,54 cm           | Taille de la marge gauche en centimètres.                                    |
| Order                 | string            | true     | false            | "DownThenOver"    | Ordre utilisé par Excel pour numéroter les pages lors de l’impression d’une grande feuille de calcul. |
| Orientation           | string            | false    | false            | "Portrait"        | Orientation de la page : **Landscape** (paysage) ou **Portrait** (portrait). |
| PaperSize             | string            | true     | false            | "A4"              | Format du papier utilisé pour l’impression.                                  |
| PrintArea             | string            | true     | false            | (aucune)          | Plage de cellules à imprimer (par exemple, `"A1:D20"`).                      |
| PrintComments         | string            | true     | false            | "NoComments"      | Mode d’impression des commentaires avec la feuille.                          |
| PrintCopies           | int               | true     | false            | 1                 | Nombre d’exemplaires à imprimer.                                             |
| PrintDraft            | bool              | false    | false            | false             | Imprime la feuille de calcul en mode brouillon (sans graphismes).            |
| PrintErrors           | string            | true     | false            | "Display"         | Type d’erreur d’impression affichée.                                         |
| PrintGridlines        | bool              | false    | false            | false             | Imprime les lignes de grille des cellules.                                   |
| PrintHeadings         | bool              | false    | false            | false             | Imprime les en-têtes de lignes et de colonnes.                                |
| PrintQuality          | int               | true     | false            | 600               | Paramètre de qualité d’impression (points par pouce).                        |
| PrintTitleColumns     | string            | true     | false            | (aucune)          | Colonnes à répéter sur le côté gauche de chaque page imprimée.               |
| PrintTitleRows        | string            | true     | false            | (aucune)          | Lignes à répéter en haut de chaque page imprimée.                            |
| RightMargin           | float             | true     | false            | 2,54 cm           | Taille de la marge droite en centimètres.                                    |
| TopMargin             | float             | true     | false            | 2,54 cm           | Taille de la marge supérieure en centimètres.                                 |
| Zoom                  | int               | false    | false            | 100               | Facteur de mise à l’échelle en pourcentage (10–400 %).                        |
| Header                | object            | true     | false            | (aucun)           | Configuration de l’en-tête de page.                                          |
| Footer                | object            | true     | false            | (aucun)           | Configuration du pied de page.                                               |

## Objets associés

- **Header** – Configure l’en-tête de la feuille de calcul.  
- **Footer** – Configure le pied de page de la feuille de calcul.  
- **PrintOptions** – Paramètres supplémentaires liés à l’impression, tels que les sauts de page et la zone d’impression.  
---