---
title: "Mettre à jour une forme sur une feuille de calcul Excel"
second_title: "Document"
linktitle: "Mettre à jour"
type: docs
url: /shapes/update/
aliases: [/update-a-shape-inside-the-worksheet/]
keywords: "mettre à jour une forme via l’API Excel, Aspose.Cells Cloud, mise à jour de forme Excel, API REST, SDK, C#, Java, Python, Node.js, Go, Ruby, PHP, Perl, Swift"
description: "Découvrez comment mettre à jour une forme sur une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut l’endpoint HTTPS, les détails d’authentification, le schéma DTO, un guide pas à pas, un exemple cURL et des extraits de code SDK pour plusieurs langages."
ArticleTitle: "Mettre à jour une forme sur une feuille de calcul Excel – API Aspose.Cells Cloud"
weight: 31
---

Cet API REST permet de mettre à jour une forme sur une feuille de calcul Excel.

## Sécurité et authentification

Les API REST Aspose.Cells Cloud sont sécurisées et nécessitent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes/{shapeindex}
```

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description                                                                              |
| ---------------- | ------- | ----------- | ---------------------------------------------------------------------------------------- |
| **name**         | string  | path        | Le nom du fichier classeur.                                                              |
| **sheetName**    | string  | path        | Le nom de la feuille de calcul contenant la forme.                                      |
| **shapeindex**   | integer | path        | L’index de la forme (à partir de 0) au sein de la feuille de calcul.                    |
| **dto**          | object  | body        | L’objet de transfert de données (DTO) contenant les propriétés mises à jour (voir *Schéma DTO* ci-dessous). |
| **folder**       | string  | query       | Le dossier dans lequel le classeur est stocké.                                          |
| **storageName**  | string  | query       | Le nom du stockage Aspose Cloud.                                                        |

### Schéma DTO

L’objet `dto` contient les propriétés modifiables. Tous les champs sont facultatifs sauf mention contraire.

| Champ                | Type    | Obligatoire | Description                                                                 |
| -------------------- | ------- | ----------- | --------------------------------------------------------------------------- |
| **Name**             | string  | Non         | Nouveau nom de la forme.                                                    |
| **UpperLeftRow**     | integer | Non         | Indice de ligne du coin supérieur gauche de la forme.                       |
| **UpperLeftColumn**  | integer | Non         | Indice de colonne du coin supérieur gauche de la forme.                     |
| **Width**            | integer | Non         | Largeur de la forme (en points).                                            |
| **Height**           | integer | Non         | Hauteur de la forme (en points).                                            |
| **RotationAngle**    | integer | Non         | Angle de rotation en degrés.                                                |
| **IsHidden**         | boolean | Non         | `true` pour masquer la forme.                                               |
| **IsLocked**         | boolean | Non         | `true` pour verrouiller la forme.                                           |
| **Font**             | object  | Non         | Paramètres de police (voir la spécification OpenAPI pour les sous-propriétés). |
| **...**              | …       | Non         | Autres propriétés telles que `HtmlText`, `AlternativeText`, `ZOrderPosition`, etc. |

> Pour une liste complète, consultez la spécification OpenAPI officielle : <https://apireference.aspose.cloud/cells/#/Shapes/PostWorksheetShape>.

### En-têtes de la requête

- `Content-Type: application/json`
- `Accept: application/json`
- `Authorization: Bearer <accessToken>` _(le jeton JWT obtenu lors de l’authentification)_

### Corps de la requête (exemple)

```json
{
  "Name": "MyShape",
  "UpperLeftRow": 2,
  "UpperLeftColumn": 3,
  "Width": 150,
  "Height": 80,
  "RotationAngle": 0,
  "IsHidden": false,
  "IsLocked": false,
  "Font": {
    "Name": "Calibri",
    "Size": 12,
    "IsBold": true,
    "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }
  }
}
```

## Exemple avec cURL (outil en ligne de commande)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes/0?folder=Temp" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <accessToken>" \
  -d '{
        "Name": "UpdatedShape",
        "UpperLeftRow": 1,
        "UpperLeftColumn": 1,
        "Width": 120,
        "Height": 60,
        "IsHidden": false,
        "IsLocked": false
      }'
```

### Réponse

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Gestion des erreurs** – L’API peut renvoyer les codes HTTP suivants :

| Code | Signification           | Cause typique                                                   |
| ---- | ----------------------- | --------------------------------------------------------------- |
| 400  | Bad Request (Requête incorrecte) | Payload JSON invalide ou champs obligatoires manquants.        |
| 401  | Unauthorized (Non autorisé)      | Jeton JWT manquant ou invalide.                                 |
| 404  | Not Found (Introuvable)          | Le classeur, la feuille de calcul ou l’index de forme n’existe pas. |
| 500  | Internal Server Error (Erreur interne) | Problème inattendu côté serveur.                              |

**Exemples de réponses d’erreur**

*400 – Bad Request*

```json
{
  "Code": 400,
  "Message": "Invalid request payload. 'Name' field exceeds maximum length."
}
```

*401 – Unauthorized*

```json
{
  "Code": 401,
  "Message": "Authentication failed. Invalid or expired JWT token."
}
```

*404 – Not Found*

```json
{
  "Code": 404,
  "Message": "The specified workbook, worksheet, or shape index was not found."
}
```

*500 – Internal Server Error*

```json
{
  "Code": 500,
  "Message": "An unexpected error occurred on the server."
}
```

## Famille de SDK Cloud

L’utilisation d’un SDK est la méthode recommandée pour accélérer le développement. Un SDK gère les détails de bas niveau, vous permettant de vous concentrer sur vos tâches de projet. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent l’appel des services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}
---