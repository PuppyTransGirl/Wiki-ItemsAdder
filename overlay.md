---
icon: circles-overlap
---

# Overlay

{% hint style="warning" %}
Cette fonctionnalité est destinée aux créateurs de packs de ressources experts.
{% endhint %}

Les overlays Vanilla sont supportés par ItemsAdder.

Vous pouvez créer votre propre `pack.mcmeta` et y insérer vos entrées `overlays`.\
ItemsAdder les fusionnera toutes dans le **pack.mcmeta** final de votre pack `.zip`.

#### Informations du Wiki Minecraft

{% embed url="https://fr.minecraft.wiki/w/Pack.mcmeta" %}

#### Version du format de pack pour chaque version de Minecraft

{% embed url="https://misode.github.io/changelog/?tags=pack" fullWidth="false" %}

### Exemple

`contents/monpack/resourcepack/assets/minecraft/pack.mcmeta`

{% code title="pack.mcmeta" %}
```json
{
   "pack":{
      "pack_format":63,
      "description":"Mon Pack"
   },
   "overlays":{
      "entries":[
         {
            "directory":"mon_overlay_1",
            "formats":[
               42,
               43
            ]
         },
         {
            "directory":"mon_overlay_3",
            "formats":[
               44,
               47
            ]
         }
      ]
   }
}
```
{% endcode %}
