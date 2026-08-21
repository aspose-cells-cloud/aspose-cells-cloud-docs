---
title: "Appliquer un formatage de texte enrichi à une cellule"
type: docs
url: /apply-rich-text-formatting-to-a-cell/
weight: 40
keywords: "Aspose.Cells, Excel, texte enrichi, formatage de cellule, API REST, Aspose.Cells Cloud"
description: "Découvrez comment appliquer un formatage de texte enrichi à une cellule spécifique d’un fichier Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut la syntaxe de la requête, les détails des paramètres, un exemple cURL et des extraits de code SDK."
ArticleTitle: "Appliquer un formatage de texte enrichi à une cellule à l’aide de l’API Aspose.Cells Cloud"
---

Cette API REST permet d’appliquer un **formatage de texte enrichi** à une cellule dans un fichier Excel.

**Prérequis :** Vous devez disposer d’un jeton JWT valide et le fichier Excel cible doit déjà exister dans le dossier de stockage spécifié avant d’invoquer cette opération.

**Contexte :** Le formatage du texte enrichi vous permet d’appliquer plusieurs styles de police au sein d’une seule cellule, permettant ainsi une présentation plus expressive des données dans les feuilles de calcul Excel.

## API PostCellCharacters

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/characters
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement                   | Description                                                                 |
|------------------|--------|-------------------------------|-----------------------------------------------------------------------------|
| name             | string | chemin (path)                 | Le nom du fichier Excel (par exemple, `Book1.xlsx`).                      |
| sheetName        | string | chemin (path)                 | La feuille de calcul contenant la cellule cible.                           |
| cellName         | string | chemin (path)                 | L’adresse de la cellule à formater (par exemple, `A1`).                    |
| options          | object | corps (body)                  | Objet JSON définissant les paramètres de formatage du texte enrichi pour la cellule.
| folder           | string | requête (query)               | Le dossier dans le stockage où se trouve le fichier Excel.                |
| storageName      | string | requête (query)               | Le nom du service de stockage (si un stockage personnalisé est utilisé).  |

### **Réponse**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                                  |
|------|-----------------------------|--------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte (Bad Request) | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé (Unauthorized) | Jeton JWT invalide ou manquant.                             |
| 413  | Payload trop volumineux (Payload Too Large) | Le fichier téléchargé dépasse la limite de taille.         |
| 500  | Erreur interne du serveur (Internal Server Error) | Erreur serveur inattendue.                                  |

## Comment utiliser l’API PostCellCharacters à l’aide des SDK

### Spécification de l’API PostCellCharacters

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostCellCharacters) définit une interface de programmation publiquement accessible et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment appeler l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/A1/characters" \
-X POST \
-d "{ \"FontSetting\": [ { \"Font\": { \"IsBold\": \"true\", \"Size\": \"24\" }, \"Length\": \"5\", \"StartIndex\": \"0\" }, { \"Font\": { \"IsItalic\": \"true\", \"Size\": \"15\" }, \"Length\": \"4\", \"StartIndex\": \"5\" } ] }" \
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

L’utilisation d’un SDK est le moyen le plus efficace d’accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
*Exemple de SDK C\#*  

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCellCharacters.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
*Exemple de SDK Java*  

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCellCharacters.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
*Exemple de SDK PHP*  

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCellCharacters.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
*Exemple de SDK Ruby*  

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCellCharacters.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
*Exemple de SDK Node.js*  

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCellCharacters.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
*Exemple de SDK Python*  

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCellCharacters.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
*Exemple de SDK Perl*  

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCellCharacters.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
*Exemple de SDK Go*  

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCellCharacters.go" >}}
{{< /tab >}}

{{< /tabs >}}