---
title: "Aspose.Cells Cloud Replace Web API – Mettre à jour le texte dans une plage de feuille de calcul distante"
second_title: "Document"
articleTitle: "Remplacement en masse du texte dans une plage – API Trouver & Remplacer pour fichiers Excel dans le cloud"
linktype: "Remplacer le contenu d’une plage distante"
type: docs
url: /fr/replace-content-in-remote-range/
keywords: "remplacer du texte dans une plage Excel distante, API Aspose.Cells Cloud, trouver et remplacer dans Excel, modifier une feuille de calcul dans le cloud, mettre à jour un fichier Excel distant"
description: "Utilisez Aspose.Cells Cloud pour rechercher et remplacer du texte dans une plage spécifique d’un fichier Excel distant. Prend en charge l’authentification, la gestion des erreurs et les SDK multilingues."
weight: 100
---

Effectuez un remplacement en masse de texte dans plusieurs fichiers Excel stockés dans le cloud. Recherchez et mettez à jour des chaînes de texte spécifiques dans des plages sélectionnées de manière efficace à l’aide de l’API Trouver & Remplacer d’Aspose.Cells Cloud.

## **Remplacer le contenu d’une plage distante via l’API**

### API Web

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/replace/content
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Paramètres de requête**

| Nom du paramètre | Type   | Emplacement (chemin / chaîne de requête / corps HTTP) | Description                                                                                                                                                       |
| :--------------- | :----- | :---------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name             | String | Chemin                                                | Nom du fichier classeur stocké dans le stockage cloud à modifier (par exemple, `"rapport.xlsx"`).                                                               |
| searchText       | String | Chaîne de requête                                     | Chaîne de texte à rechercher dans la feuille de calcul et la plage de cellules spécifiées. Prend en charge la correspondance exacte du texte.                    |
| replaceText      | String | Chaîne de requête                                     | Chaîne de texte qui remplacera toutes les occurrences de `searchText` dans la plage spécifiée.                                                                  |
| worksheet        | String | Chemin                                                | Nom de la feuille de calcul où l’opération de recherche et de remplacement sera effectuée.                                                                      |
| cellArea         | String | Chemin                                                | Plage de cellules spécifique (par exemple, `"A1:D20"`) dans laquelle la recherche et le remplacement de texte auront lieu.                                       |
| folder           | String | Chaîne de requête                                     | Chemin du dossier dans le stockage cloud où le classeur source est situé.                                                                                        |
| storageName      | String | Chaîne de requête                                     | _(Facultatif)_ Nom du stockage cloud où réside le classeur. Si omis, le stockage cloud par défaut est utilisé.                                                   |
| region           | String | Chaîne de requête                                     | _(Facultatif)_ Définit la locale pour le traitement du texte, ce qui peut affecter la sensibilité à la casse et le codage des caractères lors des recherches (par exemple, `"fr-FR"`, `"en-US"`). |
| password         | String | Chaîne de requête                                     | _(Facultatif)_ Si le classeur est protégé par un mot de passe, fournissez ce mot de passe pour l’ouvrir et le modifier.                                         |

### **Réponse**

```json
{
  "Name": "CellsCloudResponse",
  "Type": "Class",
  "Properties": [
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer"
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String"
      }
    }
  ]
}
```

Une appel réussit renvoie la charge utile JSON concrète suivante :

```json
{
  "Code": 200,
  "Status": "OK"
}
```


### Codes d’erreur

| Code | Message            | Quand cela se produit                                                                 |
| ---- | ------------------ | ------------------------------------------------------------------------------------ |
| 400  | Bad Request        | L’URI de la requête ou ses paramètres sont mal formés.                              |
| 401  | Unauthorized       | Jeton d’authentification manquant ou invalide.                                      |
| 404  | Not Found          | Le classeur spécifié est introuvable ou inaccessible.                              |
| 500  | Server Error       | Une erreur interne du serveur est survenue lors du traitement du classeur.          |

## Où utiliser l’API de remplacement du contenu d’une plage dans une feuille de calcul distante ?

- **Mise à jour en lot de fichiers dans le cloud** : Modifier le contenu de plusieurs fichiers Excel stockés dans des services de stockage cloud tels qu’AWS S3 ou Azure Blob.
- **Remplissage dynamique de modèles dans le cloud** : Remplir en lot des données dynamiques dans des modèles de rapports stockés dans le cloud.
- **Synchronisation inter-régions des fichiers** : Synchroniser la cohérence du contenu des fichiers Excel dans le stockage cloud entre différentes régions géographiques.

## Pourquoi utiliser l’API de remplacement du contenu d’une plage dans une feuille de calcul distante ?

- **Facile à utiliser pour les développeurs** : Aspose.Cells Cloud propose des bibliothèques SDK dans plusieurs langages, ce qui permet un développement rapide accompagné d’une documentation complète. Comparé à la création de solutions sur mesure, cela réduit considérablement la charge de travail de développement.
- **Réduction des coûts de main-d’œuvre** : Diminue le besoin de postes dédiés à la consolidation de documents.
- **Paiement à l’usage** : Aucun investissement initial ; vous ne payez que pour les appels API effectivement utilisés.
- **Zéro coût de maintenance** : Aucune nécessité de maintenir des serveurs, de mettre à jour des logiciels ou de gérer des problèmes de compatibilité.
- **Préservation du formatage Excel complexe** dans un format PDF universellement accessible.

## Comment utiliser l’API de remplacement du contenu d’une plage dans une feuille de calcul distante à l’aide des SDK

### Spécification OpenAPI

La [Spécification OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceContentInRemoteRange) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation des SDK est le moyen le plus efficace d’accélérer le développement. Les SDK gèrent les détails sous-jacents, vous permettant ainsi de simplement implémenter le remplacement de contenu dans des feuilles de calcul avec un minimum de code. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}

```csharp
```

{{</tab>}}
{{<tab tabNum="2" >}}

```java
```

{{</tab>}}
{{<tab tabNum="3" >}}

```php
```

{{</tab>}}
{{<tab tabNum="4" >}}

```ruby
```

{{</tab>}}
{{<tab tabNum="5" >}}

```javascript
```

{{</tab>}}
{{<tab tabNum="6" >}}

```python
```

{{</tab>}}
{{<tab tabNum="7" >}}

```perl
```

{{</tab>}}
{{<tab tabNum="8" >}}

```go
```

{{</tab>}}
{{< /tabs >}}