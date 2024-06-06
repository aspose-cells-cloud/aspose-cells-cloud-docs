---
title: Aspose.Cells SDK Cloud pour G
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/available-sdks/aspose-cells-cloud-go/
description: Aspose.Cells Cloud SDK for Go offre une solide prise en charge multiplateforme pour les développeurs Go, ce qui facilite son intégration et son utilisation pour Windows, Linux ou macOS. Il prend en charge Excel pour créer, convertir, fusionner, diviser, protéger, opération d'objet interne, etc.
weight: 30
kwords: Go, Excel, Office Cloud, REST API, graphique, tableau croisé dynamique, tableau, feuille de calcul, PDF, CSV, Json, Markdown
---
 Le SDK est open source et sous licence MIT. Vous pouvez accéder au code source de la bibliothèque Go pour Aspose.Cells Cloud[ici](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go).

# **Comment utiliser la bibliothèque Go de Aspose.Cells Cloud**

Aspose.Cells Cloud SDK for Go est une bibliothèque puissante qui permet aux développeurs de manipuler et de traiter Microsoft Excel fichiers à l'aide du langage de programmation Go. Avec ce SDK, vous pouvez créer, modifier et convertir des documents Excel dans le cloud, sans installer de logiciel ou de dépendances supplémentaires sur votre ordinateur local.

Dans cet article, nous verrons comment utiliser le SDK Cloud Aspose.Cells pour Go pour effectuer certaines tâches courantes, telles que la création d'un nouveau classeur Excel, l'insertion de données dans des cellules et l'enregistrement du classeur modifié dans le cloud.

## **Commencer**

 Avant de pouvoir commencer à utiliser le SDK Cloud Aspose.Cells pour Go, vous devez configurer votre environnement de développement et installer les dépendances nécessaires. Faire référence à[l'article](https://docs.aspose.cloud/cells/quickstart/) sur le site Aspose pour obtenir votre identifiant client et votre secret client.

## Comment installer le package Go pour Aspose.Cells Cloud

Vous pouvez installer Aspose.Cells Cloud SDK for Go à l'aide de la commande `go get`. Ouvrez votre terminal ou votre invite de commande et exécutez la commande suivante :

```bash
go get -u github.com/aspose-cells-cloud/aspose-cells-cloud-go
```

Cela téléchargera et installera la dernière version du SDK sur votre espace de travail Go.


## Comment importer la bibliothèque Go dans votre projet


```golang
package main

import (
	asposecellscloud "github.com/aspose-cells-cloud/aspose-cells-cloud-go"
)
```

## Comment utiliser le package Go pour convertir Xlsx en PDF

- Importer la bibliothèque cloud Aspose.Cells
Commencez par importer le package nécessaire du SDK Cloud Go Aspose.Cells dans votre projet.
- Configurer le client API avec les informations d'identification
 Authentifiez votre client API avec votre identifiant client unique et votre secret client.
- Préparer les paramètres de conversion
 Définissez les paramètres de la tâche de conversion, notamment le nom du fichier source, le format de sortie souhaité et le chemin du dossier de stockage.
- Exécuter la conversion du classeur
 Appelez le processus de conversion à l'aide de la méthode PostConvertWorkbook et gérez la réponse.

### **Exemple de code**

```golang
package main

import (
	"os"
	asposecellscloud "github.com/aspose-cells-cloud/aspose-cells-cloud-go"
)
func main() {
	instance := asposecellscloud.NewCellsApiService(os.Getenv("ProductClientId"), os.Getenv("ProductClientSecret"), "https://api.aspose.cloud", "v3.0")
    remoteFolder := "TestData/In"

    localName := "Book1.xlsx"
    remoteName := "Book1.xlsx"

    format := "pdf"

    var mapFiles map[string]string       
    mapFiles = make(map[string]string)
    mapFiles[localName]=  localName 

    request := new (asposecellscloud.PutConvertWorkbookRequest)
    request.File =         mapFiles    
    request.Format =         format    
    _, httpResponse, err := instance.PutConvertWorkbook(request)
    if err != nil {
      print(err)
    } else if httpResponse.StatusCode < 200 || httpResponse.StatusCode > 299 {
      print("Test fail")
    }
}

```
