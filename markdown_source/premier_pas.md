# Premier Pas

# Interface

Bienvenu sur Unreal 5 ! 😁

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled.png)

# Editor Configuration

Avant toutes choses, nous allons configurer Unreal pour que vous ayez la possibilité de l’utiliser avec un clavier AZERTY.

Rendez-vous dans Edit > Editor Preferences puis dans All Settings, tapez Viewport Navigation et attribuez vos touches comme ci-dessous.

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%201.png)

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%202.png)

## Déplacement & Contrôles

<aside>
⚠️ Exclusivement si vous avez suivi les étapes précédentes

</aside>

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%203.png)

# Le Viewport

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%204.png)

<aside>
📝 **Realtime** permet d’update votre Level en permanence (VFX, Effets, etc…). Pour du Level Design, je vous recommande de le désactiver pour augmenter les perfs et ainsi avoir un control plus précis sur vos actions (sans lag moteur)

</aside>

<aside>
📝 **Show** **FPS** vous montre en un clin d’œil vos performances (15-20ms Max), je vous incite très fortement à l’activer tout le temps.

</aside>

<aside>
📝 **Game** **View** est très pratique si vous voulez masquer tous les icones comme les lights, Gizmos etc…

</aside>

# Le Content Drawer

### Gestion du Contenu de votre Projet

Pour ouvrir le **Content** **Drawer** rapidement, vous pouvez utiliser la commande **CTRL** **+** **ESPACE**. Elle est très utile lorsque vous êtes sur un Blueprint ou encore en Immersive Mode (Fullscreen F11) pour faire du LD.

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%205.png)

Il vous permet de créer du contenu, d’en importer et d’en exporter. Par défaut, il n’est pas dock à votre interface pour plus de confort et lisibilité c’est pourquoi il prend la forme d’un onglet rétractable.

Le dossier Content est votre dossier racine, c’est la dedans que vous mettrez et importerez tout votre contenu.

<aside>
⚠️ ATTENTION, la structure de votre projet est capitale sur Unreal. Vous ne pourrez pas déplacer et supprimer facilement les éléments. Donc veiller à bien organiser votre projet en amont.

</aside>

### Ajouter du contenu

Pour ajouter du contenu, appuyer simplement sur le bouton +Add ou clic droit directement dans le content drawer.

Vous pouvez tapez, directement sur votre clavier, dès l’apparition de la liste, des mots-clés pour trouver plus facilement ce que vous cherchez.

Pour l’importation d’asset, vous pouvez les Drag&Drop sur le content drawer ou utiliser le bouton Import.

Vous avez la Nomenclature des Assets via ce Lien: **[UnrealAssetsNaming](https://docs.unrealengine.com/4.27/en-US/ProductionPipelines/AssetNaming/)**

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%206.png)

<aside>
🚨 **! Attention ! Unreal convertit tout son contenu en .uasset, c’est pourquoi vous ne devez pas importer d’asset dans le dossier du projet. Unreal va les reimporter et ainsi vos fichiers seront en double. Veiller à passer toujours par Unreal.**

</aside>

### Déplacer des éléments

Déplacer du contenu change les références de celui-ci. Il est possible que des dossiers résiduels persistent après un déplacement.

C’est pourquoi, effectuez toujours un **Fix Up Redirectors** sur les dossiers résiduels après chaque déplacement pour vous assurer que tout est en ordre et ainsi les supprimer proprement. Clic-Droit sur le dossier pour avoir accès à cette fonctionnalité.

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%207.png)

<aside>
🚨 **NE FAITE JAMAIS AUCUNE OPERATION DE DEPLACEMNT DANS LE DOSSIER DU PROJET AU RISQUE DE CASSER DES ELEMENTS. PASSEZ PAR UNREAL TOUT LE TEMPS.**

</aside>

### Supprimer des éléments

Si vous voulez supprimer des éléments, supprimez-les toujours dans Unreal.

Il vous montrera si l’objet possède des références dans d’autres assets et si il y a des références en mémoire (Undo Historique principalement, vous pouvez les ignorez).

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%208.png)

<aside>
🚨 **NE FAITE JAMAIS AUCUNE OPERATION DE SUPPRESSION DANS LE DOSSIER DU PROJET AU RISQUE DE CASSER DES ELEMENTS. PASSEZ PAR UNREAL TOUT LE TEMPS.**

