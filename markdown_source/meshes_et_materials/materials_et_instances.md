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
