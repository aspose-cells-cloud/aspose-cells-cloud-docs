---
title: "API de fractionnement de texte – Segmenter les cellules Excel en colonnes | Aspose.Cells Cloud"
second_title: "Document"
ArticleTitle: "Diviseur de texte Excel – Segmenter le contenu des cellules en plusieurs colonnes | Aspose.Cells Cloud"
linktitle: "Fractionner le texte"
type: docs
url: /fr/split-text/
keywords: "Aspose, Cells, API de fractionnement de texte, Excel, délimiteur, segmentation de texte, API cloud"
description: "Divisez facilement le texte des cellules Excel en colonnes ou lignes distinctes à l’aide d’Aspose.Cells Cloud. Prend en charge les délimiteurs personnalisés, masques, sauts de ligne et la conservation éventuelle des délimiteurs. Commencez en quelques minutes avec curl ou les SDK."
weight: 100
---

Segmentez le texte des cellules Excel en plusieurs colonnes à l’aide de règles de segmentation personnalisées. Divisez le contenu par délimiteur et exportez-le dans des plages spécifiées grâce à l’API Web de fractionnement de texte d’Aspose.Cells Cloud.

## **Introduction** : Fractionner le texte

L’API de segmentation de texte divise le contenu des cellules en plusieurs cellules en fonction de délimiteurs, motifs ou sauts de ligne spécifiés, puis écrit les résultats dans une plage cible. Elle prend en charge des méthodes de fractionnement flexibles, une sortie directionnelle (colonnes ou lignes) et la possibilité de conserver les délimiteurs — idéal pour analyser des données concaténées, du contenu de type CSV ou du texte multiligne afin de les structurer.

- **Fractionner une cellule selon un caractère spécifique** – décomposez le contenu d’une cellule en plusieurs cellules en sélectionnant n’importe quel caractère comme délimiteur (virgule, espace, point-virgule, etc.).
- **Fractionner des cellules selon une chaîne** – séparez les cellules selon n’importe quelle combinaison de caractères que vous spécifiez.
- **Fractionner le texte selon un masque** – utilisez des caractères génériques pour diviser le texte selon un motif particulier, offrant une méthode encore plus flexible et puissante pour le fractionnement de texte.
- **Diviser le contenu des cellules selon des sauts de ligne** – créez une présentation plus organisée en fractionnant selon les sauts de ligne.
- **Diviser les cellules en colonnes ou en lignes** – choisissez si les résultats du fractionnement sont écrits dans des colonnes ou des lignes consécutives.
- **Supprimer ou conserver les délimiteurs** – décidez si les délimiteurs sont supprimés ou conservés au début ou à la fin des cellules résultantes.

## **API SplitText**

**Prérequis** : Pour utiliser cette API, vous devez disposer d’un jeton d’accès Aspose Cloud valide, et le classeur à traiter doit être téléchargé dans le stockage Aspose Cloud ou fourni directement dans la requête. L’API prend en charge les formats de feuille de calcul courants tels que XLSX, XLS, ODS et CSV.

### API Web

