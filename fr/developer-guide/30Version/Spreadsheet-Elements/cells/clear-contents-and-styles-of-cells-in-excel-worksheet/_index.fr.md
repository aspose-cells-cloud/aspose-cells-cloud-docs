---
title: "Effacer le contenu et les styles des cellules d'une feuille Excel"
type: docs
url: /fr/clear-contents-and-styles-of-cells-in-excel-worksheet/
weight: 50
keywords:
  - Aspose.Cells
  - API Excel
  - effacer le contenu des cellules
  - effacer les styles des cellules
  - feuille de calcul cloud
  - API REST
description: "Découvrez comment utiliser l'API REST Aspose.Cells Cloud pour effacer le contenu et les styles des cellules dans une feuille Excel, avec des exemples cURL et des extraits de code SDK."
ArticleTitle: "Effacer le contenu et les styles des cellules d'une feuille Excel – API Aspose.Cells Cloud"
---

Avant d'utiliser le point de terminaison **Clear Contents and Styles**, assurez-vous de disposer de :

* D'un **jeton JWT** valide obtenu via le flux d'authentification Aspose.Cells Cloud.  
* Du classeur uploadé vers l'emplacement de stockage de votre choix (ou accessible via le paramètre `folder`).  
* De la version SDK requise installée, si vous préférez utiliser l'une des bibliothèques clientes spécifiques à un langage.

Cette API REST permet d'effacer le contenu des cellules d'un fichier Excel.

## API PostClearContents

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/clearcontents
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Réponse**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l'opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant. |
| 413  | Charge utile trop volumineuse | Le fichier uploadé dépasse la limite de taille. |
| 500  | Erreur interne du serveur   | Erreur serveur inattendue. |
## Comment utiliser l’API PostClearContents avec les SDK

### Spécification de l’API PostClearContents

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostClearContents) définit une interface de programmation publiquement accessible et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/clearcontents?range=A2:C11" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

L'utilisation d’un SDK est le moyen le plus efficace d’accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostClearContents.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostClearContents.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostClearContents.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostClearContents.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostClearContents.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostClearContents.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostClearContents.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostClearContents.go" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Effacer le contenu et les styles des cellules d'une feuille Excel",
  "description": "Comment utiliser l'API REST Aspose.Cells Cloud pour effacer le contenu et les styles des cellules d'une feuille Excel.",
  "url": "https://docs.aspose.cloud/cells/clear-contents-and-styles-of-cells-in-excel-worksheet/",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2023-07-08",
  "publisher": {
    "@type": "Organization",
    "name": "Aspose",
    "logo": {
      "@type": "ImageObject",
      "url": "https://docs.aspose.cloud/cells/images/Aspose-image-for-open-graph.jpg",
      "caption": "Aspose.Cells Cloud – Effacer le contenu et les styles des cellules"
    }
  },
  "keywords": "Aspose.Cells, API Excel, effacer le contenu des cellules, effacer les styles des cellules, API REST, feuille de calcul cloud"
}
</script>
---