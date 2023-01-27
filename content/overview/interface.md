+++
title = "Interface"
description = "What Urbit feels like to an everyday user"
weight = 4
[extra]
+++

Nous avons construit Urbit OS + Urbit ID pour être la stack de logiciels à l'échelle humaine pour l’informatique dans le cloud. Ce système n'a pas été conçu uniquement pour être une nouvelle infrastructure, il a été conçu pour que nous puissions créer de meilleures interfaces et que les gens puissent utiliser Urbit sans n’avoir à connaître la technologie. Pour qu'Urbit compte réellement, nous devons aller de la VM à l'UI.

Landscape {% .font-bold .subpixel-antialiased .pt-8 %}

Pour traiter le composant d'interface de la stack de logiciels, Tlon a créé Landscape : une interface simple, douce et basée sur un navigateur, pour créer des communautés numériques.

Aujourd'hui, une fois que vous avez un nœud Urbit OS opérationnel, vous pouvez accéder à Landscape à partir d'un navigateur de bureau ou mobile pour discuter, écrire, et partager avec un groupe d’amis, de manière pseudonyme.

![](https://media.urbit.org/site/understanding-urbit/uu-interface-3.png)

Landscape n'est en aucun cas la seule interface possible pour Urbit OS + Urbit ID, mais c'est celle dont nous avons le plus besoin. À l'avenir, nous attendons avec impatience qu'il y ait de nombreuses interfaces Urbit différentes (et si vous souhaitez tenter de créer une interface, faites-le.)

Quel problème Landscape résout-il ? Commençons par la situation actuelle en matière de services cloud.

Dans le monde actuel des applications et des services, il n'y a pas de système d'exploitation dans un sens significatif. Nos communautés, nos collègues et nos vies sont répartis entre ces services, et le travail de les combiner est laissé à l'utilisateur. C'est à vous de vous souvenir de tous vos mots de passe, qui a envoyé quel message, où, quels fichiers se trouvent sur quelle plateforme, etc.

C’est ennuyeux et déroutant de basculer entre les interfaces ; vous ne pouvez pas étendre ou construire par-dessus, et la confidentialité et la sécurité ne sont pas entre vos mains. Cette expérience fragmentée, cloisonnée, et étroitement surveillée, est simplement un sous-produit du fait que d'autres personnes exécutent et contrôlent votre logiciel. Pour l'utilisateur ordinaire, le résultat est contraignant, ennuyeux et pénible à gérer. La possibilité de créativité quotidienne avec les outils avec lesquels nous sommes coincés est proche de zéro. L'ordinateur n'était-il pas censé être un vélo pour l'esprit ?

Les systèmes d'exploitation pour PC ont pris `le bureau` des années 1970 et l'ont rendu numérique. Le papier, les tiroirs et les enveloppes sont devenus des `fichiers` et des `dossiers`. C'est une grande abstraction, mais c'est ancien. Nous vivons dans un monde connecté et multijoueur ; nous avons besoin d'un système d'exploitation qui reconnaît ce monde.

Le `bureau` d'aujourd'hui est encombré d'applications et de services, de structures de données et d'interfaces. Unifier cette expérience utilisateur décousue est le problème le plus important qu'une plate-forme comme Urbit puisse résoudre. Landscape est conçu pour tout rassembler dans une interface unifiée. Sans Urbit ID + Urbit OS, cela serait impossible.

Landscape est une interface minimaliste et polyvalente permettant de réunir un groupe pour discuter, partager des liens, écrire et engager des discussions. Il est exempt de toute publicité, suivi, ou surveillance (comme c'est la norme pour tout ce qui est construit sur Urbit). Il s'agit d'un utilitaire social simplifié conçu pour une communication et une collaboration directes à haut niveau de confiance. C'est l'endroit idéal pour que les petites communautés se sentent chez elles.

Conception {% .font-bold .subpixel-antialiased .pt-8 %}

Landscape repose sur deux blocs base : les groupes et les modules. Un groupe est exactement ce à quoi il fait penser : une ou plusieurs personnes. Un module est un peu comme une application sans le verrouillage des données. Un module est juste un outil pour faire quelque chose, comme des “tâches”, des “liens” ou des “votes” partagés par un groupe.

Pour donner quelques exemples simples, un groupe de membres d’une famille peut simplement discuter et partager des photos. Un groupe de commerçants peut partager des recherches annotées, surveiller les marchés et gérer les paiements sur une blockchain.

L'idée est la suivante : toute communauté doit pouvoir personnaliser librement son environnement numérique. Pour la plupart des utilisateurs, il s'agit simplement de choisir les bons modules. Pour toute personne disposant d'un peu de temps libre, l'ajout de vos propres modules devrait être plus simple que la création d'une simple application Web.

Lorsque nous projetons ce que nous pourrons faire avec Landscape à l'avenir, il est difficile de nous voir revenir aux outils que nous utilisons aujourd'hui. Les services centralisés que nous avons maintenant sont comme les médias de diffusion : ils servent à distribuer le contenu d'un producteur à un groupe d'abonnés.

Landscape est pour tout le reste. Landscape est pour une véritable communication bidirectionnelle.
