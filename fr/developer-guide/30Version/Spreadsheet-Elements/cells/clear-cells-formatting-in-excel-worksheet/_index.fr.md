---
title: "Effacer le formatage des cellules dans une feuille Excel"
type: docs
url: /fr/clear-cells-formatting-in-excel-worksheet/
weight: 100
keywords: "Aspose.Cells Cloud, Excel, Effacer le formatage des cellules, API REST, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "Utilisez l’API REST Aspose.Cells Cloud pour effacer le formatage des cellules dans une feuille Excel. Inclut les détails de la requête, un exemple cURL et des extraits de code SDK pour plusieurs langages."
ArticleTitle: "Effacer le formatage des cellules dans une feuille Excel - Aspose.Cells Cloud API"
---

**Remarque :** Tous les appels à l’API Aspose.Cells Cloud doivent être effectués via **HTTPS**. Les points de terminaison HTTP sont obsolètes et peuvent être bloqués par les navigateurs.

- **Méthode :** POST  
- **Point de terminaison :** `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/clearformats`

Cette API REST efface le formatage des cellules dans un fichier Excel et fait partie de la suite Aspose.Cells Cloud dédiée à l’effacement du formatage des cellules dans les feuilles Excel.

## API PostClearFormats

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/clearformats
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

**Schéma de réponse**

| Champ   | Type    | Description                                            |
|---------|---------|--------------------------------------------------------|
| Code    | entier  | Code de statut HTTP renvoyé par l’API (par ex., 200). |
| Status  | chaîne  | Résultat de l’opération (`OK` en cas de succès).      |

**Codes de statut HTTP**

| Code | Signification               | Description                                               |
|------|-----------------------------|-----------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par ex., type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                           |
| 413  | Charge utile trop volumineuse | Le fichier chargé dépasse la limite de taille.          |
| 500  | Erreur interne du serveur   | Erreur inattendue sur le serveur.                         |

## Comment utiliser l’API PostClearFormats à l’aide des SDK

### Spécification de l’API PostClearFormats

La <a href="https://apireference.aspose.cloud/cells/#/Cells/PostClearFormats" rel="noopener noreferrer">spécification OpenAPI</a> définit une interface de programmation publiquement accessible et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer un appel à l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/clearformats?range=a1%3Aa10&startRow=1&startColumn=1&endRow=10&endColumn=10" \
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

L’utilisation d’un SDK est le moyen le plus rapide de développer. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostClearFormats.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostClearFormats.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostClearFormats.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostClearFormats.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostClearFormats.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostClearFormats.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostClearFormats.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostClearFormats.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Voir également**

- [Effacer le contenu et les styles des cellules](https://docs.aspose.cloud/cells/clear-contents-and-styles)  
- [Définir le style d’une cellule](https://docs.aspose.cloud/cells/set-cell-style)
---