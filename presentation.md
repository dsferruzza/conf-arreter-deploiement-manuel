% Le déploiement manuel : non merci, j'essaie d'arrêter !
% David Sferruzza
% 30/09/2016


# À propos de moi

- [\@d_sferruzza](https://twitter.com/d\_sferruzza)
- [github.com/dsferruzza](https://github.com/dsferruzza)
- Responsable R&D chez [Startup Palace](http://www.startup-palace.com)
- Doctorant en génie logiciel à l'Université de Nantes

<figure class="stretch"><img src="img/sp.gif" alt=""></figure>


# Startup Palace

Nous concevons et développons des applications web.
<br><small>(parmi d'autres activités)</small>

Nous aidons des startups à proposer de la valeur à leurs marchés : la **qualité** des applications est importante.

On veut éviter un *facteur bus* trop faible.

<figure class="stretch"><img src="img/bus.gif" alt=""></figure>


# Startup Palace

Le développement, la qualité et le déploiement d'un projet ne doivent **pas** reposer sur une seule personne !

> Il faut **documenter** et **automatiser** un maximum de choses pour pouvoir travailler collaborativement.

<figure class="stretch"><img src="img/team.gif" alt=""></figure>


# Mais revenons un peu en arrière...

&nbsp;

<figure class="stretch"><img src="img/back.gif" alt=""></figure>

... quand il n'y avait qu'un seul développeur.


# Collaboration unipersonnelle

La source de vérité du projet est sur le poste du dev.

Le dev gère tout manuellement :

- écriture du code
- dépendances externes
- construction de l'application
- déploiement de l'application

<figure class="stretch"><img src="img/alone.gif" alt=""></figure>


# Écriture du code

On prend l'exemple d'un site développé avec Jekyll.

> ![](img/jekyll.png)
>
> Transform your plain text into static websites and blogs.
>
> <https://jekyllrb.com/>


# Écriture du code

Le dev est seul.
Il n'a pas besoin de partager son code ou d'y incorporer des modifications faites par d'autres.

<div class="smallcode">
```text
.
├── _config.yml
├── _drafts
|   ├── begin-with-the-crazy-ideas.md
|   └── on-simplicity-in-technology.md
├── _includes
|   ├── footer.html
|   └── header.html
├── _layouts
|   ├── default.html
|   └── post.html
├── _posts
|   ├── 2007-10-29-why-every-programmer-should-play-nethack.md
|   └── 2009-04-26-barcamp-boston-4-roundup.md
├── _data
|   └── members.yml
├── _site
├── .jekyll-metadata
└── index.html
```
</div>


# Dépendances externes

Le projet a besoin de [jQuery](https://jquery.com/) pour fonctionner.

Le dev va donc :

- télécharger le fichier `jquery-3.1.1.min.js` depuis le site officiel
- le placer dans l'arborescence du projet Jekyll

S'il veut mettre à jour jQuery, il supprime l'ancienne version et recommence.

<figure class="stretch"><img src="img/jquery.svg" alt=""></figure>


# Construction de l'application

Le dev a installé sur son système :

- Ruby
- Jekyll

Il lance une commande pour produire le site final :
<br>`bundle exec jekyll build`

Le dossier `_site/` contient maintenant une version déployable de l'application.

<figure class="stretch"><img src="img/machine.gif" alt=""></figure>


# Déploiement de l'application

Le dev envoie le contenu du dossier `_site/` vers son hébergement.

Il peut utiliser (notamment) :

- FTP
- SFTP
- rsync

<figure class="stretch"><img src="img/throw.gif" alt=""></figure>


# Quelques temps plus tard...

Plus de projets &rarr; plus de devs

&nbsp;

<figure class="stretch"><img src="img/300.gif" alt=""></figure>

&nbsp;

Les devs doivent collaborer sur les projets, ce qui pose des problèmes.


# Problèmes de collaboration

Quelques exemples :

- le code source ne peut **pas** être sur le poste d'un seul dev, la source de vérité non plus
- il faut pouvoir travailler à plusieurs *simultanément* sur le même projet
- tous les devs doivent être capable de :
	- **construire** l'application (avec une recette *identique*)
	- la **tester** (dans un environnement *identique*)
	- la **déployer**


# Version Control System

Ou *VCS*, *logiciel de gestion de versions*.

> Permet de stocker un ensemble de fichiers en conservant la chronologie de toutes les modifications qui ont été effectuées dessus.

On code normalement, et on utilise le *VCS* pour organiser la journalisation de nos modifications.

Aujourd'hui, on ne va parler que de [Git](https://git-scm.com/).
<br>(mais il y en a d'autres)


# Git

<figure class="stretch"><img src="img/git-log.png" alt=""></figure>


# Git

<figure class="stretch"><img src="img/git-diff.png" alt=""></figure>


# Git

<figure class="stretch"><img src="img/git-branch.png" alt=""></figure>


# Avantages de Git

On peut :

- bosser à plusieurs sur les mêmes fichiers *simultanément*
- garder trace de chaque changement
- naviguer dans l'historique
- bosser sur plusieurs versions du projet en parallèle (anciennes version, fonctionnalités expérimentales, ...)
