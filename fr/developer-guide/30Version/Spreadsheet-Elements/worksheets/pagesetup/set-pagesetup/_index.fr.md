---
title: "Définir la mise en page pour une feuille de calcul"
second_title: "Document"
linktype: "Définir la mise en page"
type: docs
url: /fr/set-page-setup/
keywords: "Aspose.Cells, Excel, mise en page, API REST, feuille de calcul, SDK cloud"
description: "Découvrez comment définir la mise en page d'une feuille de calcul Excel à l'aide de l'API REST Aspose.Cells Cloud. Inclut les détails de la requête, un exemple sécurisé en HTTPS utilisant cURL, les codes de statut de réponse et des extraits de code SDK pour plusieurs langages de programmation."
weight: 20
ArticleTitle: "Définir la mise en page pour une feuille de calcul – Guide de l'API Aspose.Cells Cloud"
---

Conditions préalables : Pour appeler cette API, vous devez disposer d’un jeton JWT (OAuth) valide, et le classeur doit se trouver dans un emplacement de stockage Aspose Cloud où vous avez les autorisations de lecture/écriture. Assurez-vous que le jeton est inclus dans l’en-tête **Authorization** et que votre compte dispose du quota API nécessaire.

Cette API REST permet de définir la mise en page d’une feuille de calcul Excel.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pagesetup
```

### **Sécurité et authentification**

Les API REST d’Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de la requête**

| Nom du paramètre | Type   | Emplacement | Description                   |
| ---------------- | ------ | ----------- | ----------------------------- |
| name             | string | path        | Nom du document.              |
| sheetName        | string | path        | Nom de la feuille de calcul.  |
| pageSetup        | object | body        | Description de la mise en page. |
| folder           | string | query       | Dossier du document.          |
| storageName      | string | query       | Nom du stockage.              |

**Exemple de charge utile JSON pour l’objet `pageSetup`**

```json
{
  "pageSetup": {
    "orientation": "Portrait",
    "paperSize": "A4",
    "fitToPagesTall": 1,
    "fitToPagesWide": 1,
    "centerHorizontally": true,
    "centerVertically": false
  }
}
```

La <a href="https://reference.aspose.cloud/cells/#/PageSetup/PostPageSetup" target="_blank" rel="noopener noreferrer">spécification OpenAPI</a> définit une interface de programmation publiquement accessible et permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web d’Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Tasks/pagesetup" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jeton jwt>" \
-d '{
  "pageSetup": {
    "orientation": "Portrait",
    "paperSize": "A4",
    "fitToPagesTall": 1,
    "fitToPagesWide": 1,
    "centerHorizontally": true,
    "centerVertically": false
  }
}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

L’API renvoie un objet JSON indiquant le résultat de l’opération :

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Codes de statut de réponse possibles**

| Code | Signification               | Cas                                                                 |
|------|-----------------------------|---------------------------------------------------------------------|
| 200  | OK                          | Mise à jour de la mise en page réussie                             |
| 400  | Requête incorrecte          | Charge utile JSON invalide ou champs obligatoires manquants        |
| 401  | Non autorisé                | Jeton JWT manquant ou invalide                                     |
| 404  | Non trouvé                  | Le classeur ou le nom de la feuille de calcul n’existe pas         |
| 500  | Erreur interne du serveur   | Échec inattendu du serveur                                         |

## Famille de SDK Cloud

L’utilisation d’un SDK est le meilleur moyen d’accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK d’Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostPageSetup.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostPageSetup.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostPageSetup.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostPageSetup.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostPageSetup.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostPageSetup.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostPageSetup.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostPageSetup.go" >}}

{{< /tab >}}

{{< /tabs >}}