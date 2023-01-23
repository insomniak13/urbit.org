+++
title = "Utilisation de l’application en ligne de commandes"
weight = 2
description = "Instructions d’installation pour les Super Utilisateurs."
+++

Si vous êtes un utilisateur Power User, vous pouvez exécuter Urbit runtime (Vere) en utilisant des lignes de commande. Cela peut être exécuté sur votre machine locale ou sur un serveur dans le cloud, nous ne couvrons ici que le cas local. Le runtime est ce qui interprète le code du noyau Urbit (Arvo) en commandes que votre machine spécifique (macOS ou Linux) comprend.

Notez qu'il existe un [guide d'hébergement sur le cloud](https://operators.urbit.org/manual/running/hosting) beaucoup plus complet qui explique comment configurer Urbit sur un VPS [Digital Ocean](https://www.digitalocean.com/).

Note there is a much more comprehensive [cloud hosting
guide] which walks through
setting up Urbit on a [Digital Ocean] VPS.

### 1. **Configuration système requise**

- **Processeur** : 1
- **Mémoire** : 2 Go
- **Stockage** : au moins quelques Go, 40 à 50Go de préférence
- **Réseau** : N'importe lequel

**Concernant la mémoire** : Par défaut, le runtime Urbit a besoin de 2Go de mémoire libre et ne pourra pas démarrer sans. Urbit n'en utilise généralement qu'une fraction, il est donc possible d'utiliser un fichier d'échange pour combler un manque sans dégrader les performances. Pour savoir comment configurer un fichier d'échange sous Linux, consultez ce [guide sur linuxize.com](https://linuxize.com/post/create-a-linux-swap-file/).

**Concernant le stockage** : Urbit enregistre chaque événement qu'il traite dans son [journal des événements](https://developers.urbit.org/reference/glossary/eventlog). Cela signifie qu’avec le temps, son utilisation du disque augmente. Jusqu'à ce que la troncature du journal des événements soit implémentée, il est conseillé de disposer de 40 ou 50Go d'espace disque disponible. Ainsi, vous n’aurez pas à vous soucier d'en manquer pendant une longue période. Si vous n'en avez pas autant, votre vaisseau fonctionnera toujours aussi bien, mais vous risquez de manquer d'espace dans quelques mois.

### 2. Installer Urbit
Pour télécharger le Urbit Runtime, choisissez votre système d’exploitation et exécutez les commandes fournies ci-dessous dans votre terminal. Ces commandes téléchargent les dernières versions et exécutent le code binaire sans arguments pour vous permettre d’accéder au service d’aide :

{% tabs %}

{% tab label="Linux x86_64" %}

```shell
curl -L https://urbit.org/install/linux-x86_64/latest | tar xzk --transform='s/.*/urbit/g' && ./urbit
```

{% /tab %}

{% tab label="Linux AArch64" %}

```shell
curl -L https://urbit.org/install/linux-aarch64/latest | tar xzk --transform='s/.*/urbit/g' && ./urbit
```

{% /tab %}

{% tab label="macOS x86_64" %}

```bash
curl -L https://urbit.org/install/macos-x86_64/latest | tar xzk -s '/.*/urbit/' && ./urbit
```

{% /tab %}

{% tab label="macOS AArch64" %}

```bash
curl -L https://urbit.org/install/macos-aarch64/latest | tar xzk -s '/.*/urbit/' && ./urbit
```

{% /tab %}

{% /tabs %}

Si l’exécution est réussie, vous verrez apparaître un bloc commençant par la ligne :

```
Urbit: a personal server operating function
```

### 3. Initialiser Urbit

Une instance Urbit est intrinsèquement liée à une identité unique appelée **Urbit ID**. Il existe cinq classes d'Urbit ID, mais nous n’en considérerons que deux ici : les comètes et les planètes.

**Comète :** Une comète est une identité que n'importe qui peut générer gratuitement. C'est une bonne option pour essayer Urbit. Les comètes sont limitées par le fait qu'elles ne peuvent pas être "réinitialisées", ce qui signifie que si votre urbit devient en quelque sorte cassé ou corrompu, vous devrez recommencer avec une nouvelle identité. En ce sens, ils sont impermanents.

**Planète :** Une planète est une identité permanente que vous possédez pour toujours. Les planètes sont la classe destinée aux individus. Alors qu'il existe essentiellement un nombre illimité de comètes, les planètes sont plus rares (empêchant les spams, entre autres). Cette rareté signifie qu'elles ne sont généralement pas gratuites (bien que parfois des gens sympas les donnent). Ce guide supposera que vous avez déjà acquis une planète. Si ce n'est pas le cas, vous pouvez vous référer au [guide "Obtenez une planète"](https://urbit.org/getting-started/get-planet) avant de continuer.

Suivez les instructions pour votre cas :

Dans le terminal sur lequel vous avez précédemment installé le binaire Urbit, une comète peut être générée en utilisant l’option -c :

{% tabs %}

{% tab label="Inialiser une comète " %}

Dans le terminal sur lequel vous avez précédemment installé le binaire `urbit`, une comète peut être générée en utilisant l’option `-c` :

```bash
./urbit -c mycomet
```

> `mycomet` sera le nom donné au dossier qui sera créé. 
> Vous pouvez choisir un autre nom de votre choix.

Cela peut prendre un certain temps de générer une comète (quelques minutes ordinairement, mais cela pourrait prendre plus longtemps). Lorsque c’est fait, vous serez redirigé vers l’invitation du Dojo. Le Dojo est l’interface système d’Urbit :

```
ames: live on 31337
http: web interface live on http://localhost:8080
http: loopback live on http://localhost:12321
~sampel_marzod:dojo>
```

Vous pouvez ensuite fermer votre comète en tapant `|exit` dans le dojo ou en tapant `Ctrl+D`. Lorsqu’il s’agit de la première clôture de session, le runtime sera copié dans le fichier, vous permettant ainsi de le relancer avec la commande :

```bash
./mycomet/.run
```
> Les utilisateurs Linux doivent exécuter cette commande dans une autre fenêtre du terminal pour accéder
> à leur urbit sur le port 80 chaque fois qu’ils mettent à niveau leur runtime
>  (sinon, le port 8080 sera par défaut) :
>  
> ```shell
> sudo apt-get install libcap2-bin
> sudo setcap 'cap_net_bind_service=+ep' <pier>/.run
> ```

Étant donné que les comètes sont souvent utilisées temporairement puis supprimées, les mises à jour du noyau ne sont pas activées par défaut. Si vous prévoyez d'utiliser votre comète pendant un certain temps, c'est une bonne idée d'activer les mises à jour avec la commande suivante dans le dojo :

```
|ota (sein:title our now our)
```

Enfin, la plupart des gens utilisent leur urbit via Landscape, l'interface utilisateur basée sur un navigateur. Pour accéder à Landscape, vous avez besoin de votre code de connexion Web. Vous pouvez l'obtenir en exécutant la commande suivante dans le dojo :

```
+code
```

Vous vous retrouverez avec un code qui ressemblera à `lidlut-tabweb-pillex-ridrup`.
Copiez le code reçu dans le bloc note.


{% /tab %}

{% tab label="Initialiser une planète" %}

In order to boot a planet, you need a copy of its private keys. If you got your
planet via a claim link, the passport backup `.zip` file you downloaded will
contain a file called something like `sampel-palnet-1.key`. If you don't have
the passport backup or you got your planet by another method, you can instead
login to [Bridge](https://bridge.urbit.org/), select your planet, go to the OS
section, and hit the "Download Keyfile" button.

Back in the terminal, with the `urbit` binary you installed in the previous
step, you can boot your planet with the following command (replacing
`sampel-palnet` with your own planet and pointing to the location of your
keyfile):

```bash
./urbit -w sampel-palnet -k sampel-palnet-1.key
```

This will create a folder with the name of your planet and begin booting.
It may take a while to initialize the planet (usually only a couple of minutes,
but it could take longer). When it's done, it'll take you to the dojo prompt
(the dojo is Urbit's shell):

```
ames: live on 31337
http: web interface live on http://localhost:8080
http: loopback live on http://localhost:12321
~sampel-palnet:dojo>
```

You can shut down the planet again by typing `|exit` in the dojo or hitting
`Ctrl+D`. When it's first shut down, the runtime will be copied inside the data
folder, so you can start it up again by doing:

```bash
./sampel-palnet/.run
```
> Linux users need to run this command in another terminal window to access
> your urbit on port 80 every time you upgrade your runtime (otherwise it'll 
> default to port 8080):
>
> ```shell
> sudo apt-get install libcap2-bin
> sudo setcap 'cap_net_bind_service=+ep' <pier>/.run
> ```

Most people use their urbit via Landscape, the browser-based UI. 
In order to access Landscape, you need your web login code.
You can get this by running the following command in the dojo:

```
+code
```

It'll spit out a code that'll look something like `lidlut-tabwed-pillex-ridrup`
(note this is a separate code to your master ticket). Copy the code it gives you
to the clipboard.

One last thing: The `sampel-palnet-1.key` keyfile is only needed once, when you
first boot your planet. **Now that it's booted, it's good security practice to
delete that keyfile.**

{% /tab %}

{% /tabs %}

### 4. Lorsque votre Urbit est exécuté et fonctionne, il est possible d’accéder à l’interface web Landscape avec votre navigateur. Les URL seront généralement soit `localhost` ou `localhost:8080` en fonction de votre plateforme. Pour vérifier l’adresse, vous pouvez consulter le message de démarrage dans le terminal. Vous devriez voir la ligne : 

```
http: web interface live on http://localhost:8080
```

Quelle que soit l'adresse et le port indiqués, il s’agit de celui à ouvrir dans le navigateur.

Une fois ouvert, l'écran de connexion sera affiché. Collez le code de connexion Web que vous avez copié depuis le dojo à l'étape précédente et cliquez sur "continuer". Vous serez maintenant redirigé vers votre écran d'accueil, avec des icônes pour les applications par défaut telles que Groupes, Talk et Terminal.


### 5. Mises à niveau du runtime

Lorsque de nouvelles versions du runtime Urbit (Vere) sont disponibles, vous devrez arrêter votre urbit, puis exécuter la commande suivante afin de mettre à niveau.
```
:dojo> |exit
<pier>/.run next
```
Notez que dans ce cas `<pier>` est le dossier qui a été créé lors du lancement de la première instance Urbit. Lorsque vous exécutez cette commande, votre urbit téléchargera le dernier binaire et le sauvegardera dans le fichier `.bin` du dossier pier. Vous pourrez ensuite démarrer votre vaisseau sur la version la plus récente du runtime avec la commande suivante :
```
<pier>/.run
```
> Les utilisateurs Linux doivent exécuter la commande suivante dans un autre terminal pour accéder
> à leur Urbit sur le port 80 à chaque fois qu’ils mettent à niveau le runtime 
> (sinon il se remettra à utiliser le port 8080) :
>
> ```shell
> sudo apt-get install libcap2-bin
> sudo setcap 'cap_net_bind_service=+ep' <pier>/.run
> ```

Si vous utilisez Urbit depuis un certain temps (avant la version 1.9) et que ces commandes .run ne fonctionnent pas pour vous, cela signifie probablement que vous devez vous amarrer au pier. Vous pouvez le faire avec la commande suivante :
```
./urbit dock <pier>
```
Ensuite, le `.run` devrait fonctionner comme prévu et les prochaines mise à niveau pourront être exécuté avec la commande `next`.

### Prochaine étape

Apprenez à [explorer votre urbit](https://urbit.org/getting-started/getting-around).
