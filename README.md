# Plan-action-devops

## Présentation

- [Miro](https://miro.com/app/board/uXjVLXGDKW0=/)

## Contexte

En tant que Consultant DevOps dans l'entreprise RealCompany, vous êtes missionné pour optimiser les processus internes de production. 

Vous avez trois objectifs concrets à remplir cette semaine : 

- Établir diverses recommandations et en appliquer certaines tout de suite pour optimiser le flow général de la production.
- Créer un environnement de développement Docker hébergé sur GitHub, contenant des micro-services.
- Créer un pipeline d'intégration continue.

## Problématiques

La société RealCompany a bien grandi ces dernières années, et la taille des projets aussi. Cela fait déjà un moment que des problèmes apparaissent pendant le développement des projets et au moment de leur sortie en production :

- Il n'y a pas assez de communication et de collaboration entre les équipes de dev et d'ops. Les problématiques d'administration système et de déploiement n'ont jamais été optimisées, et les mêmes erreurs sont souvent reproduites.
- Les développeurs modifient leurs couches logicielles en cours de projet mais ne communiquent pas forcément l'information à l'administrateur système en charge du déploiement. Ceci provoque un décalage entre les environnements de dev et de prod. Le temps de déploiement final est impacté, puisque l'administrateur système est alors dans l'urgence de la modification du stack de production.
- Les environnements de développement sont systématiquement différents entre les développeurs : certains utilisent Windows, d'autres Linux ou Mac.
- Les Administrateurs Systèmes font également leurs propres choix sur la production sans consulter les devs.
- Les développeurs ont tendance à bâcler leurs projets en fin de cycle, pour coller aux délais toujours plus serrés. La qualité est donc parfois variable en fonction de ce paramètre.
- Le déploiement des mises à jour est devenu extrêmement long, par manque de tests consistants et par l'absence d'intégration continue.
- Sur certains projets, des bugs inacceptables et bloquants sont parfois poussés en production, à cause de l'absence de tests unitaires et fonctionnels sur les parcours principaux de l'application.
- Le style du code et sa pertinence souffrent d'une qualité très variable. Aucun processus d'uniformisation et de prévention n'ont été mis en place.
- Créer un environnement de développement prêt à être codé est un processus trop long, qui limite notre capacité à faire intervenir des nouveaux développeurs sur nos projets.
- Nous disons haut et fort que nous pratiquons l'agilité, mais la réalité nous pousse souvent à dévier vers un modèle plus conventionnel. C'est parce que les clients n'acceptent pas facilement cette méthode de travail où le montant final d'un projet n'est pas connu à l'avance.
- Nous n'avons que très peu de vision sur la capacité de charge de nos serveurs. Il est critique qu'on puisse surveiller nos serveurs et planifier notre besoin d'échelonnage.
- Nous pensions gagner du temps en nous basant uniquement sur ce que l'on sait faire, et c'est vrai à court terme ou pour les petits projets. L'impact sur les moyens et gros projets est en revanche aujourd'hui très visible.

## Solution

Un nouveau projet vient d'être signé, le projet One, et c'est l'occasion parfaite pour appliquer vos recommandations et faire entrer l'entreprise dans une nouvelle ère d'automatisation continue entre Dev et Ops.

Ce projet sera composé d'un frontend React, d'une admin React, connectée à une API Symfony.

En tant que DevOps, vous n'aurez pas à coder le projet. Les développeurs s'en chargent. En revanche, vous devrez construire et coder toutes les étapes qui permettent au développeur de commencer sa première ligne de code métier dans un environnement autogéré qui lui fera gagner du temps.

Le projet One est donc un projet pilote qui servira de modèle pour tous les prochains. Les développeurs suivront toutes vos recommandations, ainsi vous ne pratiquez pas seulement le DevOps. **Vous l'enseignez.**

Pour convaincre la direction, vous devrez justifier tous vos choix en citant les avantages en termes de productivité ou de qualité.

Vous devez configurer un projet automatiquement testable, validé ou refusé à chaque commit sur les branches de son projet Git. Le projet est composé d'un frontend React et d'un backend Symfony 6. Toutes les spécifications sont précisées plus bas dans les contraintes.
Le déploiement doit être automatisé au maximum, et sécurisé par les tests en utilisant tous les outils disponibles. C'est une des étapes fondamentales pour l'intégration continue.

Votre rôle est d'apporter tout le confort qui permettra aux développeurs de démarrer rapidement le développement de l'application tout en suivant des conventions que vous aurez établies. Vous connaissez sans doute la pratique "Convention plutôt que configuration". Essayez de l'appliquer partout où c'est possible. Vous décidez de la configuration pour que les développeurs se contentent de suivre des conventions.

Vous devrez fournir en fin de semaine des réponses cohérentes et personnalisées sur les sujets suivants : 

- Quels sont les bénéfices évalués de votre travail chez RealCompany ?
- Comment avez-vous optimisé le travail des développeurs de l'application ou amélioré leur confort de travail ? Et celui des Administrateurs Systèmes ?
- Quelles sont vos recommandations pour le développement ?
  - En termes de tests
  - En termes de collaboration
- Quel rapport avec Agile ?
  - A-t-on besoin d'Agile pour passer à l'ère du DevOps ?
  - Comment vendre Agile à nos clients ?

## Contraintes

Vos seules contraintes sont imposées par le stack choisi par les développeurs en charge du projet. Nous savons à l'avance que ce stack évoluera au fil des jours, donc il faut rester le plus flexible possible. Pour tout le reste, vous avez carte blanche ! 
Je vous colle ici leur demande :

"Nous avons besoin de pouvoir déployer deux applications web indépendantes pour le back et le front, respectivement avec Symfony 6 + EasyAdmin, et React ou Next JS."

Après avoir creusé un peu, une liste plus complète a été établie : 

### Serveur
- PHP-FPM
- Nginx 

### Langages / Technos requises 
- PHP8
- NodeJS
- Composer

### Base de données
- MariaDB
- Adminer 

### Back end 
- Symfony Framework 6

### Front end 
- React/Next JS

## Rédaction de documentation

Vous devez bien sûr documenter votre processus afin de fournir à RealCompany une vue d'ensemble et détaillée sur la nouvelle façon de travailler. Les développeurs de RealCompany seront alors capables de se débrouiller avec votre documentation sur les questions suivantes : 

- Comment ça marche ??
- Comment générer un environnement de développement identique partout ?
- De quelle façon GIT est-il lié à l'intégration continue ?
- À quoi sert Docker ? Et Docker Compose ? Un diagramme aiderait
- De quelle façon faut-il pousser sur GIT ? (décrire un workflow)
- Comment déployer en production ?
- Comment s'y prendre pour faire de la TDD ?
- Quels sont les nouveaux outils et processus à adopter ?

RealCompany compte sur vous pour passer à l'ère du DevOps.
