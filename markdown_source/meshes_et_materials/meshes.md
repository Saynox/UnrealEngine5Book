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
