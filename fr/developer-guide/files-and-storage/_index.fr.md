---
title: "API Cloud Aspose.Cells – Gestion des fichiers et dossiers (Téléversement, Téléchargement, Copie, Déplacement)"
second_title: "Document"
ArticleTitle: "Gestion cloud des fichiers pour Excel – Une solution efficace et sécurisée pour le stockage et l’organisation intelligente des fichiers Excel"
linktitle: "Fichiers et stockage"
type: docs
url: /files-and-storage/
aliases: [/working-with-files-and-storage-using-aspose-cells-cloud/]
keywords: "Aspose.Cells Cloud, API de stockage de fichiers, téléverser un fichier Excel, télécharger un fichier Excel, copier un fichier, déplacer un fichier, supprimer un fichier, gestion des dossiers, API REST, exemples cURL"
description: "Guide complet pour gérer les fichiers Excel et les dossiers dans le stockage Aspose.Cells Cloud. Inclut les opérations de téléversement, téléchargement, copie, déplacement, suppression et gestion des dossiers, avec exemples cURL, paramètres requis et notes d’authentification."
weight: 100
---

Aspose.Cells Cloud fournit un ensemble complet de fonctions utilitaires pour manipuler les fichiers stockés dans le stockage Aspose.Cells Cloud ou dans n’importe quel service de stockage tiers de votre choix. Pour obtenir de l’aide concernant la configuration d’un stockage tiers, veuillez consulter les [Sujets d’aide de l’interface utilisateur Aspose Cloud](https://docs.aspose.cloud/display/totalcloud/Aspose+Cloud+UI+Help+Topics).

**Aspose.Cells Cloud propose une variété d’API pour gérer les fichiers, les dossiers et le stockage.**

> **Remarque :** Tous les appels d’API doivent utiliser **HTTPS**. Consultez le [Guide d’authentification](/cells/authentication/) pour obtenir des détails sur l’obtention d’un jeton JWT.

**Prérequis :** Pour utiliser ces API, vous devez disposer d’un compte Aspose Cloud valide, obtenir un jeton d’accès JWT et avoir configuré un emplacement de stockage (soit le stockage Aspose Cloud, soit un stockage tiers connecté).

**Dernière mise à jour :** 2024-12-01

## **Comment téléverser un fichier**

### Informations sur l’API de téléversement de fichier

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

Les paramètres de la requête sont les suivants :

| Nom du paramètre | Type   | Emplacement | Description |
|------------------|--------|-------------|-------------|
| path             | string | path        | Chemin d’accès du fichier à téléverser, incluant le nom de fichier et l’extension (par exemple `/dossier1/Report.xlsx`). |
| file             | file   | formData    | Le fichier à téléverser. |
| storageName      | string | query       | Nom du stockage à utiliser. |

**Réponses HTTP**

| Code | Description                                      |
|------|--------------------------------------------------|
| 200  | Fichier téléversé avec succès.                   |
| 400  | Requête incorrecte – paramètres manquants ou invalides. |
| 401  | Non autorisé – jeton JWT invalide ou manquant.  |
| 404  | Stockage introuvable.                            |
| 500  | Erreur interne du serveur.                       |

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/File/UploadFile) définit une interface de programmation publiquement accessible, permettant des interactions REST directement depuis un navigateur web.

