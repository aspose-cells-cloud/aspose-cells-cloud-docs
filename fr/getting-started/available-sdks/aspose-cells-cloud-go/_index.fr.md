---
title: Aspose.Cells Cloud SDK pour G
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/available-sdks/aspose-cells-cloud-go/
description: Le SDK Cloud pour Go (Aspose.Cells) offre une prise en charge multiplateforme performante pour les développeurs Go, facilitant ainsi son intégration et son utilisation sous (Windows), Linux ou macOS. Il prend en charge (Excel) la création, la conversion, la fusion, le fractionnement, la protection, les opérations sur objets internes, etc.
weight: 30
kwords: Go, Excel, Office Cloud, REST API, Graphique, Tableau croisé dynamique, Tableau, Feuille de calcul, PDF, CSV, Json, Markdown
---
 Le SDK est open source et sous licence MIT. Vous pouvez accéder au code source de la bibliothèque Go pour Aspose.Cells Cloud.[ici](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go).

# **Comment utiliser la bibliothèque Go du Cloud Aspose.Cells**

Aspose.Cells Cloud SDK for Go est une bibliothèque puissante qui permet aux développeurs de manipuler et de traiter des fichiers Microsoft Excel à l'aide du langage de programmation Go. Grâce à ce SDK, vous pouvez créer, modifier et convertir des documents Excel dans le cloud, sans installer de logiciel ni de dépendances supplémentaires sur votre machine locale.

Dans cet article, nous allons explorer comment utiliser Aspose.Cells Cloud SDK for Go pour effectuer certaines tâches courantes, telles que la création d'un nouveau classeur Excel, l'insertion de données dans des cellules et l'enregistrement du classeur modifié dans le cloud.

## **Commencer**

 Avant de commencer à utiliser le SDK Cloud Aspose.Cells pour Go, vous devez configurer votre environnement de développement et installer les dépendances nécessaires. Consultez[l'article](https://docs.aspose.cloud/cells/quickstart/) sur le site Aspose pour obtenir votre identifiant client et votre secret client.

## Comment installer le package Go pour Aspose.Cells Cloud

Vous pouvez installer le SDK Cloud Aspose.Cells pour Go à l'aide de la commande `go get`. Ouvrez votre terminal ou votre invite de commande et exécutez la commande suivante :

```bash
go install github.com/aspose-cells-cloud/aspose-cells-cloud-go@latest
```

Cela téléchargera et installera la dernière version du SDK sur votre espace de travail Go.

## Comment importer la bibliothèque Go dans votre projet

```golang
package main

import (
 . "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v25"
)
```

## Comment démarrer avec Aspose.Cells Cloud for Go, suivez ces étapes

- Créez un compte au Aspose pour Cloud et obtenez votre identifiant client et votre secret d'application.
- Créez un répertoire pour votre projet et un fichier main.go à l'intérieur. Ajoutez le code suivant à votre fichier main.go.

### **Exemple de code**

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_AvailableSDKs.go" >}}

- Initialisez le projet go.mod, récupérez les dépendances de votre projet et exécutez votre application créée.

```bash
go mod init main
go mod tidy
go run main.go

```
