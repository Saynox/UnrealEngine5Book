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
