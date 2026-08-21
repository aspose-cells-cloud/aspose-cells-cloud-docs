---
title: "ConvertWorksheetToPdf"
ArticleTitle: "Convertir une feuille de calcul en PDF – API Aspose.Cells Cloud"
second_title: "Document"
linktitle: "ConvertWorksheetToPdf"
type: docs
url: /fr/cells/convert/worksheet/pdf
aliases: []
keywords: "Aspose.Cells, Convertir une feuille de calcul en PDF, API"
description: "Convertit une feuille de calcul d’un fichier de feuille de calcul en PDF à l’aide d’Aspose.Cells Cloud."
weight: 10
---

## La méthode ConvertWorksheetToPdf des services web Aspose.Cells Cloud

Cette méthode lit un fichier de feuille de calcul à partir du système de fichiers local, convertit sa feuille de calcul en fichier PDF, puis renvoie le résultat converti. Le chemin d’accès au fichier source et le format cible doivent être spécifiés correctement. Assurez-vous que les autorisations nécessaires sont en place pour lire le fichier source et écrire le fichier converti le cas échéant. Le processus de conversion s’effectue entièrement sur le serveur cloud, éliminant ainsi le besoin de stockage cloud ou de téléchargements externes.

Les fonctionnalités clés incluent la conversion native cloud, une réduction de la charge sur les ressources cloud et un flux de travail simplifié.

### Point de terminaison de l’API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la demande

| Nom du paramètre | Type    | Emplacement (chemin / chaîne de requête / corps HTTP) | Description                                                                                                                                                     |
|------------------|---------|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | File    | FormData                                               | Télécharger le fichier de feuille de calcul.                                                                                                                    |
| worksheet        | String  | Query                                                  | Nom de la feuille de calcul dans le classeur.                                                                                                                   |
| outPath          | String  | Query                                                  | (Facultatif) Chemin du dossier où le classeur est stocké. La valeur par défaut est null.                                                                       |
| outStorageName   | String  | Query                                                  | Nom du stockage pour le fichier de sortie.                                                                                                                      |
| fontsLocation    | String  | Query                                                  | Utiliser des polices personnalisées.                                                                                                                            |
| AutoRowsFit      | Boolean | Query                                                  | (Facultatif) Ajustement automatique de toutes les lignes dans les feuilles de calcul.                                                                          |
| AutoColumnsFit   | Boolean | Query                                                  | (Facultatif) Ajustement automatique de toutes les colonnes dans les feuilles de calcul.                                                                        |
| region           | String  | Query                                                  | Paramètres régionaux/langue du fichier de feuille de calcul (par exemple, `en-US`, `fr-FR`). Affecte le formatage des nombres, l’analyse des dates et le comportement spécifique à la locale. |
| password         | String  | Query                                                  | Mot de passe pour ouvrir le fichier de feuille de calcul.                                                                                                       |

### Paramètre du corps de la demande

| Nom du paramètre | Type | Description |
| ---------------- | ---- | ----------- |
| [À déterminer]   |      |             |

### **Réponse**

```json
{
  "file": "<flux binaire du PDF généré>"
}
```

**Codes d’état de la réponse**

| Code | Signification | Description |
|------|---------------|-------------|
| 200 | OK | La feuille de calcul a été convertie avec succès en PDF et renvoyée sous forme de flux de fichier. |
| 400 | Mauvaise demande | Paramètres de demande invalides ou URL mal formée. |
| 401 | Non autorisé | L’authentification a échoué, ou aucune information d’identification n’a été fournie. |
| 404 | Non trouvé | Le fichier source n’est pas accessible. |
| 413 | Charge utile trop volumineuse | Le fichier téléchargé dépasse la limite de taille autorisée. |
| 500 | Erreur interne du serveur | Une anomalie s’est produite lors de la conversion du fichier de feuille de calcul. |

## Comment utiliser ConvertWorksheetToPdf avec les SDK

### Spécification ConvertWorksheetToPdf

La [spécification de l’API ConvertWorksheetToPdf](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#Conversion/ConvertWorksheetToPdf) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API cloud avec cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Demande" tabName2="Réponse" >}

{< tab tabNum="1" >}

```bash
# Utiliser HTTPS pour une connexion sécurisée
curl -v "https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf?worksheet=Feuil1&outPath=output%2Fdossier&outStorageName=MyStorage&fontsLocation=%2Fpolices%2Fpersonnalisees&AutoRowsFit=true&AutoColumnsFit=true&region=fr-FR&password=MotDePasseSecret" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jeton jwt>" \
  -F "Spreadsheet=@exemple.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<flux binaire du PDF généré>"
}
```

{< /tab >}

{< /tabs >}

### Utiliser les SDK Aspose Cells Cloud

L’utilisation d’un SDK est le moyen le plus rapide d’accélérer le développement. Un SDK abstrait les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose Cells Cloud à l’aide de divers SDK :
`[À déterminer]`
---