# rendu-LIFPROJET-groupe-devaux-gifu

Cyril Devaux p2101844
Ionut Gifu p1209917

Ce projet est un jeu de simulation en 3D de bataille de deux équipes.
Il a été réalisé grâce au moteur de jeu Unreal Engine en version 5.3 .

Pour lancer le projet avec l'Unreal Editor (uniquement si Unreal Engine est installé), aller dans le dossier "projet" puis double-cliquer le fichier "LIFPROJET_V1.uproject", cela va lancer l'éditeur, ce qui permet de faire des modifications. Pour lancer une simulation de ce que le jeu va donner lorsqu'on est dans l'éditeur, il suffit de cliquer sur le bouton vert "play this level in a new window" (ou "play this level in the active level editor viewport" selon les paramètres de l'éditeur) situé en haut de la fenetre.

Pour lancer le projet si Unreal n'est pas installé, un executable est fourni dans le répertoire github. Aller dans le dossier "windows" puis double-cliquer le fichier "LIFPROJET_V1.exe", cela lancera le jeu dans sa version final.


Lorsque le jeu se lance, on arrive sur un menu. Il faut appuyer sur le bouton "Start", puis selectionner une carte parmis les deux disponible en appuyant sur l'image représentant la carte (pour changer de carte, appuyer sur les boutons à droite ou à gauche de l'image). Ensuite on choisit le nombre de personnage de chaque équipe en précisant un nombre en face de "Number of fighters". Il faut après choisir quelle intelligence utiliser pour chaque équipe ("Team" ou "Solo"). Si l'intelligence "Team" est choisie, il faut préciser la taille maximum des groupe créé en précisant un nombre en face de "Maximum Group Size". Enfin on lance le jeu avec les paramètres choisi en appuyant sur le bouton "START".


Bugs :
Pour une raison inconnu, lorsque nous avons exporté le projet pour créer un executable, nous avons rencontré une complication : la première carte ne se charge pas entièrement, ce qui ne rends pas le jeu jouable (la deuxieme carte fonctionne bien). Ce problème n'est pas présent lorsqu'on lance le jeu avec l'Unreal Editor.

Autre problème rencontré : à chaque fois qu'on lance l'Unreal Editor, dans les deux behavior tree "BT_ArbreEtat" et "BT_GroupBehavior", la valeur de la tache "SetFocus" se remet par défaut à "self actor".
Pour une meilleure expérience de jeu, il est conseillé de changé cette valeur à "ActorAttack" pour le "BT_ArbreEtat" et à "DetectedEnnemy" pour "BT_GroupBehavior".
Après avoir fait des recherches sur internet, le fait que des valeurs soit remise à "self actor" dans un Behavoir Tree est un bug connu sur Unreal Engine qui pose problème à de nombreuses personnes. 