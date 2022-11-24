---
layout: page-s
title: Prise en main
permalink: /prise-en-main/
lang: fr
---


Ce site a été conçu pour être immédiatement utilisable pour votre rendu. Sur Gitlab, vous allez : 1) "forker" le projet Gitlab de ce site, 2&3) faire quelques adaptations de configuration pour le personnaliser et le rendre fonctionnel.

- toc
{:toc}

## 0. Définitions

Quelques définitions avant de voir [la procédure détaillée](#1-fork):

### Forker ?
> Il s'agit d'un terme consacré à l'univers Git qui veut dire _**"dupliquer le projet Gitlab de quelqu'un d'autre pour en faire mon propre projet"**_. Le fork est une fonctionnalité qui concrétise l'idée du partage des sources ouvertes (open source). En un clic, on s'approprie un projet et on peut librement retravailler, exploiter, développer, etc.


{: .warning}
**Attention :** l'étape 1 (fork) ne doit être effectuée qu'une fois par groupe de travail.

## 1. Fork
1. Ouvrez [la page du projet Gitlab](https://gitlab.com/p8hn/avun2022/site-portfolio-tobeforked) et cliquez en haut à droite sur le bouton "fork" ![fork]({{ site.baseurl }}/assets/media/fork-button.png){: .shadow}
2. Dans l'écran qui s'ouvre, renommez le _Project Name_ et le _Project Slug_ par le nom de votre enquête ou groupe de travail, par exemple `empreinte-numerique`
  ![Fork]({{ site.baseurl }}/assets/media/fork.png){: .shadow}
3. Dans le menu déroulant `namespace`, choisissez où vous souhaitez dupliquer le projet. Pour l'évaluation, il vous est demandé de livrer votre site dans votre sous-groupe de projet, par exemple `/p8hn/avun2022/ub-risation`.
  - Choisissez alors : `p8hn/avun2022/votre-projet` tel qu'il est indiqué dans [la liste des sous-groupes](https://gitlab.com/p8hn/avun2022).
4. Validez en cliquant sur le bouton `Fork project`. Votre projet Gitlab est créé.


## 2. Configuration et déploiement

1. Dans l'interface d'édition de Gitlab, ouvrez le fichier `_config.yml` en cliquant dessus puis en cliquant sur le bouton [Edit] ;  
   modifiez à votre guise les différents paramètres : `title`, `description`, `author`, `url_repository` (c'est l'url de votre projet Gitlab), `base_url` (modifier avec le nom de votre projet), etc.
4. Validez vos modifications.
5. La modification a entraîné une opération qui peut prendre plusieurs minutes. Votre site est en train d'être "généré".
5. Une fois que l'opération est terminée et si elle s'est bien passée, votre site devrait être généré et déployé sur Gitlab Pages. Vous pouvez vérifiez cela en cliquant sur le menu [Settings], puis [Pages] qui fournit l'URL de votre site.

## 3. Paramétrer le thème Tao

> Un thème est le design graphique d'un site. Pour ce site, nous avons choisi [le thème Tao](https://github.com/vfvong/jekyll-theme-tao), mais il existe beaucoup d'autres thèmes pour Jekyll (voir [l'un des catalogues](https://jamstackthemes.dev/ssg/jekyll/) en ligne).

Le thème Tao est relativement simple d'utilisation.
 Vous pouvez cependant mettre en place le thème de votre choix pour votre site de Portfolio.

Chaque thème propose différents paramètres selon son fonctionnement. Le thème Tao demande les paramétrages suivants :

1. la navigation dans le fichier `_data/navigation.yml`:
   > contrairement aux posts de blog, les pages ne sont pas référencées automatiquement dans la barre de navigation. Il faut les ajouter une par une dans ce fichier en respectant la syntaxe existante.
2. les liens vers vos réseaux sociaux dans le fichier `_data/social.yml`
   > De la même manière, ce fichier rassemble toutes vos données sociales. Les icônes font références au site [Fontawesome](https://fontawesome.com/icons) sur lequel vous pouvez trouver celle·s qui vous convien·nen·t.
3. des règles CSS dans le fichier `assets/css/mystyles.css`
   > Si vous maîtriser le langage CSS, vous pouvez personnaliser l'apparence de votre site (couleurs, polices, bordures, etc.) en éditant ce fichier. Vous trouverez toutes les ressources nécessaires sur le Web.
4. des balises supplémentaires dans le `<head>` (par exemple pour ajouter un fichier css), ou des éléments de SEO ?

Le thème Tao permet d'autres paramétrages, je vous laisse consulter [sa documentation sur Github](https://github.com/vfvong/jekyll-theme-tao#usage).

## 4. Ajouter du contenu

Vous devez imaginer la structure de votre site en pages et en répertoires/sous-répertoires. Cette structure doit refléter celle de votre portfolio. Vous êtes libre d'imaginer ce que vous voulez, tant que l'on retrouve les différents livrables demandés.

Pensez à vos lecteurs en terme de parcours de lecture : accueil, Note de cadrage, Diagrammes, Synthèse bibliographique, etc.

### Ajouter une page
Pour ajouter une page, il suffit dans le projet Gitlab de créer un nouveau fichier markdown `.md` et de l'initier avec un en-tête reproduisant les lignes suivantes (sans oublier les `---`) en tête de fichier, avant d'ajouter le contenu de la page au format Markdown:

```yaml
---
layout: page-s
title: Prise en main
permalink: /prise-en-main/
lang: fr
---

Contenu de la page au format *markdown*.
```
### Ajouter un post de blog
Vous pouvez également documenter votre travail tout au long de l'année dans un "journal de bord" à l'aide des posts de blog. Ce "journal de bord" n'a pas besoin d'être hyper complet ou finalisé. Vous pouvez par exemple y publier régulièrement les différentes étapes de conception du projet. C'est facultatif bien entendu, mais vous verrez que l'exercice en vaut la peine. Après tout, le process est plus intéressant que le résultat..

## Rappels

Vous pouvez utiliser toutes les subtilités du markdown et du HTML/CSS pour éditer et personnaliser votre site :

- premiers pas en markdown : [markdowntutorial.com](https://www.markdowntutorial.com/fr/)
- pour aller plus loin avec "kramdown" (format markdown étendu) utilisé dans Jekyll : [kramdown.gettalong.org](https://kramdown.gettalong.org/quickref.html)
- et au-delà en ajoutant vos propres classes et règles CSS.
