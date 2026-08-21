---
title: "Ajouter un saut de page horizontal"
second_title: "Document"
linktitle: "Ajouter un saut de page horizontal"
type: docs
url: /fr/page-breaks/add-horizontal-page-break/
aliases: [  /fr/insert-horizontal-page-break-inside-worksheet/ ]
keywords: "saut de page horizontal, Aspose.Cells Cloud, API Excel, REST, SDK, feuille de calcul, cURL"
description: "Découvrez comment ajouter un saut de page horizontal à une feuille de calcul Excel à l'aide de l'API REST Aspose.Cells Cloud. Inclut les détails de la requête, un exemple cURL et des extraits de code SDK pour plusieurs langages de programmation."
weight: 30
ArticleTitle: "Ajouter un saut de page horizontal – API Aspose.Cells Cloud"
---

L’API **Ajouter un saut de page horizontal** insère un saut de page horizontal dans une feuille de calcul Excel.

**Conditions préalables et authentification**  
Un jeton JWT valide est requis pour toutes les requêtes vers l’API Aspose.Cells Cloud. Obtenez le jeton via le flux OAuth 2.0 décrit dans le guide d’authentification, puis incluez-le dans l’en-tête de la requête sous la forme `Authorization: Bearer <jeton JWT>`. Le classeur cible doit se trouver dans un emplacement de stockage accessible à l’API (stockage par défaut ou un `storageName` personnalisé que vous spécifiez).

## API PutHorizontalPageBreak

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification par jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description                                                               |
| ---------------- | ------- | ----------- | ------------------------------------------------------------------------- |
| name             | string  | path        | Nom du fichier Excel.                                                     |
| sheetName        | string  | path        | Nom de la feuille de calcul dans laquelle le saut de page sera ajouté.   |
| cellname         | string  | query       | Référence de cellule (par exemple **A1**) indiquant le début du saut de page. |
| row              | integer | query       | Indice de ligne (à zéro) du saut de page.                                 |
| column           | integer | query       | Indice de colonne (à zéro) du saut de page.                               |
| startColumn      | integer | query       | Colonne de début d’une plage lors de l’insertion d’un saut de page.      |
| endColumn        | integer | query       | Colonne de fin d’une plage lors de l’insertion d’un saut de page.        |
| folder           | string  | query       | Chemin du dossier contenant le fichier Excel.                             |
| storageName      | string  | query       | Nom du stockage Aspose Cloud.                                             |

La <a href="https://apireference.aspose.cloud/cells/#/PageBreaks/PutHorizontalPageBreak" target="_blank" rel="noopener noreferrer">spécification OpenAPI</a> définit une interface publique accessible permettant d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour accéder facilement aux services web Aspose.Cells. L’exemple ci-dessous montre comment appeler l’API avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
# Utiliser HTTPS pour garantir une communication chiffrée
curl -v "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/horizontalpagebreaks?row=18" \
  -X PUT \
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

{{< /tab >}}

{{< /tabs >}}

Exemple de réponse d’erreur en cas de jeton JWT manquant ou invalide :

```json
{
  "Code": 401,
  "Status": "Unauthorized",
  "Message": "Jeton JWT invalide ou manquant."
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                                |
|------|-----------------------------|------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou invalides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                           |
| 413  | Payload trop volumineux     | Le fichier téléchargé dépasse la taille limite.          |
| 500  | Erreur interne du serveur   | Erreur inattendue du serveur.                             |

Pour plus de détails sur les opérations connexes, consultez les pages d’API pour **[Obtenir les sauts de page horizontaux](../get-horizontal-page-breaks/)** et **[Supprimer un saut de page horizontal](../delete-horizontal-page-break/)**.

## Famille de SDK Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour développer. Un SDK abstractise les détails de bas niveau afin que vous puissiez vous concentrer sur votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code ci-dessous montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutHorizontalPageBreak.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutHorizontalPageBreak.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutHorizontalPageBreak.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutHorizontalPageBreak.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutHorizontalPageBreak.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutHorizontalPageBreak.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutHorizontalPageBreak.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutHorizontalPageBreak.go" >}}
{{< /tab >}}

{{< /tabs >}}