### Exemple de téléversement de fichier

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment téléverser un fichier à l’aide de cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}
{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/MyFolder/Report.xlsx" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>" \
  -F "File=@Report.xlsx"
```

{{< /tab >}}
{{< tab tabNum="12" >}}

```json
{
  "Uploaded": [
    "MyFolder/Report.xlsx"
  ],
  "Errors": []
}
```

{{< /tab >}}
{{< /tabs >}}

*Remarque : La taille maximale autorisée pour le téléversement est de 100 Mo. Des limites de débit peuvent s’appliquer.*

## **Comment télécharger un fichier**

### Informations sur l’API de téléchargement de fichier

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

Les paramètres de la requête sont les suivants :

| Nom du paramètre | Type   | Emplacement | Description |
|------------------|--------|-------------|-------------|
| path             | string | path        | Chemin d’accès du fichier (par exemple `/dossier/Report.xlsx`). |
| storageName      | string | query       | Nom du stockage à utiliser. |
| versionId        | string | query       | Identifiant de la version du fichier à télécharger (facultatif). |

**Réponses HTTP**

| Code | Description                                      |
|------|--------------------------------------------------|
| 200  | Fichier téléchargé ; flux binaire renvoyé.      |
| 400  | Requête incorrecte – paramètres invalides.      |
| 401  | Non autorisé – jeton JWT manquant ou invalide.  |
| 404  | Fichier introuvable.                             |
| 500  | Erreur interne du serveur.                       |

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/File/DownloadFile) définit une interface de programmation publiquement accessible, permettant des interactions REST directement depuis un navigateur web.

### Exemple de téléchargement de fichier

{{< tabs tabTotal="2" tabID="13" tabName13="Requête" tabName14="Réponse" >}}
{{< tab tabNum="13" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/MyFolder/Report.xlsx" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}
{{< tab tabNum="14" >}}

```json
{
  "Stream": "<données binaires>"
}
```

{{< /tab >}}
{{< /tabs >}}

*Remarque : La réponse contient le flux binaire du fichier. Sauvegardez la sortie dans un fichier lors de l’utilisation de cURL (`-o nomfichier.xlsx`).*

## **Comment supprimer un fichier**

### Informations sur l’API de suppression de fichier

```bash
DELETE https://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

Les paramètres de la requête sont les suivants :

| Nom du paramètre | Type   | Emplacement | Description |
|------------------|--------|-------------|-------------|
| path             | string | path        | Chemin d’accès du fichier (par exemple `/dossier/Report.xlsx`). |
| storageName      | string | query       | Nom du stockage à utiliser. |
| versionId        | string | query       | Identifiant de la version du fichier à supprimer (facultatif). |

**Réponses HTTP**

| Code | Description                                      |
|------|--------------------------------------------------|
| 200  | Fichier supprimé avec succès.                    |
| 400  | Requête incorrecte – paramètres manquants ou invalides. |
| 401  | Non autorisé – jeton JWT invalide.               |
| 404  | Fichier introuvable.                             |
| 500  | Erreur interne du serveur.                       |

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/File/DeleteFile) définit une interface de programmation publiquement accessible, permettant des interactions REST directement depuis un navigateur web.

### Exemple de suppression de fichier

