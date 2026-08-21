---
title: "Aspose.Cells Cloud Web API – Extraire du texte"
second_title: "Aspose.Cells Cloud – Short-codes en ligne"
linktitle: "Extraire du texte"
type: docs
url: /fr/extract-text/
keywords: "Aspose.Cells Cloud, extraire du texte, API Excel, extraction de texte cellulaire, API REST"
description: "Extrayez des sous-chaînes, des nombres ou des caractères à partir de cellules Excel à l’aide de l’API Aspose.Cells Cloud. Prend en charge l’extraction basée sur le texte avant/après, l’extraction basée sur la position, et l’écriture directe dans une nouvelle plage."
weight: 100
ArticleTitle: "Documentation de l’API Aspose.Cells Cloud d’extraction de texte"
---

Extrait des sous-chaînes, des caractères ou des nombres d’une cellule de feuille de calcul vers une autre cellule, éliminant ainsi la nécessité d’utiliser des formules complexes telles que FIND, MIN, LEFT ou RIGHT.

## **API ExtractText**

```http
PUT https://api.aspose.cloud/v4.0/cells/content/extract/text
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Paramètres de la requête de l’API **extractText**

| Nom du paramètre | Type    | Emplacement        | Description                                                                                                                                                  |
| ---------------- | ------- | ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet      | File    | FormData           | Télécharger le fichier de feuille de calcul.                                                                                                                |
| extractTextType  | String  | Query              | Énumération indiquant le mode d’extraction. Valeurs autorisées : `Before`, `After`, `BeforePosition`, `AfterPosition`.                                    |
| beforeText       | String  | Query              | Texte qui doit apparaître **avant** la sous-chaîne extraite. Utilisé lorsque `extractTextType=Before`.                                                      |
| afterText        | String  | Query              | Texte qui doit apparaître **après** la sous-chaîne extraite. Utilisé lorsque `extractTextType=After`.                                                       |
| beforePosition   | Integer | Query              | Nombre de caractères à renvoyer depuis le côté gauche de la cellule. Utilisé lorsque `extractTextType=BeforePosition`.                                     |
| afterPosition    | Integer | Query              | Nombre de caractères à renvoyer depuis le côté droit de la cellule. Utilisé lorsque `extractTextType=AfterPosition`.                                      |
| outPositionRange | String  | Query              | La plage cible (par exemple, `Sheet1!A1`) dans laquelle le texte extrait sera écrit.                                                                        |
| worksheet        | String  | Query              | Nom de la feuille de calcul contenant la cellule source.                                                                                                    |
| range            | String  | Query              | La cellule ou la plage source (par exemple, `A1`).                                                                                                          |
| outPath          | String  | Query _(Facultatif)_ | Chemin du dossier dans le stockage où le classeur résultant sera enregistré. Si omis, le résultat est retourné dans le corps de la réponse.                |
| outStorageName   | String  | Query              | Nom du stockage à utiliser pour le fichier de sortie.                                                                                                       |
| region           | String  | Query              | Paramètre de région de la feuille de calcul (par exemple, `US`, `EU`).                                                                                       |
| password         | String  | Query              | Mot de passe pour ouvrir un classeur protégé.                                                                                                               |

**Exemple de requête cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/extract/text?extractTextType=Before&beforeText=Total&outPositionRange=Sheet1!B1&worksheet=Sheet1&range=A1" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Sample.xlsx"
```

### **Réponse**

Lorsque la requête réussit, l’API renvoie une charge utile JSON contenant le texte extrait et l’adresse de la cellule dans laquelle il a été écrit :

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

Si le paramètre `outPath` est fourni, la réponse contient uniquement un message de statut ; le classeur est écrit à l’emplacement spécifié.

**Exemple de réponse lorsque `outPath` est omis**

```json
{
  "Code": 200,
  "Status":"OK"
}
```

### Codes d’erreur

- **200 OK** – Extraction terminée avec succès.  
- **202 Accepted** – Requête acceptée pour traitement asynchrone.  
- **400 Bad Request** – URI d’API Aspose.Cells Cloud invalide ou paramètres requis manquants.  
- **401 Unauthorized** – Jeton d’accès, ID client ou secret client invalide.  
- **404 Not Found** – Le fichier de feuille de calcul spécifié ne peut pas être accessible.  
- **500 Server Error** – Une erreur inattendue s’est produite lors du traitement du classeur.

## Spécification OpenAPI

La [Spécification OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/ExtractText) définit une interface de programmation publiquement accessible et permet d’effectuer des interactions REST directement depuis un navigateur web.

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK constitue la meilleure façon d’accélérer le développement. Le SDK gère les détails sous-jacents, vous permettant ainsi de simplement implémenter l’**extraction de texte** pour les cellules avec un minimum de code. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{<tab tabNum="1" >}}

```csharp
// Exemple en C# – extraction de texte (code omis pour concision)
```

{{</tab>}}

{{<tab tabNum="2" >}}

```java
// Exemple en Java – extraction de texte (code omis pour concision)
```

{{</tab>}}

{{<tab tabNum="3" >}}

```php
// Exemple en PHP – extraction de texte (code omis pour concision)
```

{{</tab>}}

{{<tab tabNum="4" >}}

```ruby
# Exemple en Ruby – extraction de texte (code omis pour concision)
```

{{</tab>}}

{{<tab tabNum="5" >}}

```javascript
// Exemple en Node.js – extraction de texte (code omis pour concision)
```

{{</tab>}}

{{<tab tabNum="6" >}}

```python
# Exemple en Python – extraction de texte (code omis pour concision)
```

{{</tab>}}

{{<tab tabNum="7" >}}

```perl
# Exemple en Perl – extraction de texte (code omis pour concision)
```

{{</tab>}}

{{<tab tabNum="8" >}}

```go
// Exemple en Go – extraction de texte (code omis pour concision)
```

{{</tab>}}

{{< /tabs >}}