+++
title = "Urbit OS"
description = "Ce à quoi Urbit devrait ressembler pour un utilisateur quotidien"
weight = 2
[extra]
image = "https://media.urbit.org/site/understanding-urbit/intro/intro-5.jpg"
+++

Pour la plupart, nous utilisons nos ordinateurs portables simplement comme points d'accès aux services de MEGACORP. Nos téléphones sont les mêmes. Ces services sont incroyables et pratiques. Mais pour cette commodité, nous avons échangé le contrôle, la propriété et la vie privée. La façon dont nous vivons nos vies numériques nous échappe complètement.

Aujourd’hui, les monopoles MEGACORP conservent leurs contrôles grâce à un avantage technique central : ils rendent le côté serveur utilisable.

Urbit OS est conçu pour briser ces monopoles en ce point de contrôle central. Urbit OS rend le côté serveur utilisable par les individus sans que les MEGACORP aient besoin d'exécuter leur software.

Nous avons déjà vécu cela auparavant. En 1974, un ordinateur était une unité centrale de la taille d'une pièce et était partagé par des centaines de personnes. En 1984, un ordinateur avait la taille d'un bureau et tout le monde avait son propre ordinateur. Le PC était plus flexible et plus amusant, et c’est pour cela qu’il a donc gagné une importante marge. Puis, avec la montée d'Internet, la flexibilité du PC est devenue peu à peu hors de propos.

Aujourd’hui, nous revenons plus ou moins au modèle de multipropriété des années 1970. Urbit OS est le PC auquel est l'unité centrale de MEGACORP. Il est plus souple, plus amusant et, surtout, prêt à capturer la créativité quotidienne de l’individu.

Parlons de la façon dont nous pensons que nous allons y arriver d’un point de vue technique, et de notre vision de l’utilisation d’Urbit.

Architecture {% .font-bold .subpixel-antialiased .pt-8 %}

Urbit OS est une toute nouvelle stack de logiciels soigneusement conçue : une machine virtuelle (VM), un langage de programmation et un noyau conçus pour exécuter des logiciels pour les utilisateurs. Urbit OS est un programme qui s’exécute sur presque tous les serveurs cloud, la plupart des ordinateurs portables et de nombreux téléphones : tout avec Unix et une connexion Internet.

![](https://media.urbit.org/site/overview/overview-os.png)

La principale chose à comprendre à propos de notre “overlay OS”, comme nous l’appelons, est que la fondation est une fonction simple et unique. Cette fonction est la machine virtuelle Urbit OS. Nous l’appelons «Nock». L'ensemble d’Urbit OS se compile jusqu'à Nock, et Nock contient seulement 33 lignes de code.

Dans le même esprit, Nock est similaire à WASM ou à JVM : il s’agit d’un code machine, uniforme pour tous les vaisseaux Urbit. Des fondations figées font de belles fonctionnalités :

L'état de votre Urbit OS est une pure fonction de son historique d'événements. Il est possible de l’analyser, l’inspecter, et le reproduire. Vous pouvez lui faire confiance. Écrire des applications décentralisées devient beaucoup plus simple que dans l'ancien monde, puisque chaque nœud calcule exactement de la même façon. Toute la stack Urbit OS, du langage de programmation aux applications, peut-être mise à jour via le réseau. Pour les utilisateurs ordinaires, cela ne nécessite pratiquement pas d'administration système.

Étant donné que Nock est un protocole de calcul en lui-même, deux nœuds du réseau Urbit peuvent facilement partager des données, communiquer et connecter leurs logiciels. Les systèmes du XXe siècle ne pourraient jamais le faire sans un MEGACORP agissant comme intermédiaire.

En plus de cette toute petite VM, nous avons construit un langage de programmation auto-hébergé, purement fonctionnel, un noyau écrit dans ce langage et un ensemble de modules du noyau qui répondent à tous les besoins de l'informatique personnelle. Plus précisément : un système de fichiers, un système de construction, un environnement de test, un stockage secret, un serveur web, un pilote de terminal et un protocole réseau.

Cela semble être beaucoup, mais l'ensemble de la stack est incroyablement compact. L'ensemble du système enregistre environ 50K lignes de code. Nous avons vu des développeurs seuls comprendre entièrement ceci. Quelle est la dernière personne que vous avez rencontrée qui comprenne l’intégralité de leur ordinateur ? Urbit OS est comme la Porsche 911 de 1968 des systèmes d'exploitation : extrêmement simple, élégant et construit pour l'individu.

Mais pourquoi avons-nous construit toute cette technologie ?

Tout d'abord, pour offrir une meilleure expérience utilisateur. Urbit OS seul n'est qu'une nouvelle layer pour l'informatique personnelle dans le cloud. Mais avec cette nouvelle layer, nous ouvrons la possibilité de construire une interface totalement unifiée permettant à des gens de calculer dans le cloud.

Dans une perspective plus large, il est clair que l’informatique connectée est importante et qu’elle est là pour durer. Nous voulons simplement qu’elle soit aussi calme, simple et fiable que possible, et nous ne pensons pas que cela puisse se faire avec la technologie existante.

L'ensemble d'Urbit est conçu pour fonctionner comme une seule stack, et nous pensons que construire un produit utile est le meilleur moyen de faire mûrir le système dans son ensemble. Cela dit, chaque composant de ce système peut être utilisé séparément. Vous n’aimez pas notre client ? C’est ok, vous pouvez construire votre propre client. Vous ne voulez pas utiliser Urbit OS ? Aucun problème, vous pouvez utiliser Urbit ID comme système d'authentification pour un autre OS, ou pour n'importe quoi, vraiment.
