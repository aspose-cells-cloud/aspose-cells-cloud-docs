---
title: "Comment fusionner des cellules dans une feuille Excel – Aspose.Cells Cloud API (v3.0)"
type: docs
url: /merge-cells-in-excel-worksheet/
weight: 110
keywords: "fusionner des cellules, Aspose.Cells, API cloud, Excel"
description: "Guide pour fusionner des cellules dans une feuille Excel à l’aide de l’API REST Aspose.Cells Cloud avec des exemples cURL et des SDK."
ArticleTitle: "Comment fusionner des cellules dans une feuille Excel – Aspose.Cells Cloud API (v3.0)"
---

L’API REST Aspose.Cells Cloud permet de fusionner un bloc rectangulaire de cellules en une seule cellule s’étendant sur les lignes et colonnes spécifiées.

**Conditions préalables**  
- Un jeton JWT valide pour l’authentification.  
- Le classeur doit déjà exister dans le dossier de stockage spécifié.  
- La configuration du stockage (nom du dossier et nom du stockage) doit être définie dans votre compte Aspose.Cloud.

## API PostWorksheetMerge

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/merge
```

### **Sécurité et authentification**

Les API REST Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom             | Type    | Emplacement | Description                                                  |
|-----------------|---------|-------------|--------------------------------------------------------------|
| name            | string  | path        | Nom du classeur.                                             |
| sheetName       | string  | path        | Nom de la feuille de calcul.                                 |
| startRow        | integer | query       | Indice de la première ligne (à partir de zéro ; 0 = première ligne). |
| startColumn     | integer | query       | Indice de la première colonne (à partir de zéro ; 0 = première colonne). |
| totalRows       | integer | query       | Nombre de lignes à fusionner.                                |
| totalColumns    | integer | query       | Nombre de colonnes à fusionner.                              |
| folder          | string  | query       | Dossier contenant le classeur.                               |
| storageName     | string  | query       | Nom du stockage.                                             |

*Aucun corps de requête n’est requis pour cette opération.*

## **Réponse**

Renvoie un objet CellsCloudResponse.

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
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                              |
| 413  | Charge utile trop grande     | Le fichier téléchargé dépasse la limite de taille.          |
| 500  | Erreur interne du serveur   | Erreur serveur inattendue.                                   |

## Comment utiliser l’API PostWorksheetMerge avec les SDK

### Spécification de l’API PostWorksheetMerge

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetMerge) définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API cloud via cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/merge?startRow=10&startColumn=10&totalRows=10&totalColumns=10" \
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

L’utilisation d’un SDK constitue la méthode optimale pour accélérer le développement. Un SDK gère les détails de bas niveau, vous permettant ainsi de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMerge.go" >}}

{{< /tab >}}

{{< /tabs >}}