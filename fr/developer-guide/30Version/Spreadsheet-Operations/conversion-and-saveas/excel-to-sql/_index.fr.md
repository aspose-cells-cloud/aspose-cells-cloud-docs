---
title: "Excel vers SQL"
second_title: "Document"
linktitle: "Excel vers SQL"
type: docs
url: /fr/convert-excel-file-to-sql-file/
keywords: "Aspose.Cells, Excel vers SQL, API cloud, conversion de feuille de calcul, REST"
description: "Utilisez l’API REST Aspose.Cells Cloud pour convertir des feuilles de calcul Excel en fichiers SQL. Prend en charge de multiples SDK et langages de programmation pour une intégration fluide dans vos applications."
weight: 100
ArticleTitle: "Convertir Excel en SQL – Aspose.Cells Cloud API"
---

Cette API REST convertit un fichier de feuille de calcul en un fichier au format SQL.

**Prérequis**  
Pour utiliser ce point de terminaison, vous devez posséder un jeton JWT valide généré comme décrit dans le guide <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>. L’API prend en charge les fichiers Excel jusqu’à la limite de taille définie dans la documentation du service et peut gérer les classeurs protégés par mot de passe lorsque le paramètre de requête `password` est fourni.

## API PostConvertWorkbookToSQL

```http
POST https://api.aspose.cloud/v3.0/cells/convert/sql
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètre de requête**

| Nom du paramètre      | Type   | Description                                                                 |
| --------------------- | ------ | --------------------------------------------------------------------------- |
| password              | string | Mot de passe requis pour ouvrir le fichier Excel.                         |
| storageName           | string | Nom du stockage où le fichier est stocké.                                 |
| checkExcelRestriction | bool   | Indique s’il faut vérifier les restrictions des fichiers Excel lors de la modification d’objets liés aux cellules. |

### **Paramètre du corps de la requête**

| Nom du paramètre | Type      | Description                                                           |
| ---------------- | --------- | --------------------------------------------------------------------- |
| datafile         | fichier | Le fichier de feuille de calcul à convertir, inclus comme première partie de la requête. |

### Réponse

L’API renvoie un objet **FileInfo** contenant le fichier SQL généré.

| Champ           | Type   | Description                                        |
| --------------- | ------ | -------------------------------------------------- |
| **Filename**    | string | Nom du fichier SQL (par exemple, `exemple.sql`). |
| **FileSize**    | int    | Taille du fichier en octets.                       |
| **FileContent** | string | Contenu du fichier SQL encodé en Base64.          |

[FileInfo](/cells/file-info/)

**Codes de statut HTTP**

| Code | Signification                | Description                                                   |
|------|------------------------------|---------------------------------------------------------------|
| 200  | OK                           | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte           | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                 | Jeton JWT invalide ou manquant.                               |
| 413  | Charge utile trop grande     | Le fichier téléchargé dépasse la limite de taille.           |
| 500  | Erreur interne du serveur    | Erreur inattendue du serveur.                                 |

## Comment utiliser l’API PostConvertWorkbookToSQL avec les SDK

### Spécification de l’API PostConvertWorkbookToSQL

La <a href="https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToSQL" rel="noopener noreferrer">spécification OpenAPI</a> définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels vers l’API cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/sql" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d '{"File":{}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "exemple.sql",
  "FileSize": 1024,
  "FileContent": "chaîne_encodée_en_base64"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est le meilleur moyen d’accélérer le développement. Un SDK gère les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToSQL.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToSQL.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToSQL.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToSQL.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToSQL.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToSQL.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToSQL.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToSQL.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Autres API implémentant cette fonctionnalité

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Enregistre un classeur dans un autre format et stocke le résultat dans le stockage spécifié.

- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Convertit un classeur dans un autre format avec des paramètres facultatifs et renvoie le résultat dans la réponse.

- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Récupère un classeur avec des paramètres de conversion facultatifs.

**Notes**  
- Lors de la conversion de fichiers Excel protégés par mot de passe, assurez-vous que le paramètre de requête `password` est fourni ; sinon, la conversion échouera avec une erreur 400.  
- Le service renvoie le contenu du fichier SQL encodé en Base64 ; décodez-le avant de l’enregistrer dans un fichier `.sql`.  

**Fichiers d’exemple**  
Téléchargez un classeur Excel d’exemple [ici](https://example.com/sample.xlsx) et un résultat SQL pré-généré [ici](https://example.com/sample.sql) pour tester rapidement l’API.