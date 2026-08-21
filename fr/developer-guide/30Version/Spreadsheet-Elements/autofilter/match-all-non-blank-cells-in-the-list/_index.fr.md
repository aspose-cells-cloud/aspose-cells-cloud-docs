---
title: "Correspondre à toutes les cellules non vides d'une feuille Excel"
second_title: "Document"
linktitle: "Correspondre à toutes les cellules non vides"
type: docs
url: /fr/autofilter/match-all-non-blank/
aliases: [/match-all-non-blank-cells-in-the-list/]
keywords: "Aspose.Cells Cloud, correspondre aux cellules non vides, AutoFilter, API Excel"
description: "Découvrez comment utiliser l’API REST Aspose.Cells Cloud pour correspondre à toutes les cellules non vides dans une liste AutoFilter d’une feuille Excel. Inclut l’endpoint, les paramètres, l’authentification, le schéma de réponse, les codes d’erreur et des exemples de SDK."
ArticleTitle: "Correspondre à toutes les cellules non vides d'une feuille Excel à l’aide de l’API Aspose.Cells Cloud"
weight: 100
---

**Vue d’ensemble**  
L’opération *Correspondre à toutes les cellules non vides* applique un filtre automatique (AutoFilter) à une feuille de calcul et retourne uniquement les lignes où la colonne spécifiée contient des données, en ignorant les cellules vides. Cette fonctionnalité est utile pour nettoyer des jeux de données, générer des rapports ou préparer les données pour une analyse ultérieure.

**Conditions préalables**  
- Un jeton JWT valide pour l’authentification auprès d’Aspose.Cells Cloud.  
- Le classeur doit être téléchargé dans le stockage Aspose Cloud.  
- Vous devez connaître le nom du fichier, le nom de la feuille de calcul et l’index de colonne (indexé à partir de zéro, `fieldIndex`) que vous souhaitez filtrer.

Cette API REST permet de correspondre à toutes les cellules non vides dans la liste AutoFilter d’une feuille Excel.

## API PostWorksheetMatchNonBlanks

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/matchNonBlanks
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description                                                    |
| ---------------- | ------- | ----------- | -------------------------------------------------------------- |
| name             | string  | chemin      | Le nom du fichier Excel.                                       |
| sheetName        | string  | chemin      | Le nom de la feuille de calcul contenant le filtre automatique. |
| fieldIndex       | integer | requête     | Index (à partir de zéro) de la colonne à laquelle le filtre est appliqué. |
| folder           | string  | requête     | _(Facultatif)_ Chemin du dossier où le fichier est stocké.    |
| storageName      | string  | requête     | _(Facultatif)_ Nom du service de stockage à utiliser.         |

### **Réponse**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                                    |
|------|-----------------------------|----------------------------------------------------------------|
| 200  | OK                          | Le filtre a été appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                               |
| 413  | Charge utile trop grande    | Le fichier téléchargé dépasse la taille limite.              |
| 500  | Erreur interne du serveur   | Erreur serveur inattendue.                                     |

*Exemple de réponse d’erreur (400)*  

```json
{
  "Code": 400,
  "Message": "Paramètre invalide : fieldIndex doit être un entier non négatif."
}
```

## Comment utiliser l’API PostWorksheetMatchNonBlanks avec les SDK

### Spécification de l’API PostWorksheetMatchNonBlanks

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PostWorksheetMatchNonBlanks) définit une interface de programmation publiquement accessible et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple ci-dessous montre comment effectuer des appels à l’API Cloud via cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/matchNonBlanks?fieldIndex=0" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK constitue la meilleure méthode pour accélérer le développement. Un SDK gère les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMatchNonBlanks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMatchNonBlanks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMatchNonBlanks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMatchNonBlanks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMatchNonBlanks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMatchNonBlanks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMatchNonBlanks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMatchNonBlanks.go" >}}

{{< /tab >}}

{{< /tabs >}}
---