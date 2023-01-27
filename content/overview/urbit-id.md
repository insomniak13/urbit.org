+++
title = "Urbit ID"
description = "Un aperçu du système Urbit ID"
weight = 3
[extra]
flatten_pagination = "true"
hide_next_title = "true"
hide_previous_title = "true"
image = "https://media.urbit.org/site/understanding-urbit/urbit-id/urbit-id-cards%402x.png"
+++

En supposant que Urbit OS soit assez simple pour un utilisateur ordinaire à posséder et à exploiter, comment se connectent-ils ? Comment les gens s'identifient-ils sur ce nouveau réseau ? Quand les gens veulent s’échanger des données, des fichiers et des messages, comment s'y prennent-ils ? Et comment prévenir les spams ?

Urbit ID est la réponse à toutes ces questions. Urbit ID est une infrastructure d’adressage décentralisée et de clé publique conçue pour Urbit OS.

Parlons d’abord de ce qu’est une Urbit ID et de ce qu’elle fait. Ensuite, nous aborderons nos objectifs de conception et le fonctionnement général du système.

![](https://media.urbit.org/site/understanding-urbit/urbit-id/urbit-id-cards%402x.png)

Résumé {% .font-bold .subpixel-antialiased .pt-8 %}

Votre Urbit ID est un court nom de quatre syllabes telles que ~ravmel-ropdyl que vous possédez avec un mot de passe maître de huit syllabes suivant le format ~palfun-foslup-fallyn-balfus. Ce nom et la clé vous permettent de vous connecter à Urbit OS, et elle est utilisée pour crypter les paquets que vous envoyez sur le réseau Urbit. Bientôt, ce sera également une master key permettant la détention et l'envoi de Bitcoin et d'autres cryptocurrencies. Votre Urbit ID et votre mot de passe vous appartiennent comme tous les autres actifs cryptographiques. Personne ne peut vous les enlever (assurez-vous juste de garder la clé en sécurité).

Le registre Urbit ID est en direct et déployé sur la blockchain Ethereum. Urbit ID n'est pas spécifiquement marié à Ethereum - un jour, nous aimerions qu'il soit hébergé par Urbit OS lui-même. En outre, Urbit ID est le seul composant de la stack utilisant Ethereum, votre nœud Urbit OS est hébergé où vous le souhaitez. La fonction première du registre Urbit ID est de savoir à qui appartient quoi, de préciser quelles clés sont associées à quels noms et de faire respecter les règles de répartition des adresses.

Chaque Urbit ID n'est en faite qu'un nombre. À partir de ce nombre, nous générons un nom prononçable et un sigil visuellement identifiable. ~dalwel-fadrun est 3,509,632,436, par exemple.

Les Urbit ID sont distribuées par un arbre de sponsors. Au sommet de l'arbre se trouvent 2^8^ (256) galaxies. Chaque galaxie émet 2^8^ étoiles, soit un total de 2^16^ (65K). Chaque étoile peut alors émettre 2^16^ planètes, soit 2^32^ (~4B). Comme vous vous en doutez, chaque planète émet 2^32^ lunes.

![](https://media.urbit.org/site/overview/overview-id.png)

Vous pouvez également appeler les étoiles “nodes d’infrastructure” et les galaxies “nodes de gouvernance”, car ce sont des noms plus descriptifs pour leurs rôles. Les étoiles aident à acheminer les paquets, un peu comme un ISP. Et les galaxies sont un peu comme les serveurs racine DNS ou les membres de l'ICANN. La différence, bien sûr, est que les Urbit ID sont détenus à travers un protocole cryptographique par de nombreuses personnes différentes et acquièrent une réputation indépendante.

Conception {% .font-bold .subpixel-antialiased .pt-8 %}

À un haut niveau, il y a trois choses importantes à comprendre à propos de la conception globale du système Urbit ID.

Premièrement, la rareté : il n'y a que 2^32 (~4B) Urbit IDs, donc elles en dérivent une valeur intrinsèque. Comme elles en dérivent une valeur intrinsèque, les gens sont moins susceptibles de les utiliser pour spammer ou abuser du réseau. Lorsque vous rencontrez un inconnu avec une Urbit ID, vous savez qu'ils sont investis dans le jeu (même sans divulguer de données personnelles dans les deux sens). Cela dit, chaque Urbit ID est purement pseudonyme, ainsi ~dalwel-fadrun, par exemple, est la preuve d'un certain intérêt dans le réseau, mais pas beaucoup plus.

Deuxièmement, la décentralisation : les Urbit ID sont distribuées par un arbre de sponsors. Chaque sponsor émet un nombre fixe d'adresses. Comme il existe de nombreux sponsors, il y a beaucoup de façons d'obtenir Urbit ID et non seulement via une autorité centrale. Une fois que vous en avez une, elle est à vous pour toujours.

Un point utile de comprendre à propos des sponsors est que même si les Urbit ID ont toujours besoin d’un sponsor, ou d’un node parent sur le réseau (principalement pour la découverte par les pairs), il est toujours possible de changer de sponsor, et les sponsors peuvent toujours rejeter les enfants. Cela signifie que les  acteurs malfaisants  peuvent être interdits et que les sponsors abusifs peuvent être ignorés. Nous pensons que cela établit un bon équilibre entre la responsabilité et la liberté.

Troisièmement, la gouvernance : les galaxies (en haut de l'arbre des sponsors) forment un Sénat pouvant améliorer la logique du système Urbit ID par un vote majoritaire. Nous pensons que la durée de vie d’Urbit ID devrait être assez longue, mais si jamais il a besoin d'être mis à jour, les galaxies peuvent voter afin d’approuver, rejeter ou proposer des modifications aux contrats. Le code est peut-être la loi, mais en fin de compte, nous reconnaissons que le jugement humain ne peut être ignoré.

L'arbre de sponsors Urbit ID n'est pas destiné à être un système social en aucune façon. Les interactions entre les personnes et les communautés sur le réseau Urbit sont peer-to-peer, entièrement organiques et totalement incontrôlées par la hiérarchie des adresses. Urbit ID n'est qu'un substrat d'authentification sur lequel construire des systèmes de réputation et de communication. (Nous avons même envisagé de renommer les étoiles et les galaxies respectivement par “infrastructure” et “gouvernance”.)

Votre relation avec votre sponsor devrait ressembler à celle de votre ISP ou d'un fournisseur de services publics : une relation passive et non invasive. Si ce n’est pas à votre goût, il est facile de passer à un nouveau sponsor.

Digital Land {% .font-bold .subpixel-antialiased .pt-8 %}

Les Urbit ID sont des propriétés, et nous considérons l'ensemble du registre des Urbit ID comme un vaste territoire numérique.

![](https://media.urbit.org/site/understanding-urbit/urbit-id/urbit-id-sigils%402x.png)

La rareté de l’infrastructure d’adresse Urbit ID lui donne de la valeur, et cela contribue à amorcer la décentralisation même lorsque le projet est jeune. Une vaste distribution est importante : pour qu'Urbit puisse durer longtemps et réussir en tant qu'infrastructure neutre, il doit être possédé et contrôlé par un ensemble de personne le plus varié possible. 

Lorsque nous avons lancé le système Urbit ID, en janvier 2019, quelques milliers d’holders d'étoiles et de galaxies différents agissants en tant que gardiens de cette terre numérique. Depuis lors, ce nombre n'a cessé de croitre.

En fin de compte, nous voulons que votre Urbit ID ressemble à la clé d’une civilisation. Si votre Urbit ID était un élément matériel, vous pourriez le toucher pour déverrouiller une porte, et le brancher à n'importe quel ordinateur pour vous connecter. Votre Urbit ID devrait être un magnifique objet unique et à la fois une adresse et un portefeuille. C’est la clé d’un club secret et le ticket pour votre vie numérique.

Si vous êtes curieux de voir exactement comment ce système fonctionne, le code est bien sûr [open source](https://github.com/urbit/urbit). Y compris le code source de notre [système de dénomination phonémique](https://github.com/urbit/urbit-ob/blob/master/src/internal/co.js) et les [représentations visuelles](https://github.com/urbit/sigil-js). Il y a même un [plugin Figma](https://github.com/urbit/sigil-figma-plugin) pour les utiliser. Il y a aussi une interface pour interagir avec Urbit ID dont la [source est ouverte](https://github.com/urbit/bridge). Comme le registre Urbit ID est active et déployée, vous pouvez même la [regarder on-chain](https://github.com/urbit/azimuth#live-contracts).

