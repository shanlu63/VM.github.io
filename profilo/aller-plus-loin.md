---
layout: page-s
title: Pour aller plus loin
permalink: /aller-plus-loin/
lang: fr
---

Vous savez maintenant

Ce site a été conçu pour être immédiatement utilisable pour votre rendu. Sur Gitlab, vous allez : 1) "forker" le projet Gitlab de ce site, 2) "cloner" votre nouveau projet sur votre machine, 3&4) faire quelques adaptations de configuration pour le personnaliser et le rendre fonctionnel.

- toc
{:toc}

## 0. Définitions

Quelques définitions avant de voir [la procédure détaillée](#1-fork):


### Cloner ?
> Encore un terme Git qui veut dire **"dupliquer et synchroniser un projet Gitlab vers un répertoire 'local' (sur mon PC)"**. C'est en fait la même chose qu'un "fork", mais au lieu de dupliquer de Gitlab à Gitlab, ca duplique de Gitlab à votre PC. Une alternative est de télécharger le ZIP du projet Gitlab, mais le clone a le mérite de conserver la synchronisation avec le projet Gitlab.

{: .warning}
**Attention :** Les étapes suivantes (clone) peuvent être effectuées par chacun des membres du groupe pour que chacun puisse développer/alimenter votre site.

## 1. Fork
1. Ouvrez [la page du projet Gitlab](https://gitlab.com/p8hn/net2022/site-projet-tobeforked) et cliquez en haut à droite sur le bouton "fork" ![fork]({{ site.baseurl }}/assets/media/fork-button.png){: .shadow}
2. Dans l'écran qui s'ouvre, renommez le _Project Name_ et le _Project Slug_ par le nom de votre enquête ou groupe de travail, par exemple `empreinte-numerique`
  ![Fork]({{ site.baseurl }}/assets/media/fork.png){: .shadow}
3. Dans le menu déroulant `namespace`, choisissez où vous souhaitez dupliquer le projet. Pour l'évaluation, il vous est demandé de livrer votre site dans le sous-groupe `/p8hn/net2022/`.
  - Choisissez alors : `p8hn/net2022`.
4. Validez en cliquant sur le bouton `Fork project`. Votre projet Gitlab est créé.

## 2. Clone
Vous pouvez maintenant cloner votre projet, c'est-à-dire le dupliquer sur votre PC.

1. Cliquez sur le bouton Clone et copier l'url `https`.
1. Dans un terminal sur votre PC, placez-vous "au bon endroit" en utilisant la commande `cd`, puis lancez la commande `git clone [url]` en remplaçant `[url]` par l'url que vous venez de copier sur Gitlab.
1. Un nouveau répertoire vient d'être créé sur votre PC. Il a le nom de votre projet Gitlab, par exemple `empreinte-numerique`

## 3. Configuration et déploiement
1. Déplacez le terminal dans votre répertoire : par exemple `cd empreinte-numerique`.
2. Installez les dépendances du Gemfile : `bundle install`
2. Ouvrez le fichier `_config.yml` et modifiez à votre guise les différents paramètres : `title`, `description`, `author`, `url_repository` (c'est l'url de votre projet Gitlab), `base_url` (modifier avec le nom de votre projet), etc.
3. Vérifier que le site fonctionne bien en lançant le serveur Jekyll: `bundle exec jekyll serve`
4. Validez vos modifications (add/commit) et synchronisez les avec votre projet Gitlab : `git push`
5. Vérifiez sur Gitlab que votre site est bien déployé sur Gitlab Pages.

## 4. Paramétrer le thème Tao

Vous devez/pouvez paramétrer :

1. la navigation dans le fichier `_data/navigation.yml`
2. les liens vers vos réseaux sociaux dans le fichier `_data/social.yml`
4. des règles CSS dans le fichier `assets/css/mystyles.css`
3. des balises supplémentaires dans le `<head>` (par exemple pour ajouter un fichier css), ou des éléments de SEO ?

Tao permet d'autres paramétrages, je vous laisse consulter [sa documentation sur Github](https://github.com/vfvong/jekyll-theme-tao#usage).

## 5. Ajouter du contenu

Vous devez imaginer la structure de votre site en pages et en répertoires/sous-répertoires. Cette structure doit refléter votre enquête. Vous êtes libre d'imaginer ce que vous voulez. Pensez à vos lecteurs en terme de parcours de lecture : accueil, problématique, volets de l'enquête, etc.

Vous pouvez également documenter votre enquête dans un "journal de bord" à l'aide des posts de blog. Ce "journal de bord" n'a pas besoin d'être hyper complet ou finalisé. Vous pouvez par exemple y publier régulièrement les différentes étapes de conception du projet. C'est facultatif bien entendu, mais vous verrez que l'exercice en vaut la peine. Après tout, le process est plus intéressant que le résultat..

## Rappels

Vous pouvez utiliser toutes les subtilités du markdown et du HTML/CSS pour éditer et personnaliser votre site :

- premiers pas en markdown : [markdowntutorial.com](https://www.markdowntutorial.com/fr/)
- pour aller plus loin avec "kramdown" (format markdown étendu) utilisé dans Jekyll : [kramdown.gettalong.org](https://kramdown.gettalong.org/quickref.html)
- et au-delà en ajoutant vos propres classes et règles CSS.
