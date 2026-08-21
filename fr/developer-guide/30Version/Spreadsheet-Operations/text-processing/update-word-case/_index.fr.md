---
title: "Aspose.Cells – API de mise à jour de la casse des mots"
second_title: "Document"
linktitle: "Casse des mots"
type: docs
url: /fr/post-update-word-case/
keywords: "Aspose.Cells, API de mise à jour de la casse des mots, conversion de la casse du texte, Excel, CSV, Google Sheets, API REST"
description: "Convertissez la casse du texte dans des fichiers Excel, CSV ou Google Sheets à l’aide de l’API de mise à jour de la casse des mots d’Aspose.Cells Cloud. Prend en charge les cas majuscule/minuscule, la casse de titre et la majuscule initiale."
weight: 100
ArticleTitle: "Aspose.Cells – Documentation de l’API de mise à jour de la casse des mots"
---

**Version de l’API :** 3.0

Gérer l’incohérence de la casse du texte dans les feuilles de calcul (Excel, Google Sheets, CSV) peut être fastidieux, surtout avec de grands jeux de données. L’**API web PostUpdateWordCase** automatise les conversions de casse du texte, garantissant des données propres et normalisées avec un effort minimal.


## **API web Excel – API de mise à jour de la casse des mots**

```http
POST https://api.aspose.cloud/v3.0/cells/updatewordcase
```
### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Description de la fonction**

L’API web PostUpdateWordCase résout le problème courant de l’incohérence de la casse du texte dans les feuilles de calcul, ce qui peut avoir un impact significatif sur l’analyse et le traitement des données. Cette API automatise la conversion de la casse, garantissant que vos données sont propres, normalisées et prêtes à être manipulées ou analysées davantage.

- **Conversion automatique de la casse du texte**
  - **Majuscules en minuscules** – Convertir toutes les lettres majuscules en minuscules.
  - **Minuscules en majuscules** – Convertir toutes les lettres minuscules en majuscules.
  - **Mettre la première lettre en majuscule** – Mettre en majuscule la première lettre de chaque mot.
  - **Casse de titre** – Convertir le texte en casse de titre, où la première lettre de chaque mot majeur est mise en majuscule.

- **Prise en charge de plusieurs formats** – L’API fonctionne avec une large gamme de formats de feuilles de calcul, notamment Excel, OpenOffice, JSON, CSV et d’autres. Cette polyvalence la rend adaptée à divers besoins de traitement des données.

### **Paramètres de la requête**

| Nom du paramètre  | Type   | Emplacement   | Description                                                                                                               |
| ----------------- | ------ | ------------- | ------------------------------------------------------------------------------------------------------------------------- |
| `wordCaseOptions` | objet  | Corps de la requête | Options définissant la transformation de casse souhaitée, telles que la plage source, le type de casse cible et les paramètres supplémentaires. |

**Schéma de `wordCaseOptions`**

```json
{
  "Range": "A1:B10", // Plage au format Excel à traiter (obligatoire)
  "CaseType": "Upper", // Énumération : Upper, Lower, Capitalize, Title (obligatoire)
  "IgnoreBlank": true // Booléen, facultatif – si vrai, les cellules vides restent inchangées
}
```

**Exemple de corps de requête**

```json
{
  "Range": "A1:B10",
  "CaseType": "Upper",
  "IgnoreBlank": true
}
```

- **Range** – La plage de cellules à laquelle la conversion de casse sera appliquée (par exemple, `A1:C5`).
- **CaseType** – Le type de conversion de casse. Les valeurs autorisées sont `Upper`, `Lower`, `Capitalize` et `Title`.
- **IgnoreBlank** – Si `true`, les cellules vides sont ignorées ; la valeur par défaut est `false`.

### **Réponse**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[nom de fichier fusionné]",
    "Filesize" : [taille du fichier],
    "FileContent" : "[ChaîneBase64]"
}
```

- **Filename** – Nom du fichier traité.
- **FileSize** – Taille du fichier en octets.
- **FileContent** – Contenu du fichier transformé, codé en base64.

**Codes d’état HTTP**

| Code | Signification               | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT non valide ou manquant. |
| 413  | Charge utile trop grande     | Le fichier téléchargé dépasse la limite de taille. |
| 500  | Erreur interne du serveur    | Erreur inattendue du serveur. |
## Comment utiliser l’API PostUpdateWordCase avec les SDK

### Spécification de l’API PostUpdateWordCase

La <a href="https://reference.aspose.cloud/cells/#/TextProcessingController/PostUpdateWordCase" target="_blank" rel="noopener noreferrer">Spécification OpenAPI</a> définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est le meilleur moyen d’accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostUpdateWordCase.cs" >}}
{{</ tab>}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_PostUpdateWordCase.java" >}}
{{</ tab>}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_PostUpdateWordCase.php" >}}
{{</ tab>}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_PostUpdateWordCase.rb" >}}
{{</ tab>}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_PostUpdateWordCase.ts" >}}
{{</ tab>}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_PostUpdateWordCase.py" >}}
{{</ tab>}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_PostUpdateWordCase.pl" >}}
{{</ tab>}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_PostUpdateWordCase.go" >}}
{{</ tab>}}
{{</ tabs >}}
---