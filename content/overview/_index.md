+++
title = "Introduction"
description = "We think the internet can’t be saved."
sort_by = "weight"
+++

Nous pensons qu'Internet ne peut pas être sauvé. Au rythme où vont les choses, les conglomérats contrôleront toujours nos applications et services, car nous ne pouvons, ni ne savons plus les exécuter nous-mêmes.

Le seul moyen de sortir de cette situation désastreuse est d'utiliser une toute nouvelle plate-forme détenue et contrôlée par ses utilisateurs.

Urbit est un nouveau système d'exploitation et un réseau peer-to-peer de conception simple, conçu pour durer éternellement, et détenu à 100% par ses utilisateurs. Sous le capot, Urbit est une stack de logiciels reprenant tout à zéro et qui est suffisamment compacte pour qu'un développeur individuel puisse la comprendre et la contrôler complètement.

Nous avons construit cette nouvelle stack de logiciels pour donner aux gens un outil intégré unique pour communiquer et créer des communautés, un outil auquel ils peuvent faire confiance, contrôler et étendre à leur guise. Nous voulons éliminer la terrible expérience utilisateur de la "frankenstack" actuelle d'applications et de services que nous utilisons tous aujourd'hui.

Urbit est conçu pour devenir un outil de productivité efficace et personnalisable pour les collaborateurs, et un outil de communication doux et non invasif pour les amis et les familles.

Cela semble probablement fou, alors soyons concrets et parlons (1) d'Urbit en tant que technologie et (2) d'Urbit en tant qu'expérience utilisateur.

Technologie {% .font-bold .subpixel-antialiased .pt-8 %}

Techniquement, Urbit est composé de deux composants principaux : Urbit OS et Urbit ID. 
Les deux sont entièrement open source et sous licence MIT.

{% div className="flex justify-between space-x-4" %}
{% div %}
![](https://media.urbit.org/site/understanding-urbit/uu-intro-2.svg) 
{% /div %}

{% div %}
![](https://media.urbit.org/site/understanding-urbit/uu-intro-3.svg)
{% /div %}

{% /div %}

**Urbit OS** Urbit OS est une nouvelle stack de logiciels soigneusement conçue : une machine virtuelle, un langage de programmation et un noyau conçus pour exécuter des logiciels pour un individu.

Urbit OS est un programme qui s'exécute sur presque tous les serveurs de cloud ainsi que sur la plupart des ordinateurs portables et de nombreux téléphones : n'importe quel outils fonctionnant avec Unix et une connexion Internet. Urbit OS est complètement isolé du système sur lequel il s'exécute, similaire à WASM ou  JVM. Nous l'appelons parfois un “OS superposé”.

Dans un monde Urbit, chaque personne a son propre nœud Urbit OS, ou « urbit ». Votre urbit est sécurisé et privé pour vous et entièrement sous votre contrôle. Lorsque vous souhaitez vous connecter avec d'autres, vous vous connectez directement à leur urbit, plutôt que de passer par un service centralisé.

Si vous êtes curieux de plonger encore plus profondément dans Urbit OS, n'hésitez pas à passer ces parties et sauter à la prochaine partie.

**Urbit ID** Urbit ID est un système d'identité et d'authentification spécialement conçu pour fonctionner avec Urbit OS. Lorsque vous démarrez ou vous vous connectez à Urbit OS, vous utilisez votre Urbit ID.

Votre Urbit ID est un nom court et mémorable (comme ~ravmel-ropdyl) qui est un nom d'utilisateur, une adresse réseau et un portefeuille crypto tout-en-un. Il est enregistré sur une blockchain, vous le possédez avec une clé et personne ne peut vous le retirer. Les Urbit ID sont des propriétés cryptographiques.

Les Urbit ID ne sont pas de l'argent, mais ils sont rares, donc chacun a un coût. Cela signifie que lorsque vous rencontrez un étranger sur le réseau Urbit, il a investi dedans et, de fait, est moins susceptible d'être un bot ou un spammeur.

Expérience {% .font-bold .subpixel-antialiased .pt-8 %}

Nous voulons qu'Urbit soit une interface unique et simple répondant à tous les besoins de votre vie numérique.

Au fil des ans, Urbit a été construit avec l’aide de la communauté en tant que projet open source. Tout le monde peut rejoindre le réseau et découvrir ce que nous faisons. C'est un peu comme s'inscrire sur IRC au début des années 90.

Début 2020, Tlon a sorti Urbit OS 1, désormais nommé Landscape : une interface de base pour la communication de groupe. Ce fut notre première interface complète. Landscape est un outil pour discuter, partager des notes et des liens, et rester connecté.

Au fil du temps, Urbit deviendra un système capable de rassembler tous nos différents modes de communication : chat, paiements, documents, images, données biométriques. Nous voulons que les individus et leurs communautés puissent à la fois contrôler effectivement leur logiciel, via le code source tout en utilisant une interface simple.

Nous voulons laisser derrière nous un monde d'applications et de services pour un monde où nous pouvons tout rassembler en un seul endroit. Ce faisant, les utilisateurs ordinaires pourront créer des environnements numériques personnalisés pour leurs amis et leurs communautés.

Pour voir comment nous allons y arriver, passons en revue ces deux nouvelles technologies individuellement, Urbit OS et Urbit ID. Nous parlerons ensuite de notre vision de l'avenir et de la manière dont nous y parviendrons.

Pour les techniciens, il est important de noter qu'Urbit en tant que stack de logiciel, ne doit en aucun cas être forcément utilisé ensemble. Vous n'aimez pas notre client ? N'hésitez pas à créer le vôtre. Vous n’aimez que le système Urbit ID ? Pas de problème - utilisez-le !

En fin de compte, nous pensons que les nouvelles technologies sont plus susceptibles d'être adoptées si elles peuvent offrir une bien meilleure expérience utilisateur. C'est donc sur cela que nous nous concentrons.
