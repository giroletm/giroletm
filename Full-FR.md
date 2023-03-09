# *Pas* en bref — L'histoire de ma vie de programmeur
## Préambule
La plupart des travaux passés mentionnés ici n'auront aucun lien.

C'est pour éviter que ce compte soit relié à mes autres comptes, même si il suffit d'une petite recherche dans votre moteur de recherche favoris pour trouver les outils que j'ai mentionné, accompagné de tout le reste.

**Tout ce qui est écrit ici a été rédigé en [anglais](https://github.com/giroletm/giroletm/blob/main/Full.md) puis seulement ensuite traduit en français par mes soins. Donc si certaines phrases sont un peu bancales, c'est normal !**

## Modding de NSMBW — 2017-Aujourd'hui
Cette partie représente une partie énorme de ma vie. Mes premiers essais se sont passés en fin 2017, mais j'ai commencé à avoir un niveau potable vers 2020. J'ai arrêté d'en faire régulièrement en fin 2022, mais je fais toujours quelques trucs de temps en temps.

Pour poser les bases, NSMBW, ou [New Super Mario Bros. Wii](https://wikipedia.org/wiki/New_Super_Mario_Bros._Wii) est un jeu sorti sur la [Nintendo Wii](https://wikipedia.org/wiki/Wii) en 2009. Le modding consistant à modifier le jeu pour y ajouter ce que l'on désire.

Mon activité de modding principale est évidemment la programmation. Mais avant ça, j'ai essayé le level design et le tileset design mais malheureusement, je suis très nul à ces choses là.

Mais en fin 2018, j'ai réussi à compiler le [code source](https://github.com/Newer-Team/NewerSMBW/tree/clang-no-translations) de [NewerSMBW](https://newerteam.com/wii/), à savoir le truc de base à faire pour pouvoir faire de la programmation dans le jeu.

Au départ c'était surtout du C++, mais j'ai fini par apprendre l'assembleur PowerPC, ce qui a ÉNORMÉMENT étendu mes capacités de modding. Absolument n'importe quoi peut être supprimé, changé ou ajouté dans le jeu grâce au C++ et à l'assembleur PowerPC.

À peu près l'intégralité de mon expérience en programmation d'avant 2023 vient de là, et ça m'a donné pas mal d'expérience en reverse engineering que j'espère pouvoir utiliser dans le futur.

## Outils en C# — 2019-Aujourd'hui
J'ai fait *plein* d'outils CLI (ligne de commande) et GUI (interface) en C#, dont la plupart sont liés d'une manière ou d'une autre à [NSMBW](https://wikipedia.org/wiki/New_Super_Mario_Bros._Wii).

Les outils notables que j'ai pu faire sont:

CLI:
* Un outil pour patcher des roms de Nintendo Wii avec d'autres fichiers en utilisant un fichier XML standardisé
* Un outil pour patcher les exécutables de Nintendo Wii executables en utilisant un fichier XML standardisé (groupé avec l'outil précédent)

GUI:
* Des éditeurs de sauvegarde pour [NSMB](https://wikipedia.org/wiki/New_Super_Mario_Bros.), [NSMBW](https://wikipedia.org/wiki/New_Super_Mario_Bros._Wii) et [NSMBU](https://wikipedia.org/wiki/New_Super_Mario_Bros._U)
* Des éditeurs pour le formats de fichier des cinématiques et celui de la danse des crédits utilisés dans [NewerSMBW](https://newerteam.com/wii/)
* Un outil pour simplifier la génération de fichiers YAML utilisés pour créer de nouveaux ennemis et acteurs NSMBW

## Robot-guide — 2021-2022
Pendant ma dernière année de terminale en fillière technologie (STI2D), on m'a donné pour projet, avec trois camarades, de faire un petit robot qui guiderai des gens à travers le pôle technologique de l'école pendant la journée portes ouvertes.

Le project était en deux parties:
* Une borne de contrôle qui aurait une interface sur laquelle les gens pourraient choisir l'endroit où ils veulent aller et voir une carte du bâtiment avec le chemin à suivre mis en évidence, avec la possibilité de demander au robot de nous y emmener
* Le robot lui-même, fonctionnant avec une carte [BBC micro:bit](https://microbit.org/) qui recevrait son chemin de la borne de contrôle en utilisant des ondes radio, et qui se repérerais en utilisant des balises (représentées par d'autres cartes micro:bit) éparpillées partout à travers le bâtiment

L'un de mes camarades a été chargé de faire un support pour la borne de contrôle, et les deux autres ont été chargés de faire le programme du robot et des balises. Quand à moi, j'ai été chargé de faire le programme de la borne de contrôle.

Au final, j'ai fait non seulement mon boulot sur la borne, mais aussi celui sur le robot et sur les balises, puisque mes deux camarades n'avaient aucune expérience en programmation et le peu de cours de programmation qu'on a eu étaient très incomplets.

Merci infiniment à mon dernier camarade qui a fait le support de la borne de contrôle, puisque lui et moi ont au final été les seuls à avoir vraiment bossé sur ce projet.

Le robot et ses balises ont été programmées en Python (avec le module micro:python) et la borne de contrôle a été programmée en C# (avec la librairie Windows Forms pour l'interface)

Je me suis heurté à un obstacle majeur quand j'ai fait la borne de contrôle cependant: j'avais besoin d'envoyer son chemin au robot, mais je ne voulais pas avoir des programmes pré-faits pour chaque possiblité de chemin, puisque j'avais envie que n'importe qui soit capable d'ajouter, modifier ou supprimer des chemins de la borne de contrôle sans avoir à toucher à son code.

Les chemins sont transférés au robot en utilisant encore une autre carte micro:bit, connectée à la borne de contrôle et qui envoie le chemin à suivre sous forme d'une suite d'octets grâce à un programme que la borne de contrôle écrirait sur ladite carte.

Cependant, ce programme aurait besoin d'être modifié pour pouvori envoyer n'importe quelle suite d'octets selon les besoins de la borne de contrôle. Mais même si les programmes des cartes micro:bit sont écrits en python, ils sont convertis dans un format que la carte peut comprendre avoir d'être écrits dessus.

Mais ce format est très peu documenté. J'ai donc du trouver par moi-même comment il fonctionnait en lisant le code source de l'IDE qui convertissait les programmes du python vers ledit format.

Je me suis retrouvé à écrire un manuel (assez simpliste) de 20 pages sur l'aventure qu'à été la création de cette borne de contrôle, comment le format des cartes micro:bit fonctionne et comment j'ai fait pour pouvoir le modifier en temps réel.

Notre projet a été choisi pour participé à la 13ème édition des *Olympiades de Sciences de l'Ingénieur de l'académie de Dijon*. On est donc allé à Dijon (oui c'est là où ils font la moutarde de Dijon) pour participer. On a eu aucun prix, mais une autre équipe de notre école en a eu un donc je suppose que je doit être content pour eux. Après tout, ce qui compte réellement c'est l'expérience qu'on y a gagné, ou un truc comme ça..?

## Autres travaux

### Club de programmation — 2016-2017
De 2016 à 2017 j'ai été dans une espèce de club de programmation indépendant, où on nous a appris les bases du C# pour faire un jeu [Unity](https://unity.com/) très basique.

Ça a commencé avec un petit jeu de bowling, puis ça s'est étendu à un jeu simple avec un joueur controllable, un ennemi qui essaie de le tuer, et des collectibles.

### Bot Discord — 2018-2021
En avril 2018 j'ai fait un bot discord en Java pour un serveur roleplay privé dont le thème était un restaurant tenu par le [Chef Kawasaki](https://kirby.fandom.com/wiki/Chef_Kawasaki).

Quand des gens parlaient dans le chat, ils recevaient une certaine quantité d'argent virtuel nommé le *Kawadollard*

Puis, en tappant certaines commandes dans le chat, ils pouvaient recevoir la liste des plats disponibles avec leur prix, et ils pouvaient en commander un à l'aide d'une autre commande.

Le bot envoyait ensuite une photo du plat demandé (avec un message "voici votre plat") et retirait du compte de la personne le prix du plat commandé.

Le bot avait également quelques commandes administrateur qui utilisaient un système de power (un utilisateur normal avait un power de 0, un modérateur en avait un de 50 et un administrateur en avait un de 150) qui permettait de faire quelques bêtises avec, comme ajouter ou enlever de l'argent du compte des utilisateurs, ou envoyer un message donné dans un salon spécifique.

Après 7 mois, le serveur a fermé puis a réouvert en mai 2019 pendant deux mois. Le bot a reçu une mise à jour 2.0, qui contenait de nouveaux plats des des jeux comme le morpion

Puis après avoir à nouveau fermé, le serveur est revenu pour une saison trois en mars 2020 pendant le confinnement, pour une durée de deux mois. J'ai ajouté de nouveaux plats au bot et l'ai mis à jours vers la dernière version de la librairie Discord de l'époque.

Puis avec le COVID et la canicule, la saison quatre du serveur s'est invitée plus tôt que prévu en août 2020 (encore pendant deux mois) avec un système de plats complètement réécrit et un meilleur système pour gérer son argent.

Enfin, en juillet 2021, le serveur a eu sa cinquième et dernière saison à ce jour, encore une fois pendant deux mois. Le bot a eu sa plus grosse mise à jour: un jeu de gestion complet était en cours de création qui consistait en la culture d'ingrédients et essayer de créer des plats en utilisant ces derniers, ou se tromper était fréquent mais réussir valait sacrément le coup! Malheureusement, je n'ai pas pu le finir à temps. Quelques changements de QdV ont été aussi effectués, comme l'ajout d'un salaire quotidien qui serait plus haut pour les membres les plus actifs.

J'adorerais reprendre ce projet un jour et faire une saison six, mais pour ça il faudrait que je trouve la motivation de finir le jeu de gestion! Mais qui sait, peut-être pendant l'été 2023...

### Outils divers — 2019-Aujourd'hui

À chaque fois que j'ai besoin d'automatiser quelque chose sur mon ordinateur, j'ai pris l'habitude d'écrire un programme pour le faire.

Besoin de convertir en masse des fichiers d'un format vers un autre ? Écrit un programme pour le faire. Besoin d'ajouter ou soustraire un nombre donné à chaque nombre dans un fichier texte spécifique ? Écrit un programme pour le faire.

Ce genre de petits programme, quoi.

## Université — 2022-Aujourd'hui

J'ai commencé l'université en septembre 2022. Le nom officiel de ma formation est "BUT Informatique, Parcours Réalisation d'applications : conception, développement, validation".

Pour le dire un peu plus clairement, c'est une formation dans l'informatique qui porte sur la conception, le développement et la validation d'applications. (Par "application" je ne veux pas dire application mobile, je veux dire tout type d'application. Le mot le plus approprié serait "logiciel".)

Ma formation se fait en trois ans, donc elle devrait se terminer vers juillet 2025 pour moi.

Dans cette section, je vais écrire des petites entrées de journal sur mon ressenti là-bas et sur ce que j'ai appris jusqu'ici.

### Entrée 1: 9 mars 2023

L'université se passe bien mieux que ce à quoi je m'attendait en fait, mis à part quelques trucs.

Pendant le premier semestre, on a vu:
* Les concepts de base de la programmation (avec du C++)
* La base du HTML/CSS, quelques trucs en JS
* La base de l'architecture des ordinateurs (avec [Logisim](http://www.cburch.com/logisim/|Logisim))
* La base des bases de données (En théorie et en pratique avec du SQL)
* La base des systèmes d'exploitation (surtout les bases de Linux, honnêtement)

Je connaissait déjà la plupart de ce qu'on a vu en C++, mais le reste était nouveau pour moi. J'ai été complètement ébloui par les cours d'architecture des ordinateurs, même si j'ai déjà quelques bases grâce à mes deux années passées à écrire de l'assembleur PowerPC.

Donc ouais, des trucs cool ! Mais je m'attendait à plus niveau web: on n'est pas allé très en profondeur sur le JS, et on a à peine mentionné le PHP. J'espère que je pourrait m'améliorer là dessus à un moment ou à un autre, car actuellement je suis incapable de faire un site web correct.

Pourtant, la partie la plus surprenante de tout ça est le fait que je me soit fais des amis. C'était le truc qui m'inquiétait le plus, et ça s'est si bien passé ! Je ne mange plus seul le midi et j'ai des gens avec qui parler, donc c'est cool !

Bien entendu, il faut que je parle de mes notes. J'en suis assez fier et je pense que ça peut servir de les exposer ici.

On divise nos notes en six modules, dans lequels notre moyenne est divisée. Il n'y a pas de moyenne "générale", c'est six moyennes avec un nom associé à chacune.
Beaucoup de notes comptent dans plusieurs modules, donc certaines moyennes sont très proches.

On note sur 20 ici, d'ailleurs:
* Réaliser une application: 19.87/20 (rang 1/26)
* Optimiser une application: 19.86/20 (rang 1/26)
* Administrer, configurer, déployer et maintenir un système informatique ou une application: 17.66/20 (rang 1/26)
* Gérer des données et une base de données: 16.92/20 (rang 1/26)
* Conduite un projet: 14.40/20 (rang 5/26)
* Travailler en équipe: 14.61/20 (rang 8/26)

Donc ouais, des bonnes notes quoi, je suis surtout fier des rangs.
Le nom des modules ne représentent pas vraiment ce qu'ils contiennent, donc ne vous concentrez pas trop dessus.

C'est tout pour cette fois! Je pense rendre public certains des projets sur lesquels on a bossé un jour.

## Conclusion

Voilà qui conclut ce "Qui suis-je", j'espère que vous avez apprécié votre temps en le lisant!

Je vais essayer de faire des mises à jour annuelles avec mes nouvelles expériences.

Merci d'avoir lu!

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Matthieu GIROLET, 9 mars 2023
