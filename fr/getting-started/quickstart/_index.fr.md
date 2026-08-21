---
title: "Aspose.Cells Cloud – Démarrage rapide : Créer une application de feuille de calcul en 5 minutes"
second_title: "Document"
ArticleTitle: "Aspose.Cells Cloud – Démarrage rapide"
linktype: "Démarrage rapide"
type: docs
url: /fr/quickstart/
description: "Aspose.Cells Cloud permet de créer, convertir, fusionner, découper, protéger des fichiers Excel, ainsi que d’effectuer des opérations internes sur les objets, entre de nombreuses autres fonctionnalités."
weight: 20
keywords: "Aspose.Cells Cloud, Excel, Feuille de calcul, API, SDK cloud, API REST, PDF, CSV, JSON, Démarrage rapide"
---

Ces instructions vous guident pas à pas pour initialiser l’API Aspose.Cells Cloud et installer les bibliothèques nécessaires au traitement des feuilles de calcul.

Vous pouvez facilement intégrer des fonctionnalités de conversion, génération et édition de feuilles de calcul dans des applications s’exécutant sur n’importe quel système d’exploitation moderne. Elles vous permettent de lire, modifier, fusionner et découper des feuilles de calcul, ainsi que de les convertir vers divers formats de fichiers. Ces bibliothèques de programmation vous donnent accès à un ensemble complet de composants de feuille de calcul : données, styles, formules, tableaux, graphiques, tableaux croisés dynamiques, en-têtes, pieds de page, commentaires, objets graphiques, liens hypertexte, filigranes, et bien plus encore.

## Créer un compte gratuit

Aspose Cloud repose sur un modèle de tarification clair et confortable, qui vous permet d’évaluer et de tester pleinement le produit avant de procéder à un achat.

Tout d’abord, vous devez créer un compte gratuit pour accéder à l’infrastructure cloud :

- Veuillez vous rendre sur la page de connexion du [Tableau de bord Aspose Cloud](https://dashboard.aspose.cloud/#/)
- Pour une connexion plus rapide, cliquez sur le bouton **Se connecter avec GitHub** ou **Se connecter avec Google**
- Fournissez les informations requises

{{% alert style="info" %}}

Félicitations ! Vous vous êtes inscrit avec succès à Aspose Cloud.

{{% /alert %}}

## Consulter et mettre à jour vos informations de compte

Ensuite, vous devez effectuer des ajustements individuels sur votre compte :

- Accédez à vos [Paramètres de compte Aspose](https://id.containerize.com/admin/) en cliquant sur l’icône située dans le coin supérieur droit de la page.

![dashboard.png](dashboard.png)

- Sélectionnez l’élément **Paramètres de compte** dans la barre de menu. Vérifiez vos paramètres, puis cliquez sur le bouton **Enregistrer les modifications** pour confirmer.

![settings.png](settings.png)

## Obtenir vos identifiants de sécurité (Client Id & Secret)

Aspose accorde une grande importance à la sécurité. Nous utilisons un jeton JWT pour l’authentification et un chiffrement HTTPS de bout en bout pour sécuriser toutes les interactions client-serveur.

Une **Application** est un ensemble d’identifiants API uniques : **Client Id** et **Client Secret**. Vous pouvez les utiliser pour vous authentifier lors de l’appel à notre API Cloud. Dans la plupart des cas, une seule Application suffit. Dans certains scénarios avancés, vous pouvez souhaiter enregistrer et utiliser plusieurs Applications dotées de credentials **Client Id** et **Client Secret** distincts.

Pour accéder aux informations relatives à vos Applications, procédez comme suit :

1. Connectez-vous au [Tableau de bord Aspose Cloud](https://dashboard.aspose.cloud/#/)
2. Cliquez, sur le côté gauche de la page, sur l’onglet [Applications](https://dashboard.aspose.cloud/applications).

![applications.png](applications.png)

3. Faites défiler vers le bas de la page ; vous trouverez un bouton **Créer une nouvelle application**. Cliquez dessus pour créer une nouvelle application.

![createnewapplication.png](createnewapplication.png)

4. Sur la page de création, saisissez le nom, la description et l’adresse de stockage souhaités, puis cliquez sur le bouton **Enregistrer** pour revenir à la page précédente après la création réussie.

![applicationinfo.png](applicationinfo.png)

5. Faites à nouveau défiler vers le bas de la page ; vous verrez la boîte d’informations concernant l’Application que vous venez de créer. Cliquez dessus pour consulter et mettre à jour vos identifiants de sécurité.

![firstapp.png](firstapp.png)

{{% alert style="info" %}}

Félicitations ! Vous avez obtenu avec succès vos identifiants de sécurité permettant d’authentifier vos appels à l’API Aspose.Cells.

{{% /alert %}}

## Choisir et installer un SDK

Veuillez prendre quelques instants pour vous familiariser avec la large gamme de produits Aspose.Cells Cloud, afin de mieux comprendre vos possibilités. Ces logiciels sont construits autour de l’[API Cloud](https://apireference.aspose.com/) haute performance, disponible 24h/24 et 7j/7.

Pour une utilisation efficace de l’API Cloud, nous proposons une famille d’[SDK Cloud](https://products.aspose.cloud/cells/family) puissants, adaptés à presque tous les principaux systèmes d’exploitation (Windows, macOS, Linux, Android) et aux langages de programmation les plus populaires, notamment [Android](https://products.aspose.cloud/cells/android), [C#](https://products.aspose.cloud/cells/net), [Python](https://products.aspose.cloud/cells/python), [Golang](https://products.aspose.cloud/cells/go), [Java](https://products.aspose.cloud/cells/java), [Node.js](https://products.aspose.cloud/cells/nodejs), [Perl](https://products.aspose.cloud/cells/perl), [PHP](https://products.aspose.cloud/cells/php), [Ruby](https://products.aspose.cloud/cells/ruby) et [Swift](https://products.aspose.cloud/cells/swift).

Tous ces SDK sont hébergés sur [GitHub](https://github.com/aspose-cells-cloud/). Chaque dépôt contient une large variété d’exemples de code illustrant leur utilisation.

## Consulter la documentation développeur et les exemples de code

Votre compte est désormais entièrement configuré et votre environnement de développement installé. Vous pouvez désormais commencer à écrire du code à l’aide de l’SDK choisi. Veuillez consulter le [Guide du développeur](https://docs.aspose.cloud/cells/developer-guide/) pour obtenir des informations sur l’utilisation facile de l’API Cloud.

Par exemple : convertir un classeur vers d’autres formats.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_Quickstart.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_Quickstart.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_Quickstart.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Demander une assistance, si nécessaire

N’hésitez pas à décrire vos problèmes et à poser vos questions sur nos [Forums Cloud](https://forum.aspose.cloud/c/cells/7). L’équipe d’assistance technique d’Aspose est prête à vous aider. Notez qu’Aspose ne fournit pas de support technique par téléphone ; le support téléphonique est uniquement réservé aux questions relatives à la vente et à l’achat.