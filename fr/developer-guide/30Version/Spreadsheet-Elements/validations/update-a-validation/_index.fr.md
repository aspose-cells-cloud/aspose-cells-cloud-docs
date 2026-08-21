---
title: "Mettre à jour une validation de feuille de calcul dans une feuille de calcul Excel"
second_title: "Document"
linktitle: "Mettre à jour"
type: docs
url: /validations/update/
keywords: "Aspose.Cells Cloud, mise à jour de la validation Excel, API REST, validation de feuille de calcul, API Excel"
description: "Comment mettre à jour une validation de feuille de calcul dans un fichier Excel à l’aide de l’API REST Aspose.Cells Cloud, avec des exemples cURL et des extraits de code SDK pour plusieurs langages de programmation."
weight: 10
ArticleTitle: "Mettre à jour la validation de feuille de calcul à l’aide de l’API Aspose.Cells Cloud"
---

Cette API REST met à jour une validation de feuille de calcul à partir de son index dans une feuille de calcul Excel.

Avant d’appeler ce point de terminaison, obtenez un jeton d’accès JWT avec les portées appropriées (par exemple, `Cells.ReadWrite`). Incluez le jeton dans l’en-tête `Authorization`, comme indiqué dans les exemples.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
```

### **Paramètres de la requête**

| Nom du paramètre | Type    | Emplacement | Description                                                    |
| ---------------- | ------- | ----------- | -------------------------------------------------------------- |
| name             | string  | path        | Le nom du fichier du classeur.                                 |
| sheetName        | string  | path        | Le nom de la feuille de calcul contenant la validation.       |
| validationIndex  | integer | path        | L’index de base zéro de la validation à mettre à jour.        |
| validation       | object  | body        | Un objet JSON définissant les paramètres mis à jour de la validation. |
| folder           | string  | query       | Le dossier dans le stockage cloud où se trouve le classeur.   |
| storageName      | string  | query       | Le nom du service de stockage (si un stockage personnalisé est utilisé). |

La <a href="https://apireference.aspose.cloud/cells/#/WorksheetValidations/PostWorksheetValidation" target="_blank" rel="noopener noreferrer">Spécification OpenAPI</a> définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour appeler facilement les services web Aspose.Cells. L’exemple suivant montre comment effectuer un appel vers l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations/0" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jeton jwt>" \
-d '{ "AlertStyle":"Warning" }'
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

**Codes d’état HTTP possibles**

| Code | Signification                             | Description |
|------|-------------------------------------------|-------------|
| 200  | OK                                        | La validation a été mise à jour avec succès. |
| 400  | Requête incorrecte                        | La requête est mal formée ou des paramètres obligatoires sont manquants. |
| 401  | Non autorisé                              | Le jeton JWT est invalide ou manquant. |
| 403  | Interdit                                  | Le jeton ne dispose pas des portées suffisantes. |
| 404  | Non trouvé                                | Le classeur, la feuille de calcul ou l’index de validation spécifié n’existe pas. |
| 500  | Erreur interne du serveur                 | Une erreur inattendue s’est produite sur le serveur. |

Pour plus de détails sur la gestion des erreurs, reportez-vous à la <a href="https://apireference.aspose.cloud/cells/#/Errors" target="_blank" rel="noopener noreferrer">documentation d’erreurs Aspose.Cells Cloud</a>.

Vous souhaiterez peut-être également explorer des opérations associées, telles que l’ajout d’une nouvelle validation ou la suppression d’une validation existante :

- [Ajouter une validation de feuille de calcul](https://docs.aspose.cloud/cells/validations/add/)
- [Supprimer une validation de feuille de calcul](https://docs.aspose.cloud/cells/validations/delete/)

## Famille de SDK Cloud

Utiliser un SDK est le moyen le plus rapide de développer. Un SDK masque les détails de bas niveau, vous permettant de vous concentrer sur votre logique métier. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}