# Liquid Metal Aesthetic

## Blender

### Passer d'un dessin à une forme 3D simple

!['avant après'](./images/avant.png)
*Le dessin de base et le final dans Blender*

Tout d'abord, vectoriser le dessin et l'exporter en .svg .
!['export d'illustrator'](./images/screen1.png)

Importer le .svg dans Blender en faisant `File` > `Import` > `Scalable Vector Graphics (.svg)`.
!['import dans blender'](./images/screen2.png)

Sélectionner l'objet créé, appuyer sur "J" et agrandir la forme en bougeant la souris.
!['rescale dans blender'](./images/screen3.png)

Placer l'objet à l'origine de la scène en faisant `click droit` > `Set Origin` > `Geometry to Origin`.
!['origin dans blender'](./images/screen4.png)

Dans le menu "Data" à droite de l'écran, scroller jusqu'à la partie "Geometry" et faire un Extrude en mettant un petit chiffre dans le paramètre `Extrude`.
!['extrude dans blender'](./images/screen5.png)

Créer un mesh à partir de la forme en faisant `click droit` > `Convert To` > `Mesh`.
!['mesh dans blender'](./images/screen6.png)

Dans le menu "Modifier" à droite de l'écran, cliquer sur `Add Modifier` et choisir `Remesh`.
!['modifier dans blender'](./images/screen7.png)

Dans la partie `Voxel`, il doit y avoir "0.1 m" comme taille de Voxel par défaut, il faut réduire ce chiffre jusqu'à voir ré-apparaître la forme.
!['remesh dans blender'](./images/screen8.png)

Il faut réduire ce chiffre jusqu'à voir ré-apparaître la forme.
!['remesh dans blender'](./images/screen9.png)

Continuer à réduire la taille de Voxel jusqu'à ce que la forme soit plus ou moins lisse.
!['remesh dans blender'](./images/screen10.png)

Cliquer sur la flèche vers le bas et faire `Apply`.
!['remesh dans blender'](./images/screen11.png)

À nouveau dans le menu "Modifier", choisir `Smooth`.
!['smooth dans blender'](./images/screen12.png)

!['smooth dans blender'](./images/screen13.png)

!['smooth dans blender'](./images/screen14.png)

Si besoin, aller dans le mode `Sculpt` et lisser encore plus par endroit avec l'outil "Smooth".

### Créer le material chrome


!['material dans blender'](./images/screen15.png)

Aller dans le menu "Material" et supprimer le material par défaut "SVGMat".

!['material dans blender'](./images/screen16.png)

Créer un nouveau material.

!['material dans blender'](./images/screen17.png)

Mettre le paramètre "Metallic" au max et baisser le paramètre "Roughness".

!['material dans blender'](./images/screen18.png)

En haut à droite, cliquer sur la troisième sphère pour activer le Viewport Shading et voir le material chrome avec l'Environnement Texture par défaut.

!['rendu! dans blender'](./images/screen19.png)

!['rendu! dans blender'](./images/screen22.png)

Pour changer l'Environnement Texture par défaut, aller dans l'onglet "Shading", puis dans Scene > World.

Il y a une node Background et une node World Output.

!['rendu! dans blender'](./images/screen23.png)

Faire Add > Environment Texture pour créer la node de l'Environnement Texture.

Cliquer sur Open pour ajouter la texture choisie.

!['rendu! dans blender'](./images/screen24.png)


!['rendu! dans blender'](./images/screen25.png)

Activer la dernière sphère en haut à droite pour voir le rendu du Material avec le background.


## TouchDesigner

Exporter la forme créée dans Blender en .obj.

!['rendu! dans blender'](./images/screen26.png)

Créer un `File In` SOP et importer l'obj.

!['rendu! dans blender'](./images/screen27.png)

Avec un `Transform` SOP, remettre l'obj dans le bon sens.

!['rendu! dans blender'](./images/screen30.png)

Créer un `Geo` COMP, une `Camera` COMP, un `Render` TOP et un `PBR` MAT.

!['rendu! dans blender'](./images/screen28.png)

Dans le `PBR` MAT, mettre "Metallic" à 1 et "Roughness" à 0.

!['rendu! dans blender'](./images/screen29.png)

Créer un `Environment Light` COMP et mettre l'environnement texture de notre choix dans "Environment Map". Si l'environnement texture est une image en mouvement, le nombre de FPS va crasher.

!['rendu! dans blender'](./images/screen31.png)





