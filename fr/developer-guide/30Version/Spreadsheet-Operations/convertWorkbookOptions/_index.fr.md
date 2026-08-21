---
title: "Options de conversion de classeur"
second_title: "Document"
linktitle: "Options de conversion de classeur"
type: docs
url: /fr/convert-workbook-options/
keywords: "Aspose.Cells, ConvertWorkbookOptions, conversion Excel, PDF, CSV, API"
description: "Options de conversion de classeur – configurez la conversion de classeur Excel en PDF, CSV, HTML et plus encore avec l'API Aspose.Cells Cloud."
weight: 79
ArticleTitle: "Options de conversion de classeur – API Aspose.Cells Cloud"
---

# Propriétés de ConvertWorkbookOptions

**Version de l'API :** 23.12 (2024‑03)

`ConvertWorkbookOptions` est le modèle de requête utilisé par l'API de conversion Aspose.Cells Cloud pour spécifier comment un classeur Excel doit être transformé dans un autre format (PDF, CSV, HTML, etc.). Il regroupe les informations sur le fichier source, le format cible, les paramètres de mise en page et les options de sauvegarde spécifiques au format.

| Nom                                | Type        | Description                                                                                                   | Notes |
| ----------------------------------- | ----------- | ------------------------------------------------------------------------------------------------------------- | ----- |
| **DataSource**                      | **Object**  | Source du fichier de données : `CloudFileSystem`, `RequestFiles` ou `HttpUri`.                                |       |
| **[FileInfo](/cells/file-info/)**   | **Object**  | Décrit le nom du fichier, sa taille et le contenu encodé en base64.                                           |       |
| **[PageSetup](/cells/page-setup/)** | **Object**  | Propriétés de mise en page telles que les marges, l'orientation et l'échelle.                                 |       |
| **SaveOptions**                     | **Object**  | Conteneur pour les objets d'options de sauvegarde spécifiques au format (par exemple, `PdfSaveOptions`, `HtmlSaveOptions`). |       |
| **ConvertFormat**                   | **string**  | Format de fichier cible (par exemple, **PDF**, **CSV**, **HTML**, **XLSX**, **TIFF**, etc.).                    |       |
| **CheckExcelRestriction**           | **boolean** | Obtient ou définit si les restrictions spécifiques à Excel (nombre maximal de lignes, de colonnes, longueur des noms de feuille, etc.) doivent être appliquées. |       |

**Conditions préalables**

- Obtenir un jeton d’accès OAuth 2.0 valide pour Aspose.Cells Cloud.  
- Vérifier que le fichier source est accessible via l’un des types `DataSource` pris en charge.

**Exemple rapide**

```json
{
  "DataSource": {
    "FileInfo": {
      "FileName": "Exemple.xlsx",
      "FileContent": "<contenu‑encodé‑en‑base64>"
    }
  },
  "ConvertFormat": "pdf",
  "SaveOptions": {
    "PdfSaveOptions": {
      "CompressImages": true,
      "ImageQuality": 90
    }
  }
}
```

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d @request.json \
     -o Exemple.pdf
