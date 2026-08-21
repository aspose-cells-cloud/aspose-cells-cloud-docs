---
title: "Aspose.Cells Cloud Web API – Supprimer automatiquement les feuilles de calcul vierges/vides"
second_title: "Document"
ArticleTitle: "Supprimer toutes les feuilles vierges dans Excel – Guide pour supprimer les feuilles vides"
linktype: "docs"
url: /fr/delete-spreadsheet-blank-worksheets/
keywords: "Aspose.Cells Cloud, supprimer les feuilles vierges, Excel API, nettoyage du classeur, optimisation des feuilles de calcul"
description: "Utilisez l’API Aspose.Cells Cloud pour supprimer automatiquement les feuilles de calcul vierges ou vides des classeurs Excel. Découvrez comment identifier et supprimer les feuilles ne contenant aucune donnée, formule, graphique ou objet, améliorant ainsi la performance et l’organisation des classeurs."
weight: 100
---

Supprimez automatiquement toutes les feuilles de calcul vierges des classeurs Excel à l’aide de l’API Aspose.Cells Cloud. Notre API intelligente détecte et supprime les feuilles ne contenant aucune donnée, formule, graphique, commentaire ou objet, tout en conservant toutes les feuilles contenant des éléments. Prend en charge le traitement par lots, l’automatisation cloud et une intégration transparente pour les flux de travail d’entreprise de nettoyage de classeurs.

## **DeleteSpreadsheetBlankWorksheets API**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/delete/blank-worksheets
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Paramètres de la requête :**

| Nom du paramètre | Type   | Emplacement (chemin / chaîne de requête / corps HTTP) | Description                                                                                                                                                                                                                        |
| :--------------- | :----- | :-------------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | Fichier | FormData                                      | **Obligatoire**. Le fichier de classeur Excel à nettoyer. Prend en charge les formats tels que `.xlsx`, `.xls`, `.xlsm`, `.xlsb` et `.ods`.                                                                                       |
| outPath          | Chaîne  | Chaîne de requête                             | **Facultatif**. Le chemin du dossier cible dans le stockage cloud où le fichier de sortie sera enregistré. S’il est laissé vide ou défini sur `null`, le fichier traité sera stocké à l’emplacement par défaut ou dans le même répertoire que le fichier source. |
| outStorageName   | Chaîne  | Chaîne de requête                             | **Obligatoire**. Le nom du service de stockage cloud configuré où le fichier de sortie doit être enregistré (par exemple, `MyFirstStorage`). Ce paramètre spécifie l’espace de stockage dans lequel écrire les résultats.                               |
| region           | Chaîne  | Chaîne de requête                             | **Facultatif**. Le paramètre régional/linguistique appliqué lors du traitement du classeur, tel que `en-US` ou `zh-CN`. Celui-ci peut affecter le traitement des formats de date, nombre et texte.                                                          |
| password         | Chaîne  | Chaîne de requête                             | **Facultatif**. Le mot de passe requis pour ouvrir un fichier Excel protégé par mot de passe. Ce paramètre peut être omis si le fichier téléchargé n’est pas chiffré.                                                                                  |

## **Réponse**

L’API renvoie le classeur traité sous forme de flux de fichiers.

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

- **Code d’état de réussite :** `200 OK` – le classeur a été traité et le fichier nettoyé est renvoyé dans le corps de la réponse.  
- **Content‑Type :** `application/octet-stream`

### Codes d’erreur

- **400 Bad Request** : URI d’API Aspose.Cells Cloud invalide.  
- **401 Unauthorized** : Jeton d’accès invalide, ou identifiant client et secret invalides.  
- **404 Not Found** : Le fichier de feuille de calcul n’est pas accessible.  
- **500 Server Error** : Une anomaly s’est produite lors de l’extraction des données de calcul dans la feuille de calcul.

## Où utiliser l’API Delete Spreadsheet Blank Worksheets ?

- **Nettoyage après consolidation de données** : Après avoir fusionné des données provenant de plusieurs fichiers sources dans un seul classeur, supprimez automatiquement les feuilles restantes ou les feuilles de remplacement créées pendant le processus mais ne contenant aucune donnée.  
- **Génération de rapports basée sur des modèles** : Dans les flux de travail utilisant des modèles Excel contenant plusieurs feuilles prédéfinies, nettoyez toutes les feuilles de modèle inutilisées après avoir rempli uniquement celles nécessaires avec des données.  
- **Pipelines automatisés de traitement de données (ETL)** : Comme étape de prétraitement pour nettoyer les classeurs Excel reçus de divers systèmes ou téléchargements utilisateurs avant analyse, stockage ou intégration supplémentaires, afin de ne traiter que les feuilles contenant effectivement du contenu.  
- **Optimisation et migration de classeurs hérités** : Lors de la modernisation ou de la consolidation d’anciens fichiers Excel volumineux, qui accumulent souvent de nombreuses feuilles vides ou obsolètes au fil du temps.  
- **Portails de contenus générés par les utilisateurs** : Nettoyez et standardisez les classeurs soumis par les utilisateurs via des applications web ou des formulaires, en supprimant les feuilles vides accidentelles pour maintenir une qualité professionnelle et cohérente des fichiers.

## Pourquoi utiliser l’API Delete Spreadsheet Blank Worksheets ?

- **Adapté aux développeurs** : Aspose.Cells Cloud propose des bibliothèques SDK dans plusieurs langages, facilitant un développement rapide, accompagné d’une documentation complète. Comparé à la création de solutions sur mesure, cela réduit considérablement la charge de développement.  
- **Réduction des coûts en main-d’œuvre** : Réduit la nécessité de recruter des postes dédiés à la consolidation de documents.  
- **Pay-per-use** : Aucun investissement initial, vous ne payez que pour les appels API effectivement utilisés.  
- **Coûts de maintenance nuls** : Aucune maintenance serveur, mise à jour logicielle ou gestion des problèmes de compatibilité nécessaire.

## Comment utiliser l’API Delete Spreadsheet Blank Worksheets avec les SDK ?

### Spécification de l’API Delete Spreadsheet Blank Worksheets

La [Spécification de l’API Delete Spreadsheet Blank Worksheets](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Transform/RemoveSpreadsheetBlankWorksheets) définit une interface de programmation publiquement accessible, vous permettant d’effectuer des interactions REST directement depuis un navigateur web.

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK constitue la méthode la plus rapide pour développer, car elle masque les détails de bas niveau, vous permettant de supprimer les feuilles de calcul vierges à l’aide de peu de code. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteSpreadsheetBlankWorksheets.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteSpreadsheetBlankWorksheets.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteSpreadsheetBlankWorksheets.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteSpreadsheetBlankWorksheets.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteSpreadsheetBlankWorksheets.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteSpreadsheetBlankWorksheets.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteSpreadsheetBlankWorksheets.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteSpreadsheetBlankWorksheets.go" >}}
{{</tab>}}
{{< /tabs >}}