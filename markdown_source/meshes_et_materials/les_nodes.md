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
