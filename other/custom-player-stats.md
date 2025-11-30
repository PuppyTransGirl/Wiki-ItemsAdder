---
icon: database
---

# Les statistiques personnalisées des joueurs

## Qu'est-ce que les statistiques des joueurs ?

Ce sont des attributs personnalisés ajoutés par ItemsAdder, vous pouvez les ajouter et les lire à l'aide d'une commande spéciale : `/iaplayerstat`

Vous pouvez ensuite utiliser **PlaceholderAPI** pour les afficher n'importe où ou les lier à un HUD.\
Je l'ai fait pour créer la soif et le mana. Consultez mes [configs par défaut](https://github.com/search?q=repo%3AItemsAdder%2FDefaultPack+player_stat_name\&type=code) pour des exemples.

### Example:&#x20;

`/iaplayerstat write LoneDev soif 6`\
`/iaplayerstat read LoneDev soif float`

## Sauvegarde des statistiques des joueurs

### Fichier NBT personnalisé

Les sauvegarder dans un fichier NBT personnalisé géré par ItemsAdder, qui peut être supprimé facilement par la suite.\
Ce fichier est enregistré dans le dossier `plugins\ItemsAdder\storage\players\stats\`.

```yaml
player_stats:
  save_type: CUSTOM_NBT
```

<figure><img src="../.gitbook/assets/image (236).png" alt=""><figcaption></figcaption></figure>

### fichier player.dat

Les sauvegarder dans le fichier `player.dat` vanilla.\
Ceci est utile si vous souhaitez synchroniser votre serveur et que vous synchronisez déjà les fichiers player dat.

```yaml
player_stats:
  save_type: PLAYER_DAT
```

<figure><img src="../.gitbook/assets/image (237).png" alt=""><figcaption></figcaption></figure>
