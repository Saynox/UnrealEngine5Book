# Problèmes de Performances

<aside>
⚠️ **Unreal Engine 5 active par défaut les technologies Next-Gen comme Lumen, Virtual Shadow Maps, Nanite, etc… C’est ce qui peut provoquer des chutes de performances.**

</aside>

Vous pouvez changer cela dans les Project Settings pour changer les configurations par défaut ou dans le Post Process Volume d’un niveau pour l’appliquer au Level seulement.

### Désactiver Lumen

Lumen fonctionne en deux parties, via la global Illumination et via les Reflection.

<aside>
📝 Pour retirer lumen, il faut passer a None la global illumination et Screen Space les reflections.

</aside>

Par défaut, dans le Project Settings

![Project Settings > Rendering > Global Illumination & Reflection](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%2038.png)

Project Settings > Rendering > Global Illumination & Reflection

Dans le Post Process du Level 

![Post Process du Level > Global Illumination & Reflection](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%2039.png)

Post Process du Level > Global Illumination & Reflection

### Désactiver Virtual Shadow Maps

Dans le project Settings, Rendering, catégorie Shadows

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%2040.png)

Passez en Shadow Map

### Framerate Bridé

Unreal scale ses performances en fonction de votre PC. Par exemple, sur un Laptop vous serez capé à 30-60fps alors que sur un Desktop vous serez à 120fps.

Le problème étant que ce cap cause des problèmes de performance et de fluidité lors de l’édition du Level ou la simulation du jeu.

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%2041.png)

**Activez Fixed** **Framerate et inscrivez +200fps** pour débrider Unreal en editor.

<aside>
🚨 Attention, ajuster ce paramètre selon vos besoins car il peut aussi créer un effet de lenteur In-Game. Ne le mettez pas trop élevée sauf pour du Debug.

</aside>

### Résultat après Config

Voici à quoi ressemble le Level après avoir paramétré correctement le projet.

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%2042.png)

Comme vous le voyez, ce n’est pas très joli… Cela est dû au Lighting et au Materials. En effet, nous avons désactiver les technologies Next-Gen dans un premier temps. Nous verrons plus tard comment les utilisées et les optimisées.

<aside>
⚠️ **Cependant, Unreal vous indique que le Lighting doit être Rebuilt. Cela arrive quand vous utilisez le Bake Lighting. Nous verrons le Lighting un peu plus tard dans le cours**.

</aside>
