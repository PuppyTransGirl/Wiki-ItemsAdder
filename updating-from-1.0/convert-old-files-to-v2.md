# Convertir les anciens fichiers vers la v2



{% hint style="danger" %}
**Il est recommandé de commencer sur un tout nouveau monde et de ne pas utiliser l'ancien car les convertisseurs fonctionnent mais sont expérimentaux.**
{% endhint %}

{% hint style="warning" %}
## Si vous n'avez créé aucun item personnalisé et que vous utilisez uniquement mes items, veuillez sauter ce tutoriel, vous n'avez pas besoin de convertir les fichiers. Mais assurez-vous de suivre le tutoriel "Convert old items ingame"

Vous devez simplement renommer le dossier ItemsAdder en ItemsAdder_backup, supprimer l'ancien plugin et installer la version 2.0
{% endhint %}

### Qu'est-ce qui a changé ?

ItemsAdder v2 est une réécriture complète de la version précédente d'ItemsAdder. Cela a changé CHAQUE configuration et chaque chemin/propriété/format de fichier du resourcepack. \
C'est comme un tout nouveau plugin, avec plus de fonctionnalités, mieux optimisé et plus facile à maintenir.

### Comment puis-je convertir les anciens fichiers de configuration et les resourcepacks vers le nouveau format ?

Vous devez suivre ce tutoriel :D

{% hint style="warning" %}
**Veuillez vous assurer de suivre le tutoriel attentivement**, ne soyez pas pressé ou vous pourriez faire des erreurs et mettre plus de temps à faire la conversion.
{% endhint %}

{% hint style="danger" %}
Faites cette opération uniquement sur un serveur de test local sur votre PC pour ne pas faire d'erreurs et risquer de perdre des données.
{% endhint %}



## Étape 1

* Désactivez l'ancien plugin ItemsAdder de votre serveur de test (supprimez le fichier ItemsAdder.jar et arrêtez le serveur)
* Téléchargez le [Convertisseur ItemsAdder](https://www.spigotmc.org/resources/itemsadder-converter.75952/) et mettez-le dans le dossier plugins de votre serveur de test.

## Étape 2 - copier les configs des items

* Ouvrez le dossier **plugins** du serveur et créez un **nouveau** dossier nommé **ItemsAdder_old**
* Ouvrez votre **ANCIEN** dossier ItemsAdder et copiez les fichiers du dossier items **(voir capture d'écran)**

![](<../.gitbook/assets/image (6).png>)

* Collez le dossier **items** dans **ItemsAdder_old**

![](<../.gitbook/assets/image (5).png>)

## Étape 3 - copier le resourcepack

* Créez un **nouveau** dossier nommé **pack** à l'intérieur de **ItemsAdder_old**
* Extrayez le **CONTENU** exact de votre ancien fichier **.zip** de resourcepack à l'intérieur du nouveau dossier **pack**

![](../.gitbook/assets/image.png)

## Étape 4 - Préparer le nouveau ItemsAdder 2.0

{% hint style="info" %}
**Si vous ne vous souciez pas de mes items personnalisés et que vous ne voulez pas les obtenir, mais juste créer vos propres items :**

ouvrez `config.yml` dans le dossier **ItemsAdder** (qui vient d'être généré par la version **ItemsAdder 2.0**) et définissez ces propriétés sur false.

```
extract-default-items: false
extract-default-resources: false
```

Ensuite, supprimez tous les dossiers à l'intérieur de `ItemsAdder\data\items_packs\...` **mais gardez** le dossier `minecraft`.\
Et supprimez tous les dossiers à l'intérieur de `ItemsAdder\data\resource_pack\assets\...` **mais gardez** le dossier `minecraft`.

Vous devez également supprimer mes catégories de `ia_gui.yml`
{% endhint %}

## Étape 5 - préparer le convertisseur

{% hint style="success" %}
Le convertisseur ItemsAdder sautera automatiquement mes items personnalisés, il créera donc un pack qui contient uniquement les items que vous avez créés vous-même.
{% endhint %}

#### Configurez-le avant de lancer la conversion

* Ouvrez le fichier `plugins/ItemsAdderConverter/config.yml`
* Modifiez le `namespace` avec un nom personnalisé. Vous pouvez choisir le nom de votre serveur ou ce que vous voulez. Par exemple, certains de mes items ont le **namespace** "`itemsadder`", donc vous pourrez utiliser une commande comme `/iaget itemsadder:ruby` (mais comme vous pouvez le remarquer, j'ai créé plus de namespaces dans le nouveau plugin, afin de séparer les fonctionnalités)

## Étape 6 - conversion

Pour lancer la conversion :

* démarrez le serveur
* attendez qu'il finisse de tout charger
* utilisez la commande `/itemsadderconverter:iaconvert`
* **ATTENDEZ** QU'IL **FINISSE**
* Vérifiez s'il renvoie une erreur
* **Arrêtez** le serveur **uniquement** quand il a **fini de convertir**.

## Installation d'ItemsAdder v2

{% hint style="danger" %}
* **Arrêtez** le serveur
* Veuillez vous assurer d'avoir **SUPPRIMÉ l'ancien ItemsAdder.jar**
* Si vous avez l'ANCIEN dossier ItemsAdder dans les plugins, veuillez le **RENOMMER** EN **ItemsAdder_backup** ou **supprimez-le** si vous avez déjà des sauvegardes.
* **Téléchargez** ItemsAdder 2.0 et mettez-le dans votre dossier plugins
* **Démarrez** le serveur
* Attendez qu'ItemsAdder 2.0 finisse de créer ses fichiers
* Si vous obtenez une erreur, veuillez la lire et vérifier si vous avez fait quelque chose de mal (dépendance manquante, mauvaise version de Spigot...) et réessayez cette étape.
* (IGNOREZ si vous obtenez une erreur concernant l'URL du resourcepack, c'est normal car vous le configurerez plus tard)
* Ouvrez le dossier **ItemsAdder_converted** qui vient d'être créé
* copiez les deux dossiers `items_packs` et `resource_pack` dans le nouveau dossier `ItemsAdder` (remplacez tous les fichiers si demandé)
* **Redémarrez** le serveur
  {% endhint %}

## Dernières tâches

* supprimez les dossiers `ItemsAdderConverter`, `ItemsAdder_converted`, `ItemsAdder_old`.
* supprimez `ItemsAdderConverter.jar`

## Configuration du Resourcepack

Veuillez suivre ce tutoriel rapide pour activer le resourcepack :

{% content-ref url="../plugin-usage/resourcepack-hosting/resourcepack-self-hosting.md" %}
[resourcepack-self-hosting.md](../plugin-usage/resourcepack-hosting/resourcepack-self-hosting.md)
{% endcontent-ref %}



****