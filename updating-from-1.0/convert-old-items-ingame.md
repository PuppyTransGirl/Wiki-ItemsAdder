# Convertir les anciens items/blocs en jeu

{% hint style="danger" %}
**Il est recommandé de commencer sur un tout nouveau monde et de ne pas utiliser l'ancien car les convertisseurs fonctionnent mais sont expérimentaux.**
{% endhint %}

{% hint style="danger" %}
Ces fonctionnalités PEUVENT causer des lags, laissez-les activées seulement pendant quelques jours et désactivez-les ensuite pour éviter des lags inutiles.
{% endhint %}

## Comment convertir automatiquement les anciens items dans vos mondes

Lorsque vous passez d'ItemsAdder 1.0 à 2.0, vous remarquerez que la plupart des items ont changé, ils ne sont donc plus les mêmes que les anciens items avant la mise à jour.\
C'est pourquoi j'ai dû coder une fonctionnalité qui remplace automatiquement les anciens items par les nouveaux. Ce processus s'exécute chaque fois qu'un joueur ouvre un inventaire dans le monde (coffres, conteneurs... mais PAS son propre inventaire).

Pour activer ceci, vous devez définir cette propriété sur true dans le fichier `converter.yml` d'**ItemsAdder 2.0**.

#### Assurez-vous de définir inventory-open: true

```
items-auto-update:
  debug: false
  inventory-open: true
```

## Comment convertir automatiquement les anciens blocs placés dans les mondes

Vous devez ouvrir `converter.yml` et faire correspondre le **model_id** de vos propres anciens blocs avec le nouveau bloc **namespaced** d'IA 2.0. Par exemple, j'ai déjà ajouté la table de correspondance des anciens blocs d'ItemsAdder 1.0 pour les convertir vers les blocs namespaced de la 2.0.

#### Assurez-vous de définir enabled: true

```
blocks:
  enabled: true
  debug: false
  conversion-map:
    "1": "itemsadder:ruby_block"
    "2": "itemsadder:crystal_block"
    "3": "itemsadder:spinel_block"
    "4": "itemsadder:turquoise_block"
    "5": "itemsadder:aqua_aura_block"
    "6": "itemsadder:amethyst_block"
    "7": "itemsadder:amethyst_prism_block"
    "8": "itemsadder:crying_obsidian"
    "9": "itemsadder:nice_stone"
    "10": "itemsadder:nice_wood"
    "11": "itemsadder:modern_stone"
    "12": "itemsadder:modern_sandstone"
    "13": "itemsadder:modern_quartz"
    "14": "itemsadder:ruby_ore"
    "15": "itemsadder:spinel_ore"
    "16": "itemsadder:turquoise_ore"
    "17": "itemsadder:aqua_aura_ore"
    "18": "itemsadder:amethyst_ore"
    "19": "itemsadder:bronze_ore"
    "20": "itemsadder:mysterious_ore"
    "21": "itemsadder:end_ore"
    "22": "itemsadder:restoration_table"
    "23": "itemsadder:customization_table"
    "24": "itemsadder:iron_dirt_ore"
    "25": "itemsadder:gold_dirt_ore"
    "26": "itemsadder:coal_dirt_ore"
    "27": "itemsadder:blaze_powder_ore"
    "28": "itemsadder:nether_alchemy_ore"
```
