[![CircleCI](https://circleci.com/gh/SuperEwolis/Symfony5-Base.svg?style=svg&circle-token=03425d5d38fa7f591c8ee542afaab8851f98aedb)](https://circleci.com/gh/SuperEwolis/Symfony5-Base) [![Build Status](https://travis-ci.com/SuperEwolis/Symfony5-Base.svg?token=gzNTAmE5FFhpfun2gRhq&branch=master)](https://travis-ci.com/SuperEwolis/Symfony5-Base)

### Le repository
Basé sur `Symfony5`, ce projet contient toutes les dépendances nécessaires pour le bon fonctionnement des projets web.

#### Prérequis
* Être sur un système disposant d'un terminal sous bash/shell
* Avoir une version php >= php@7.3
* Avoir composer d'installer (https://getcomposer.org/)
* Avoir une version nodeJS >= node@11 (https://nodejs.org/en/)

### Installation

* Ouvrez votre terminal

```
git clone https://github.com/SuperEwolis/Symfony5-Base.git
```

* Renomez le et allez dans le repertoire courant du projet, puis installer les dépendances nécessaires

```
cd monProjet && composer install && yarn install
```

### Préparation à l'envoi sur le serveur

* Une fois sur le serveur, ouvrez votre terminal et créez un dossier correspondant au nom de votre projet

```
cd dev && mkdir monProjet && cd monProjet
```

### Transfert sur le serveur
#### Description
L'intrégralité des projets en développements seront dans le dossier suivant `dev`

* Ouvrez votre terminal et allez dans le repertoir du projet local

```bash
#!/bin/bash
rsync -av ./ user@server:~/dev/monProjet --include=public/build --include=public/.htaccess --exclude-from=.gitignore 
```

* Toujours dans le repertoire courant du projet, exécutez cette commande pour installer les dépendances

```
composer install && composer require symfony/apache-pack
```

### Accès

* http://pormzswm.preview.infomaniak.website/monProjet/public/
* http://pormzswm.preview.infomaniak.website/monProjet/public/contact
