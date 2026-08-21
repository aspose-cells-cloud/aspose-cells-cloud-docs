---
title: "API Aspose.Cells Trim Content – Supprimer les espaces et les sauts de ligne dans Excel"
second_title: "Document"
linktitle: "Trim Content"
type: docs
url: /spreadsheet-trim-content/
keywords: "Aspose.Cells, API Trim Content, nettoyage de données Excel, suppression des espaces dans Excel, suppression des sauts de ligne, nettoyage des données de feuille de calcul"
description: "Utilisez l’API Aspose.Cells Cloud PostTrimContent pour supprimer automatiquement les espaces supplémentaires, les sauts de ligne et les caractères indésirables des cellules Excel. Découvrez le point de terminaison, le format de la requête, le code d’exemple et la gestion des erreurs."
weight: 100
---

## **API Web Excel : PostTrimContent**

L’API **PostTrimContent** traite et réduit le contenu dans une plage spécifiée d'une feuille de calcul. Elle supprime les espaces supplémentaires, les sauts de ligne et d'autres caractères inutiles du contenu des cellules sélectionnées, ce qui la rend utile pour nettoyer les saisies de données et garantir une mise en forme cohérente des feuilles de calcul.

```http
POST https://api.aspose.cloud/v3.0/cells/trimcontent
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.


### **Description des fonctionnalités**

- **Efficacité** – Réduit le contenu uniquement dans la plage désignée, économisant du temps et des ressources en évitant les opérations inutiles sur l’ensemble de la feuille de calcul.
- **Flexibilité** – Permet aux utilisateurs de définir précisément la plage de cellules à traiter, s’adaptant ainsi à divers jeux de données et exigences.
- **Intégrité des données** – Supprime les espaces et sauts de ligne superflus, aidant à maintenir des données cohérentes et fiables pour l’analyse et les rapports.
- **Facilité d’utilisation** – Intégration simple avec une configuration minimale, adaptée tant aux développeurs qu’aux utilisateurs finaux.

### **Paramètres de la requête**

| Nom du paramètre   | Type  | Emplacement | Description                                                                                      |
| ------------------ | ----- | ----------- | ------------------------------------------------------------------------------------------------ |
| trimContentOptions | Classe | Corps       | Options spécifiant comment le contenu doit être réduit (par exemple, plage cible, mode de réduction). |

### **Réponse**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[nom de fichier fusionné]",
    "Filesize" : [taille du fichier],
    "FileContent" : "[Base64String]"
}
```

**Codes de statut HTTP**

| Code | Signification              | Description                                                           |
|------|----------------------------|-----------------------------------------------------------------------|
| 200  | OK                         | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte         | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé               | Jeton JWT invalide ou manquant. |
| 413  | Charge utile trop grande   | Fichier téléchargé dépassant la taille limite. |
| 500  | Erreur interne du serveur  | Erreur serveur inattendue. |

## Comment utiliser l’API PostRemoveCharacters avec les SDK

### Spécification de l’API PostRemoveCharacters

La [spécification OpenAPI](https://reference.aspose.cloud/cells/#/TextProcessingController/PostTrimContent) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est le meilleur moyen d’accélérer le développement. Un SDK gère les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostTrimContent.cs" >}}
{{</ tab>}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_PostTrimContent.java" >}}
{{</ tab>}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_PostTrimContent.php" >}}
{{</ tab>}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_PostTrimContent.rb" >}}
{{</ tab>}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_PostTrimContent.ts" >}}
{{</ tab>}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_PostTrimContent.py" >}}
{{</ tab>}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_PostTrimContent.pl" >}}
{{</ tab>}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_PostTrimContent.go" >}}
{{</ tab>}}
{{< /tabs >}}

_Dernière mise à jour : 2026-03-30_