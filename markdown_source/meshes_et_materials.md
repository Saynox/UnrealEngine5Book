# Meshes & Materials

# Les Meshes

## Importations

Dans la Pop-Up d’importation, veillez à bien sélectionner dans Material Import Method, Do Not Create Material et décocher Import Texture.

Lorsque que vous importez un mesh, c’est préférable de créer soi-même le Material. Ainsi, vous pouvez créer un Material Master qui vous permettra de créer des instances dans lesquelles vous n’aurez qu’à attribuer les textures.

<aside>
⚠️ **! En revanche ! , cochez bien Import Texture pour vos futures importations si nécessaire. Les textures peuvent être souvent intégrés aux Meshes.**

</aside>

Le Skeletal Mesh est applicable uniquement si vous avez une Armature/Squelette (Bones) dans votre mesh comme un personnage rig, etc…

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled.png)

<aside>
⚠️ ! Attention ! Quand vous importez des éléments, ils ne sont pas sauvegardés.

</aside>

N’oublié pas de CTRL+Shift+S ou d’ouvrir le Save Checker.

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%201.png)

Pour l’organisation de votre projet, vous pouvez séparer vos Meshes de vos textures ou bien créer un dossier par Mesh.

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%202.png)

Dans notre cas, on utilise des Atlas de textures. Autrement dit, 1 texture pour plusieurs Meshes. Il est donc plus logique de séparer Textures et Meshes.

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%203.png)

## Mesh Interface

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%204.png)

Voici l’interface d’un mesh. C’est dans celle-ci que vous pouvez gérer les différents paramètres du mesh.

Voici les onglets et paramètres principaux :

- **Material** **Slots** vous permet d’attribuer des Materials ou des instances.
- **General** **Settings** vous permet de régler principalement la Résolution du Lighting du mesh.
- **Collision** vous permet de géré toute la physique du mesh.
- **Nanite** peut être activer uniquement si le mesh possède un très grand nombre de Tris (comme une Statue avec 30K tris par exemple)

<aside>
⚠️ A Noter, Nanite ne fonctionne qu’avec Lumen et Virtual Shadow Map

</aside>

### Mesh Collision – Simple & Complex

Il se peut que certain mesh ne possède pas de collision. Vous pouvez vérifier que le mesh possède des collisions dans Show > Simple Collision.

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%205.png)

- **Les Simple Collisions** sont des Primitives (Cube, Sphère, etc…). Elles sont très peu couteuses en performance mais beaucoup moins précise.
- **Les Complex Collision**, elles, prennent l’entièreté du mesh comme collision. Elles sont beaucoup plus couteuses mais beaucoup plus précise. **On** **les utilise rarement sauf lors de la détection de collisions très avancées.**

Vous pouvez changer le style de collision que le mesh utilise avec **Collision Complexity**. On utilisera le plus souvent **Use Simple Collision As Complex**.

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%206.png)

### Mesh Collision – Création de Collision

Les collisions présentent par défaut peuvent ne pas forcément être optimisées ou répondre à vos attentes.

C’est pourquoi vous pouvez refaire les collisions de votre mesh avec le bouton Collisions. Vous aurez alors la possibilité d’ajouter plusieurs primitives. Essayer et ajuster les comme bon vous sembles.

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%207.png)

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%208.png)

**Utilisez au maximum les formes Simple, le moins de Convex possible.**

**Auto Convex** **Collsion** est un outil qui va créer des Primitives Complex.

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%209.png)

Unreal va automatiquement créer des collisions qui seront le plus en accord avec votre mesh tout en essayant de garder un faible cout en performance.

Vous avez Convex Decomposition qui vous permet d’ajuster cet outil.

- **Hull** **Count** permet de définir le nombre de primitive créer.
- **Max** **Hull** **Verts** permet de définir le maximum de vertex pour 1 primitive.
- **Hull** **Precision** défini à quel point les primitives vont s’adapter à la forme du mesh.

# Les Materials & Instances

Pour créer un Material, allez dans votre Content Drawer et créez un Material avec clic droit ou le bouton Add.

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2010.png)

Si vous voulez créer des Materials basique, vous pouvez créer une base qui se déclinera en plusieurs instance. Un Material représente l’apparence de l'Object.

Une Instance de Material vous permet de n’avoir accès qu’aux paramètres que vous avez créé dans votre Material de base. Utilisez toujours les instances et pas les bases directement

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2011.png)

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2012.png)

Pour créer une instance, cliquez sur le Material de base et appuyez sur ‘Create Material Instance’

### Editor Preferences – Materials Shortcuts

Avant de commencer, nous allons ReBind quelques shortcuts pour les Materials. Ces raccourcis vous permettront de créer et contrôler des Materials beaucoup plus facilement.

Dans Editor Preferences > Keyboard Shortcuts > Material Editor, attribuez:

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2013.png)

Dans Editor Preferences > Keyboard Shortcuts > Material Editor – Spawn Nodes, attribuez:

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2014.png)

## Material Interface

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2015.png)

## Introduction – Material Basique

