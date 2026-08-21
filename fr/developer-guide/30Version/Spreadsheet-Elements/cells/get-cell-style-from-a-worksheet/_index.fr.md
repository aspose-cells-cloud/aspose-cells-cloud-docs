---
title: "Obtenir le style d'une cellule dans une feuille de calcul – API Aspose.Cells Cloud"
type: docs
url: /fr/get-cell-style-from-a-worksheet/
weight: 10
keywords: "Aspose.Cells, Excel, API REST, style de cellule, feuille de calcul, SDK cloud, documentation de l'API"
description: "Découvrez comment récupérer le style d'une cellule spécifique dans une feuille de calcul Excel à l'aide de l'API REST Aspose.Cells Cloud v3. Inclut un exemple cURL, le schéma de réponse, les codes de statut et des extraits de SDK."
ArticleTitle: "Obtenir le style d'une cellule dans une feuille de calcul à l’aide de l’API Aspose.Cells Cloud – Guide détaillé"
---

Utilisez cette API REST pour récupérer le **style** d'une cellule dans une feuille de calcul Excel.

## API GetWorksheetCellStyle

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/style
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/fr/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête


| Nom du paramètre | Type   | Emplacement | Description                                   |
| ---------------- | ------ | ----------- | --------------------------------------------- |
| name             | string | path        | Le nom du document Excel.                     |
| sheetName        | string | path        | Le nom de la feuille de calcul.               |
| cellName         | string | path        | L’adresse de la cellule (par exemple, A1).    |
| folder           | string | query       | Le dossier contenant le fichier.              |
| storageName      | string | query       | Le nom du stockage à utiliser.                |


### **Réponse**

```json
{
  "Style": {
    "Font": {
      "Color": { "A": 255, "R": 5, "G": 99, "B": 193 },
      "DoubleSize": 11,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Calibri",
      "Size": 11,
      "Underline": "Single"
    },
    "Name": null,
    "CultureCustom": "General",
    "Custom": "",
    "BackgroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "ForegroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "IsFormulaHidden": false,
    "IsDateTime": false,
    "IsTextWrapped": false,
    "IsGradient": false,
    "IsLocked": true,
    "IsPercent": false,
    "ShrinkToFit": false,
    "IndentLevel": 0,
    "Number": 0,
    "RotationAngle": 0,
    "Pattern": "None",
    "TextDirection": "Context",
    "VerticalAlignment": "Bottom",
    "HorizontalAlignment": "General",
    "BorderCollection": [
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "BottomBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalDown"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalUp"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Horizontal"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "LeftBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "RightBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "TopBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Vertical"
      }
    ],
    "BackgroundThemeColor": null,
    "ForegroundThemeColor": null,
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/cells/a1/style",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

**Codes de statut HTTP**

| Code | Signification                | Description                                               |
|------|------------------------------|-----------------------------------------------------------|
| 200  | OK                           | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte           | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                 | Jeton JWT invalide ou manquant.                           |
| 413  | Charge utile trop grande      | Le fichier téléchargé dépasse la limite de taille.       |
| 500  | Erreur interne du serveur    | Erreur inattendue sur le serveur.                         |

**Réponses d’erreur**  
Les charges utiles d’erreur typiques pour ce point de terminaison suivent le format standard d’erreur d’Aspose.Cells. Par exemple, une erreur 400 (Requête incorrecte) renvoie :

```json
{
  "Code": 400,
  "Message": "Paramètre 'cellName' non valide.",
  "Description": "Le nom de cellule fourni n'est pas au format A1 valide."
}
```

De même, une erreur 401 (Non autorisé) renvoie :

```json
{
  "Code": 401,
  "Message": "Échec de l'authentification.",
  "Description": "Le jeton JWT est manquant ou invalide."
}
```

## Comment utiliser l’API GetWorksheetCellStyle avec les SDK

### Spécification de l’API GetWorksheetCellStyle


La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCellStyle) définit une interface de programmation accessible publiquement et permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer un appel à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/a1/style" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton JWT>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Style": {
    "Font": {
      "Color": { "A": 255, "R": 5, "G": 99, "B": 193 },
      "DoubleSize": 11,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Calibri",
      "Size": 11,
      "Underline": "Single"
    },
    "Name": null,
    "CultureCustom": "General",
    "Custom": "",
    "BackgroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "ForegroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "IsFormulaHidden": false,
    "IsDateTime": false,
    "IsTextWrapped": false,
    "IsGradient": false,
    "IsLocked": true,
    "IsPercent": false,
    "ShrinkToFit": false,
    "IndentLevel": 0,
    "Number": 0,
    "RotationAngle": 0,
    "Pattern": "None",
    "TextDirection": "Context",
    "VerticalAlignment": "Bottom",
    "HorizontalAlignment": "General",
    "BorderCollection": [
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "BottomBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalDown"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalUp"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Horizontal"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "LeftBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "RightBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "TopBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Vertical"
      }
    ],
    "BackgroundThemeColor": null,
    "ForegroundThemeColor": null,
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/cells/a1/style",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Schéma de réponse

| Champ                    | Type    | Description                                                              |
| ------------------------ | ------- | ------------------------------------------------------------------------ |
| **Style**                | object  | Conteneur pour toutes les propriétés liées au style de la cellule.      |
| Style.Font               | object  | Paramètres de police (nom, taille, couleur, indicateurs de style).      |
| Style.Font.Color         | object  | Valeurs de couleur RGBA pour la police.                                  |
| Style.Font.IsBold        | boolean | `true` si la police est en gras.                                         |
| Style.Font.IsItalic      | boolean | `true` si la police est en italique.                                     |
| Style.Font.IsStrikeout   | boolean | `true` si la police est barrée.                                          |
| Style.Font.IsSubscript   | boolean | `true` si la police est en indice.                                       |
| Style.Font.IsSuperscript | boolean | `true` si la police est en exposant.                                     |
| Style.Font.Name          | string  | Nom de la famille de polices (par exemple, **Calibri**).                 |
| Style.Font.Size          | number  | Taille de la police en points.                                           |
| Style.Font.Underline     | string  | Style de soulignement (par exemple, **Single**).                         |
| Style.IsLocked           | boolean | Indique si la cellule est protégée contre les modifications.             |
| Style.IsTextWrapped      | boolean | `true` si le renvoi automatique du texte est activé.                     |
| Style.IsGradient         | boolean | `true` si un remplissage dégradé est appliqué.                           |
| Style.Pattern            | string  | Nom du motif de remplissage (par exemple, **None**).                     |
| Style.BorderCollection   | array   | Liste d’objets bordure définissant le style de ligne, la couleur et le type de bordure. |
| Style.BackgroundColor    | object  | Valeurs RGBA pour l’arrière-plan de la cellule.                          |
| Style.ForegroundColor    | object  | Valeurs RGBA pour le premier plan de la cellule.                         |
| …                        | …       | _(Les autres champs suivent le même schéma que défini dans la référence API.)_ |

### Utiliser les SDK Aspose.Cells Cloud

L'utilisation d'un SDK constitue la meilleure façon d'accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellStyle.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellStyle.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellStyle.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellStyle.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellStyle.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellStyle.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellStyle.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCellStyle.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Voir aussi**  
- [Définir le style d’une cellule](https://apireference.aspose.cloud/cells/#/Cells/SetWorksheetCellStyle)  
- [Obtenir la valeur d’une cellule](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell)
---