---
title: "Aspose.Cells Cloud Split Excel Web API – Découper localement un fichier Excel en plusieurs fichiers et exporter vers plus de 30 formats"
second_title: "Document"
ArticleTitle: "Outil de découpage Excel – Diviser une feuille de calcul locale en plusieurs fichiers dans plus de 30 formats"
linktype: "Split Spreadsheet"
type: docs
url: /fr/split-spreadsheet/
keywords: "découper, excel, aspose cells, API de feuille de calcul, exporter en pdf, csv, json"
description: "Découper un classeur Excel localement en fichiers séparés à l’aide de l’API Aspose.Cells Cloud. Exportez vers plus de 30 formats (PDF, CSV, JSON, XLSX, HTML) sans avoir à téléverser vers le cloud."
weight: 100
---

Découpez entièrement un classeur Excel local en fichiers distincts — aucun stockage dans le cloud n’est requis. Le format de sortie prend en charge plus de 30 types de fichiers, notamment PDF, CSV, JSON, ODS et XPS.

## **API de découpage de feuille de calcul**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/split/spreadsheet
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Paramètres de la requête :**

| Nom du paramètre | Type    | Emplacement (Chemin / Chaîne de requête / Corps HTTP) | Description                                                                                                                                                                                                 |
| :--------------- | :------ | :----------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | Fichier | FormData                                               | Le fichier de feuille de calcul local à découper. Les formats pris en charge incluent XLSX, XLS, ODS, CSV, etc. Le fichier est traité entièrement côté serveur, sans nécessiter de stockage cloud.           |
| from             | Entier  | Chaîne de requête                                      | L’index de départ (à partir de zéro) de l’intervalle de feuilles à découper (par exemple, `0` pour la première feuille).                                                                                 |
| to               | Entier  | Chaîne de requête                                      | L’index de fin (à partir de zéro) de l’intervalle de feuilles à découper (par exemple, `2` découpera les feuilles 0, 1 et 2).                                                                              |
| outFormat        | Chaîne  | Chaîne de requête                                      | Le format de sortie des fichiers découpés. Prend en charge plus de 30 formats, notamment `PDF`, `CSV`, `JSON`, `XLSX`, `HTML`.                                                                             |
| outPath          | Chaîne  | Chaîne de requête                                      | _(Facultatif)_ Le chemin du dossier local où les fichiers découpés seront enregistrés. Si omis, les fichiers sont enregistrés dans un emplacement temporaire par défaut.                                   |
| outStorageName   | Chaîne  | Chaîne de requête                                      | L’identifiant du stockage utilisé pour organiser les fichiers de sortie. En mode de traitement local, cela fait généralement référence à un libellé de stockage basé sur la session ou défini par l’utilisateur. |
| fontsLocation    | Chaîne  | Chaîne de requête                                      | _(Facultatif)_ Spécifie un répertoire local ou personnalisé de polices afin de garantir un rendu précis du texte lors de l’export vers les formats PDF ou images.                                          |
| region           | Chaîne  | Chaîne de requête                                      | _(Facultatif)_ Définit la localisation pour le format des nombres, des dates et des devises dans les fichiers de sortie (par exemple, `"fr-FR"`, `"en-US"`).                                                |
| password         | Chaîne  | Chaîne de requête                                      | _(Facultatif)_ Si la feuille de calcul téléchargée est protégée par mot de passe, fournir ce mot de passe pour ouvrir et traiter le fichier.                                                                 |

## **Réponse**

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

Le fichier peut être téléchargé directement ou enregistré à l’emplacement spécifié par `outPath`.

**Détails de la réponse en cas de succès**

| Code d’état | Type de contenu            | Description                                      |
| ----------- | -------------------------- | ------------------------------------------------ |
| 200 OK      | `application/octet-stream` | Flux binaire du fichier classeur fusionné.      |

**Codes d’état HTTP**

| Code | Signification             | Description                                                           |
| ---- | ------------------------- | --------------------------------------------------------------------- |
| 200  | OK                        | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte        | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé              | Jeton JWT invalide ou manquant.                                      |
| 413  | Charge utile trop grande   | Le fichier téléchargé dépasse la taille maximale autorisée.         |
| 500  | Erreur interne du serveur  | Erreur inattendue sur le serveur.                                    |

## Où utiliser l’API de découpage de feuille de calcul ?

- **Distribution des données par service** : Découper un classeur unifié contenant des données provenant de plusieurs services en fichiers spécifiques à chaque service.
- **Distribution des rapports régionaux** : Découper les états de ventes nationaux en fichiers distincts par région.
- **Distribution de données clients avec masquage** : Découper un classeur contenant des informations sensibles en fichier dédié pour une vision client.
- **Découpage périodique des rapports** : Découper automatiquement les rapports synthétiques en rapports hebdomadaires ou quotidiens sur une base mensuelle.
- **Distribution multi-format** : Découper un seul fichier Excel en plusieurs versions au format PDF, CSV, JSON, etc., simultanément.
- **Découpage selon des modèles** : Découper les fichiers de données en fichiers de sortie standardisés selon des modèles prédéfinis.
- **Prétraitement des sources de données** : Découper le fichier Excel en fichier CSV standardisé avant de charger les données dans une base de données.
- **Préparation des données pour API** : Découper de grands jeux de données en lots plus petits, adaptés au transfert via API.

## Pourquoi utiliser l’API de découpage de feuille de calcul ?

- **Adaptée aux développeurs** : Aspose.Cells Cloud propose des bibliothèques SDK dans plusieurs langages, permettant un développement rapide et accompagné d’une documentation complète. Comparé à la mise en place de solutions personnalisées de rendu de graphiques, cela réduit considérablement la charge de développement.
- **Réduction des coûts de main-d’œuvre** : Réduit la nécessité de postes dédiés à la consolidation de documents.
- **Paiement à l’usage** : Aucun investissement initial ; vous ne payez que pour les appels API réellement utilisés.
- **Zéro coût de maintenance** : Pas besoin de maintenir des serveurs, mettre à jour des logiciels ou gérer des problèmes de compatibilité.
- **Préservation de la mise en forme Excel complexe** au format PDF universellement accessible.

## Comment utiliser l’API de découpage de feuille de calcul avec les SDK ?

### Spécification de l’API de découpage de feuille de calcul

La [spécification de l’API de découpage de feuille de calcul](https://reference.aspose.cloud/cells/#/DataProcessingController/SplitSpreadsheet) fournit une interface de programmation publiquement accessible pour effectuer des interactions REST directement depuis un navigateur web.
Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/split/spreadsheet?outFormat=PDF" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@monClasseur.xlsx" \
  -o split-spreadsheet.zip
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (encodé en Base64)",
  "contentType": "type MIME",
  "fileDownloadName": "nom de fichier optionnel"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour développer, car elle masque les détails de bas niveau, vous permettant de découper la feuille de calcul en fichiers distincts à l’aide de quelques lignes de code.  
Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment invoquer les services web Aspose.Cells à l’aide de différents SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitLocalFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitLocalFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitLocalFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitLocalFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitLocalFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitLocalFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitLocalFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitLocalFile.go" >}}
{{</tab>}}
{{< /tabs >}}

---