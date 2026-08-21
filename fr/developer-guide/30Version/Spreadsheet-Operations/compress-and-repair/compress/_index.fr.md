---
title: "Compresser les données dans un fichier Excel"
ArticleTitle: "Compresser les données dans un fichier Excel – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Compresser les fichiers Excel"
type: docs
url: /compress-excel-files/
aliases: [/compress/]
keywords: "compresser fichier Excel, Aspose Cells Cloud, compression Excel, compression feuille de calcul, API REST, compression de fichiers"
description: "Compresser des fichiers Excel (XLS, XLSX, XLSM, XLSB, ODS) à l’aide de l’API REST Aspose.Cells Cloud. Définir le niveau de compression, gérer plusieurs fichiers et intégrer via les SDK."
weight: 39
---

## L’API PostCompress des services web Aspose.Cells Cloud

**Prérequis :**  
- Un jeton JWT valide est requis pour l’authentification.  
- Les formats de fichier pris en charge sont XLS, XLSX, XLSM, XLSB et ODS.  
- La taille maximale autorisée par fichier est de 500 Mo par requête (sous réserve des limites du service).

Cette API REST compresse les données d’un fichier Excel.

- Compresser XLS, XLSX, XLSM, XLSB, ODS  
- Compresser rapidement plusieurs fichiers de feuilles de calcul Excel  
- Choisir le niveau de compression  
- Prend en charge plusieurs fichiers

### Point de terminaison de l’API web

```http
POST https://api.aspose.cloud/v3.0/cells/compress
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement (chemin/chaîne de requête/ Corps HTTP) | Description                                                |
|------------------|---------|-----------------------------------------------------|------------------------------------------------------------|
| file             | fichier | formData                                            | Fichier à télécharger                                      |
| CompressLevel    | entier  | query                                               | Niveau de compression (0‑100) ; des valeurs plus élevées indiquent une compression plus forte |

### Paramètre du corps de la requête

| Nom du paramètre | Type | Description                                    |
| ------------------ | ---- | ---------------------------------------------- |
| data               | fichier | Contenu binaire du classeur à compresser. |

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

*Remarque :* `FileContent` contient le classeur compressé codé en Base64. La longueur de la chaîne correspond à la taille du fichier compressé ; vous pouvez le décoder à l’aide d’outils standards de Base64 pour récupérer le fichier Excel binaire.

**Codes de statut HTTP**

| Code | Signification               | Description                                                    |
|------|-----------------------------|----------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par ex., type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT non valide ou manquant. |
| 413  | Charge utile trop grande    | Le fichier téléchargé dépasse la limite de taille. |
| 500  | Erreur interne du serveur   | Erreur inattendue du serveur. |

## Comment utiliser l’API PostCompress avec les SDK

### Spécification de l’API PostCompress

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostCompress) définit une interface de programmation publiquement accessible et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple ci-dessous montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
# Utiliser HTTPS pour une connexion sécurisée
curl -v "https://api.aspose.cloud/v3.0/cells/compress?CompressLevel=88" \
-X POST \
-H "Content-Type: multipart/form-data" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jeton jwt>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'
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

L’utilisation d’un SDK est le moyen le plus rapide d’accélérer le développement. Un SDK masque les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCompress.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCompress.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCompress.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCompress.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCompress.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCompress.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCompress.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCompress.go" >}}

{{< /tab >}}

{{< /tabs >}}