```

**Détails de la requête API**

L’opération de conversion est exécutée via une requête **POST** vers le point de terminaison suivant :

```
https://api.aspose.cloud/v3.0/cells/convert
```

En-têtes requis :

| En‑tête               | Valeur                              |
|-----------------------|------------------------------------|
| `Authorization`       | `Bearer {access_token}`            |
| `Content-Type`        | `application/json`                |

Le corps de la requête doit être une représentation JSON de `ConvertWorkbookOptions` (voir l’exemple ci‑dessus). Toutes les propriétés sont facultatives, sauf si elles sont requises par le format `ConvertFormat` choisi.

**Réponse de l'API**

Une conversion réussie renvoie **HTTP 200 OK** (ou **202 Accepted** pour un traitement asynchrone) avec le fichier converti diffusé dans le corps de la réponse. Lorsque la réponse est diffusée, l’en‑tête `Content-Disposition` contient le nom de fichier suggéré.

Exemple de réponse JSON pour une requête asynchrone :

```json
{
  "JobId": "a1b2c3d4e5",
  "Status": "InProgress",
  "ResultUrl": "https://api.aspose.cloud/v3.0/cells/jobs/a1b2c3d4e5/result"
}
```

**Codes de statut**

| Code | Signification                                 |
|------|------------------------------------------|
| 200  | Conversion terminée ; fichier renvoyé.     |
| 202  | Conversion acceptée ; résultat disponible ultérieurement. |
| 400  | Requête incorrecte – paramètres manquants ou non valides. |
| 401  | Non autorisé – jeton non valide ou manquant. |
| 403  | Accès refusé – autorisations insuffisantes.   |
| 500  | Erreur interne du serveur.                   |

**Notes / Limitations**

- Le drapeau `CheckExcelRestriction` applique les limites d’Excel, telles que le nombre maximal de lignes (1 048 576) et de colonnes (16 384).  
- Toutes les propriétés `SaveOptions` ne sont pas prises en charge pour chaque format cible ; les options non prises en charge sont ignorées.  
- Lors de l’utilisation de `HttpUri` comme source de données, l’URL doit être publiquement accessible sans authentification.  
- Les informations sur la méthode et le point de terminaison de l’API ont été ajoutées pour améliorer la clarté pour les développeurs et réduire les erreurs d’intégration.

## Propriétés de FileSource

| Nom de la propriété | Type de propriété | Nullable | En lecture seule | Valeur par défaut | Description                                                               |
| ------------------- | ----------------- | -------- | ---------------- | ----------------- | ------------------------------------------------------------------------- |
| FileSourceType      | String            | true     | false            |                   | Indique le type de source (`CloudFileSystem`, `RequestFiles`, `HttpUri`). |
| FilePath            | String            | true     | false            |                   | Emplacement du chemin du fichier.                                         |

## Propriétés de DbfSaveOptions

| Nom de la propriété       | Type de propriété | Nullable | En lecture seule | Valeur par défaut | Description                                            |
| ------------------------- | ----------------- | -------- | ---------------- | ----------------- | ------------------------------------------------------ |
| ExportAsString            | Boolean           | true     | false            |                   | Si **true**, exporte les valeurs numériques en tant que chaînes. |
| SaveFormat                | String            | true     | false            |                   | Identifiant de format pour les fichiers DBF.          |
| CachedFileFolder          | String            | true     | false            |                   | Dossier utilisé pour les fichiers temporaires mis en cache. |
| ClearData                 | Boolean           | true     | false            |                   | Efface les données existantes avant la sauvegarde.     |
| CreateDirectory           | Boolean           | true     | false            |                   | Crée le dossier cible s’il n’existe pas.               |
| EnableHttpCompression     | Boolean           | true     | false            |                   | Active la compression HTTP pour la réponse.            |
| RefreshChartCache         | Boolean           | true     | false            |                   | Actualise les données mises en cache des graphiques avant la sauvegarde. |
| SortNames                 | Boolean           | true     | false            |                   | Trie les plages nommées par ordre alphabétique.        |
| ValidateMergedAreas       | Boolean           | true     | false            |                   | Valide la cohérence des cellules fusionnées.           |
| MergeAreas                | Boolean           | true     | false            |                   | Fusionne les cellules adjacentes si possible.          |
| SortExternalNames         | Boolean           | true     | false            |                   | Trie les références nommées externes.                   |
| CheckExcelRestriction     | Boolean           | true     | false            |                   | Applique les limites spécifiques à Excel pendant la conversion. |
| UpdateSmartArt            | Boolean           | true     | false            |                   | Met à jour les objets SmartArt vers la dernière version. |
| EncryptDocumentProperties | Boolean           | true     | false            |                   | Chiffre les propriétés du document dans le fichier de sortie. |

## Propriétés de DifSaveOptions

| Nom de la propriété       | Type de propriété | Nullable | En lecture seule | Valeur par défaut | Description                                            |
| ------------------------- | ----------------- | -------- | ---------------- | ----------------- | ------------------------------------------------------ |
| SaveFormat                | String            | true     | false            |                   | Identifiant de format pour les fichiers DIF.           |
| CachedFileFolder          | String            | true     | false            |                   | Dossier utilisé pour les fichiers temporaires mis en cache. |
| ClearData                 | Boolean           | true     | false            |                   | Efface les données existantes avant la sauvegarde.     |
| CreateDirectory           | Boolean           | true     | false            |                   | Crée le dossier cible s’il n’existe pas.               |
| EnableHttpCompression     | Boolean           | true     | false            |                   | Active la compression HTTP pour la réponse.            |
| RefreshChartCache         | Boolean           | true     | false            |                   | Actualise les données mises en cache des graphiques avant la sauvegarde. |
| SortNames                 | Boolean           | true     | false            |                   | Trie les plages nommées par ordre alphabétique.        |
| ValidateMergedAreas       | Boolean           | true     | false            |                   | Valide la cohérence des cellules fusionnées.           |
| MergeAreas                | Boolean           | true     | false            |                   | Fusionne les cellules adjacentes si possible.          |
| SortExternalNames         | Boolean           | true     | false            |                   | Trie les références nommées externes.                   |
| CheckExcelRestriction     | Boolean           | true     | false            |                   | Applique les limites spécifiques à Excel pendant la conversion. |
| UpdateSmartArt            | Boolean           | true     | false            |                   | Met à jour les objets SmartArt vers la dernière version. |
| EncryptDocumentProperties | Boolean           | true     | false            |                   | Chiffre les propriétés du document dans le fichier de sortie. |

## Propriétés de DocxSaveOptions

| Nom de la propriété               | Type de propriété | Nullable | En lecture seule | Valeur par défaut | Description                                             |
| --------------------------------- | ----------------- | -------- | ---------------- | ----------------- | ------------------------------------------------------- |
| DefaultFont                       | String            | true     | false            |                   | Police utilisée lorsqu’une police source n’est pas disponible. |
| CheckWorkbookDefaultFont          | Boolean           | true     | false            |                   | Vérifie si la police par défaut du classeur est appliquée. |
| CheckFontCompatibility            | Boolean           | true     | false            |                   | Valide la compatibilité des polices pour le format cible. |
| IsFontSubstitutionCharGranularity | Boolean           | true     | false            |                   | Contrôle la substitution de police au niveau des caractères. |
| OnePagePerSheet                   | Boolean           | true     | false            |                   | Force chaque feuille sur une page séparée.             |
| AllColumnsInOnePagePerSheet       | Boolean           | true     | false            |                   | Adapte toutes les colonnes d’une feuille sur une seule page. |
| IgnoreError                       | Boolean           | true     | false            |                   | Ignore les erreurs non critiques pendant la conversion. |
| OutputBlankPageWhenNothingToPrint | Boolean           | true     | false            |                   | Génère une page vide s’il n’y a rien à rendre.          |
| PageIndex                         | Integer           | true     | false            |                   | Index de la première page à exporter.                   |
| PageCount                         | Integer           | true     | false            |                   | Nombre de pages à exporter.                             |
| PrintingPageType                  | String            | true     | false            |                   | Spécifie le type de page pour l’impression.             |
| GridlineType                      | String            | true     | false            |                   | Détermine le rendu des traits de grille.                |
| TextCrossType                     | String            | true     | false            |                   | Définit le type de croisement pour le rendu du texte.   |
| DefaultEditLanguage               | String            | true     | false            |                   | Langue par défaut pour l’édition de texte.              |
| EmfRenderSetting                  | String            | true     | false            |                   | Paramètres de rendu EMF.                                |
| MergeAreas                        | Boolean           | true     | false            |                   | Fusionne les cellules adjacentes si possible.           |
| SortExternalNames                 | Boolean           | true     | false            |                   | Trie les références nommées externes.                   |
| UpdateSmartArt                    | Boolean           | true     | false            |                   | Met à jour les objets SmartArt vers la dernière version. |
| SaveFormat                        | String            | true     | false            |                   | Identifiant de format pour les fichiers DOCX.           |
| CachedFileFolder                  | String            | true     | false            |                   | Dossier utilisé pour les fichiers temporaires mis en cache. |
| ClearData                         | Boolean           | true     | false            |                   | Efface les données existantes avant la sauvegarde.      |
| CreateDirectory                   | Boolean           | true     | false            |                   | Crée le dossier cible s’il n’existe pas.                |
| EnableHttpCompression             | Boolean           | true     | false            |                   | Active la compression HTTP pour la réponse.             |
| RefreshChartCache                 | Boolean           | true     | false            |                   | Actualise les données mises en cache des graphiques avant la sauvegarde. |
| SortNames                         | Boolean           | true     | false            |                   | Trie les plages nommées par ordre alphabétique.         |
| ValidateMergedAreas               | Boolean           | true     | false            |                   | Valide la cohérence des cellules fusionnées.            |
| CheckExcelRestriction             | Boolean           | true     | false            |                   | Applique les limites spécifiques à Excel pendant la conversion. |
| EncryptDocumentProperties          | Boolean           | true     | false            |                   | Chiffre les propriétés du document dans le fichier de sortie. |

## Propriétés de HtmlSaveOptions

| Nom de la propriété             | Type de propriété | Nullable | En lecture seule | Valeur par défaut | Description                                           |
| ------------------------------- | ----------------- | -------- | ---------------- | ----------------- | ----------------------------------------------------- |
| ExportPageHeaders               | Boolean           | true     | false            |                   | Inclut les en‑têtes de page dans la sortie HTML.      |
| ExportPageFooters               | Boolean           | true     | false            |                   | Inclut les pieds de page dans la sortie HTML.         |
| ExportRowColumnHeadings         | Boolean           | true     | false            |                   | Exporte les en‑têtes de lignes et de colonnes.        |
| ShowAllSheets                   | Boolean           | true     | false            |                   | Affiche toutes les feuilles de calcul dans un seul fichier HTML. |
| ImageOptions                    | Class             | true     | false            |                   | Paramètres contrôlant le rendu des images.            |
| SaveAsSingleFile                | Boolean           | true     | false            |                   | Sauvegarde l’ensemble du classeur dans un seul fichier HTML. |
| ExportHiddenWorksheet           | Boolean           | true     | false            |                   | Inclut les feuilles de calcul masquées dans l’export. |
| ExportGridLines                 | Boolean           | true     | false            |                   | Rend les traits de grille dans la sortie HTML.        |
| PresentationPreference          | Boolean           | true     | false            |                   | Optimise le HTML pour le mode présentation.           |
| CellCssPrefix                   | String            | true     | false            |                   | Préfixe ajouté aux noms de classes CSS générées pour les cellules. |
| TableCssId                      | String            | true     | false            |                   | Attribut ID pour le tableau HTML généré.              |
| IsFullPathLink                  | Boolean           | true     | false            |                   | Génère des liens hypertexte avec chemin complet pour les ressources. |
| ExportWorksheetCSSSeparately    | Boolean           | true     | false            |                   | Place le CSS de chaque feuille dans un fichier séparé. |
| ExportSimilarBorderStyle        | Boolean           | true     | false            |                   | Fusionne les styles de bordure similaires pour réduire la taille du CSS. |
| MergeEmptyTdForcely             | Boolean           | true     | false            |                   | Force la fusion des éléments `<td>` vides.             |
| ExportCellCoordinate            | Boolean           | true     | false            |                   | Inclut les coordonnées des cellules (par exemple, A1) dans le HTML. |
| ExportExtraHeadings             | Boolean           | true     | false            |                   | Ajoute des lignes/colonnes d’en‑tête supplémentaires si nécessaire. |
| ExportHeadings                  | Boolean           | true     | false            |                   | Exporte les en‑têtes de lignes et de colonnes.         |
| ExportFormula                   | Boolean           | true     | false            |                   | Affiche les formules au lieu des valeurs calculées.    |
| AddTooltipText                  | Boolean           | true     | false            |                   | Ajoute des info‑bulles contenant les commentaires des cellules. |
| ExportBogusRowData              | Boolean           | true     | false            |                   | Inclut des lignes de remplacement pour les données vides. |
| ExcludeUnusedStyles             | Boolean           | true     | false            |                   | Supprime les styles CSS inutilisés.                    |
| ExportDocumentProperties        | Boolean           | true     | false            |                   | Écrit les propriétés au niveau du document dans les balises méta HTML. |
| ExportWorksheetProperties       | Boolean           | true     | false            |                   | Écrit les propriétés au niveau de la feuille dans le HTML. |
| ExportWorkbookProperties        | Boolean           | true     | false            |                   | Écrit les propriétés au niveau du classeur dans le HTML. |
| ExportFrameScriptsAndProperties | Boolean           | true     | false            |                   | Inclut les scripts et propriétés pour les cadres.      |
| AttachedFilesDirectory          | String            | true     | false            |                   | Chemin du dossier pour les fichiers joints.            |
| AttachedFilesUrlPrefix          | String            | true     | false            |                   | Préfixe d’URL pour les fichiers joints.                |
| Encoding                        | String            | true     | false            |                   | Encodage des caractères pour le fichier HTML.          |
| ExportActiveWorksheetOnly       | Boolean           | true     | false            |                   | Exporte uniquement la feuille de calcul active.        |
| ExportChartImageFormat          | String            | true     | false            |                   | Format d’image utilisé pour les graphiques intégrés.   |
| ExportImagesAsBase64            | Boolean           | true     | false            |                   | Encode les images en tant que chaînes Base64.          |
| HiddenColDisplayType            | String            | true     | false            |                   | Mode d’affichage des colonnes masquées.                |
| HiddenRowDisplayType            | String            | true     | false            |                   | Mode d’affichage des lignes masquées.                  |
| HtmlCrossStringType             | String            | true     | false            |                   | Détermine le rendu des données inter‑chaînes.          |
| IsExpImageToTempDir             | Boolean           | true     | false            |                   | Exporte les images vers un dossier temporaire.         |
| PageTitle                       | String            | true     | false            |                   | Titre utilisé pour la page HTML générée.               |
| ParseHtmlTagInCell              | Boolean           | true     | false            |                   | Analyse les balises HTML présentes dans les valeurs de cellule. |
| CellNameAttribute               | String            | true     | false            |                   | Nom de l’attribut contenant la référence de la cellule. |
| SaveFormat                      | String            | true     | false            |                   | Identifiant de format pour les fichiers HTML.          |
| CachedFileFolder                | String            | true     | false            |                   | Dossier utilisé pour les fichiers temporaires mis en cache. |
| ClearData                       | Boolean           | true     | false            |                   | Efface les données existantes avant la sauvegarde.     |
| CreateDirectory                 | Boolean           | true     | false            |                   | Crée le dossier cible s’il n’existe pas.               |
| EnableHttpCompression           | Boolean           | true     | false            |                   | Active la compression HTTP pour la réponse.            |
| RefreshChartCache               | Boolean           | true     | false            |                   | Actualise les données mises en cache des graphiques avant la sauvegarde. |
| SortNames                       | Boolean           | true     | false            |                   | Trie les plages nommées par ordre alphabétique.        |
| ValidateMergedAreas             | Boolean           | true     | false            |                   | Valide la cohérence des cellules fusionnées.           |
| MergeAreas                      | Boolean           | true     | false            |                   | Fusionne les cellules adjacentes si possible.          |
| SortExternalNames               | Boolean           | true     | false            |                   | Trie les références nommées externes.                   |
| CheckExcelRestriction           | Boolean           | true     | false            |                   | Applique les limites spécifiques à Excel pendant la conversion. |
| UpdateSmartArt                  | Boolean           | true     | false            |                   | Met à jour les objets SmartArt vers la dernière version. |
| EncryptDocumentProperties       | Boolean           | true     | false            |                   | Chiffre les propriétés du document dans le fichier de sortie. |

## Propriétés de ImageSaveOptions

| Nom de la propriété       | Type de propriété | Nullable | En lecture seule | Valeur par défaut | Description                                          |
| ------------------------- | ----------------- | -------- | ---------------- | ----------------- | ---------------------------------------------------- |
| ChartImageType            | String            | true     | false            |                   | Format d’image utilisé pour le rendu des graphiques. |
| EmbeddedImageNameInSvg    | String            | true     | false            |                   | Nom attribué aux images intégrées dans la sortie SVG. |
| HorizontalResolution      | Integer           | true     | false            |                   | Résolution horizontale (DPI) de l’image exportée.   |
| ImageFormat               | String            | true     | false            |                   | Format d’image cible (PNG, JPG, etc.).              |
| IsCellAutoFit             | Boolean           | true     | false            |                   | Ajuste automatiquement le contenu des cellules à la taille de l’image. |
| OnePagePerSheet           | Boolean           | true     | false            |                   | Rend chaque feuille de calcul sur une page séparée. |
| OnlyArea                  | Boolean           | true     | false            |                   | Exporte uniquement la zone définie de la feuille de calcul. |
| PrintingPage              | String            | true     | false            |                   | Mise en page utilisée pour l’impression.            |
| PrintWithStatusDialog     | Boolean           | true     | false            |                   | Affiche une boîte de dialogue d’état pendant l’impression. |
| Quality                   | Integer           | true     | false            |                   | Qualité de compression pour les images JPEG (0‑100). |
| TiffCompression           | String            | true     | false            |                   | Type de compression pour les images TIFF.           |
| VerticalResolution        | Integer           | true     | false            |                   | Résolution verticale (DPI) de l’image exportée.     |
| SaveFormat                | String            | true     | false            |                   | Identifiant de format pour les fichiers image.      |
| CachedFileFolder          | String            | true     | false            |                   | Dossier utilisé pour les fichiers temporaires mis en cache. |
| ClearData                 | Boolean           | true     | false            |                   | Efface les données existantes avant la sauvegarde.   |
| CreateDirectory           | Boolean           | true     | false            |                   | Crée le dossier cible s’il n’existe pas.             |
| EnableHttpCompression     | Boolean           | true     | false            |                   | Active la compression HTTP pour la réponse.          |
| RefreshChartCache         | Boolean           | true     | false            |                   | Actualise les données mises en cache des graphiques avant la sauvegarde. |
| SortNames                 | Boolean           | true     | false            |                   | Trie les plages nommées par ordre alphabétique.      |
| ValidateMergedAreas       | Boolean           | true     | false            |                   | Valide la cohérence des cellules fusionnées.         |
| MergeAreas                | Boolean           | true     | false            |                   | Fusionne les cellules adjacentes si possible.        |
| SortExternalNames         | Boolean           | true     | false            |                   | Trie les références nommées externes.                 |
| CheckExcelRestriction     | Boolean           | true     | false            |                   | Applique les limites spécifiques à Excel pendant la conversion. |
| UpdateSmartArt            | Boolean           | true     | false            |                   | Met à jour les objets SmartArt vers la dernière version. |
| EncryptDocumentProperties | Boolean           | true     | false            |                   | Chiffre les propriétés du document dans le fichier de sortie. |

## Propriétés de JsonSaveOptions

| Nom de la propriété       | Type de propriété | Nullable | En lecture seule | Valeur par défaut | Description                                               |
| ------------------------- | ----------------- | -------- | ---------------- | ----------------- | --------------------------------------------------------- |
| ExportArea                | Class             | true     | false            |                   | Définit la zone de feuille de calcul à exporter.          |
| HasHeaderRow              | Boolean           | true     | false            |                   | Indique si la première ligne contient des en‑têtes de colonne. |
| ExportAsString            | Boolean           | true     | false            |                   | Exporte toutes les valeurs sous forme de chaînes.         |
| Indent                    | String            | true     | false            |                   | Chaîne utilisée pour l’indentation (par exemple, deux espaces). |
| SaveFormat                | String            | true     | false            |                   | Identifiant de format pour les fichiers JSON.             |
| CachedFileFolder          | String            | true     | false            |                   | Dossier utilisé pour les fichiers temporaires mis en cache. |
| ClearData                 | Boolean           | true     | false            |                   | Efface les données existantes avant la sauvegarde.        |
| CreateDirectory           | Boolean           | true     | false            |                   | Crée le dossier cible s’il n’existe pas.                  |
| EnableHttpCompression     | Boolean           | true     | false            |                   | Active la compression HTTP pour la réponse.               |
| RefreshChartCache         | Boolean           | true     | false            |                   | Actualise les données mises en cache des graphiques avant la sauvegarde. |
| SortNames                 | Boolean           | true     | false            |                   | Trie les plages nommées par ordre alphabétique.           |
| ValidateMergedAreas       | Boolean           | true     | false            |                   | Valide la cohérence des cellules fusionnées.              |
| MergeAreas                | Boolean           | true     | false            |                   | Fusionne les cellules adjacentes si possible.             |
| SortExternalNames         | Boolean           | true     | false            |                   | Trie les références nommées externes.                     |
| CheckExcelRestriction     | Boolean           | true     | false            |                   | Applique les limites spécifiques à Excel pendant la conversion. |
| UpdateSmartArt            | Boolean           | true     | false            |                   | Met à jour les objets SmartArt vers la dernière version.  |
| EncryptDocumentProperties | Boolean           | true     | false            |                   | Chiffre les propriétés du document dans le fichier de sortie. |

## Propriétés de MarkdownSaveOptions

| Nom de la propriété       | Type de propriété | Nullable | En lecture seule | Valeur par défaut | Description                                                     |
| ------------------------- | ----------------- | -------- | ---------------- | ----------------- | --------------------------------------------------------------- |
| Encoding                  | String            | true     | false            |                   | Encodage des caractères pour le fichier markdown.               |
| FormatStrategy            | String            | true     | false            |                   | Stratégie utilisée pour formater le markdown (par exemple, GitHub, CommonMark). |
| LineSeparator             | String            | true     | false            |                   | Caractère(s) de saut de ligne à utiliser.                       |
| SaveFormat                | String            | true     | false            |                   | Identifiant de format pour les fichiers markdown.               |
| CachedFileFolder          | String            | true     | false            |                   | Dossier utilisé pour les fichiers temporaires mis en cache.     |
| ClearData                 | Boolean           | true     | false            |                   | Efface les données existantes avant la sauvegarde.              |
| CreateDirectory           | Boolean           | true     | false            |                   | Crée le dossier cible s’il n’existe pas.                        |
| EnableHttpCompression     | Boolean           | true     | false            |                   | Active la compression HTTP pour la réponse.                     |
| RefreshChartCache         | Boolean           | true     | false            |                   | Actualise les données mises en cache des graphiques avant la sauvegarde. |
| SortNames                 | Boolean           | true     | false            |                   | Trie les plages nommées par ordre alphabétique.                 |
| ValidateMergedAreas       | Boolean           | true     | false            |                   | Valide la cohérence des cellules fusionnées.                    |
| MergeAreas                | Boolean           | true     | false            |                   | Fusionne les cellules adjacentes si possible.                   |
| SortExternalNames         | Boolean           | true     | false            |                   | Trie les références nommées externes.                           |
| CheckExcelRestriction     | Boolean           | true     | false            |                   | Applique les limites spécifiques à Excel pendant la conversion. |
| UpdateSmartArt            | Boolean           | true     | false            |                   | Met à jour les objets SmartArt vers la dernière version.        |
| EncryptDocumentProperties | Boolean           | true     | false            |                   | Chiffre les propriétés du document dans le fichier de sortie.   |

## Propriétés de OoxmlSaveOptions

| Nom de la propriété       | Type de propriété | Nullable | En lecture seule | Valeur par défaut | Description                                          |
| ------------------------- | ----------------- | -------- | ---------------- | ----------------- | ---------------------------------------------------- |
| ExportCellName            | Boolean           | true     | false            |                   | Inclut les noms de cellule dans le fichier exporté.  |
| UpdateZoom                | Boolean           | true     | false            |                   | Met à jour le niveau de zoom dans le document de sortie. |
| EnableZip64               | Boolean           | true     | false            |                   | Active les extensions ZIP64 pour les fichiers volumineux. |
| EmbedOoxmlAsOleObject     | Boolean           | true     | false            |                   | Intègre l’OOXML en tant qu’objet OLE.                |
| CompressionType           | String            | true     | false            |                   | Type de compression appliquée (par exemple, Normal, Maximum). |
| SaveFormat                | String            | true     | false            |                   | Identifiant de format pour les fichiers OOXML.       |
| CachedFileFolder          | String            | true     | false            |                   | Dossier utilisé pour les fichiers temporaires mis en cache. |
| ClearData                 | Boolean           | true     | false            |                   | Efface les données existantes avant la sauvegarde.   |
| CreateDirectory           | Boolean           | true     | false            |                   | Crée le dossier cible s’il n’existe pas.             |
| EnableHttpCompression     | Boolean           | true     | false            |                   | Active la compression HTTP pour la réponse.          |
| RefreshChartCache         | Boolean           | true     | false            |                   | Actualise les données mises en cache des graphiques avant la sauvegarde. |
| SortNames                 | Boolean           | true     | false            |                   | Trie les plages nommées par ordre alphabétique.      |
| ValidateMergedAreas       | Boolean           | true     | false            |                   | Valide la cohérence des cellules fusionnées.         |
| MergeAreas                | Boolean           | true     | false            |                   | Fusionne les cellules adjacentes si possible.        |
| SortExternalNames         | Boolean           | true     | false            |                   | Trie les références nommées externes.                 |
| CheckExcelRestriction     | Boolean           | true     | false            |                   | Applique les limites spécifiques à Excel pendant la conversion. |
| UpdateSmartArt            | Boolean           | true     | false            |                   | Met à jour les objets SmartArt vers la dernière version. |
| EncryptDocumentProperties | Boolean           | true     | false            |                   | Chiffre les propriétés du document dans le fichier de sortie. |

## Propriétés de PclSaveOptions

| Nom de la propriété       | Type de propriété | Nullable | En lecture seule | Valeur par défaut | Description                                          |
| ------------------------- | ----------------- | -------- | ---------------- | ----------------- | ---------------------------------------------------- |
| fontFullName              | String            | true     | false            |                   | Nom complet de la police à utiliser.                |
| fontPclName               | String            | true     | false            |                   | Nom de police spécifique PCL.                       |
| SaveFormat                | String            | true     | false            |                   | Identifiant de format pour les fichiers PCL.         |
| CachedFileFolder          | String            | true     | false            |                   | Dossier utilisé pour les fichiers temporaires mis en cache. |
| ClearData                 | Boolean           | true     | false            |                   | Efface les données existantes avant la sauvegarde.   |
| CreateDirectory           | Boolean           | true     | false            |                   | Crée le dossier cible s’il n’existe pas.             |
| EnableHttpCompression     | Boolean           | true     | false            |                   | Active la compression HTTP pour la réponse.          |
| RefreshChartCache         | Boolean           | true     | false            |                   | Actualise les données mises en cache des graphiques avant la sauvegarde. |
| SortNames                 | Boolean           | true     | false            |                   | Trie les plages nommées par ordre alphabétique.      |
| ValidateMergedAreas       | Boolean           | true     | false            |                   | Valide la cohérence des cellules fusionnées.         |
| MergeAreas                | Boolean           | true     | false            |                   | Fusionne les cellules adjacentes si possible.        |
| SortExternalNames         | Boolean           | true     | false            |                   | Trie les références nommées externes.                 |
| CheckExcelRestriction     | Boolean           | true     | false            |                   | Applique les limites spécifiques à Excel pendant la conversion. |
| UpdateSmartArt            | Boolean           | true     | false            |                   | Met à jour les objets SmartArt vers la dernière version. |
| EncryptDocumentProperties | Boolean           | true     | false            |                   | Chiffre les propriétés du document dans le fichier de sortie. |

## Propriétés de PDFSaveOptions

| Nom de la propriété       | Type de propriété | Nullable | En lecture seule | Valeur par défaut | Description                                            |
| ------------------------- | ----------------- | -------- | ---------------- | ----------------- | ------------------------------------------------------ |
| DisplayDocTitle           | Boolean           | true     | false            |                   | Utilise le titre du document comme titre PDF.          |
| ExportDocumentStructure   | Boolean           | true     | false            |                   | Préserve la structure logique du document.             |
| EmfRenderSetting          | String            | true     | false            |                   | Paramètres de rendu des images EMF.                    |
| CustomPropertiesExport    | String            | true     | false            |                   | Contrôle l’export des propriétés personnalisées du document. |
| OptimizationType          | String            | true     | false            |                   | Type d’optimisation PDF (par exemple, Size, Speed).    |
| Producer                  | String            | true     | false            |                   | Nom de l’application productrice du PDF.               |
| PDFCompression            | String            | true     | false            |                   | Algorithme de compression pour les flux PDF.           |
| FontEncoding              | String            | true     | false            |                   | Encodage utilisé pour les polices intégrées.           |
| Watermark                 | Class             | true     | false            |                   | Paramètres de filigrane appliqués au PDF.              |
| CalculateFormula          | Boolean           | true     | false            |                   | Calcule les formules avant l’export.                   |
| CheckFontCompatibility    | Boolean           | true     | false            |                   | Valide la compatibilité des polices pour le rendu PDF. |
| Compliance                | String            | true     | false            |                   | Niveau de conformité PDF/A ou PDF/X.                   |
| DefaultFont               | String            | true     | false            |                   | Police utilisée lorsqu’une police source n’est pas disponible. |
| OnePagePerSheet           | Boolean           | true     | false            |                   | Place chaque feuille de calcul sur une page PDF séparée. |
| PrintingPageType          | String            | true     | false            |                   | Spécifie le type de page pour l’impression.            |
| SecurityOptions           | Class             | true     | false            |                   | Paramètres de sécurité tels que mots de passe et autorisations. |
| desiredPPI                | Integer           | true     | false            |                   | Résolution souhaitée en pixels par pouce (PPI).        |
| jpegQuality               | Integer           | true     | false            |                   | Qualité d’image JPEG (0‑100).                          |
| ImageType                 | String            | true     | false            |                   | Type d’image utilisé pour la rasterisation.            |
| SaveFormat                | String            | true     | false            |                   | Identifiant de format pour les fichiers PDF.           |
| CachedFileFolder          | String            | true     | false            |                   | Dossier utilisé pour les fichiers temporaires mis en cache. |
| ClearData                 | Boolean           | true     | false            |                   | Efface les données existantes avant la sauvegarde.     |
| CreateDirectory           | Boolean           | true     | false            |                   | Crée le dossier cible s’il n’existe pas.               |
| EnableHttpCompression     | Boolean           | true     | false            |                   | Active la compression HTTP pour la réponse.            |
| RefreshChartCache         | Boolean           | true     | false            |                   | Actualise les données mises en cache des graphiques avant la sauvegarde. |
| SortNames                 | Boolean           | true     | false            |                   | Trie les plages nommées par ordre alphabétique.        |
| ValidateMergedAreas       | Boolean           | true     | false            |                   | Valide la cohérence des cellules fusionnées.           |
| MergeAreas                | Boolean           | true     | false            |                   | Fusionne les cellules adjacentes si possible.          |
| SortExternalNames         | Boolean           | true     | false            |                   | Trie les références nommées externes.                   |
| CheckExcelRestriction     | Boolean           | true     | false            |                   | Applique les limites spécifiques à Excel pendant la conversion. |
| UpdateSmartArt            | Boolean           | true     | false            |                   | Met à jour les objets SmartArt vers la dernière version. |
| EncryptDocumentProperties | Boolean           | true     | false            |                   | Chiffre les propriétés du document dans le fichier de sortie. |

## Propriétés de PptxSaveOptions

| Nom de la propriété               | Type de propriété | Nullable | En lecture seule | Valeur par défaut | Description                                             |
| --------------------------------- | ----------------- | -------- | ---------------- | ----------------- | ------------------------------------------------------- |
| IgnoreHiddenRows                  | Boolean           | true     | false            |                   | Ignore les lignes masquées pendant l’export.            |
| AdjustFontSizeForRowType          | String            | true     | false            |                   | Contrôle l’ajustement de la taille de police selon le type de ligne. |
| ExportViewType                    | String            | true     | false            |                   | Détermine la vue à exporter (diapositive, notes).       |
| DefaultFont                       | String            | true     | false            |                   | Police utilisée lorsqu’une police source n’est pas disponible. |
| CheckWorkbookDefaultFont          | Boolean           | true     | false            |                   | Vérifie si la police par défaut du classeur est appliquée. |
| CheckFontCompatibility            | Boolean           | true     | false            |                   | Valide la compatibilité des polices pour le format cible. |
| IsFontSubstitutionCharGranularity | Boolean           | true     | false            |                   | Contrôle la substitution de police au niveau des caractères. |
| OnePagePerSheet                   | Boolean           | true     | false            |                   | Place chaque feuille de calcul sur une diapositive séparée. |
| AllColumnsInOnePagePerSheet       | Boolean           | true     | false            |                   | Adapte toutes les colonnes d’une feuille sur une seule diapositive. |
| IgnoreError                       | Boolean           | true     | false            |                   | Ignore les erreurs non critiques pendant la conversion. |
| OutputBlankPageWhenNothingToPrint | Boolean           | true     | false            |                   | Génère une diapositive vide s’il n’y a rien à rendre.    |
| PageIndex                         | Integer           | true     | false            |                   | Index de la première diapositive à exporter.            |
| PageCount                         | Integer           | true     | false            |                   | Nombre de diapositives à exporter.                      |
| PrintingPageType                  | String            | true     | false            |                   | Spécifie le type de page pour l’impression.              |
| GridlineType                      | String            | true     | false            |                   | Détermine le rendu des traits de grille.                 |
| TextCrossType                     | String            | true     | false            |                   | Définit le type de croisement pour le rendu du texte.    |
| DefaultEditLanguage               | String            | true     | false            |                   | Langue par défaut pour l’édition de texte.               |
| EmfRenderSetting                  | String            | true     | false            |                   | Paramètres de rendu EMF.                                 |
| MergeAreas                        | Boolean           | true     | false            |                   | Fusionne les cellules adjacentes si possible.            |
| SortExternalNames                 | Boolean           | true     | false            |                   | Trie les références nommées externes.                    |
| UpdateSmartArt                    | Boolean           | true     | false            |                   | Met à jour les objets SmartArt vers la dernière version. |
| SaveFormat                        | String            | true     | false            |                   | Identifiant de format pour les fichiers PPTX.            |
| CachedFileFolder                  | String            | true     | false            |                   | Dossier utilisé pour les fichiers temporaires mis en cache. |
| ClearData                         | Boolean           | true     | false            |                   | Efface les données existantes avant la sauvegarde.       |
| CreateDirectory                   | Boolean           | true     | false            |                   | Crée le dossier cible s’il n’existe pas.                 |
| EnableHttpCompression             | Boolean           | true     | false            |                   | Active la compression HTTP pour la réponse.              |
| RefreshChartCache                 | Boolean           | true     | false            |                   | Actualise les données mises en cache des graphiques avant la sauvegarde. |
| SortNames                         | Boolean           | true     | false            |                   | Trie les plages nommées par ordre alphabétique.          |
| ValidateMergedAreas               | Boolean           | true     | false            |                   | Valide la cohérence des cellules fusionnées.             |
| CheckExcelRestriction             | Boolean           | true     | false            |                   | Applique les limites spécifiques à Excel pendant la conversion. |
| EncryptDocumentProperties         | Boolean           | true     | false            |                   | Chiffre les propriétés du document dans le fichier de sortie. |

## Propriétés de SqlScriptSaveOptions

| Nom de la propriété       | Type de propriété | Nullable | En lecture seule | Valeur par défaut | Description                                               |
| ------------------------- | ----------------- | -------- | ---------------- | ----------------- | --------------------------------------------------------- |
| CheckIfTableExists        | Boolean           | true     | false            |                   | Vérifie si la table cible existe déjà.                    |
| ColumnTypeMap             | String            | true     | false            |                   | Mappage des noms de colonnes vers les types de données SQL. |
| CheckAllDataForColumnType | Boolean           | true     | false            |                   | Analyse toutes les lignes pour déduire les types de colonnes. |
| AddBlankLineBetweenRows   | Boolean           | true     | false            |                   | Insère une ligne vide entre les lignes générées.          |
| Separator                 | String            | true     | false            |                   | Chaîne utilisée pour séparer les colonnes (par exemple, virgule, tabulation). |
| OperatorType              | String            | true     | false            |                   | Opérateur SQL utilisé (INSERT, UPDATE, etc.).             |
| PrimaryKey                | Integer           | true     | false            |                   | Index de colonne servant de clé primaire.                 |
| CreateTable               | Boolean           | true     | false            |                   | Génère une instruction CREATE TABLE.                      |
| IdName                    | String            | true     | false            |                   | Nom de la colonne d’identifiant.                          |
| StartId                   | Integer           | true     | false            |                   | Valeur initiale pour les identifiants auto‑incrémentés.   |
| TableName                 | String            | true     | false            |                   | Nom de la table de base de données cible.                 |
| ExportAsString            | Boolean           | true     | false            |                   | Exporte toutes les valeurs sous forme de chaînes.         |
| ExportArea                | Class             | true     | false            |                   | Définit la zone de feuille de calcul à exporter.          |
| HasHeaderRow              | Boolean           | true     | false            |                   | Indique si la première ligne contient des en‑têtes de colonne. |
| SaveFormat                | String            | true     | false            |                   | Identifiant de format pour les fichiers de script SQL.   |
| CachedFileFolder          | String            | true     | false            |                   | Dossier utilisé pour les fichiers temporaires mis en cache. |
| ClearData                 | Boolean           | true     | false            |                   | Efface les données existantes avant la sauvegarde.        |
| CreateDirectory           | Boolean           | true     | false            |                   | Crée le dossier cible s’il n’existe pas.                  |
| EnableHttpCompression     | Boolean           | true     | false            |                   | Active la compression HTTP pour la réponse.               |
| RefreshChartCache         | Boolean           | true     | false            |                   | Actualise les données mises en cache des graphiques avant la sauvegarde. |
| SortNames                 | Boolean           | true     | false            |                   | Trie les plages nommées par ordre alphabétique.           |
| ValidateMergedAreas       | Boolean           | true     | false            |                   | Valide la cohérence des cellules fusionnées.              |
| MergeAreas                | Boolean           | true     | false            |                   | Fusionne les cellules adjacentes si possible.             |
| SortExternalNames         | Boolean           | true     | false            |                   | Trie les références nommées externes.                     |
| CheckExcelRestriction     | Boolean           | true     | false            |                   | Applique les limites spécifiques à Excel pendant la conversion. |
| UpdateSmartArt            | Boolean           | true     | false            |                   | Met à jour les objets SmartArt vers la dernière version.  |
| EncryptDocumentProperties | Boolean           | true     | false            |                   | Chiffre les propriétés du document dans le fichier de sortie. |

## Propriétés de SvgSaveOptions

| Nom de la propriété       | Type de propriété | Nullable | En lecture seule | Valeur par défaut | Description                                          |
| ------------------------- | ----------------- | -------- | ---------------- | ----------------- | ---------------------------------------------------- |
| SheetIndex                | Integer           | true     | false            |                   | Index de la feuille de calcul à exporter.           |
| ChartImageType            | String            | true     | false            |                   | Format d’image utilisé pour le rendu des graphiques. |
| EmbeddedImageNameInSvg    | String            | true     | false            |                   | Nom attribué aux images intégrées dans la sortie SVG. |
| HorizontalResolution      | Integer           | true     | false            |                   | Résolution horizontale (DPI) du SVG exporté.        |
| ImageFormat               | String            | true     | false            |                   | Format d’image cible pour les éléments rasterisés.  |
| IsCellAutoFit             | Boolean           | true     | false            |                   | Ajuste automatiquement le contenu des cellules à la taille du SVG. |
| OnePagePerSheet           | Boolean           | true     | false            |                   | Rend chaque feuille de calcul sur une page SVG séparée. |
| OnlyArea                  | Boolean           | true     | false            |                   | Exporte uniquement la zone définie de la feuille de calcul. |
| PrintingPage              | String            | true     | false            |                   | Mise en page utilisée pour l’impression.            |
| PrintWithStatusDialog     | Boolean           | true     | false            |                   | Affiche une boîte de dialogue d’état pendant l’impression. |
| Quality                   | Integer           | true     | false            |                   | Qualité de compression pour les images rasterisées. |
| TiffCompression           | String            | true     | false            |                   | Type de compression pour les images TIFF intégrées dans le SVG. |
| VerticalResolution        | Integer           | true     | false            |                   | Résolution verticale (DPI) du SVG exporté.          |
| SaveFormat                | String            | true     | false            |                   | Identifiant de format pour les fichiers SVG.         |
| CachedFileFolder          | String            | true     | false            |                   | Dossier utilisé pour les fichiers temporaires mis en cache. |
| ClearData                 | Boolean           | true     | false            |                   | Efface les données existantes avant la sauvegarde.   |
| CreateDirectory           | Boolean           | true     | false            |                   | Crée le dossier cible s’il n’existe pas.             |
| EnableHttpCompression     | Boolean           | true     | false            |                   | Active la compression HTTP pour la réponse.          |
| RefreshChartCache         | Boolean           | true     | false            |                   | Actualise les données mises en cache des graphiques avant la sauvegarde. |
| SortNames                 | Boolean           | true     | false            |                   | Trie les plages nommées par ordre alphabétique.      |
| ValidateMergedAreas       | Boolean           | true     | false            |                   | Valide la cohérence des cellules fusionnées.         |
| MergeAreas                | Boolean           | true     | false            |                   | Fusionne les cellules adjacentes si possible.        |
| SortExternalNames         | Boolean           | true     | false            |                   | Trie les références nommées externes.                 |
| CheckExcelRestriction     | Boolean           | true     | false            |                   | Applique les limites spécifiques à Excel pendant la conversion. |
| UpdateSmartArt            | Boolean           | true     | false            |                   | Met à jour les objets SmartArt vers la dernière version. |
| EncryptDocumentProperties | Boolean           | true     | false            |                   | Chiffre les propriétés du document dans le fichier de sortie. |

## Propriétés de TxtSaveOptions

| Nom de la propriété       | Type de propriété | Nullable | En lecture seule | Valeur par défaut | Description                                                              |
| ------------------------- | ----------------- | -------- | ---------------- | ----------------- | ------------------------------------------------------------------------ |
| QuoteType                 | String            | true     | false            |                   | Type de guillemet utilisé (par exemple, double, simple).                |
| Separator                 | String            | true     | false            |                   | Caractère séparateur de colonnes (par exemple, virgule, tabulation).     |
| SeparatorString           | String            | true     | false            |                   | Chaîne complète utilisée comme séparateur si plusieurs caractères sont nécessaires. |
| AlwaysQuoted              | Boolean           | true     | false            |                   | Force tous les champs à être mis entre guillemets.                      |
| SaveFormat                | String            | true     | false            |                   | Identifiant de format pour les fichiers TXT.                            |
| CachedFileFolder          | String            | true     | false            |                   | Dossier utilisé pour les fichiers temporaires mis en cache.             |
| ClearData                 | Boolean           | true     | false            |                   | Efface les données existantes avant la sauvegarde.                      |
| CreateDirectory           | Boolean           | true     | false            |                   | Crée le dossier cible s’il n’existe pas.                                |
| EnableHttpCompression     | Boolean           | true     | false            |                   | Active la compression HTTP pour la réponse.                             |
| RefreshChartCache         | Boolean           | true     | false            |                   | Actualise les données mises en cache des graphiques avant la sauvegarde. |
| SortNames                 | Boolean           | true     | false            |                   | Trie les plages nommées par ordre alphabétique.                         |
| ValidateMergedAreas       | Boolean           | true     | false            |                   | Valide la cohérence des cellules fusionnées.                            |
| MergeAreas                | Boolean           | true     | false            |                   | Fusionne les cellules adjacentes si possible.                           |
| SortExternalNames         | Boolean           | true     | false            |                   | Trie les références nommées externes.                                    |
| CheckExcelRestriction     | Boolean           | true     | false            |                   | Applique les limites spécifiques à Excel pendant la conversion.         |
| UpdateSmartArt            | Boolean           | true     | false            |                   | Met à jour les objets SmartArt vers la dernière version.                |
| EncryptDocumentProperties | Boolean           | true     | false            |                   | Chiffre les propriétés du document dans le fichier de sortie.           |

## Propriétés de XlsSaveOptions & XlsbSaveOptions

| Nom de la propriété       | Type de propriété | Nullable | En lecture seule | Valeur par défaut | Description                                          |
| ------------------------- | ----------------- | -------- | ---------------- | ----------------- | ---------------------------------------------------- |
| MatchColor                | Boolean           | true     | false            |                   | Préserve les couleurs exactes des cellules pendant l’export. |
| WpsCompatibility          | Boolean           | true     | false            |                   | Active la compatibilité avec WPS Office.            |
| SaveFormat                | String            | true     | false            |                   | Identifiant de format pour les fichiers XLS/XLSB.    |
| CachedFileFolder          | String            | true     | false            |                   | Dossier utilisé pour les fichiers temporaires mis en cache. |
| ClearData                 | Boolean           | true     | false            |                   | Efface les données existantes avant la sauvegarde.   |
| CreateDirectory           | Boolean           | true     | false            |                   | Crée le dossier cible s’il n’existe pas.             |
| EnableHttpCompression     | Boolean           | true     | false            |                   | Active la compression HTTP pour la réponse.          |
| RefreshChartCache         | Boolean           | true     | false            |                   | Actualise les données mises en cache des graphiques avant la sauvegarde. |
| SortNames                 | Boolean           | true     | false            |                   | Trie les plages nommées par ordre alphabétique.      |
| ValidateMergedAreas       | Boolean           | true     | false            |                   | Valide la cohérence des cellules fusionnées.         |
| MergeAreas                | Boolean           | true     | false            |                   | Fusionne les cellules adjacentes si possible.        |
| SortExternalNames         | Boolean           | true     | false            |                   | Trie les références nommées externes.                 |
| CheckExcelRestriction     | Boolean           | true     | false            |                   | Applique les limites spécifiques à Excel pendant la conversion. |
| UpdateSmartArt            | Boolean           | true     | false            |                   | Met à jour les objets SmartArt vers la dernière version. |
| EncryptDocumentProperties | Boolean           | true     | false            |                   | Chiffre les propriétés du document dans le fichier de sortie. |

## Propriétés de XmlSaveOptions

| Nom de la propriété       | Type de propriété | Nullable | En lecture seule | Valeur par défaut | Description                                               |
| ------------------------- | ----------------- | -------- | ---------------- | ----------------- | --------------------------------------------------------- |
| SheetIndexes              | Array             | true     | false            |                   | Liste des index de feuilles de calcul à inclure dans l’export. |
| ExportArea                | Class             | true     | false            |                   | Définit la zone de feuille de calcul à exporter.          |
| HasHeaderRow              | Boolean           | true     | false            |                   | Indique si la première ligne contient des en‑têtes de colonne. |
| XmlMapName                | String            | true     | false            |                   | Nom de la carte XML appliquée à la feuille de calcul.     |
| SheetNameAsElementName    | Boolean           | true     | false            |                   | Utilise le nom de la feuille comme nom d’élément XML.      |
| DataAsAttribute           | Boolean           | true     | false            |                   | Exporte les données de cellule en tant qu’attributs XML au lieu d’éléments. |
| SaveFormat                | String            | true     | false            |                   | Identifiant de format pour les fichiers XML.              |
| CachedFileFolder          | String            | true     | false            |                   | Dossier utilisé pour les fichiers temporaires mis en cache. |
| ClearData                 | Boolean           | true     | false            |                   | Efface les données existantes avant la sauvegarde.        |
| CreateDirectory           | String            | true     | false            |                   | Crée le dossier cible s’il n’existe pas.                  |
| EnableHttpCompression     | Boolean           | true     | false            |                   | Active la compression HTTP pour la réponse.               |
| RefreshChartCache         | Boolean           | true     | false            |                   | Actualise les données mises en cache des graphiques avant la sauvegarde. |
| SortNames                 | Boolean           | true     | false            |                   | Trie les plages nommées par ordre alphabétique.           |
| ValidateMergedAreas       | Boolean           | true     | false            |                   | Valide la cohérence des cellules fusionnées.              |
| MergeAreas                | Boolean           | true     | false            |                   | Fusionne les cellules adjacentes si possible.             |
| SortExternalNames         | Boolean           | true     | false            |                   | Trie les références nommées externes.                     |
| CheckExcelRestriction     | Boolean           | true     | false            |                   | Applique les limites spécifiques à Excel pendant la conversion. |
| UpdateSmartArt            | Boolean           | true     | false            |                   | Met à jour les objets SmartArt vers la dernière version.  |
| EncryptDocumentProperties | Boolean           | true     | false            |                   | Chiffre les propriétés du document dans le fichier de sortie. |

## Propriétés de XpsSaveOptions

| Nom de la propriété               | Type de propriété | Nullable | En lecture seule | Valeur par défaut | Description                                             |
| --------------------------------- | ----------------- | -------- | ---------------- | ----------------- | ------------------------------------------------------- |
| DefaultFont                       | String            | true     | false            |                   | Police utilisée lorsqu’une police source n’est pas disponible. |
| CheckWorkbookDefaultFont          | Boolean           | true     | false            |                   | Vérifie si la police par défaut du classeur est appliquée. |
| CheckFontCompatibility            | Boolean           | true     | false            |                   | Valide la compatibilité des polices pour le format cible. |
| IsFontSubstitutionCharGranularity | Boolean           | true     | false            |                   | Contrôle la substitution de police au niveau des caractères. |
| OnePagePerSheet                   | Boolean           | true     | false            |                   | Place chaque feuille de calcul sur une page XPS séparée. |
| AllColumnsInOnePagePerSheet       | Boolean           | true     | false            |                   | Adapte toutes les colonnes d’une feuille sur une seule page. |
| IgnoreError                       | Boolean           | true     | false            |                   | Ignore les erreurs non critiques pendant la conversion. |
| OutputBlankPageWhenNothingToPrint | Boolean           | true     | false            |                   | Génère une page vide s’il n’y a rien à rendre.           |
| PageIndex                         | Integer           | true     | false            |                   | Index de la première page à exporter.                    |
| PageCount                         | Integer           | true     | false            |                   | Nombre de pages à exporter.                              |
| PrintingPageType                  | String            | true     | false            |                   | Spécifie le type de page pour l’impression.              |
| GridlineType                      | String            | true     | false            |                   | Détermine le rendu des traits de grille.                 |
| TextCrossType                     | String            | true     | false            |                   | Définit le type de croisement pour le rendu du texte.    |
| DefaultEditLanguage               | String            | true     | false            |                   | Langue par défaut pour l’édition de texte.               |
| EmfRenderSetting                  | String            | true     | false            |                   | Paramètres de rendu EMF.                                 |
| MergeAreas                        | Boolean           | true     | false            |                   | Fusionne les cellules adjacentes si possible.            |
| SortExternalNames                 | Boolean           | true     | false            |                   | Trie les références nommées externes.                    |
| UpdateSmartArt                    | Boolean           | true     | false            |                   | Met à jour les objets SmartArt vers la dernière version. |
| SaveFormat                        | String            | true     | false            |                   | Identifiant de format pour les fichiers XPS.             |
| CachedFileFolder                  | String            | true     | false            |                   | Dossier utilisé pour les fichiers temporaires mis en cache. |
| ClearData                         | Boolean           | true     | false            |                   | Efface les données existantes avant la sauvegarde.       |
| CreateDirectory                   | Boolean           | true     | false            |                   | Crée le dossier cible s’il n’existe pas.                 |
| EnableHttpCompression             | Boolean           | true     | false            |                   | Active la compression HTTP pour la réponse.              |
| RefreshChartCache                 | Boolean           | true     | false            |                   | Actualise les données mises en cache des graphiques avant la sauvegarde. |
| SortNames                         | Boolean           | true     | false            |                   | Trie les plages nommées par ordre alphabétique.          |
| ValidateMergedAreas               | Boolean           | true     | false            |                   | Valide la cohérence des cellules fusionnées.             |
| CheckExcelRestriction             | Boolean           | true     | false            |                   | Applique les limites spécifiques à Excel pendant la conversion. |
| EncryptDocumentProperties         | Boolean           | true     | false            |                   | Chiffre les propriétés du document dans le fichier de sortie. |
---