</aside>

Si Unreal ne supprime pas les dossiers, c’est qu’il reste toujours des assets ou qu’il y a des références mémoires non nettoyées. Relancé l’Editor et supprimer de nouveau les dossiers en question.

### Migrate & Export

L’exportation de contenu sur Unreal est protégée. Vous ne pouvez pas aller dans votre dossier de projet et copier-coller. Tous les fichiers sont encryptés en .uasset, .umap.

Pour exporter du contenu d’un projet à un autre, vous devrez passer par l’option **Migrate**. En effet, sur Unreal, vous ne pouvez pas créer comme sur Unity  des Packages. Vous devrez transférer, via Migrate, les éléments de votre projet vers un autre projet.

Vous pouvez aussi Export des assets en FBX par exemple avec Export…

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%209.png)

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%2010.png)

<aside>
📝 A noter, la Migration se fait uniquement vers le Dossier Content du nouveau projet.

</aside>

# Nouveau Level

Pour créer un nouveau niveau, appuyer sur **CTRL+N** dans le Level actuel pour ouvrir la fenêtre de création.

Vous aurez le choix entre deux types de niveau ainsi que deux template. Dans notre exemple, on utilisera **Empty Level**.

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%2011.png)

<aside>
📝 **N’oubliez de le sauvegarder directement avec CTRL+S et de le nommer correctement avec une nomenclature définie comme LVL_ par exemple.**

</aside>

Open World est réservé aux Levels nécessitant un landscape de moyenne à grande taille. Il est configuré pour utiliser certaines technologies sur lesquelles on reviendra plus tard dans ce cours.

Vous pouvez également créer un Level depuis le Content Drawer mais ce sera un Empty Level.

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%2012.png)

### Ajout d’un Environnement

Un empty level ne possède aucun élément par défaut, il est donc vide et complètement noir.

Selon votre usage, vous aurez besoin d’un environnement classique (Skybox, lumière, etc…) pour pouvoir avoir un visuel sur votre niveau.

Pour ce faire, vous aurez besoin de l’**Environment Light Mixer**. Il vous permet de créer un environnement très rapidement pour votre level. 

Il se trouve dans Windows > Env. Light Mix.

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%2013.png)

Pour un environnement classique, ajoutez une SkyLight, une Atmospheric Light, une SkyAtmosphere et un Height Fog.

Si vous le souhaitez, vous pouvez également créer un Volumetric Cloud.

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%2014.png)

### L’Environnement Light Mixer

Cette fenêtre vous permet de créer et de contrôler votre environnement très facilement et d’ajuster les paramètres essentiels des différents éléments qui le composent.

**Minimal** vous montre les paramètres essentiels

**Normal** vous montre les paramètres des éléments comme dans le Detail panel.

**Normal + Advanced** vous montre tous les paramètres sans exceptions.

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%2015.png)

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%2016.png)

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%2017.png)

Pour contrôler très facilement l’orientation du Soleil, appuyez sur **CTRL+L ou AltGr+L** et **maintenez CTRL ou AltGr** puis bougez votre souris.

# Le Save Checker, votre meilleur ami

Le Save Checker peut vous sauvez la mise de temps en temps car il vous signalera et vous montrera tout ce qui n’est pas sauvegardé. Jetez toujours un coup d’œil en bas à droite de votre editor.

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%2018.png)

Extrêmement utiles quand vous travaillez sur plusieurs onglets ou que vous importez beaucoup de contenu d’un coup.

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%2019.png)

Unreal possède également un system d’Auto Save qui peut être config dans Editor Config > Loading & Saving > Auto – Save. Warning est un pop-up pour vous prévenir de l’Auto Save

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%2020.png)

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%2021.png)

# Ajouter des éléments dans votre Level

Une fois votre Level créé et configuré, on peut commencer à y ajouter du contenu.

Pour ce faire, il y a plusieurs manières de faire:

1 – Vous pouvez Drag&Drop vos éléments depuis votre content drawer directement dans le Level.

2 – Vous pouvez cliquer sur le petit cube avec un + vert et drag & drop des éléments.

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%2022.png)

3 – Ou bien ouvrir le Place Actor panel dans Window > Place Actor et Drag&Drop des éléments dans le Level.

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%2023.png)

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%2024.png)

