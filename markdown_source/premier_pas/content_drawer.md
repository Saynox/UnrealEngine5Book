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