{{< tabs tabTotal="2" tabID="15" tabName15="Requête" tabName16="Réponse" >}}
{{< tab tabNum="15" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/MyFolder/OldReport.xlsx" \
  -X DELETE \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}
{{< tab tabNum="16" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*Remarque : La suppression d’un fichier est définitive ; assurez-vous d’avoir une sauvegarde si nécessaire.*

## **Comment copier un fichier**

### Informations sur l’API de copie de fichier

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/file/copy/{srcPath}
```

Les paramètres de la requête sont les suivants :

| Nom du paramètre | Type   | Emplacement | Description |
|------------------|--------|-------------|-------------|
| srcPath          | string | path        | Chemin d’accès du fichier source (par exemple `/dossier/Source.xlsx`). |
| destPath         | string | query       | Chemin d’accès du fichier de destination (par exemple `/dossier/Destination.xlsx`). |
| srcStorageName   | string | query       | Nom du stockage source (facultatif). |
| destStorageName  | string | query       | Nom du stockage de destination (facultatif). |
| versionId        | string | query       | Identifiant de version du fichier à copier (facultatif). |

**Réponses HTTP**

| Code | Description                                      |
|------|--------------------------------------------------|
| 200  | Fichier copié avec succès.                       |
| 400  | Requête incorrecte – paramètres invalides.      |
| 401  | Non autorisé – jeton JWT manquant ou invalide.  |
| 404  | Fichier source introuvable.                      |
| 500  | Erreur interne du serveur.                       |

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/File/CopyFile) définit une interface de programmation publiquement accessible, permettant des interactions REST directement depuis un navigateur web.

### Exemple de copie de fichier

{{< tabs tabTotal="2" tabID="17" tabName17="Requête" tabName18="Réponse" >}}
{{< tab tabNum="17" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/copy/MyFolder/Report.xlsx?destPath=MyFolder/ReportCopy.xlsx" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}
{{< tab tabNum="18" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*Remarque : L’opération de copie ne supprime pas le fichier source.*

## **Comment déplacer un fichier**

### Informations sur l’API de déplacement de fichier

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/file/move/{srcPath}
```

Les paramètres de la requête sont les suivants :

| Nom du paramètre | Type   | Emplacement | Description |
|------------------|--------|-------------|-------------|
| srcPath          | string | path        | Chemin d’accès du fichier source (par exemple `/dossier/Source.xlsx`). |
| destPath         | string | query       | Chemin d’accès du fichier de destination (par exemple `/dossier/Destination.xlsx`). |
| srcStorageName   | string | query       | Nom du stockage source (facultatif). |
| destStorageName  | string | query       | Nom du stockage de destination (facultatif). |
| versionId        | string | query       | Identifiant de version du fichier à déplacer (facultatif). |

**Réponses HTTP**

| Code | Description                                      |
|------|--------------------------------------------------|
| 200  | Fichier déplacé avec succès.                     |
| 400  | Requête incorrecte – paramètres invalides.      |
| 401  | Non autorisé – jeton JWT manquant ou invalide.  |
| 404  | Fichier source introuvable.                      |
| 500  | Erreur interne du serveur.                       |

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/File/MoveFile) définit une interface de programmation publiquement accessible, permettant des interactions REST directement depuis un navigateur web.

### Exemple de déplacement de fichier

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/move/MyFolder/Report.xlsx?destPath=MyFolder/ReportMoved.xlsx" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*Remarque : Le déplacement d’un fichier conserve l’historique des versions du fichier.*

## **Comment créer un dossier**

### Informations sur l’API de création de dossier

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

Les paramètres de la requête sont les suivants :

| Nom du paramètre | Type   | Emplacement | Description |
|------------------|--------|-------------|-------------|
| path             | string | path        | Chemin d’accès du dossier à créer (par exemple `dossier1/dossier2/`). |
| storageName      | string | query       | Nom du stockage à utiliser. |

**Réponses HTTP**

| Code | Description                                      |
|------|--------------------------------------------------|
| 200  | Dossier créé avec succès.                        |
| 400  | Requête incorrecte – chemin ou paramètres invalides. |
| 401  | Non autorisé – jeton JWT manquant ou invalide.  |
| 500  | Erreur interne du serveur.                       |

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/CreateFolder) définit une interface de programmation publiquement accessible, permettant des interactions REST directement depuis un navigateur web.

### Exemple de création de dossier

{{< tabs tabTotal="2" tabID="3" tabName3="Requête" tabName4="Réponse" >}}
{{< tab tabNum="3" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/newfolder" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}
{{< tab tabNum="4" >}}

```json
{
  "Uploaded": [
    "newfolder"
  ],
  "Errors": []
}
```

{{< /tab >}}
{{< /tabs >}}

*Remarque : Les chemins d’accès aux dossiers sont sensibles à la casse.*

## **Comment obtenir la liste des fichiers d’un dossier**

### Informations sur l’API d’obtention des fichiers

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

Les paramètres de la requête sont les suivants :

| Nom du paramètre | Type   | Emplacement | Description |
|------------------|--------|-------------|-------------|
| path             | string | path        | Chemin d’accès du dossier (par exemple `/dossier`). |
| storageName      | string | query       | Nom du stockage à utiliser. |

**Réponses HTTP**

| Code | Description                                      |
|------|--------------------------------------------------|
| 200  | Liste des fichiers et sous-dossiers renvoyée.   |
| 400  | Requête incorrecte – chemin invalide.           |
| 401  | Non autorisé – jeton JWT manquant ou invalide.  |
| 404  | Dossier introuvable.                             |
| 500  | Erreur interne du serveur.                       |

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/GetFilesList) définit une interface de programmation publiquement accessible, permettant des interactions REST directement depuis un navigateur web.

### Exemple d’obtention des fichiers

{{< tabs tabTotal="2" tabID="5" tabName5="Requête" tabName6="Réponse" >}}
{{< tab tabNum="5" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/desfolder" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}
{{< tab tabNum="6" >}}

```json
{
  "Value": [
    {
      "Name": "Report.xlsx",
      "IsFolder": false,
      "ModifiedDate": "2021-12-08T12:38:45.739Z",
      "Size": 102400,
      "Path": "/desfolder/Report.xlsx"
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}

*Remarque : La réponse répertorie à la fois les fichiers et les sous-dossiers situés dans le chemin spécifié.*

## **Comment supprimer un dossier**

### Informations sur l’API de suppression de dossier

```bash
DELETE https://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

Les paramètres de la requête sont les suivants :

| Nom du paramètre | Type    | Emplacement | Description |
|------------------|---------|-------------|-------------|
| path             | string  | path        | Chemin d’accès du dossier (par exemple `/dossier`). |
| storageName      | string  | query       | Nom du stockage à utiliser. |
| recursive        | boolean | query       | Mettre à `true` pour supprimer le dossier de façon récursive. |

**Réponses HTTP**

| Code | Description                                      |
|------|--------------------------------------------------|
| 200  | Dossier supprimé avec succès.                    |
| 400  | Requête incorrecte – paramètres invalides.      |
| 401  | Non autorisé – jeton JWT manquant ou invalide.  |
| 404  | Dossier introuvable.                             |
| 500  | Erreur interne du serveur.                       |

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/DeleteFolder) définit une interface de programmation publiquement accessible, permettant des interactions REST directement depuis un navigateur web.

### Exemple de suppression de dossier

{{< tabs tabTotal="2" tabID="7" tabName7="Requête" tabName8="Réponse" >}}
{{< tab tabNum="7" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/desfolder" \
  -X DELETE \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}
{{< tab tabNum="8" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*Remarque : La suppression d’un dossier avec `recursive=true` supprime définitivement tout son contenu.*

## **Comment copier un dossier**

### Informations sur l’API de copie de dossier

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/folder/copy/{srcPath}
```

Les paramètres de la requête sont les suivants :

| Nom du paramètre | Type   | Emplacement | Description |
|------------------|--------|-------------|-------------|
| srcPath          | string | path        | Chemin d’accès du dossier source (par exemple `/src`). |
| destPath         | string | query       | Chemin d’accès du dossier de destination (par exemple `/dst`). |
| srcStorageName   | string | query       | Nom du stockage source (facultatif). |
| destStorageName  | string | query       | Nom du stockage de destination (facultatif). |

**Réponses HTTP**

| Code | Description                                      |
|------|--------------------------------------------------|
| 200  | Dossier copié avec succès.                       |
| 400  | Requête incorrecte – paramètres invalides.      |
| 401  | Non autorisé – jeton JWT manquant ou invalide.  |
| 404  | Dossier source introuvable.                      |
| 500  | Erreur interne du serveur.                       |

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/CopyFolder) définit une interface de programmation publiquement accessible, permettant des interactions REST directement depuis un navigateur web.

### Exemple de copie de dossier

{{< tabs tabTotal="2" tabID="21" tabName21="Requête" tabName22="Réponse" >}}
{{< tab tabNum="21" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/copy/srcfolder?destPath=desfolder" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}
{{< tab tabNum="22" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*Remarque : L’opération de copie crée un nouveau dossier contenant les mêmes éléments que le dossier source.*

## **Comment déplacer un dossier**

### Informations sur l’API de déplacement de dossier

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/folder/move/{srcPath}
```

Les paramètres de la requête sont les suivants :

| Nom du paramètre | Type   | Emplacement | Description |
|------------------|--------|-------------|-------------|
| srcPath          | string | path        | Chemin d’accès du dossier source (par exemple `/dossier`). |
| destPath         | string | query       | Chemin d’accès du dossier de destination (par exemple `/dst`). |
| srcStorageName   | string | query       | Nom du stockage source (facultatif). |
| destStorageName  | string | query       | Nom du stockage de destination (facultatif). |

**Réponses HTTP**

| Code | Description                                      |
|------|--------------------------------------------------|
| 200  | Dossier déplacé avec succès.                     |
| 400  | Requête incorrecte – paramètres invalides.      |
| 401  | Non autorisé – jeton JWT manquant ou invalide.  |
| 404  | Dossier source introuvable.                      |
| 500  | Erreur interne du serveur.                       |

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/MoveFolder) définit une interface de programmation publiquement accessible, permettant des interactions REST directement depuis un navigateur web.

### Exemple de déplacement de dossier

{{< tabs tabTotal="2" tabID="23" tabName23="Requête" tabName24="Réponse" >}}
{{< tab tabNum="23" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/move/desfolder?destPath=destfolder" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}
{{< tab tabNum="24" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*Remarque : Le déplacement d’un dossier conserve sa structure interne et les versions des fichiers.*

## **Comment vérifier si un stockage existe**

### Informations sur l’API de vérification d’existence du stockage

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/{storageName}/exist
```

Les paramètres de la requête sont les suivants :

| Nom du paramètre | Type   | Emplacement | Description |
|------------------|--------|-------------|-------------|
| storageName      | string | path        | Nom du stockage à vérifier. |

**Réponses HTTP**

| Code | Description                                      |
|------|--------------------------------------------------|
| 200  | Indication d’existence du stockage renvoyée (`true` ou `false`). |
| 401  | Non autorisé – jeton JWT manquant ou invalide.  |
| 404  | Stockage introuvable.                            |
| 500  | Erreur interne du serveur.                       |

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/StorageExists) définit une interface de programmation publiquement accessible, permettant des interactions REST directement depuis un navigateur web.

### Exemple de vérification d’existence du stockage

{{< tabs tabTotal="2" tabID="33" tabName33="Requête" tabName34="Réponse" >}}
{{< tab tabNum="33" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/MyStorage/exist" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}
{{< tab tabNum="34" >}}

```json
{
  "Exists": true
}
```

{{< /tab >}}
{{< /tabs >}}

## **Comment vérifier si un fichier ou un dossier existe**

### Informations sur l’API de vérification d’existence d’un objet

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/exist/{path}
```

Les paramètres de la requête sont les suivants :

| Nom du paramètre | Type   | Emplacement | Description |
|------------------|--------|-------------|-------------|
| path             | string | path        | Chemin d’accès du fichier ou dossier (par exemple `/fichier.xlsx` ou `/dossier`). |
| storageName      | string | query       | Nom du stockage à vérifier. |
| versionId        | string | query       | Identifiant de version du fichier (facultatif). |

**Réponses HTTP**

| Code | Description                                      |
|------|--------------------------------------------------|
| 200  | Informations d’existence renvoyées.             |
| 401  | Non autorisé – jeton JWT manquant ou invalide.  |
| 404  | Fichier ou dossier introuvable.                 |
| 500  | Erreur interne du serveur.                       |

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/ObjectExists) définit une interface de programmation publiquement accessible, permettant des interactions REST directement depuis un navigateur web.

### Exemple de vérification d’existence d’un objet

{{< tabs tabTotal="2" tabID="37" tabName37="Requête" tabName38="Réponse" >}}
{{< tab tabNum="37" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/exist/Book1.xlsx" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}
{{< tab tabNum="38" >}}

```json
{
  "Exists": true,
  "IsFolder": false
}
```

{{< /tab >}}
{{< /tabs >}}

## **Comment obtenir l’utilisation du disque**

### Informations sur l’API d’obtention de l’utilisation du disque

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/disc
```

Les paramètres de la requête sont les suivants :

| Nom du paramètre | Type   | Emplacement | Description |
|------------------|--------|-------------|-------------|
| storageName      | string | query       | Nom du stockage à interroger. |

**Réponses HTTP**

| Code | Description                                      |
|------|--------------------------------------------------|
| 200  | Informations sur l’utilisation du disque renvoyées. |
| 401  | Non autorisé – jeton JWT manquant ou invalide.  |
| 500  | Erreur interne du serveur.                       |

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/GetDiscUsage) définit une interface de programmation publiquement accessible, permettant des interactions REST directement depuis un navigateur web.

### Exemple d’obtention de l’utilisation du disque

{{< tabs tabTotal="2" tabID="40" tabName40="Requête" tabName41="Réponse" >}}
{{< tab tabNum="40" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/disc?storageName=MyStorage" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}
{{< tab tabNum="41" >}}

```json
{
  "UsedSize": 12345678,
  "TotalSize": 987654321
}
```

{{< /tab >}}
{{< /tabs >}}

## **Comment obtenir les versions d’un fichier**

### Informations sur l’API d’obtention des versions d’un fichier

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/version/{path}
```

Les paramètres de la requête sont les suivants :

| Nom du paramètre | Type   | Emplacement | Description |
|------------------|--------|-------------|-------------|
| path             | string | path        | Chemin d’accès du fichier (par exemple `/fichier.xlsx`). |
| storageName      | string | query       | Nom du stockage à interroger. |

**Réponses HTTP**

| Code | Description                                      |
|------|--------------------------------------------------|
| 200  | Liste des versions du fichier renvoyée.         |
| 401  | Non autorisé – jeton JWT manquant ou invalide.  |
| 404  | Fichier introuvable.                             |
| 500  | Erreur interne du serveur.                       |

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/GetFileVersions) définit une interface de programmation publiquement accessible, permettant des interactions REST directement depuis un navigateur web.

### Exemple d’obtention des versions d’un fichier

{{< tabs tabTotal="2" tabID="46" tabName46="Requête" tabName47="Réponse" >}}
{{< tab tabNum="46" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/version/Report.xlsx?storageName=MyStorage" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}
{{< tab tabNum="47" >}}

```json
{
  "Value": [
    {
      "Name": "Report.xlsx",
      "IsFolder": false,
      "ModifiedDate": "2021-12-08T18:57:46.128Z",
      "Size": 102400,
      "Path": "/Report.xlsx",
      "VersionId": "1",
      "IsLatest": true
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}