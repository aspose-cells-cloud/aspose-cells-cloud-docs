---
title: "Aspose.Cells Cloud – Modifier la casse des mots (Majuscule, minuscule, césure, phrase)"
ArticleTitle: "Convertisseur de casse Excel – Majuscule, minuscule, césure et casse phrase"
linktype: "Casse des mots"
type: docs
url: /change-word-case/
keywords: "API de modification de la casse des mots, Aspose.Cells, conversion de casse Excel, majuscule, minuscule, césure, casse phrase, mise en forme du texte"
description: "Convertissez facilement la casse des mots dans des fichiers Excel à l'aide de l'API Aspose.Cells Cloud. Prend en charge Majuscule, Minuscule, Césure et Casse phrase. Obtenez des exemples de code en C#, Java, Python et plus encore."
weight: 100
---

## **Modifier la casse des mots**

Utilisez l’API Web Aspose.Cells Cloud pour convertir instantanément la casse des mots dans votre feuille de calcul — passez entre majuscule, minuscule, césure (mettre en majuscule la première lettre de chaque mot) ou casse phrase (mettre en majuscule la première lettre de chaque phrase) sur une plage sélectionnée. Seules les cellules contenant des chaînes de caractères sont affectées ; les nombres, les booléens, les erreurs et les cellules vides sont ignorés. Les formules, la mise en forme et la validation des données restent inchangées.

- **UpperCase** – chaque caractère est mis en majuscule.
- **LowerCase** – chaque caractère est mis en minuscule.
- **ProperCase** – la première lettre de chaque mot est mise en majuscule, les autres en minuscule.
- **SentenceCase** – la première lettre de chaque phrase est mise en majuscule, les autres en minuscule.

<img src="images/result.png" alt="Capture d'écran avant/après conversion de casse" width="800" height="450" />

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/content/wordcase
```


### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```
### Paramètres de requête pour l’API **UpdateWordCase**

| Nom du paramètre | Type   | Emplacement | Description                                                                                                                                                           |
| :--------------- | :----- | :---------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| spreadsheet      | Fichier | FormData    | Le fichier de feuille de calcul à traiter. Les formats pris en charge incluent XLSX, XLS, ODS, CSV, etc.                                                             |
| wordCaseType     | Chaîne  | Query       | Spécifie le type de conversion de casse : `UpperCase`, `LowerCase`, `ProperCase` ou `SentenceCase`.                                                                   |
| worksheet        | Chaîne  | Query       | _(Facultatif)_ Le nom de la feuille de calcul sur laquelle la conversion de casse sera appliquée. Si omis, l’opération s’applique à la première feuille du classeur.               |
| range            | Chaîne  | Query       | _(Facultatif)_ La plage de cellules sur laquelle la conversion de casse sera appliquée (par exemple, `"A1:C10"`). Si omis, l’opération s’applique à toutes les cellules utilisées de la feuille spécifiée. |
| outPath          | Chaîne  | Query       | _(Facultatif)_ Le chemin du dossier dans le stockage cloud où le classeur traité sera enregistré. Si omis, le fichier est enregistré dans le dossier source.                            |
| outStorageName   | Chaîne  | Query       | Le nom du stockage cloud dans lequel le fichier de sortie sera enregistré.                                                                                                   |
| region           | Chaîne  | Query       | _(Facultatif)_ Définit la locale pour les règles de conversion de casse, particulièrement pertinent pour les règles d’orthographe spécifique à la langue (par exemple, `"en-US"`, `"tr-TR"`).                 |
| password         | Chaîne  | Query       | _(Facultatif)_ Si la feuille de calcul envoyée est protégée par mot de passe, fournissez le mot de passe pour ouvrir et traiter le fichier.                                                    |

### Réponse

En cas de succès, le service renvoie **200 OK** (ou **202 Accepted**) avec une charge utile JSON contenant le flux binaire du classeur traité.

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