Vous avez la possibilité de créer des Constantes via les raccourcis 1 (&), 2 (é), 3 ( “ ) et 4 ( ‘ ), configurés précédement, pour les différents paramètres proposés et actif (En blanc). Appuyez sur la touche et Clic gauche pour placer une constante.

**Les Paramètres principaux:**

| Base Color (Vector 3/4) | Couleur du Material |
| --- | --- |
| Metallic (Float) | Aspect Métallique |
| Roughness (Float) | Réflexion du Material (Matte = 1 ou Miroir = 0) |
| Emissive Color (Vector 3/4) | Emission de lumière |
| Ambiant Occlusion (Float) | Ombre dans les recoins & crevasses du Material* |

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2016.png)

Nous allons commencer par créer une base de Material basique pour pouvoir créer des couleurs avec quelques effets. Dans un dossier Material, créer un nouveau dossier Bases ainsi qu’un Material appelé M_SimpleColor.

### Ajout de Node

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2017.png)

Vous pouvez Clic-Droit dans le graph pour ouvrir le menu des Nodes ou vous avez le menu Palette sur votre droite. Il est docker mais vous pouvez le Pin ou l’Undock.

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2018.png)

Vous avez aussi plein de petit raccourci pour ajouter des Nodes rapidement. Précédemment, vous avez vu comment configuré les constantes et plus.

## Preview du Material

### La preview de Node

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2019.png)

Vous pouvez Preview un Node pour avoir le rendu jusqu’à un Node en particulier.

> Comme précédemment, on a configuré cette fonctionnalité sur la touche ².
> 

Vous pouvez également faire clic-droit sur le Node et Start Previewing Node.

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2020.png)

### Configurer la Preview

Pour configurer le mesh afficher, vous avez des petites icônes en bas à droite de la Preview. Pour un mesh spécial, vous devrez d’abord le sectionner dans le Content Drawer.

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2021.png)

<aside>
📝 **Le mesh utilisé est celui présent dans l’Engine Content. (SM_MatPreviewMesh_01)**

</aside>

Vous pouvez également changer tout l’environnement de la Preview ainsi que le Lighting ou bien le post process. **Allez dans Windows > Preview Scene Settings**

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2022.png)

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2023.png)

Assurez de le configurer de sorte à ce que le rendu soit le même que dans votre Level pour éviter d’avoir à faire des retouches inutiles.

## Les Nodes

### Shortcuts

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2024.png)

<aside>
📝 Veillez a bien suivre les étapes précédentes pour obtenir le même résultat.

</aside>

### Valeurs Brutes

Ainsi, nous pouvons créer et connecter des Nodes pour pouvoir contrôler le rendu de notre Material.

Le problème étant que les valeurs sont « Brutes ». Ce ne sont pas des paramètres.

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2025.png)

## Créations de Paramètres

Pour créer des paramètres, vous pouvez en créer directement avec les nodes :

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2026.png)

Ou bien clic-Droit sur vos valeurs brutes et Convert to Parameter.

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2027.png)

Dans Details, vous pouvez ranger vos parameters avec Group, inscrivez le nom de votre catégorie directement dedans et organisez les priorités pour les trier.

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2028.png)

Parameters vous permet de voir comment vos paramètres sont organisés et triés ainsi que de contrôler leurs valeurs.

### L’Onglet Parameters

Parameters vous permet de voir comment vos paramètres sont organier et triés. Vous pouvez également ajuster les valeurs directement dans cet onglet.

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2029.png)

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2030.png)

Plus le nombre que vous mettez dans priorité est élevé (ex: 50), plus votre paramètre apparaitra bas et inversement.

Desc signifie description, vous pouvez décrire l’usage de chaque paramètre que vous créez.
Save Child va créer une Instance de votre Material.

### Le Switch Parameter

Le Swith Parameter (Node: StaticSwitchParameter) vous permet de contrôler quels paramètres votre Material doit utiliser en fonction d’un Bolean.

Dans le Material Instance, On utilise un Switch pour contrôler l’Emissive: 

![Avant](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2031.png)

Avant

![Après](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2032.png)

Après

Par défaut, il est Static. Autrement dit, vous ne pouvez pas le faire évoluer durant l’exécution de votre jeu. En revanche, vous pouvez changer cela dans le Detail panel avec le paramètre Dynamic Branch.

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2033.png)

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2034.png)

## Materials de Textures

Pour ce faire, nous allons utiliser le node TextureSample2D qu’il faudra convertir en paramètre. Vous avez également un node Parameter qui s’appel TextureSampleParameter2D.

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2035.png)

On utilise souvent une texture qui possède plusieurs informations comme la Roughness, la Metalness, etc… Chaque information correspond à un chanel R, G, B et A.

Vous pouvez utiliser un node de texture pour chaque attribut mais attention, vous êtes limité à un totale de 16 nodes de texture connecté et activé.

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2036.png)

### Texture par défaut

Lorsque vous utilisez ce node, il vous faut obligatoirement une texture par défaut. Lorsque vous sélectionnez la texture, vous ne verrez peut être pas le contenu du moteur.

Sur le choix de la texture, cliquer sur l’engrenage à côté de la barre de recherche et cochez Show Engine Content puis taper defaultTexture. Prenez la première, avec la couleur unis et faite de même pour l’attribut Normal

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2037.png)

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2038.png)

