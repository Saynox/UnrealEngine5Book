# Modeling Tool & Level Design

# Introduction

![Untitled](Modeling%20Tool%20&%20Level%20Design%209620dde170da48e2814851d45b6d7476/Untitled.png)

Le Modeling Tool (disponible en changeant de Mode) est un outil de création et de modification de Mesh. Il est comparable à un vrai outil de modélisation 3D (Maya/Blender)

Il possède un grand nombre d’outils et fonctionnalités diverses et variés. Vous pouvez créer, par exemple, des assets pour du Block Design.

Il se décompose en deux panneaux, le menu des Outils et le menu Modeling qui possède les paramètres de l’outil sélectionné.

Faite attention à New Asset Location, veillez à bien sélectionner Current Folder et donc par conséquent créer/sélectionner un dossier de Meshes.

# Création de Meshes

Vous pouvez créer des objets avec Shapes.

![Untitled](Modeling%20Tool%20&%20Level%20Design%209620dde170da48e2814851d45b6d7476/Untitled%201.png)

![Untitled](Modeling%20Tool%20&%20Level%20Design%209620dde170da48e2814851d45b6d7476/Untitled%202.png)

![Untitled](Modeling%20Tool%20&%20Level%20Design%209620dde170da48e2814851d45b6d7476/Untitled%203.png)

Vous pouvez ainsi modifier les attributs de la forme selectionnée comme la largeur, les subdivisions, le material, etc…

Assurez-vous de bien config New Asset Location lors de la création du Mesh.

Une fois fini, appuyez sur Accept et cela vous créera un Mesh dans le dossier sélectionner.

N’oubliez pas de rename votre mesh !

![Untitled](Modeling%20Tool%20&%20Level%20Design%209620dde170da48e2814851d45b6d7476/Untitled%204.png)

# Output Type – Static vs Dynamic

L’Output Static Mesh va créer, dans votre content drawer, un nouveau mesh.

![Untitled](Modeling%20Tool%20&%20Level%20Design%209620dde170da48e2814851d45b6d7476/Untitled%205.png)

L’Output Dynamic, elle, va créer dans le Level, un Actor avec le composant Dynamic Mesh Component.

Le Dynamic Mesh permet de modifier un mesh sans modifier l’original et donc créer une Copie dans le Level.

<aside>
⚠️ En revanche, le Dynamic Mesh n’est pas optimisé pour le Rendering et coûte cher en ressources. Il est donc à utiliser avec parcimonie.

</aside>
