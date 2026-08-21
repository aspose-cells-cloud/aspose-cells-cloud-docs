---
title: "Aspose.Cells Cloud Web API – Traduire un fichier texte avec conversion linguistique alimentée par l’IA"
second_title: "Document"
ArticleTitle: "Comment traduire des fichiers texte à l’aide de l’API de traduction IA d’Aspose.Cells Cloud"
linktitle: "Traduire un fichier texte"
type: docs
url: /translate-text-file/
keywords: "Aspose.Cells, API Cloud, traduction IA, traduire un fichier texte, conversion multilingue, REST PUT, code de langue cible, traduction par téléchargement de fichier, traduction de texte brut, feuille de calcul IA"
description: "Découvrez comment utiliser le point de terminaison Aspose.Cells Cloud AI TranslateTextFile pour convertir des fichiers texte dans n’importe quelle langue prise en charge. Prend en charge à la fois le téléchargement de fichier en multipart et le payload de texte brut, préserve le formatage, et renvoie un fichier traduisible en téléchargement."
weight: 100
---

Le point de terminaison **TranslateTextFile** exploite les services d’IA d’Aspose.Cells Cloud pour traduire le contenu d’un fichier texte dans une langue cible spécifiée. Il prend en charge deux modes d’opération : (1) **Mode de téléchargement de fichier** – envoyer un fichier texte via multipart/form-data et recevoir un fichier traduit ; (2) **Mode de contenu direct** – envoyer du texte brut dans le corps de la requête et obtenir directement le texte traduit. Le service préserve les sauts de ligne et le formatage d’origine, ajoute automatiquement le suffixe "\_translated" au nom de fichier, et renvoie le résultat sous forme de flux téléchargeable. Idéal pour la traduction en lot de documents, l’intégration dans des flux de travail multilingues ou la traduction en temps réel de contenus générés par les utilisateurs.

## **API de traduction de fichier texte**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/ai/translate/text-file
```

### **Paramètres de la requête :**

| Nom du paramètre | Type   | Emplacement | Obligatoire/Optionnel | Description                                                                                                                                                                                                 |
| :--------------- | :----- | :---------- | :------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | Fichier | Obligatoire | FormData             | Le fichier texte source à traduire. Doit s’agir d’un fichier texte brut (.txt) ou d’un format de feuille de calcul pris en charge. Exemple : télécharger `document.txt` via le champ "file" de multipart/form-data. |
| targetLanguage   | Chaîne  | Obligatoire | Query                | Code de langue ISO‑639‑1 de la langue cible souhaitée (par exemple, "es" pour l’espagnol, "fr" pour le français, "de" pour l’allemand). Le code est insensible à la casse.                                     |
| region           | Chaîne  | Optionnel   | Query                | Identifiant de région de la feuille de calcul qui influence le formatage spécifique à la localisation (dates, nombres, devise). Valeurs courantes : "US", "EU", "CN". Si omis, le paramètre de région original du classeur est utilisé. |
| password         | Chaîne  | Optionnel   | Query                | Mot de passe requis pour ouvrir les fichiers de feuille de calcul chiffrés. Inutile pour les fichiers texte brut.                                                                                           |

### **Réponse**

Réponse réussie (200 OK)
En‑têtes :
Content-Type: application/octet-stream // flux binaire du fichier traduit
Content-Disposition: attachment; filename="<nom_original>\_translated.txt"
Content-Length: <taille en octets>

Corps : flux binaire contenant le texte traduit, préservant les sauts de ligne et le formatage d’origine.

**Codes d’état HTTP**

| Code | Signification        | Description                                                      |
| ---- | -------------------- | ---------------------------------------------------------------- |
| 200  | OK                   | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Demande incorrecte   | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé         | Jeton JWT non valide ou manquant.                                |
| 413  | Payload trop volumineux | Fichier téléchargé dépassant la taille limite.                  |
| 500  | Erreur interne du serveur | Erreur serveur inattendue.                                       |

## Où utiliser l’API de traduction de fichier texte ?

- **Portails de documentation multilingues** – Traduire automatiquement les manuels utilisateurs ou les fichiers d’aide téléchargés en tant que documents texte, afin de fournir des versions localisées à la demande.
- **Systèmes de gestion de contenu (CMS)** – Intégrer dans un flux de travail CMS pour traduire des articles ou des blogs avant leur publication auprès d’un public international.
- **Pipelines de données d’entreprise** – Utiliser dans des tâches par lot qui traitent de grands volumes de rapports CSV ou TXT, en les convertissant dans la langue des bureaux régionaux tout en préservant le formatage original.
- **Plateformes d’assistance client** – Traduire en temps réel les tickets ou journaux de discussion reçus en texte brut pour aider les agents d’assistance travaillant dans des langues différentes.

## Pourquoi utiliser l’API de traduction de fichier texte ?

- **Précision alimentée par l’IA** – Exploite des modèles de traduction neuronale de pointe pour un résultat naturel et contextuellement pertinent.
- **Flexibilité de saisie double** – Accepte à la fois les fichiers uploadés et les payloads de texte brut, simplifiant l’intégration avec des applications clientes variées.
- **Préservation de la mise en page d’origine** – Maintient les sauts de ligne, l’indentation et les caractères spéciaux, éliminant les opérations de nettoyage post‑traitement.
- **Gestion fluide des fichiers** – Renvoie un fichier prêt au téléchargier avec un suffixe "\_translated" généré automatiquement, réduisant la complexité du code côté client.

## Comment utiliser l’API de traduction de fichier texte avec les SDK ?

### Spécification de l’API de traduction de fichier texte

La [spécification de l’API de traduction de fichier texte](https://reference.aspose.cloud/cells/#/AIController/TranslateTextFile) fournit une interface de programmation accessible publiquement pour exécuter directement des interactions REST depuis un navigateur web.

## SDK pour l’API Excel

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour développer, car elle masque les détails de bas niveau et permet de fusionner une feuille de calcul dans une autre à l’aide d’un code minimal.
Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Aspose.Cells Cloud.
Les exemples de code suivants montrent comment interagir avec les services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v4.0_TranslateTextFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v4.0_TranslateTextFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v4.0_TranslateTextFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v4.0_TranslateTextFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v4.0_TranslateTextFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v4.0_TranslateTextFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v4.0_TranslateTextFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v4.0_TranslateTextFile.go" >}}
{{</tab>}}
{{< /tabs >}}