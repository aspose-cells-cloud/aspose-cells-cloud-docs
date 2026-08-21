---
title: "Supprimer des caractères dans Excel – API Aspose.Cells Cloud (POST /cells/removecharacters)"
second_title: "Document"
linktype: "Documentation"
type: docs
url: /excel-remove-characters/
keywords: "supprimer des caractères, Aspose.Cells, API Excel, traitement de texte, cloud"
description: "Découvrez comment supprimer des caractères, des ensembles de caractères ou des sous-chaînes à partir de feuilles de calcul Excel à l’aide de l’API Aspose.Cells Cloud. Inclut le schéma de requête, un exemple cURL, du code SDK et la gestion des erreurs."
weight: 100
ArticleTitle: "Supprimer des caractères dans Excel – API Aspose.Cells Cloud (POST /cells/removecharacters)"
---

## Supprimer des caractères dans l’API Web Excel

Un ensemble complet d’outils permettant de nettoyer le contenu textuel des cellules sélectionnées. L’API supprime des caractères spécifiques, des ensembles de caractères prédéfinis ou des sous-chaînes, garantissant ainsi que le texte des feuilles de calcul est normalisé et dépourvu de symboles indésirables.

**Conditions préalables**

- Un compte Aspose Cloud actif.  
- Un jeton d’accès JWT valide obtenu conformément aux indications du guide d’authentification.  
- Le fichier Excel doit être uploadé dans le stockage avant d’appeler ce point de terminaison.  
- Les formats de fichier pris en charge incluent `.xlsx`, `.xls`, `.xlsm` et d'autres types Excel courants.

```http
POST https://api.aspose.cloud/v3.0/cells/removecharacters
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Description des fonctions

- **Supprimer des caractères personnalisés** – Spécifiez les caractères que vous souhaitez supprimer. Entrez chaque caractère dans le champ _Supprimer des caractères personnalisés_ ; l’API supprimera chaque occurrence de ces caractères dans les cellules sélectionnées.  
- **Supprimer des ensembles de caractères** – Choisissez parmi les ensembles prédéfinis suivants :  
  - **Caractères non imprimables** – Supprime les sauts de ligne et les 32 premiers caractères ASCII non imprimables (0 à 31), ainsi que les codes supplémentaires (127, 129, 141, 143, 144, 157).  
  - **Caractères textuels** – Supprime toutes les lettres.  
  - **Caractères numériques** – Supprime tous les chiffres.  
  - **Symboles** – Supprime les symboles mathématiques, géométriques, techniques, monétaires ainsi que les symboles ressemblant à des lettres, tels que « ? », « 1 » et « ™ ».  
  - **Signes de ponctuation** – Supprime tous les signes de ponctuation.  
- **Supprimer une sous-chaîne** – Supprime la sous-chaîne spécifiée (par exemple, un mot) dans les cellules sélectionnées.

### Paramètres de la requête

| Nom du paramètre        | Type  | Emplacement | Description                                                                 |
| ----------------------- | ----- | ----------- | --------------------------------------------------------------------------- |
| removeCharactersOptions | Classe | Corps       | Options définissant les caractères, ensembles de caractères ou sous-chaînes à supprimer. |

**Schéma de `removeCharactersOptions`**

| Propriété        | Type    | Obligatoire | Description                                                                                               |
| ---------------- | ------- | ----------- | --------------------------------------------------------------------------------------------------------- |
| Range            | string  | Oui         | Notation A1 ou nom de plage identifiant les cellules à traiter (par exemple, `"A1:C10"`).                |
| CustomCharacters | string  | Non         | Chaîne contenant chaque caractère personnalisé à supprimer (par exemple, `"@#$"`).                        |
| CharacterSet     | string  | Non         | Valeur d’énumération spécifiant un ensemble prédéfini (`"NonPrinting"`, `"Text"`, `"Numeric"`, `"Symbols"`, `"Punctuation"`). |
| Substring        | string  | Non         | La sous-chaîne exacte à supprimer (par exemple, `"USD"`).                                                 |
| IgnoreCase       | boolean | Non         | Lorsque la valeur est `true`, la suppression des caractères est insensible à la casse.                   |

**Exemple de corps de requête JSON**

```json
{
  "Range": "A1:B20",
  "CustomCharacters": "@#$",
  "CharacterSet": "NonPrinting",
  "Substring": "USD",
  "IgnoreCase": true
}
```

**Exemple de requête cURL**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/removecharacters" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "Range": "A1:B20",
           "CustomCharacters": "@#$",
           "CharacterSet": "NonPrinting",
           "Substring": "USD",
           "IgnoreCase": true
         }'
```

### **Réponse**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[nom du fichier fusionné]",
    "Filesize" : [taille du fichier],
    "FileContent" : "[Base64String]"
}
```

**Codes de statut HTTP**

| Code | Signification              | Description                                                               |
|------|----------------------------|---------------------------------------------------------------------------|
| 200  | OK                         | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte         | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé               | Jeton JWT invalide ou manquant.                                          |
| 413  | Charge utile trop grande    | Le fichier uploadé dépasse la limite de taille.                         |
| 500  | Erreur interne du serveur  | Erreur inattendue sur le serveur.                                        |

## Comment utiliser l’API PostRemoveCharacters à l’aide des SDK

### Spécification de l’API PostRemoveCharacters

La <a href="https://reference.aspose.cloud/cells/#/TextProcessingController/PostRemoveCharacters" rel="noopener noreferrer">spécification OpenAPI complète du point de terminaison PostRemoveCharacters</a> définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est le meilleur moyen d’accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :
---