```http
POST https://api.aspose.cloud/v4.0/cells/content/split/text
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Paramètres de requête de l’API **splitText**

| Nom du paramètre               | Type    | Emplacement | Obligatoire ? | Valeur par défaut | Description                                                                                                                                                     |
| ------------------------------ | ------- | ----------- | ------------- | ----------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| spreadsheet                    | File    | FormData    | Oui           | —                 | Fichier de feuille de calcul à traiter. Les formats pris en charge incluent XLSX, XLS, ODS, CSV, etc.                                                          |
| delimiters                     | String  | Query       | Non           | —                 | Un ou plusieurs caractères délimiteurs utilisés pour fractionner le texte à l’intérieur des cellules (par ex., `","`, `";"`, `Space`, `LineBreak`, `Tab`, `Pipe`, `Custom`). |
| keepDelimitersInResultingCells | Boolean | Query       | Non           | false             | Si `true`, les caractères délimiteurs sont conservés dans les cellules fractionnées résultantes.                                                              |
| keepDelimitersPosition         | String  | Query       | Non           | None              | Emplacement de conservation des délimiteurs si `keepDelimitersInResultingCells` est `true`. Options : `None`, `AtTheBeginning`, `AtTheEnd`, `BeforeText`, `AfterText`. |
| howToSplit                     | String  | Query       | Non           | SplitToColumns    | Méthode de segmentation du texte. Options : `None`, `SplitToColumns`, `SplitToRows`.                                                                           |
| outPositionRange               | String  | Query       | Oui           | —                 | Plage cible où les résultats du fractionnement seront écrits (par ex., `"D1:F10"`).                                                                             |
| worksheet                      | String  | Query       | Non           | —                 | Nom de la feuille de calcul à laquelle le fractionnement de texte sera appliqué. Si omis, la première feuille est utilisée.                                   |
| range                          | String  | Query       | Non           | —                 | Plage de cellules source à laquelle l’opération de fractionnement est appliquée (par ex., `"A1:A10"`). Si omis, toutes les cellules utilisées de la feuille sont traitées. |
| outPath                        | String  | Query       | Non           | —                 | Chemin du dossier dans le stockage cloud où le classeur traité sera enregistré. Si omis, le fichier est enregistré dans le dossier source.                    |
| outStorageName                 | String  | Query       | Non           | —                 | Nom du stockage cloud où le fichier de sortie sera stocké.                                                                                                     |
| region                         | String  | Query       | Non           | —                 | Paramètres régionaux pour la segmentation de texte, pouvant affecter l’interprétation des délimiteurs et l’encodage des caractères (par ex., `"en-US"`, `"ja-JP"`). |
| password                       | String  | Query       | Non           | —                 | Mot de passe pour ouvrir une feuille de calcul protégée par mot de passe.                                                                                      |

### **Réponse**

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

### Codes d’erreur

- **400 Bad Request** – URI de l’API Aspose.Cells Cloud invalide ou paramètres mal formés.
- **401 Unauthorized** – Jeton d’accès manquant ou invalide (ou client-id/secret).
- **404 Not Found** – Le fichier de feuille de calcul spécifié n’a pas pu être accessible.
- **500 Server Error** – Une anomaly interne s’est produite lors du traitement de la feuille de calcul.

## Où faut-il utiliser l’API de fractionnement de texte ?

### **Nettoyage des importations CSV et fichiers texte**

Lors de l’importation de données depuis des systèmes externes, les champs sont souvent concaténés dans des cellules uniques :

- **Importations de données ERP/CRM** – divisez `"Jean Dupont;jeandupont@email.com;0123456789"` en colonnes séparées pour nom, email et téléphone.
- **Exportations de bases de données** – analysez des clés combinées comme `"COM-2024-001|Premium|Express"` en ID de commande, niveau et méthode d’expédition.
- **Analyse de journaux** – décomposez des journaux semi-structurés tels que `"2024-01-15 10:30:00|ERROR|ConnectionTimeout"` pour les filtrer.

### **Migration des systèmes hérités**

- Les anciens systèmes stockent des champs à valeurs multiples dans des cellules uniques ; divisez-les pour correspondre aux nouveaux schémas de base de données.
- Convertissez les exports de fichiers plats en tables Excel normalisées, prêtes à être utilisées avec Power BI ou Tableau.

### **Nettoyage et standardisation des données**

- **Normalisation des délimiteurs** – convertissez des délimiteurs mixtes (`"A,B;C|D"`) en un format uniforme à l’aide d’un fractionnement multi-délimiteur.
- **Nettoyage des espaces** – divisez selon les espaces pour identifier et supprimer les espaces supplémentaires entre les mots.
- **Données financières** – divisez des codes de transaction combinés comme `"DEP-CHK-3847"` en type de transaction, source et référence.
- **Dossiers médicaux** – analysez les données patient telles que `"Dupont,Jean_F_1985"` en nom de famille, prénom, sexe et année de naissance.

## Pourquoi utiliser l’API de fractionnement de texte ?

- **Caractères spécifiques** – fractionnez selon n’importe quel caractère unique (virgule, point-virgule, tabulation, espace).
- **Combinaisons de chaînes** – utilisez des délimiteurs multi-caractères comme `||`, `->` ou des séparateurs personnalisés.
- **Sauts de ligne** – analysez instantanément les cellules multilignes en lignes distinctes (adresses, commentaires, descriptions).
- **Délimiteurs personnalisés** – définissez n’importe quelle combinaison de caractères comme délimiteur pour les formats de données propriétaires.
- **Adapté aux développeurs** – Aspose.Cells Cloud propose des bibliothèques SDK dans plusieurs langages, permettant un développement rapide, accompagné d’une documentation complète. Comparé à la construction de solutions personnalisées, cela réduit considérablement la charge de développement.
- **Économique** – vous pouvez supprimer les caractères en double sans avoir à télécharger préalablement le classeur, ce qui économise de l’espace de stockage et réduit les coûts.

## Spécification OpenAPI

La [Spécification OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/SplitText) définit une interface de programmation publiquement accessible et vous permet d’effectuer directement des interactions REST depuis un navigateur web.

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est le meilleur moyen d’accélérer le développement. Le SDK gère les détails sous-jacents, vous permettant ainsi de simplement implémenter le fractionnement de texte pour les cellules avec un minimum de code. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitText.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitText.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitText.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitText.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitText.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitText.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitText.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitText.go" >}}  
{{</tab>}}  
{{< /tabs >}}