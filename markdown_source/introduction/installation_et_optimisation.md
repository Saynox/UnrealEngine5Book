# Installation & Optimisation

![Untitled](Introduction%20ed0b79ec10bd4f55bceca469218d9b7e/Untitled%205.png)

Après avoir installé le launcher Epic, allez dans l’onglet Bibliothèque et ajouter la version du moteur souhaité (5.2.1 dans notre cas)

> Il y a la Génération du moteur (5.0), les Versions (5.2) et les Patchs (5.2.1). Je vous recommande d’installer les patchs dès qu’ils sont disponibles (votre team entière devra l’installer également). En revanche changer la version du moteur peut impacter votre projet.

Faite attention, le moteur est très gourmand en espace (Plus de 70Go), c’est pourquoi vous devez le nettoyer juste après l’installation (>40Go après nettoyage).

## Libération de l’espace de stockage

![Untitled](Introduction%20ed0b79ec10bd4f55bceca469218d9b7e/Untitled%206.png)

Décocher bien Contenus de démarrage ainsi que tout autres options excepté les packs si vous le souhaiter.

![Untitled](Introduction%20ed0b79ec10bd4f55bceca469218d9b7e/Untitled%207.png)

Vous pouvez supprimer également toutes les plateformes, elles ne seront pas nécessaires sauf si vous faites un projet sur celles-ci.

![Untitled](Introduction%20ed0b79ec10bd4f55bceca469218d9b7e/Untitled%208.png)

## Optimisation technique du moteur

Une fois l’installation et le nettoyage du moteur terminé, je vous recommande de suivre ces étapes afin d’optimiser le fonctionnement d’Unreal ainsi que sa puissance.

Vous aurez besoin d’ouvrir un fichier moteur appelé BaseEngine.ini

<aside>
📎 Emplacement par défaut: 
*C:\Program Files\Epic Games\UE_5.2\Engine\Config\BaseEngine.in*

</aside>

Ensuite, mettez =1 aux deux paramètres puis Sauvegardez et fermez et c’est terminé.

![Untitled](Introduction%20ed0b79ec10bd4f55bceca469218d9b7e/Untitled%209.png)

## Unreal Launcher

![Untitled](Introduction%20ed0b79ec10bd4f55bceca469218d9b7e/Untitled%2010.png)

![Untitled](Introduction%20ed0b79ec10bd4f55bceca469218d9b7e/Untitled%2011.png)

Le launcher vous propose les différents projets que vous avez créé et ouvert récemment.
Vous avez différentes catégories permettant de créer et setup un projet selon plusieurs types prédéfinis.

Je vous recommande très fortement de toujours commencer un projet avec le Blank Template pour éviter qu’Unreal autoconfigure votre projet. Vous pourrez toujours importé le contenu des Presets plus tard.

### Project Creation

![Untitled](Introduction%20ed0b79ec10bd4f55bceca469218d9b7e/Untitled%2012.png)

Lorsque vous créez un nouveau projet, comme dis précédemment, prenez toujours le Blank Template.

<div class="warning">

Assurez-vous de choisir correctement l’emplacement de votre projet avec Project Location  et que le nom de votre projet ne peut pas contenir d’espace ou de caractère spécial. Uniquement majuscule, tiret «–» et underscore «_»

</div>

Pour les paramètres de projet, assurez-vous également de bien :

- Décocher Starter Content & RayTracing
- Sélectionner Blueprint
- Quality Preset en Maximum
