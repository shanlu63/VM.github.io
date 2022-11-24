---
layout: page-s
title: About
permalink: /about/
---

Ce site est réalisé avec [Jekyll](https://jekyllrb.com/), un générateur de site statique.

- toc
{:toc}


### Structure
Il peut contenir (pour le moment) deux types de contenus:
1. des "pages" : ce sont des contenus non datés et organisés entre eux dans une structure arborescente (par exemple par thèmes)
2. des "posts de blog": ce sont des contenus datés, en général signé par un ou plusieurs auteurs, organisé entre eux selon une structure chronologique, formant ainsi un blog ou un journal avec des publications régulières.

Le site contient actuellement :
- 3 pages :[Accueil]({% link index.md %}), [À propos](./), [Prise en main]({% link prise-en-main.md %})
- 1 post de blog : [Welcome to Jekyll!]({% link _posts/2022-10-10-welcome-to-jekyll.markdown %})

### Thème et améliorations
Ce site est construit avec le thème Tao et quelques améliorations :
- ajout d'un fichier `/assets/css/mystyles.css` pour personnaliser votre site.
- ajout d'un _include_ `/_includes/gitlab-source.html` pour ajouter un bouton "Éditez cette page sur Gitlab".
- ajout d'un _layout_ `_layouts/page-s.html` exploitant l'_include_ `gitlab-source`.

Ces améliorations sont là pour vous inspirer et vous aider à créer vos propres améliorations.

Pour utiliser ce thème, [suivez le guide de prise en main]({% link prise-en-main.md %}).