- **400 Bad Request** – URI de l’API Aspose.Cells Cloud invalide.
- **401 Unauthorized** – Jeton d’accès invalide ou identifiants client incorrects.
- **404 Not Found** – Le fichier de feuille de calcul n’est pas accessible.
- **500 Server Error** – Une erreur interne s’est produite lors du traitement de la feuille de calcul.

## Où utiliser l’API de modification de la casse des mots ?

### Nettoyage et standardisation des données

- **Gestion des données clients** – Standardiser la capitalisation des noms et adresses clients (par exemple, `jean dupont` → `Jean Dupont`).
- **Traitement du catalogue de produits** – Standardiser les titres et descriptions des produits (par exemple, `IPHONE 15 PRO` → `iPhone 15 Pro`).
- **Génération de rapports financiers** – Normaliser les intitulés et descriptions dans les états financiers.

### Intégration de données multi-sources

- **ETL entrepôt de données** – Standardiser le format du texte lors du chargement des données provenant de divers systèmes.
- **Réception de données via API** – Gérer les données retournées par des API externes avec une capitalisation incohérente.
- **Fusion de données inter-services** – Standardiser le format du texte dans les rapports Excel provenant de services différents.

### Système de gestion de contenu

- **Diffusion automatique d’actualités** – Formater automatiquement les titres et contenus d’actualités (règles de capitalisation pour les titres).
- **Génération de documentation produit** – Assurer la cohérence dans la mise en forme des termes techniques.
- **Maintenance de la base de connaissances** – Standardiser le format du texte dans les FAQ et documents d’aide.

### Intégration d’applications d’entreprise

- **Intégration CRM** – Formater automatiquement les noms et informations d’entreprise lors de l’import/export des données clients.
- **Traitement de données ERP** – Standardiser les champs clés tels que les descriptions de matériaux et les noms de fournisseurs.
- **Système de gestion des ressources humaines** – Standardiser les informations employés et intitulés de postes.

### Traitement par lots de documents

- **Préparation de documents juridiques** – Traitement par lots des formats de clauses dans les contrats et accords.
- **Génération de supports marketing** – Standardiser les formats de texte dans les brouillons publicitaires et les modèles d’emails.
- **Mise en forme d’articles académiques** – Standardiser les exigences de format pour les références et titres.

### Traitement en temps réel

- **Validation des entrées utilisateur** – Mise en forme en temps réel des données de formulaires soumises par les utilisateurs.
- **Réponses de chatbot** – Standardisation du format du texte pour les réponses générées automatiquement.
- **Génération instantanée de rapports** – Création dynamique de rapports commerciaux uniformément mis en forme.

### Internationalisation et localisation

- **Traitement multilingue** – Gérer les différences dans les règles de capitalisation pour les textes dans diverses langues.
- **Préparation de contenus localisés** – Préparer du contenu localisé formaté pour différentes régions.
- **Gestion de projets de traduction** – Assurer la cohérence du format du texte avant et après traduction.

## Pourquoi utiliser l’API de modification de la casse des mots ?

- **Adapté aux développeurs** – Aspose.Cells Cloud propose des bibliothèques SDK dans plusieurs langages, permettant un développement rapide et accompagné d’une documentation complète. Comparé à la création de solutions personnalisées, cela réduit considérablement la charge de développement.
- **Économique** – Vous pouvez modifier la casse des mots sans avoir à télécharger préalablement le classeur, ce qui économise de l’espace de stockage et réduit les coûts.

## Spécification OpenAPI

La [Spécification OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/UpdateWordCase) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation du SDK est le meilleur moyen d’accélérer le développement. Le SDK gère les détails sous-jacents, vous permettant d’implémenter simplement **UpdateWordCase** pour les cellules avec un minimum de code. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour une liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UpdateWordCase.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UpdateWordCase.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UpdateWordCase.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UpdateWordCase.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UpdateWordCase.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UpdateWordCase.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UpdateWordCase.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UpdateWordCase.go" >}}
{{</tab>}}
{{< /tabs >}}
---