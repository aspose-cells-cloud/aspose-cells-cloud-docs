---
title: "Actualiser un filtre automatique dans une feuille Excel"
second_title: "Document"
linktitle: "Actualiser le filtre automatique"
type: docs
url: /fr/autofilter/refresh/
aliases: [  /fr/refresh-an-autofilter/ ]
weight: 100
keywords: "Aspose.Cells, AutoFilter, actualiser, Excel, API, REST"
description: "Actualiser un filtre automatique existant sur une feuille Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut des exemples cURL et des SDK pour C#, Java, Python, etc."
ArticleTitle: "Actualiser un filtre automatique dans une feuille Excel"
---

### Que fait l’opération **Actualiser** ?

L’appel de l’endpoint réapplique les critères de filtrage actuels après que les données de la feuille de calcul ont été modifiées (par exemple, des lignes ont été ajoutées ou supprimées). Cette opération ne modifie pas la définition du filtre ; elle met simplement à jour l’affichage et renvoie une réponse indiquant le statut.

### API REST

Cette API REST actualise un filtre automatique dans une feuille Excel (version de l’API **v3.0**).

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/refresh
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

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
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant. |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la taille maximale autorisée. |
| 500  | Erreur interne du serveur   | Erreur inattendue du serveur. |

*Exemples de réponses d’erreur*  

```json
// 400 Requête incorrecte
{
    "Code": 400,
    "Message": "Paramètre non valide : sheetName introuvable."
}

// 401 Non autorisé
{
    "Code": 401,
    "Message": "Échec de l’authentification. Le jeton JWT est manquant ou non valide."
}

// 413 Charge utile trop volumineuse
{
    "Code": 413,
    "Message": "Le fichier téléchargé dépasse la taille maximale autorisée."
}

// 500 Erreur interne du serveur
{
    "Code": 500,
    "Message": "Une erreur inattendue s’est produite sur le serveur."
}
```

## Comment utiliser l’API PostWorksheetAutoFilterRefresh à l’aide des SDK

### Spécification de l’API PostWorksheetAutoFilterRefresh

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PostWorksheetAutoFilterRefresh) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple ci-dessous montre comment effectuer des appels à l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/refresh" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <votre-jeton-jwt>"
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

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetAutoFilterRefresh.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetAutoFilterRefresh.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetAutoFilterRefresh.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetAutoFilterRefresh.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetAutoFilterRefresh.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetAutoFilterRefresh.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetAutoFilterRefresh.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetAutoFilterRefresh.go" >}}

{{< /tab >}}

{{< /tabs >}}
---