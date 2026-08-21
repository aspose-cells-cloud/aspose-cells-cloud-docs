---
title: "Protéger un classeur Excel avec l'API Aspose.Cells Cloud"
second_title: "Document"
linktitle: "Protéger un fichier Excel"
type: docs
url: /protect-excel-file/
aliases: [/protect-excel-workbooks/, /workbook/protect/]
keywords: "Aspose.Cells, protection Excel, API, REST, SDK"
description: "Découvrez comment protéger un classeur Excel via l’API REST Aspose.Cells Cloud. Inclut les étapes d’authentification, les paramètres de requête et de corps, la requête cURL ainsi que des exemples de code pour les SDK C#, Java, PHP, Ruby, Node.js, Python, Perl et Go."
weight: 30
ArticleTitle: "Protéger un classeur Excel à l’aide de l’API Aspose.Cells Cloud"
---

Cette API REST **protège** un classeur Excel, vous permettant de le sécuriser efficacement à l’aide d’un mot de passe et d’options de protection via Aspose.Cells Cloud.

## API PostProtectDocument

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/protection
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de requête

| Nom du paramètre | Type   | Description                                                                 |
| ---------------- | ------ | --------------------------------------------------------------------------- |
| folder           | string | Dossier contenant le classeur source. _(facultatif)_                       |
| storageName      | string | Nom de l’emplacement de stockage. _(facultatif ; valeur par défaut = "Default")_ |

### Paramètres du corps de la requête

| Nom du paramètre | Type                      | Description                                                       |
| ---------------- | ------------------------- | ----------------------------------------------------------------- |
| protection       | WorkbookProtectionRequest | Objet définissant les paramètres de protection du classeur.      |

#### WorkbookProtectionRequest

| Nom du paramètre | Type   | Description                                                                                                                                              |
| ---------------- | ------ | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ProtectionType   | string | Type de protection à appliquer. Valeurs autorisées (insensibles à la casse) : **ALL**, **CONTENTS**, **NONE**, **OBJECTS**, **SCENARIOS**, **STRUCTURE**, **WINDOWS**. |
| Password         | string | Mot de passe facultatif à définir pour la protection.                                                                                                    |

### Réponse

```json
{
  "Status":"OK",
  "Code":200
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                                                 |
|------|-----------------------------|----------------------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête            | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                                             |
| 413  | Charge utile trop grande     | Le fichier téléchargé dépasse la limite de taille.                         |
| 500  | Erreur interne du serveur    | Erreur serveur inattendue.                                                 |

## Comment utiliser l’API PostProtectDocument avec les SDK

### Conditions préalables

Avant d’appeler l’API, assurez-vous d’avoir effectué les étapes suivantes :

- **Obtenir un jeton d’accès JWT** conformément au processus d’authentification décrit dans la section **Sécurité et authentification**.  
- **Télécharger le classeur** dans votre stockage Aspose Cloud ou vérifier qu’il existe déjà dans le dossier cible.  
- **Connaître le nom du stockage** (valeur par défaut : `"Default"` si non spécifié) et le nom exact du fichier à protéger.

### Spécification de l’API PostProtectDocument

La <a href="https://apireference.aspose.cloud/cells/#/Workbook/PostProtectDocument" target="_blank" rel="noopener noreferrer">spécification OpenAPI</a> définit une interface de programmation accessible publiquement et permet d’effectuer directement des interactions REST depuis un navigateur web.

### Exemple : protéger un classeur à l’aide de cURL

1. Obtenir un jeton d’accès comme décrit dans **Conditions préalables / Authentification**.  
2. Exécuter la requête :

   ```bash
   curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/protection?folder=MyFolder&storageName=MyStorage" \
        -H "accept: application/json" \
        -H "Content-Type: application/json" \
        -H "Authorization: Bearer <access_token>" \
        -d '{ "ProtectionType": "ALL", "Password": "aspose" }'
   ```

   La réponse contiendra un objet d’état confirmant que la protection a réussi.

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK constitue la méthode la plus rapide pour développer avec Aspose.Cells Cloud. Un SDK abstrait les détails de bas niveau, vous permettant de vous concentrer sur votre logique métier. Consultez le <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostProtectWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostProtectWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostProtectWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostProtectWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostProtectWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostProtectWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostProtectWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostProtectWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

### Réponse complète d’exemple

```json
{
  "Status": "OK",
  "Code": 200,
  "Workbook": {
    "Name": "test.xlsx",
    "Path": "/MyFolder/test.xlsx",
    "Protection": {
      "ProtectionType": "ALL",
      "Password": true
    }
  }
}
```