## Les Instances de Materials

Vous avez vu précédemment comment créer des instances via différentes méthodes. Via l’onglet Parameters du Material et via le content Drawer en faisant un clic droit sur un Material.

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2039.png)

<aside>
📝 Utilisez toujours les instances et pas les material de base sur vos meshes, landscape, vfx, etc…

</aside>

Les Instances vous permettent de décliner un Material en plusieurs variantes via les paramètres créés.

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2040.png)

# Les Nodes

### Les Operators & Utilitaires

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2041.png)

### Le TexCoordinate, Panner & Time

Time vous permet de récupérer le temps et de définir si il doit continuer de s’exécuter pendant que le jeu est en Pause.

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2042.png)

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2043.png)

<aside>
📝 Panner & TexCoords sont des notes d’UV.

</aside>

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2044.png)

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2045.png)

TextureCoordinate vous permet de controller facilement le Tilling de votre texture.

Panner est un node vous permettant de faire bouger, selon X et Y, votre texture. (l’input Time & Coordinate n’est pas obligatoire)

### Le Absolute World Position

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2046.png)

Ce node vous permet de récupérer la position absolue mondiale de chaque pixel visuel de l’objet.

On peut grâce à ce node appliquer et effectuer un Tilling par rapport au monde et pas par rapport à l’objet.

Il vous permet, par exemple, de créer un Material de texture qui pourra s’appliquer à n’importe quel objet qui a été rescale ou rotate sans que la texture soit déformée.

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2047.png)

### Les BreakOut & Make

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2048.png)

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2049.png)

Souvent, vous aurez besoin de modifier ou de récupérer une valeur en particulier. C’est pourquoi vous avez les BreakOutComponents et MakeFloat

Comme avec le Panner par exemple, vous pouvez utiliser MakeFloat2 pour pouvoir attribuer deux Float parameters individuels.

### Le Sine Remaped & Lerp

Le Sine Remaped permet de créer une Courbe Sinusoïdale selon deux valeurs définies.

Vous pouvez utilisé des Float, des Vector2 ou encore des Couleurs (Vector3).

Vous pouvez attribuer Time à Sine Phase pour pouvoir créer une sinusoïde perpétuelle et ainsi pouvoir alterner entre les deux valeurs.

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2050.png)

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2051.png)

Le Lerp permet de créer une interpolation classique entre deux valeurs entre A et B. L’Alpha permet de contrôler le rapport entre les deux valeurs, c’est une valeur Float.

Si on attribue le résultat d’un Sine Remaped (0, 1) avec Time, le Lerp alternera entre les deux valeurs indéfiniment.

### Fresnel & Fresnel Function

Vous avez deux Nodes de Fresnel, le Basique et l’Avancé.

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2052.png)

Avec le Node avancé, vous avez un contrôle plus important sur le Fresnel. Privilégiez ce node en priorité.

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2053.png)

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2054.png)

Vous pouvez, par exemple, créer un Fresnel Inversé très facilement en utilisant Invert Fresnel (Static Bolean).

### Le Power

Le node Power est, en mathématique, l’Exposant. Il va multiplier X fois l’Input Base par elle-même.

### Le Noise

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2055.png)

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2056.png)

Le Node Noise vous permet de créer plusieurs de Noise procéduralement. Attention à ne pas confondre avec le VectorNoise. Le Noise est une texture en Alpha uniquement.

**FilterWidth** représente «la densité» du Noise.

**Level** vous permet de géré le niveau de détail de Noise. Je vous recommande de rester en 1 et 4 car il peut devenir très gourmand en performance.

**Le Voronoi** possède le paramètre de Qualité. Faite attention car plus elle est élevée comme le Level, plus le Material consommera de ressource.

Vous pouvez créer du mouvement comme ci-dessous :

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2057.png)

## Les Materials Transparent

![Translucent](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2058.png)

Translucent

![Additive](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2059.png)

Additive

Les Materials de transparences peuvent être créer en changeant le Blend Mode en Translucent ou Additive.

Dans le Detail panel: 

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2060.png)

**Translucent** : Plus couteux en performance et ne se Blend pas avec les couleurs de la scène.

**Additive** : Moins couteux en performance et se Blend avec les couleurs de la scène.

**Masked** : Pas de transparence, permet de «découper» (ex: Un plane avec une texture de feuille, il va découper le plane en fonction de la feuille pour ne faire apparaître que celle-ci).

# Les Fonctions

Vous pouvez créer des fonctions pour vos materials pour réutiliser certains effets comme du Noise custom.

Pour en créer, vous pouvez aller dans votre Content Drawer puis dans la catégorie material > Material Function

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2061.png)

Expose to Library permet d’afficher la fonction dans la liste des Nodes.

Vous pouvez ajouter des Inputs à votre fonction avec le Node FunctionInput. Dans celui-ci, vous pouvez configurer le type.

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2062.png)

![Untitled](Meshes%20&%20Materials%205ca27dfe6b1e459392a2886a71398849/Untitled%2063.png)
