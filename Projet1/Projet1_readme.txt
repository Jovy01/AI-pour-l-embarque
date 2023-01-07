Projet 1: 

En utilisant TensorFlow Lite, Arduino ainsi que la carte Nano 33 Sense BLE,
réalisez un projet qui permet de détecter le signe Yes (✓) ainsi que le signe (X)

à l'aide du fichier imo_capture, on capture les données d'accérélation et de positions
du bras selon le mouvement effectuer: 

 On tient dans sa main la carte nano BLE, et on effectue à plusieurs reprise 
 le moubement (✓) respectivement no (X) pour capturer les données relatifs à ces derniers.

dans deux fichier csv que l'on appelé yes et no on enregistre ces données obtenue du moniteur série
et on passe sur google colab pour entrainer  le modèle. 

on inclus dans nos fichier dans google collab, on se rassure que les noms des fichiers sont bel et bien 
ceux utilisé par la code d'entrainement sinon on effectu le changement grace à la fonction de collab 
qui permet de rechercher "X" et remplacer par "Y"
et enfin on passe aux étapes de compilation. 


à la fin de l'entrainement, celui ci nous génère 2 fichiers; un fichier .h (model.h) qui représente les données 
d'entrainement du modèle. 

on ouvre le fichier IMU_classifier qui nous permet ici de faire la classification

du geste effectuer et on remplace et le comtenu du (model.h)par le notre.

dans le void set up, on pose simplement nos questions à l'aide du serialt.print ce qui
nous permettra de les afficher sur le moniteur série. 

on inclut le tableau qui nous permet de faire le choix du geste éfectuer et l'affichage
de l'émojie en se referent sur la cotation de l'émojie correspondant au geste approprié
