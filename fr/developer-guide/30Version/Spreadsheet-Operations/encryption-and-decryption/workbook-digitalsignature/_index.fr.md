---
title: "Ajouter une signature numérique à un classeur Excel"
ArticleTitle: "Ajouter une signature numérique à un classeur Excel – API Aspose.Cells Cloud"
second_title: "Document"
linktype: "Signature numérique"
type: docs
url: /fr/excel-digital-signature/
aliases:
  - /protect/digital-signature/
  - /workbook/digital-signature/
keywords: "Aspose.Cells Cloud, signature numérique, classeur Excel, API REST, .pfx, JWT, API de signature"
description: "Découvrez comment ajouter une signature numérique à un classeur Excel à l’aide de l’API REST Aspose.Cells Cloud (v4.0). Inclut l’endpoint, les paramètres, l’authentification, le schéma de réponse, la gestion des erreurs et des exemples de SDK pour plusieurs langages."
weight: 35
---


**Conditions préalables :**  
Avant d’appeler cet endpoint, assurez-vous d’avoir :

- Un jeton d’accès JWT valide obtenu via l’authentification Aspose Cloud.  
- Le classeur cible téléchargé dans votre stockage Aspose Cloud.  
- Un fichier de signature numérique au format `.pfx` ou `.p12` ainsi que son mot de passe.

Cette API REST ajoute une **signature numérique** à un classeur Excel.

## API PostDigitalSignature

```http
POST https://api.aspose.cloud/v4.0/cells/{name}/digitalsignature
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification par jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre         | Type   | Emplacement           | Description                                            |
| ------------------------ | ------ | --------------------- | ------------------------------------------------------ |
| **name**                 | string | `<code>path</code>`   | Nom du classeur.                                       |
| **digitalsignaturefile** | string | `<code>query</code>`  | Chemin du fichier de signature numérique (`.pfx` ou `.p12`). |
| **password**             | string | `<code>query</code>`  | Mot de passe du classeur, le cas échéant.             |
| **folder**               | string | `<code>query</code>`  | Dossier dans lequel le classeur est stocké.           |
| **storageName**          | string | `<code>query</code>`  | Nom du service de stockage à utiliser.                |

*Remarque : Si le nom de fichier contient des caractères spéciaux, effectuez une codage URL avant de l’ajouter à la chaîne de requête.*

### Gestion des erreurs

| Statut HTTP | Signification                                          |
| ----------- | ------------------------------------------------------ |
| 200         | Signature appliquée avec succès.                      |
| 400         | Requête incorrecte – paramètres manquants ou invalides. |
| 401         | Non autorisé – jeton OAuth invalide ou expiré.        |
| 403         | Accès refusé – permissions insuffisantes ou accès refusé. |
| 500         | Erreur interne du serveur – échec inattendu.          |

### Réponses d’erreur selon le statut HTTPS

| Statut HTTP | Code                | Description                                              |
| ----------- | ------------------- | -------------------------------------------------------- |
| 400         | BadRequest          | Paramètres manquants ou invalides.                      |
| 401         | Unauthorized        | Jeton d’accès invalide ou manquant.                     |
| 404         | NotFound            | Classeur spécifié introuvable dans le dossier/stockage indiqué. |
| 500         | InternalServerError | Erreur serveur inattendue.                              |


## Comment utiliser l’API PostDigitalSignature avec les SDK

### Spécification de l’API PostDigitalSignature

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Protection/PostDigitalSignature) définit une interface de programmation publiquement accessible et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour appeler les services web Aspose.Cells. L’exemple ci-dessous illustre une requête vers l’API :

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/digitalsignature?digitalsignaturefile=signature.pfx&password=VotreMotDePasse" \
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

**Schéma de réponse**  
L’API renvoie un objet JSON contenant les champs suivants :

| Champ         | Type   | Description                                           |
| ------------- | ------ | ----------------------------------------------------- |
| `Code`        | int    | Code de statut similaire à HTTP indiquant le résultat. |
| `Status`      | string | Court texte décrivant le résultat (par ex., `OK`).   |
| `SignatureId` | string | Identifiant de la signature numérique appliquée (facultatif). |
| `Message`     | string | Informations supplémentaires ou détails d’erreur (facultatif). |

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK simplifie l’intégration et réduit le code boilerplate. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostDigitalSignature.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostDigitalSignature.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostDigitalSignature.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostDigitalSignature.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82a2de2e4189bc27ae92abf73c36b4df0" "Example_PostDigitalSignature.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostDigitalSignature.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostDigitalSignature.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostDigitalSignature.go" >}}

{{< /tab >}}

{{< /tabs >}}