---
title: Comment mettre en place le système de recherche algolia sur votre blog jekyll
layout: post
categories: ["website development"]
language: French
image: algolia.png
---

<p>L’objectif de ce mini tutoriel est de mettre en place un formulaire de recherche  sur un site web statique développé avec le générateur de site web statique Jekyll. </p>

<h4> Pré-requis: </h4>
<ul>
<li>vous disposez d’un site web Jekyll configuré sur votre machine local </li>
<li>Vous avez un theme sur votre site jekyll et savez exactement ou placer votre formulaire de recherche.</li>
</ul>


<h4> Introduction </h4>

<p>Un site web statique à l’avantage d’une très simple à mettre en place mais son coté statique (pas de bases de données) a un inconvénient lorsqu’il faut mettre en place des fonctionnalités comme un système de commentaire, un système de recherche… donc la mise en oeuvre est très intégré pour les sites dynamiques. Cependant, avec l’avancé des technologies API (Application Programming Interface), toutes les fonctionnalités que vous désirez sur votre site web statique existent sous forme de services que vous pouvez intégrer dans votre site web statique.</p>

<p>Algolia est un service web qui offre un API permettant d’indexer les contenu et offre  un formulaire de recherche sur ces contenus indexés que vous pouvez mettre sur votre site web. Le résultat est nette et améliore l’expérience utilisateur. </p>

<p>Pour intégrer le service de recherche Algolia dans un site web Jekyll, un plugin a été développé par le fournisseur Algolia: <a href="https://github.com/algolia/algoliasearch-jekyll" target="_blank"> https://github.com/algolia/algoliasearch-jekyll</a></p>

<h3> Work in progress </h3>
