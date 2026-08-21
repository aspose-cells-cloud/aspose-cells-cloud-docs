---
title: "Travail avec les métadonnées et propriétés Excel"
second_title: "Document"
linktitle: "Métadonnées & Propriétés"
type: docs
url: /fr/metadata/
aliases:
  - /document-properties/
  - /working-with-document-properties/
keywords: "Aspose.Cells Cloud, métadonnées Excel, API des propriétés de document, API REST, obtenir les métadonnées, mettre à jour les propriétés Excel, supprimer les métadonnées Excel"
description: "Découvrez comment lire, ajouter, mettre à jour et supprimer les métadonnées des fichiers Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut des exemples pour cURL et les SDK Java, .NET, Python, Node.js, etc."
ArticleTitle: "Travail avec les métadonnées et les propriétés des documents Excel – Aspose.Cells Cloud"
weight: 100
---

Les fichiers Excel peuvent stocker diverses métadonnées permettant d’identifier, d’organiser et de gérer les documents. Aspose.Cells Cloud fournit une API REST simple d’utilisation pour lire, ajouter, mettre à jour et supprimer ces métadonnées, permettant aux développeurs d’intégrer la gestion des propriétés des documents dans leurs applications. Ce guide couvre les deux catégories principales de propriétés — standard et personnalisées — explique comment les manipuler, et fournit des liens directs vers les points de terminaison API pertinents. Vous trouverez également un tableau de référence API concis contenant les détails des requêtes afin d’accélérer la mise en œuvre.

**Dernière mise à jour :** 8 juillet 2026  

**Types de propriétés de document**

Avant d’apprendre à utiliser les API Aspose.Cells Cloud pour afficher, modifier et supprimer les propriétés de document (métadonnées) dans Excel, clarifions les types de propriétés qu’un document Excel peut contenir.

- **Propriétés standard** : communes à Excel, elles contiennent des informations de base telles que Titre, Objet, Auteur, Catégorie, etc. Vous pouvez attribuer des valeurs textuelles personnalisées à ces propriétés afin de faciliter la localisation du fichier.

- **Propriétés personnalisées** : définies par l’utilisateur, elles permettent d’ajouter des métadonnées supplémentaires à votre document Excel.

**Comment travailler avec les propriétés de document dans un fichier Excel**

- [Comment obtenir une propriété de document spécifique à l’aide du stockage](/cells/document-properties/get/)
- [Comment obtenir les propriétés de document sans utiliser le stockage](/cells/metadata/get/)
- [Comment obtenir toutes les propriétés de document à l’aide du stockage](/cells/document-properties/get-all/)
- [Comment mettre à jour une propriété de document spécifique à l’aide du stockage](/cells/document-properties/update/)
- [Comment mettre à jour une propriété de document spécifique sans utiliser le stockage](/cells/metadata/update/)
- [Comment supprimer une propriété de document spécifique à l’aide du stockage](/cells/document-properties/delete/)
- [Comment supprimer les propriétés de document sans utiliser le stockage](/cells/metadata/delete/)
- [Comment supprimer toutes les propriétés de document à l’aide du stockage](/cells/document-properties/clear/)

**Référence API (sans stockage)**  

| Méthode | Point de terminaison | Description |
|---------|----------------------|-------------|
| **GET** | `GET https://api.aspose.cloud/v3.0/cells/metadata` | Récupère toutes les propriétés de document du classeur stocké dans le cloud. |
| **GET** | `GET https://api.aspose.cloud/v3.0/cells/metadata/{propertyName}` | Récupère la valeur d’une propriété spécifique (standard ou personnalisée), identifiée par `propertyName`. |
| **PUT** | `PUT https://api.aspose.cloud/v3.0/cells/metadata/{propertyName}` | Met à jour la valeur d’une propriété existante. Le corps de la requête contient la nouvelle valeur au format JSON. |
| **DELETE** | `DELETE https://api.aspose.cloud/v3.0/cells/metadata/{propertyName}` | Supprime une propriété spécifique du classeur. |
| **DELETE** | `DELETE https://api.aspose.cloud/v3.0/cells/metadata` | Supprime toutes les propriétés personnalisées et standard du classeur. |

*Toutes les requêtes nécessitent un jeton d’accès OAuth 2.0 et peuvent inclure des paramètres de requête facultatifs tels que `storage` et `folder` lorsqu’un emplacement de stockage spécifique est utilisé.*