---
title: "Ajouter du texte à Excel : insérer efficacement des données avec l'API Web Spreadsheet"
second_title: "Document"
linktitle: "Ajouter du texte"
type: docs
url: /fr/excel-add-text/
keywords: "Excel, Aspose.Cells, ajouter du texte, API Spreadsheet, API REST, Office Cloud, insertion de texte, API Excel"
description: "Ajoute du texte à un emplacement spécifié dans une feuille de calcul Excel via l'API Aspose.Cells Cloud."
weight: 100
---

Ajoute du contenu textuel à un emplacement spécifié dans une feuille de calcul. Cette opération nécessite un objet qui définit le texte à ajouter ainsi que la position d'insertion.

## **API Excel : PostAddTextContent**

```
POST http://api.aspose.cloud/v3.0/cells/addtext
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Description de la fonction**

Cette méthode permet d’ajouter en toute sécurité du texte nouveau aux cellules spécifiées, en prenant en charge plusieurs modes d’insertion et la gestion des formats.

- **Ajouter du texte au début des cellules sélectionnées**  
  Préfixe le texte à toutes les cellules sélectionnées, garantissant la cohérence de vos entrées de données. Idéal pour ajouter des identifiants ou des libellés courants tels que des codes produits, des catégories ou des préfixes.

- **Insérer des caractères avant ou après un texte spécifique**  
  Place des caractères avant ou après le texte cible dans les cellules sélectionnées, vous permettant ainsi de créer facilement du contenu structuré et bien organisé.

- **Ajouter le même texte à la fin de chaque cellule sélectionnée**  
  Ajoute du texte identique à la fin de plusieurs cellules en une seule opération, simplifiant l'entrée de données et assurant une apparence uniforme.

- **Insérer du texte avant ou après un nombre spécifié de caractères**  
  Insère du texte après un nombre défini de caractères depuis le début ou la fin de chaque cellule de la plage cible. Cas d’utilisation typiques : formatage de codes, horodatages ou délimiteurs personnalisés.

### **Paramètres de la requête**

| Nom du paramètre | Type  | Emplacement | Description                                                                 |
| ---------------- | ----- | ----------- | --------------------------------------------------------------------------- |
| addTextOptions   | Classe | Corps       | Spécifie le contenu textuel ainsi que la position à laquelle le texte doit être ajouté. |

### **Réponse**

```json
{
  "Filename": "xxxxxx.pdf",
  "FileSize": xxxx,
  "FileContent": "Contenu du fichier : chaîne encodée en base64"
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                                    |
|------|-----------------------------|----------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant. |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la limite de taille autorisée. |
| 500  | Erreur interne du serveur   | Erreur serveur inattendue. |

## Comment utiliser l’API PostAddTextContent avec les SDK

### Spécification de l’API PostAddTextContent

La [spécification OpenAPI](https://reference.aspose.cloud/cells/#/TextProcessingController/PostAddTextContent) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

### Utiliser les SDK Aspose.Cells Cloud

L'utilisation d'un SDK constitue la méthode la plus efficace pour accélérer le développement. Un SDK gère les détails de bas niveau, vous permettant ainsi de vous concentrer sur vos tâches de projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostAddTextContent.cs" >}}
{{</ tab>}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_PostAddTextContent.java" >}}
{{</ tab>}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_PostAddTextContent.php" >}}
{{</ tab>}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_PostAddTextContent.rb" >}}
{{</ tab>}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_PostAddTextContent.ts" >}}
{{</ tab>}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_PostAddTextContent.py" >}}
{{</ tab>}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_PostAddTextContent.pl" >}}
{{</ tab>}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_PostAddTextContent.go" >}}
{{</ tab>}}
{{< /tabs >}}