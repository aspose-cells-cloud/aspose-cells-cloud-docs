---
title: "Supprimer les sous-chaînes dupliquées dans une feuille de calcul distante"
ArticleTitle: "Supprimer les sous-chaînes dupliquées dans une feuille de calcul distante – API Aspose.Cells Cloud"
second_title: "Document"
linktype: "docs"
url: /cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/duplicate-substrings
aliases: []
keywords: "Aspose.Cells, supprimer les sous-chaînes dupliquées, API"
description: "API permettant de rechercher et supprimer les sous-chaînes répétées dans les cellules d’une plage spécifiée d’un classeur."
weight: 1
---

## Supprimer les sous-chaînes dupliquées dans une feuille de calcul distante via les services web Aspose.Cells Cloud

Recherche et supprime les sous-chaînes répétées dans chaque cellule de la plage sélectionnée, à l’aide de délimiteurs définis par l’utilisateur ou prédéfinis, tout en préservant les formules, le formatage et la validation des données.

**Mode de détection des doublons**  
1. La valeur de chaque cellule est découpée en sous-chaînes à l’aide des délimiteurs choisis.  
2. L’outil compare les sous-chaînes **à l’intérieur de la même cellule** et conserve uniquement la **première occurrence** de chaque sous-chaîne dupliquée.  
3. Les sous-chaînes nettoyées sont réassemblées à l’aide des mêmes délimiteurs, puis réécrites dans la cellule.  

**Options de délimiteurs**  
- Liste prédéfinie : virgule, point-virgule, espace, tabulation, saut de ligne  
- `Custom` (personnalisé) – saisir tout caractère (ou ensemble de caractères) ; plusieurs caractères sont traités comme un seul délimiteur composite  
- `TreatConsecutiveDelimitersAsOne` (traiter les délimiteurs consécutifs comme un seul) – regrouper les délimiteurs adjacents en un seul séparateur  

Seules les cellules contenant des chaînes de caractères sont traitées ; les nombres, les booléens et les formules sont convertis en chaînes avant le découpage (les formules sont supprimées). Renvoie le nombre de cellules nettoyées ainsi que le flux du classeur mis à jour.

### Point de terminaison de l’API web

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/duplicate-substrings
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement (chemin / chaîne de requête / corps HTTP) | Description |
|------------------|---------|--------------------------------------------------------|-------------|
| name | string | Chemin | (Obligatoire) Nom du fichier de classeur à traiter. |
| worksheet | string | Chemin | Feuille de calcul spécifiée dans la feuille de calcul. |
| range | string | Chemin | Plage spécifiée dans la feuille de calcul. |
| delimiters | string | Chaîne de requête | Délimiteurs utilisés pour découper les valeurs des cellules (par ex. virgule, point-virgule, espace, tabulation, saut de ligne). Obligatoire. |
| treatConsecutiveDelimitersAsOne | boolean | Chaîne de requête | Regrouper les délimiteurs adjacents en un seul séparateur. Valeur par défaut : true. Facultatif. |
| caseSensitive | boolean | Chaîne de requête | Effectuer une comparaison sensible à la casse lors de la détection des doublons. Facultatif. |
| folder | string | Chaîne de requête | (Facultatif) Chemin du dossier où le classeur est stocké. Valeur par défaut : null. |
| storageName | string | Chaîne de requête | (Facultatif) Nom du stockage utilisé, si un stockage cloud personnalisé est employé. |
| region | string | Chaîne de requête | Paramètre régional/langue de la feuille de calcul (par ex. `en-US`, `fr-FR`). Facultatif. |
| password | string | Chaîne de requête | Mot de passe permettant d’ouvrir le fichier de feuille de calcul. Facultatif. |

### Paramètre du corps de la requête

| Nom du paramètre | Type | Description |
| ---------------- | ---- | ----------- |
| - | - | Aucun corps de requête n’est requis pour cette opération. |

### **Réponse**

```json
{
  "code": 200,
  "status": "OK",
  "cellsCount": 123,
  "file": "flux de classeur encodé en base64"
}
```

**Codes de statut de la réponse**

| Code | Signification | Description |
|------|---------------|-------------|
| 200 | OK | Opération réussie ; renvoie le nombre de cellules nettoyées et le flux du classeur mis à jour. |
| 400 | Mauvaise requête | Un ou plusieurs paramètres de requête sont manquants ou invalides. |
| 401 | Non autorisé | Échec de l’authentification ou jeton JWT manquant/ invalide. |
| 413 | Payload trop volumineux | La taille de la requête dépasse les limites autorisées. |
| 500 | Erreur interne du serveur | Une erreur inattendue s’est produite sur le serveur. |

## Comment utiliser la fonctionnalité de suppression des sous-chaînes dupliquées dans une feuille de calcul distante à l’aide des SDK

### Spécification de la fonctionnalité de suppression des sous-chaînes dupliquées dans une feuille de calcul distante

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveDuplicateSubstringsInRemoteSpreadsheet" rel="noopener noreferrer">spécification de l’API de suppression des sous-chaînes dupliquées dans une feuille de calcul distante</a> définit une interface de programmation accessible publiquement, vous permettant d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple ci-dessous montre comment effectuer des appels à l’API Cloud à l’aide de cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}
{< tab tabNum="1" >}
```bash
# Utiliser HTTPS pour une connexion sécurisée
curl -v "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/range/A1:C10/content/remove/duplicate-substrings?delimiters=comma%2Csemicolon&treatConsecutiveDelimitersAsOne=true&caseSensitive=false" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "code": 200,
  "status": "OK",
  "cellsCount": 123,
  "file": "flux de classeur encodé en base64"
}
```
{< /tab >}
{< /tabs >}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour accélérer le développement. Un SDK masque les détails de bas niveau, vous permettant ainsi de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells Cloud à l’aide de divers SDK :
`[À compléter]`
---