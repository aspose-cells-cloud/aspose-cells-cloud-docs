---
title: "Convertir le texte dans une feuille de calcul distante"
ArticleTitle: "Convertir le texte dans une feuille de calcul distante – Aspose.Cells Cloud"
second_title: "Document"
linktype: "docs"
url: /fr/cells/{name}/worksheets/{worksheet}/range/{range}/content/convert/text
aliases: []
keywords: "Aspose.Cells, Conversion de texte, API"
description: "Convertit le texte dans une plage spécifiée d'une feuille de calcul, incluant la conversion de nombres, le remplacement de caractères, la gestion des sauts de ligne et la normalisation des caractères accentués."
weight: 1000
---

## La conversion de texte dans une feuille de calcul distante des services web Aspose.Cells Cloud

Indique la conversion des nombres stockés comme texte dans le format numérique correct, le remplacement des caractères et sauts de ligne indésirables par les caractères souhaités, ainsi que la conversion des caractères accentués en leurs équivalents non accentués.

### Point de terminaison de l’API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/convert/text
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type   | Chemin/Chaîne de requête/Corps HTTP | Description |
|------------------|--------|-------------------------------------|-------------|
| name             | string | Chemin | (Requis) Le nom du fichier du classeur à récupérer. |
| worksheet        | string | Chemin | Spécifie la feuille de calcul de la feuille de calcul. |
| range            | string | Chemin | Spécifie la plage de la feuille de calcul. |
| convertTextType  | string | Requête | Indique le type de conversion de texte. (Requis) |
| sourceCharacters | string | Requête | Indique les caractères sources. (Optionnel) |
| targetCharacters | string | Requête | Indique les caractères cibles. (Optionnel) |
| folder           | string | Requête | (Optionnel) Le chemin du dossier où le classeur est stocké. La valeur par défaut est null. |
| storageName      | string | Requête | (Optionnel) Le nom du stockage si vous utilisez un stockage cloud personnalisé. Utilise le stockage par défaut s’il est omis. |
| region           | string | Requête | Paramètre régional/langue de la feuille de calcul (par exemple, `en-US`, `fr-FR`). Influence le formatage des nombres, l’analyse des dates et le comportement spécifique à la locale. (Optionnel) |
| password         | string | Requête | Le mot de passe pour ouvrir le fichier de la feuille de calcul. (Optionnel) |

### Paramètre du corps de la requête

| Nom du paramètre | Type | Description |
| ---------------- | ---- | ----------- |
| - | - | - |

### **Réponse**

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "Conversion de texte terminée avec succès.",
  "Data": {
    // Détails du résultat de la conversion, comme le nombre de cellules mises à jour, peuvent être ajoutés ici.
  }
}
```

**Codes d’état de la réponse**

| Code | Signification | Description |
|------|---------------|-------------|
| 200 | OK | L’opération de conversion de texte s’est déroulée avec succès. |
| 400 | Requête incorrecte | La requête était mal formée ou les paramètres obligatoires étaient manquants. |
| 401 | Non autorisé | L’authentification a échoué ou le jeton JWT est manquant/ invalide. |
| 413 | Payload trop volumineux | La charge utile de la requête dépasse la limite de taille autorisée. |
| 500 | Erreur interne du serveur | Une erreur inattendue s’est produite sur le serveur. |

## Comment utiliser la conversion de texte dans une feuille de calcul distante avec les SDK

### Spécification de la conversion de texte dans une feuille de calcul distante

La [spécification de l’API Conversion de texte dans une feuille de calcul distante](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{TextProcessingController}/{ConvertTextInRemoteSpreadsheet}) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose Cells Cloud. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}

{< tab tabNum="1" >}

```bash
# Utiliser HTTPS pour une connexion sécurisée
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/convert/text?convertTextType={convertTextType}&sourceCharacters={sourceCharacters}&targetCharacters={targetCharacters}&folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "Conversion de texte terminée avec succès.",
  "Data": {
    "UpdatedCellsCount": 124,
    "Details": "Nombres convertis, caractères remplacés, sauts de ligne normalisés."
  }
}
```

{< /tab >}

{< /tabs >}

### Utiliser les SDK Aspose Cells Cloud

L’utilisation d’un SDK est le moyen le plus rapide d’accélérer le développement. Un SDK masque les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour une liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose Cells Cloud à l’aide de divers SDK :
 `[À compléter]`
---