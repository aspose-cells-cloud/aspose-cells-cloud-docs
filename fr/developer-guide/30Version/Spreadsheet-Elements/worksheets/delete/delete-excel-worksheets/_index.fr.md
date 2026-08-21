---
title: "Supprimer plusieurs feuilles de calcul Excel"
second_title: "Document"
linktitle: "Plusieurs feuilles de calcul"
type: docs
url: /worksheets/delete-multiple/
aliases: [/delete-excel-worksheets/]
keywords: "Aspose.Cells Cloud, supprimer plusieurs feuilles de calcul, API Excel, API REST, v3.0, supprimer des feuilles de calcul"
description: "Découvrez comment supprimer plusieurs feuilles de calcul à partir d’un classeur Excel à l’aide de l’API REST Aspose.Cells Cloud (v3.0). Inclut un endpoint HTTPS sécurisé, les paramètres requis, un exemple cURL corrigé et des extraits de code SDK pour plusieurs langages de programmation."
weight: 20
ArticleTitle: "Supprimer plusieurs feuilles de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud"
---

Cet API REST permet de supprimer plusieurs feuilles de calcul à partir d’un classeur.

## Sécurité et authentification
Les API Aspose.Cells Cloud sont sécurisées et exigent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets
```

### **Paramètres de la requête**

| Nom du paramètre | Type   | Emplacement | Description                                                                 |
| ---------------- | ------ | ----------- | --------------------------------------------------------------------------- |
| name             | string | path        | Nom du fichier Excel.                                                       |
| matchCondition   | object | body        | Objet `MatchConditionRequest` spécifiant quelles feuilles de calcul supprimer. |
| folder           | string | query       | Chemin du dossier dans le stockage où le fichier est situé.                |
| storageName      | string | query       | Nom du service de stockage.                                                 |

**Propriétés de MatchConditionRequest**

| Nom                  | Type     | Description                                        | Notes    |
| -------------------- | -------- | -------------------------------------------------- | -------- |
| RegexPattern         | string   | Expression régulière pour faire correspondre les noms des feuilles de calcul. | facultatif |
| FullMatchConditions  | string[] | Noms exacts des feuilles de calcul à supprimer.   | facultatif |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheets) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL. **Un jeton JWT valide est requis dans l’en-tête `Authorization`.**

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets?folder=Temp" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>" \
  -d '{"FullMatchConditions":["Sheet1","Sheet2","Sheet3"]}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

La requête peut également renvoyer des réponses d’erreur courantes, par exemple :

| Statut HTTP | Signification                                       | Exemple de charge utile                                 |
| ----------- | --------------------------------------------------- | ------------------------------------------------------- |
| 400         | Requête incorrecte – JSON ou paramètres invalides | `{"Code":400,"Message":"Charge utile de requête invalide."}` |
| 401         | Non autorisé – jeton JWT manquant ou invalide      | `{"Code":401,"Message":"Échec de l’authentification."}` |
| 403         | Accès refusé – permissions insuffisantes           | `{"Code":403,"Message":"Accès refusé."}`               |
| 404         | Non trouvé – fichier ou feuille de calcul inexistante | `{"Code":404,"Message":"Ressource introuvable."}`      |
| 500         | Erreur interne du serveur                           | `{"Code":500,"Message":"Une erreur inattendue s’est produite."}` |

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

L’utilisation d’un SDK est le moyen optimal d’accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheets.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheets.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheets.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheets.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheets.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheets.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Voir également :**  
- [Supprimer une seule feuille de calcul](https://docs.aspose.cloud/cells/worksheets/delete/)  
- [Copier une feuille de calcul](https://docs.aspose.cloud/cells/worksheets/copy/)  
- [Déplacer une feuille de calcul](https://docs.aspose.cloud/cells/worksheets/move/)  
---