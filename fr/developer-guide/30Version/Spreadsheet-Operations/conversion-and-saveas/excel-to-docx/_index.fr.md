---
title: "Excel vers Docx"
second_title: "Document"
linktitle: "Excel vers Docx"
type: docs
url: /frconvert-excel-file-to-docx-file/
keywords: "conversion Excel vers Docx, Aspose.Cells Cloud, API REST, conversion de feuilles de calcul, génération de documents"
description: "Convertir des feuilles de calcul Excel en documents DOCX à l'aide de l'API REST Aspose.Cells Cloud. Prend en charge plusieurs SDK et langages de programmation pour une intégration fluide."
weight: 90
---

Cette API REST convertit un fichier de feuille de calcul en format DOCX.

## API REST

```http
POST https://api.aspose.cloud/v3.0/cells/convert/docx
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.



**Paramètres de requête**

| Nom du paramètre      | Type   | Description                                                                                           |
| --------------------- | ------ | ----------------------------------------------------------------------------------------------------- |
| password              | string | Le mot de passe requis pour ouvrir le fichier Excel.                                                 |
| storageName           | string | Le nom du stockage où se trouve le fichier.                                                          |
| checkExcelRestriction | bool   | Indique s’il faut vérifier les restrictions du fichier Excel lorsque l’utilisateur modifie des objets liés aux cellules. |

**Paramètre du corps de la requête**

| Nom du paramètre | Type      | Description                                                     |
| ---------------- | --------- | --------------------------------------------------------------- |
| datafile         | data file | Le fichier de données stocké dans la première partie du corps de la requête multipart. |

**Réponse**

L’API renvoie un objet **FileInfo** contenant le fichier Word généré.

| Champ           | Type   | Description                                     |
| --------------- | ------ | ----------------------------------------------- |
| **Filename**    | string | Nom du fichier Word (par ex., `exemple.docx`). |
| **FileSize**    | int    | Taille du fichier en octets.                    |
| **FileContent** | string | Contenu du fichier Word encodé en Base64.      |


[FileInfo](/cells/file-info/)

**Codes de statut HTTP**

| Code | Signification               | Description                                           |
|------|-----------------------------|-------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par ex., type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                       |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la taille maximale autorisée. |
| 500  | Erreur interne du serveur   | Erreur inattendue sur le serveur.                    |
## Comment utiliser l’API PostConvertWorkbookToDocx avec les SDK

### Spécification de l’API PostConvertWorkbookToDocx

La [spécification OpenAPI](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToDocx) définit une interface de programmation publiquement accessible et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour accéder facilement aux services web Aspose.Cells. L’exemple ci-dessous montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/docx" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d '{"File":{}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "exemple.docx",
  "FileSize": 12345,
  "FileContent": "Contenu du fichier : chaîne_encodée_en_base64"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est le meilleur moyen d’accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code ci-dessous montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToDocx.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToDocx.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToDocx.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToDocx.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToDocx.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToDocx.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToDocx.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToDocx.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Autres API implémentant cette fonctionnalité

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Enregistre un fichier Excel en tant que fichier DOCX avec des paramètres supplémentaires et stocke le résultat dans le stockage spécifié.

- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Convertit un fichier Excel en fichier DOCX avec des paramètres facultatifs et renvoie le résultat dans la réponse.

- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Récupère un classeur Excel et le convertit en fichier DOCX avec des paramètres facultatifs.

---