# Mobilité des Objets

Les éléments que vous placer dans votre Level ont une Mobility.

Les effets suivants sont pour les Meshes 3D (Cube, Sphère, etc…):

- **Static**: Ne permet aucun mouvement et bake le Lighting sur l’objet.
- **Stationary**: Ne permet aucun mouvement mais peut changer in game.
- **Movable**: Permet à l’objet d’avoir un mouvement et est complément dynamique

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%2025.png)

<aside>
📝 La plupart de vos meshes seront soit static soit Movable.

</aside>

# L’Outliner et les dossiers

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%2026.png)

Lorsque vous commencez à ajouter des éléments dans votre Level, vous allez très vite voir que votre Outliner commence à devenir désordonné. Vous ne pouvez pas repositionner les éléments à la main, **Unreal trie tout par ordre alphabétique ou via des filtres.**

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%2027.png)

C’est pourquoi, vous avez **les** **Dossiers** pour organiser votre Outliner. Comme ci-contre, vous pouvez en créer avec le **bouton** **en haut à droite** ou lorsque vous **cliquez sur un élément** et sélectionner **Move To**.

![Avant](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%2028.png)

Avant

![Après](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%2029.png)

Après

# Level - Le Post Process Volume

<aside>
📝 Il vous manque un élément crucial dans votre Level, c’est le Post Process Volume. Il vous permet de contrôler non seulement les effets visuels mais également le Rendering du Level.

</aside>

Par défaut, votre Level possède des effets de post process comme l’Auto Exposure. Mais le plus souvent, ceux-ci ne sont pas adaptés à votre ambiance/Level.

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%2030.png)

Dans notre cas, nous voulons le rendre **Global (cherchez Unbound dans la barre de recherche)** puis changer **l’Exposure en Manual** et **ajuster la Compensation.**

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%2031.png)

<aside>
⚠️ **Cela peut changer de manière assez radicale la manière dont votre Level est rendu.**

</aside>

# Le Project Settings en détails

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%2032.png)

Le Project Settings vous permet de configurer l’entièreté de votre projet. Veillez à le garder ouvert, vous y reviendrez assez souvent !

> Il est accessible via l’onglet Edit > Project Settings ou via le bouton Settings > Projects Settings en haut à droite lorsque vous êtes sur votre Level.
> 

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%2033.png)

### Project Settings - Maps & Modes

Cette catégorie permet de configurer les valeurs par défaut du jeu comme le premier Level qui se lance lors du jeu ou encore le level qui s’ouvre au lancement de l’éditor.

Dans notre cas, on a attribué LVL_Game (mais si vous avez un MainMenu, par exemple, attribuez celui-ci à Game Default Map).

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%2034.png)

### Project Settings – Supported Platforms

Cette catégorie permet de modifier les plateformes supportées par votre jeu.

On décochera toutes les catégories sauf Windows (si vous avez besoins d’activer d’autre plateformes, libre à vous)

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%2035.png)

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%2036.png)

Dans votre Level, le bouton Platforms vous permet de package votre projet sous la forme d’un dossier avec un .exe. Chaque plateforme devra être packaged individuellement.

Modifier les plateformes disponibles change les configurations proposées pour n’afficher que Windows.

### Project Settings - Rendering

Cette catégorie permet de changer tous les paramètres concernant les technologies de Rendering utilisées comme Lumen, Nanite, etc… ainsi que tous les autres paramètres de rendu du projet.

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%2037.png)

Lors de la création du projet, vous aviez la possibilité de coché RayTracing mais cela aurait préconfiguré le projet, c’est dans rendering. Vous pouvez le réactiver si vous le souhaité dans Hardware RayTracing.

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

# BUILD - Génération des Datas

L’onglet Build vous permet de générer les data de votre Level comme par exemple le Lighting, les données de Navigation AI, etc…

Il vous créera alors au même endroit que votre Level, un fichier de BuildDatas.

- **Build All Levels** va Build toutes les catégories.
- **Build Lighting Only** va Bakes les Lumière seulement.
    
    Nous reviendrons sur les autres outils de Builds plus tard.
    

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%2043.png)

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%2044.png)

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%2045.png)

Résultat après build :

![Untitled](Premier%20Pas%20c35c9092e8654bf3b517b41e177a3b57/Untitled%2046.png)
