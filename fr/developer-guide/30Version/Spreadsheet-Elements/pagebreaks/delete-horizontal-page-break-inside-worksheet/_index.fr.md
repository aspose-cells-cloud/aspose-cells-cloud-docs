---
title: "Supprimer un saut de page horizontal"
ArticleTitle: "Aspose.Cells Cloud – Supprimer un saut de page horizontal (API REST)"
second_title: "Document"
linktype: "docs"
url: /fr/page-breaks/delete-horizontal-page-break/
aliases: [  /fr/delete-horizontal-page-break-inside-worksheet/ ]
keywords: "Aspose.Cells Cloud, Supprimer un saut de page horizontal, Feuille de calcul Excel, API REST, SDK"
description: "Supprimer un saut de page horizontal d’une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud. Les SDK sont disponibles pour C#, Java, PHP, Ruby, Node.js, Python, Perl et Go."
weight: 50
---

Cette API REST supprime un saut de page **horizontal**.

**Prérequis** : Pour appeler ce point de terminaison, vous devez disposer d’un jeton d’accès JWT Aspose Cloud valide. Obtenez-le en suivant le [guide d’authentification](https://docs.aspose.cloud/cells/authentication/).

## API DeleteHorizontalPageBreak

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks/{index}
```

*Toutes les requêtes vers l’API doivent être effectuées via **HTTPS**.*

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une authentification basée sur des <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">jetons JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description                                                      |
| ---------------- | ------- | ----------- | ---------------------------------------------------------------- |
| `name`           | string  | path        | Nom du fichier Excel (classeur).                                |
| `sheetName`      | string  | path        | Nom de la feuille de calcul contenant le saut de page.         |
| `index`          | integer | path        | Index de base zéro du saut de page horizontal à supprimer.      |
| `folder`         | string  | query       | Chemin du dossier optionnel dans le stockage où se trouve le fichier. |
| `storageName`    | string  | query       | Nom optionnel du service de stockage.                           |

### Réponses d’erreur

| Code HTTP | Description                                                              |
| --------- | ------------------------------------------------------------------------ |
| 401       | Non autorisé – jeton manquant ou invalide.                              |
| 404       | Introuvable – le fichier, la feuille de calcul ou l’index du saut de page spécifié n’existe pas. |
| 400       | Requête incorrecte – syntaxe mal formée ou paramètres invalides.        |
| 500       | Erreur interne du serveur – une condition inattendue s’est produite.    |

**Voir également** :  
- [Ajouter un saut de page horizontal](/page-breaks/add-horizontal-page-break/)  
- [Obtenir les sauts de page horizontaux](/page-breaks/get-horizontal-page-breaks/)  
- [Supprimer un saut de page vertical](/page-breaks/delete-vertical-page-break/)

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/PageBreaks/DeleteHorizontalPageBreak) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer cet appel avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/horizontalpagebreaks/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton JWT>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Schéma de réponse**

| Champ   | Type    | Description                                     |
|---------|---------|-------------------------------------------------|
| Code    | integer | Code d’état HTTP (par exemple, 200).            |
| Status  | string  | Message d’état textuel (par exemple, « OK »).   |
| Message | string  | Information supplémentaire optionnelle en cas d’erreur. |

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

L’utilisation d’un SDK est le moyen le plus efficace d’accélérer le développement. Un SDK gère les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteHorizontalPageBreak.cs" >}}
*Si l’exemple ne se charge pas, consultez-le sur [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/8a5b324fdf3e574dbd747c1a1e24b05d).*

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteHorizontalPageBreak.java" >}}
*Si l’exemple ne se charge pas, consultez-le sur [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/c59aa5c02f735466a5e34751cee73f5f).*

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteHorizontalPageBreak.php" >}}
*Si l’exemple ne se charge pas, consultez-le sur [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/84283c8ba766ed815f47e6dfb0891152).*

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteHorizontalPageBreak.rb" >}}
*Si l’exemple ne se charge pas, consultez-le sur [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/36ed8b8727561b92692939513d365fca).*

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteHorizontalPageBreak.ts" >}}
*Si l’exemple ne se charge pas, consultez-le sur [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/e82de2e4189bc27ae92abf73c36b4df0).*

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteHorizontalPageBreak.py" >}}
*Si l’exemple ne se charge pas, consultez-le sur [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/61e922de11e6e7144db88adcad6501c1).*

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteHorizontalPageBreak.pl" >}}
*Si l’exemple ne se charge pas, consultez-le sur [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/f82a3a00251e34ff8766116282c8c9ca).*

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteHorizontalPageBreak.go" >}}
*Si l’exemple ne se charge pas, consultez-le sur [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/2b824d4e13644368d12682856aa49185).*

{{< /tab >}}

{{< /tabs >}}