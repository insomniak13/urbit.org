+++
title = "Obtenir une planète"
weight = 1
description = "Comment acquérir une planète, ou une Urbit ID"
tag = "additional"
+++

### Qu’est-ce qu’une planète ?

Les planètes sont un type d'[Urbit ID](https://urbit.org/overview/urbit-id) qui permet aux individus d'accéder à long terme au réseau Urbit.

### Où trouver une planète ?

Il y a plusieurs façons d'obtenir votre propre planète :

- Recevoir une invitation d'un ami (ou d'un étranger)
- Acheter une planète, y compris l'hébergement, auprès d'un hébergeur
- Configuration manuelle et hébergement d'une planète achetée sur une place de marché tierce

### Hébergeurs {% #Hébergeurs %}

Les hébergeurs vous vendront souvent une planète et l'exécuteront pour vous. Cette option est très simple, mais coûtera probablement des frais réguliers.

Urbit est conçu pour être portable. Cela signifie que si vous vous inscrivez auprès d’un hébergeur maintenant, mais vous souhaitez plus tard quitter votre hébergeur et exécuter votre Urbit vous-même, vous devriez pouvoir travailler avec eux pour obtenir toutes vos données et relancer votre planète sans rien perdre.

L'hébergement signifie que vous faites confiance à votre fournisseur pour vos données, mais tant que vous avez votre planète, vous êtes toujours propriétaire de votre identité.

Les hébergeurs actuels sont :

- [UrbitHost](https://urbithost.com/)
- [escape pod store](https://www.escapepod.store/)
- [Third Earth](https://third.earth/)
- [Tlon Corporation](https://tlon.io/)

### Acheter une planète

Il existe de nombreux endroits pour acheter une planète en utilisant soit des crypto-monnaies ou du fiat.

Les planètes sur Layer 1 sont les plus disponibles via les places de marché, mais elles peuvent être coûteuses en raison des frais de gas Ethereum. Vous aurez besoin d'un portefeuille Ethereum tel que Metamask pour acheter ces planètes, et vous devrez plus tard vous connecter à Bridge avec votre portefeuille pour configurer votre planète.

Les planètes sur layer 2 ne nécessitent pas la gestion d’un portefeuille crypto, mais sont actuellement moins facilement disponibles sur les places de marché.

Ne vous inquiétez pas, les deux options fonctionnent de la même manière sur le réseau.

Voici quelques-uns des endroits où vous pouvez acheter des planètes :
{% table .w-full .my-4 %}
* L1 Planet Markets
* L2 Planet Markets
---
*
    - [Urbitex](https://urbitex.io)
    - [Urbit.live](https://urbit.live)
    - [Urbit.me](https://urbit.me)
* 
    - [azimuth.shop](https://azimuth.shop)
    - [lanlyd](https://lanlyd.net/)
    - [~mocbel house](https://mocbel.house)
    - [\_networked subject](https://subject.network)
    - [Planet Market](https://planet.market)
    - [Wexpert Systems](https://wexpert.systems)
{% /table %}

{% callout %}

**Les planètes sur Layer 2**

En savoir plus avec les planètes sur Layer 2 à la page du manuel de l'utilisateur sur ce sujet.

{% /callout %}


### Récupérez votre planète

L’invitation pour récupérer votre planète se présente sous l’une de ces deux formes :

1. La première est une invitation par e-mail avec un Urbit ID et un Master Ticket.
2. La seconde, récemment mis à disposition via notre [solution L2](https://operators.urbit.org/manual/id/layer-2-for-planets), est un code d'activation ou un lien à activer sur [Bridge](https://bridge.urbit.org/), qui peut être considéré comme un outil de gestion de compte Urbit.

![](https://media.urbit.org/site/getting-started/Server-setup-1.jpg)

En cliquant sur le lien pour activer une planète sur Bridge, vous serez redirigé vers la page qui générera un Master Ticket pour vous. Suivez les instructions qui vous permettront de télécharger une copie de votre passeport : votre Master Ticket, un proxy de gestion, et votre fichier clé. Stockez votre Master Ticket et votre proxy de gestion dans un endroit sûr, conservez le fichier clé et passez à l'étape suivante.

{% callout %}

**Revendiquer des planètes sur L1**

Si vous avez acheté une planète sur L1, vous n’aurez pas besoin de la récupérer, car vous la possédez déjà en tant que NFT. Connectez-vous simplement à Bridge en utilisant Metamask ou le portefeuille de votre choix.

{% /callout %}


### Utiliser Bridge pour récupérer votre fichier clé

Maintenant que vous avez votre planète, vous pouvez créer votre fichier clé (par exemple `sample-palnet.key`), qui est la signature cryptographique nécessaire pour crypter et déchiffrer les messages sur le réseau P2P d'Urbit.

- **Récupérez une Planète sur L2**
Si vous avez réclamé votre L2 Planet, vous devriez déjà avoir téléchargé votre Passeport, qui contient votre Master Ticket et votre fichier clé.
- **Master Ticket Holders**
Si vous n’avez pas téléchargé votre passeport, mais que vous possédez un Master Ticket, vous pouvez simplement vous connecter avec Bridge en utilisant l’option Master Ticket avec votre nom de planète et votre mot de passe Master Ticket. Cliquez sur la case ID en bas de la page pour ouvrir la page ID, puis cliquez sur le bouton **Télécharger le passeport**, contenant votre fichier clé.
- **Acheteurs de Planet sur L1** 
Connectez-vous à Bridge avec votre portefeuille Ethereum en utilisant Metamask ou le portefeuille de votre choix avec WalletConnect. Cliquez sur la case “OS” en bas de la page pour ouvrir la page OS, puis cliquez sur le bouton télécharger le fichier clé.


### Prochaines étapes

Vous avez votre planète ?

Installez et exécutez-la avec l'une de ces options :

- Laissez un [hébergeur](https://urbit.org/getting-started/hosted) faire le travail pour vous.
- Pour les super utilisateurs, consultez le [guide d'installation en ligne de commande](https://urbit.org/getting-started/cli) et lancez votre urbit depuis le terminal.
- Si vous avez un peu d'expérience en serveur Linux, le [guide d'hébergement cloud](https://operators.urbit.org/manual/running/hosting) vous aidera à configurer Urbit sur un VPS Digital Ocean, afin que vous puissiez y accéder de n'importe où.

Rappelez-vous, votre planète est la vôtre et vous pouvez toujours changer la façon dont vous gérez votre urbit à l'avenir.
