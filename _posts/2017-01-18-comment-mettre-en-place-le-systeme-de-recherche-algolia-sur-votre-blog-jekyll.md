---
title: Comment mettre en place le système de recherche algolia sur votre blog jekyll
layout: post
categories:
- website development
language: French
image: algolia.png
---

<p>L’objectif de ce mini tutoriel est de mettre en place un formulaire de recherche  sur un site web statique développé avec le générateur de site web statique Jekyll. </p>

<h4> Pré-requis: </h4>
<ul>
<li>vous disposez d’un site web Jekyll configuré sur votre machine local </li>
<li>Vous avez un theme sur votre site jekyll et savez exactement ou placer votre formulaire de recherche.</li>
</ul>


<h3> Introduction </h3>

<p>Un site web statique à l’avantage d’être simple à mettre en place mais son coté statique (pas de bases de données) a un inconvénient lorsqu’il faut intégrer des fonctionnalités comme un système de commentaire, un système de recherche… à votre site. </p>
<p> Cependant, <b>avec l’avancé des technologies API (Application Programming Interface), toutes les fonctionnalités que vous désirez sur votre site web statique existent sous forme de services </b> que vous pouvez intégrer dans votre site web statique.</p>

<p>Algolia est un service web qui offre un API permettant d’indexer les contenus et offre  un formulaire de recherche sur ces contenus indexés que vous pouvez incorporer sur votre site web. Le résultat est nette et améliore l’expérience utilisateur. </p>

<blockquote>Voici le résultat escompté de ce tutoriel:
<img src='{{site.url}}/assets/img/algoliajekyll.gif' width="500px"></blockquote>

<p> Bon allons-y! </p>
<p> Les étapes suivantes permettront de suivre la mise en oeuvre du resultat ci-dessus: </p>
<ul>
<li id="installation"> Installer le plugin Algolia search</li>
<li id="compte">créer votre compte sur algolia.com et créer la clé API </li>
<li id="configuration">Configurer </li>
	<ul>
	<li id="formulaire"> Créer le formulaire de recherche </li>
	 <li id="librairie"> ajouter la librairie aljolia.js dans votre thème </li>
	 <li id="formulaire"> Ajouter la feuille de style CSS Algolia dans votre theme </li>
	  <li id="layout"> Modifier votre layout default.html present dans le dossier </li>
	  <li id="reference"> Mettre tout ensemble </li>
	</ul>
</ul>
