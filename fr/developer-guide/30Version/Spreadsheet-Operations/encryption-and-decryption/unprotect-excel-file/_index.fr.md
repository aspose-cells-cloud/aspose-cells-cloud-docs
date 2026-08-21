---
title: "Déproteger un classeur Excel – API Aspose.Cells Cloud"
second_title: "Document"
linktitle: "Déproteger un fichier Excel"
type: docs
url: /fr/excel-file-unprotect/
aliases:
  - /unprotect-excel-workbooks/
  - /workbook/unprotect/
keywords: "Aspose Cells, API de déprotection Excel, supprimer la protection d'un classeur, API REST, feuille de calcul cloud"
description: "Découvrez comment supprimer la protection d’un classeur Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut la syntaxe des requêtes, les paramètres, un exemple cURL et du code SDK dans plusieurs langages."
weight: 60
ArticleTitle: "Déproteger un classeur Excel – API Aspose.Cells Cloud"
---

Utilisez cette API REST pour déprotéger un classeur Excel.

## API DeleteUnProtectWorkbook

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/protection
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de chemin

| Paramètre | Type   | Description                                            | Obligatoire |
| --------- | ------ | ------------------------------------------------------ | ----------- |
| **name**  | string | Nom du fichier du classeur (y compris l’extension).   | Oui         |

### Paramètres de requête

| Nom du paramètre | Type   | Description                                              |
| ---------------- | ------ | -------------------------------------------------------- |
| folder           | string | Chemin du dossier contenant le classeur d’origine.      |
| storageName      | string | Nom du service de stockage où réside le classeur.       |

### Paramètres du corps de la requête

| Nom du paramètre | Type                      | Description                                                |
| ---------------- | ------------------------- | ---------------------------------------------------------- |
| protection       | WorkbookProtectionRequest | Objet spécifiant les paramètres de protection à supprimer. |

#### WorkbookProtectionRequest

| Nom du paramètre | Type   | Description                                                                                                      |
| ---------------- | ------ | ---------------------------------------------------------------------------------------------------------------- |
| ProtectionType   | string | Type de protection à supprimer (`ALL`, `CONTENTS`, `NONE`, `OBJECTS`, `SCENARIOS`, `STRUCTURE`, `WINDOWS`). |
| Password         | string | Mot de passe requis pour supprimer la protection (facultatif).                                                  |

#### Exemple cURL

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/protection?folder=MyFolder&storageName=MyStorage" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -d '{ "ProtectionType": "ALL", "Password": "aspose"}'
```

#### Réponse (succès)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Réponses d’erreur HTTP (statut HTTPS)

| Statut HTTP | Code                | Description                                                           |
| ----------- | ------------------- | --------------------------------------------------------------------- |
| 400         | BadRequest          | Paramètres manquants ou non valides.                                 |
| 401         | Unauthorized        | Jeton d’accès invalide ou manquant.                                  |
| 404         | NotFound            | Classeur spécifié introuvable dans le dossier/le stockage indiqué.  |
| 500         | InternalServerError | Erreur serveur inattendue.                                            |

## Comment utiliser l’API DeleteUnProtectWorkbook avec les SDK

### Spécification de l’API DeleteUnProtectWorkbook

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Protection/DeleteUnProtectWorkbook) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple ci-dessous montre comment effectuer des appels vers l’API Cloud avec cURL.

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK simplifie l’intégration et réduit le code boilerplate. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code ci-dessous illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteUnProtectWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteUnProtectWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteUnProtectWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteUnProtectWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteUnProtectWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteUnProtectWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteUnProtectWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteUnProtectWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}