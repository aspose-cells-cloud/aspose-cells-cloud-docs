---
---
title: "AutoFitterOptions – Guide des propriétés et d’utilisation | API Aspose.Cells Cloud"
second_title: "Document"
linktitle: "AutoFitterOptions"
type: docs
url: /fr/auto-fitter-options/
keywords: "AutoFitterOptions, Aspose.Cells, ajustement automatique Excel, hauteur de ligne, cellules fusionnées, API"
description: "Découvrez comment contrôler l’ajustement automatique de la hauteur des lignes, la gestion des cellules fusionnées, les lignes/colonnes masquées, les paramètres linguistiques et les options de rendu à l’aide de l’objet AutoFitterOptions dans l’API Aspose.Cells Cloud."
weight: 79
ArticleTitle: "AutoFitterOptions – Guide des propriétés et d’utilisation pour Aspose.Cells Cloud"
---

# Propriétés d’AutoFitterOptions

L’objet `AutoFitterOptions` vous permet d’ajuster finement le réglage automatique de la hauteur des lignes effectué par Aspose.Cells Cloud. Il est particulièrement utile lorsque vous avez besoin d’un contrôle précis sur la gestion des cellules fusionnées, des lignes/colonnes masquées, du formatage spécifique à une langue ou encore du comportement spécifique au rendu.

**Prérequis** – Pour utiliser ces options, vous devez être authentifié avec un jeton d’accès OAuth 2.0 valide incluant la portée **Cells.ReadWrite**. La requête fonctionne avec toute version du SDK prenant en charge l’API v3.0.

| Nom                              | Type        | Description                                                                                       | Notes                                                                                                             |
| -------------------------------- | ----------- | ------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| **AutoFitMergedCellsType**       | **string**  | Détermine comment les cellules fusionnées sont ajustées automatiquement.                         | Valeurs autorisées : `All`, `First`, `None`. Valeur par défaut : `All`. Exemple JSON : `"AutoFitMergedCellsType":"All"` |
| **IgnoreHidden**                 | **boolean** | Si **true**, les lignes et colonnes masquées sont ignorées pendant le processus d’ajustement.    | Valeur par défaut : `false`. Exemple JSON : `"IgnoreHidden":false`                                                |
| **OnlyAuto**                     | **boolean** | Indique si seules les lignes dont la hauteur n’est pas personnalisée manuellement doivent être ajustées automatiquement. | Valeur par défaut : `false`. Exemple JSON : `"OnlyAuto":false`                                                    |
| **DefaultEditLanguage**          | **string**  | Définit la langue d’édition par défaut pour le classeur.                                         | Valeur par défaut : langue du système (ex. `"fr-FR"`). Exemple JSON : `"DefaultEditLanguage":"en-US"`             |
| **MaxRowHeight**                 | **double**  | Hauteur maximale de ligne (en points) appliquée lors de l’ajustement automatique. Une valeur de **0** signifie aucune limite. | Valeur par défaut : `0`. Exemple JSON : `"MaxRowHeight":0`                                                        |
| **AutoFitWrappedTextType**       | **string**  | Contrôle comment le texte retaillé dans les cellules est ajusté automatiquement.                | Valeurs autorisées : `All`, `OnlyWrapped`, `None`. Valeur par défaut : `All`. Exemple JSON : `"AutoFitWrappedTextType":"All"` |
| **FormatStrategy**               | **string**  | Spécifie la stratégie de formatage utilisée lors de l’opération d’ajustement automatique.       | Valeurs courantes : `AutoFit`, `PreserveExisting`. Valeur par défaut : `AutoFit`. Exemple JSON : `"FormatStrategy":"AutoFit"` |
| **ForRendering**                 | **string**  | Indique si l’ajustement automatique doit être effectué dans un but de rendu (ex. PDF, image).    | Valeurs autorisées : `True`, `False`. Valeur par défaut : `False`. Exemple JSON : `"ForRendering":"False"`        |

Ci-dessous figure un exemple de charge utile JSON pouvant être envoyée à l’API lors de la configuration d’`AutoFitterOptions`.

```json
{
  "AutoFitMergedCellsType": "All",
  "IgnoreHidden": false,
  "OnlyAuto": false,
  "DefaultEditLanguage": "en-US",
  "MaxRowHeight": 0,
  "AutoFitWrappedTextType": "All",
  "FormatStrategy": "AutoFit",
  "ForRendering": "False"
}
```

Exemple de requête `cURL` permettant d’appliquer ces options à un classeur :

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/workbook/autoFitter" \
  -H "Authorization: Bearer {access_token}" \
  -H "Content-Type: application/json" \
  -d @autoFitterOptions.json
```

**Référence de l’endpoint**

| Méthode | URL                               | Paramètres requis              | Description                                                            |
|--------|-----------------------------------|--------------------------------|------------------------------------------------------------------------|
| PUT    | `/cells/workbook/autoFitter`      | `autoFitterOptions` (corps JSON) | Applique les `AutoFitterOptions` spécifiés au classeur cible.        |
| GET    | `/cells/workbook/autoFitter`      | *aucun*                        | Récupère les paramètres actuels d’`AutoFitterOptions` pour le classeur. |

**Paramètres de requête pour l’endpoint PUT**

| Paramètre                  | Type     | Requis | Description                                                            |
|----------------------------|----------|--------|------------------------------------------------------------------------|
| AutoFitMergedCellsType     | string   | Oui    | Façon dont les cellules fusionnées sont ajustées automatiquement (`All`, `First`, `None`). |
| IgnoreHidden               | boolean  | Non    | Indique si les lignes/colonnes masquées sont ignorées.                |
| OnlyAuto                   | boolean  | Non    | Ajuste uniquement les lignes dont la hauteur n’est pas personnalisée.  |
| DefaultEditLanguage        | string   | Non    | Langue d’édition (ex. `fr-FR`).                                        |
| MaxRowHeight               | double   | Non    | Hauteur maximale de ligne en points ; `0` = illimitée.                |
| AutoFitWrappedTextType     | string   | Non    | Gestion du texte retaillé (`All`, `OnlyWrapped`, `None`).             |
| FormatStrategy             | string   | Non    | Stratégie de formatage (`AutoFit`, `PreserveExisting`).               |
| ForRendering               | string   | Non    | Appliquer l’ajustement automatique pour le rendu (`True`, `False`).   |

Codes de réponse typiques :

- **200 OK** – Opération terminée avec succès.  
- **400 Bad Request** – Charge utile JSON invalide ou valeur non prise en charge.  
- **401 Unauthorized** – Jeton d’authentification manquant ou invalide.  
- **500 Internal Server Error** – Erreur serveur inattendue.

**Exemple de réponse GET**

```json
{
  "AutoFitMergedCellsType": "All",
  "IgnoreHidden": false,
  "OnlyAuto": false,
  "DefaultEditLanguage": "en-US",
  "MaxRowHeight": 0,
  "AutoFitWrappedTextType": "All",
  "FormatStrategy": "AutoFit",
  "ForRendering": "False"
}
```

Ces exemples illustrent comment configurer et invoquer le modèle `AutoFitterOptions` au sein de l’API Aspose.Cells Cloud.