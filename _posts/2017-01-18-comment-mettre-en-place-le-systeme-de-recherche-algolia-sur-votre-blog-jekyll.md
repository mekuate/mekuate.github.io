---
title: Comment mettre en place le système de recherche algolia sur votre blog jekyll
date: 2017-01-18 00:00:00 Z
categories:
- website development
layout: post
language: French
image: algolia.png
---

<h4>L’objectif de ce mini tutoriel est d'intégrer un  système  de recherche  interne sur un site web statique jekyll <h4>

<h3> Pré-requis: </h3>
<ul>
<li>vous disposez d’un site web Jekyll configuré sur votre machine local </li>
<li>Vous avez un theme sur votre site jekyll et savez exactement ou placer votre formulaire de recherche.</li>
</ul>

<h3> Introduction </h3>

<p>Un site web statique à l’avantage d’être simple à mettre en place mais son coté statique (pas de bases de données) a un inconvénient lorsqu’il faut intégrer des fonctionnalités comme un système de commentaire, un système de recherche, les formulaires... </p>
<p> Cependant, <b>avec l’avancé des technologies API (Application Programming Interface), toutes les fonctionnalités que vous désirez sur votre site web statique existent sous forme de services </b> que vous pouvez intégrer et enrichir votre site web statique en fonctionnalités .</p>

<p>Pour la mise en oeuvre d'un système de recherche interne à un site web statique, ils existent plusieurs services donc <b>Google Custom Search, Lunr.js, Algolia Search API. </b>Ce mini tutoriel présente comment intégrer Algolia Search API sur votre site web statique.  Le rendu est très remarquable,  très moderne et améliore l'expérience utilisateur, comme présenté ci-dessous:</p>

<blockquote><img src='{{site.url}}/assets/img/algoliajekyll.gif' width="500px"></blockquote>

<h3> Bon allons-y! </h3>
<p> Les étapes suivantes permettront de suivre la mise en oeuvre du resultat ci-dessus: </p>

<h3>Installer le plugin Algolia search </h3>
<p>Ajouter la commande <code>algoliasearch-jekyll gem  </code> dans la section <code> :jekyll_plugins </code> de votre fichier Gemfile situé à la racine de votre repertoire de site web . Si vous n'avez pas encore le fichier Gemfile, voici le contenu minimum requis pour commencer: 
</p>
<pre><code>
gem 'jekyll', '~> 2.5.3' 
group :jekyll_plugins do 
  gem 'algoliasearch-jekyll', '~> 0.8.0'
end
</code></pre>
<p>Télécharger  toutes les dépendances avec la commande <code> bundle install. </code></p><p>Ensuite, ajouter <code> algoliasearch-jekyll </code> dans votre fichier <code> _config.yml </code> dans la section <code>  gems </code> comme ceci:<br>
<pre><code>
gems: <br>
  - algoliasearch-jekyll<br>
	</code></pre>
	</p><p> Si tout c'est bien passé, vous devriez executer la commande <code> jekyll help </code> et voir afficher algolia dans la liste des commandes.</p>
<h3> créer votre compte sur algolia.com et créer la clé API </h3>
[redaction en cours]
 
<h3>Créer le formulaire de recherche sur votre site</h3>
<p>créer le fichier recherche.html dans votre dossier _includes. Le fichier recherche.html contient le code HTML suivant:</p>
<pre><code>
&lt;div class="container search-form"&gt;
  &lt;input type="text" class="algolia__input js-algolia__input" autocomplete="off" name="query" placeholder="Search on this site..."  /&gt;
 &lt;/div&gt;
 </code></pre>
<p> Et le résultat est le suivant:  <input type="text" class="algolia__input js-algolia__input" autocomplete="off" name="query" placeholder="Search on this site..."  /></p> <p> NB: Le fichier recherche.html doit être inclus à l'emplacement prévu avec l'instruction  <pre><code> &#123;% include recherche.html  % &#125;</code></pre></p>
 <h3>ajouter la librairie algolia.js dans votre thème </h3>
 <p>Télécharger le fichier (ou copier/ coller son contenu)  
 <a href="https://github.com/algolia/algoliasearch-jekyll-hyde/blob/master/public/js/algolia.js" target="_blank"> algolia.js </a> et le placer dans le dossier javascript (js) où vous sauvegardez vos librairies dans votre theme. Par exemple le chemin <code>assets/js/algolia.js</code> peut contenir la librairie algolia.js. </p>
 <h3>Ajouter la feuille de style CSS Algolia dans votre thème</h3>
 <p>  Ajouter le <a href ="https://github.com/algolia/algoliasearch-jekyll-hyde/blob/master/public/css/algolia.css" target="_blank">script css  </a>de Algolia pour configurer l’apparence (Design) du formulaire de recherche et le résultat de recherche dans votre propre fichier CSS ou SCSS.

</p>
 <h3>Modifier votre layout default.html </h3>
 [redaction en cours]
 <h3>Mettre tout ensemble </h3>
 [redaction en cours]

