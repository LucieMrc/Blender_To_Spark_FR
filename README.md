# Blender_To_Spark_FR


## Blender : passer d'un dessin à une forme 3D simple

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

!['material dans blender'](./images/screen15.png)

!['material dans blender'](./images/screen16.png)

!['material dans blender'](./images/screen17.png)

!['material dans blender'](./images/screen18.png)

!['rendu! dans blender'](./images/screen19.png)

!['export dans blender'](./images/screen20.png)

## Spark

