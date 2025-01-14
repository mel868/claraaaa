mel
melissa187533
Invisible

mel
 — 
06/12/2024 01:04
0 idée
Mois de Mai
 — 
06/12/2024 01:04
mdrrrr
Je vais vraiment lui prendre le sextoy
mel
 — 
06/12/2024 01:05
wat ???
Mois de Mai
 — 
06/12/2024 01:05
Il a un restaurant de sushis
Mois de Mai
 — 
06/12/2024 01:05
Elle a mis ça dans sa liste mdrr
mel
 — 
06/12/2024 01:06
AH mmdrrrr
ben oui prends ça de fou hahaha
Mois de Mai
 — 
06/12/2024 01:06
🤣🤣
Qui connaît bien Axel ici ?
mel
 — 
06/12/2024 01:07
jsppp
bilal i guess
Mois de Mai
 — 
06/12/2024 01:07
Il connaît tout le monde
mel
 — 
06/12/2024 01:07
il a pas de wishlist
Mois de Mai
 — 
06/12/2024 01:08
Des chaussettes en forme de sushis
Est ce que ça fait rager juste pcq il a un resto de sushis
mel
 — 
06/12/2024 01:08
mdrrr c'est si nul
Mois de Mai
 — 
06/12/2024 01:08
Y’en a qui rêverait d’avoir des chaussettes : Gaël et Clara
mel
 — 
06/12/2024 01:08
une place en check in
Mois de Mai
 — 
06/12/2024 01:09
Ça c’est un beau cadeau
mel
 — 
06/12/2024 01:09
un coffret scorpio
Mois de Mai
 — 
06/12/2024 01:09
Le rêve
Mois de Mai
 — 
06/12/2024 01:47
Je stress
Mais je fais tjrs rien
Bonne nuit jtm
mel
 — 
06/12/2024 01:47
buena noche
Mois de Mai
 — 
06/12/2024 01:48
Mois de Mai
 — 
10/12/2024 19:43
Transféré
Type de fichier joint : acrobat
push_swap_fr.subject.pdf
1.27 MB
mel
 — 
11/12/2024 14:07
je peux avoir le checker please ?
Mois de Mai
 — 
11/12/2024 14:08
Transféré
Type de fichier joint : unknown
checker_linux
37.30 KB
mel
 — 
11/12/2024 14:08
merci !
Mois de Mai
 — 
11/12/2024 14:08
j’avais grv oublié
mel
 — 
11/12/2024 14:08
ça vient d'où mdrr comment ça tranféré
Mois de Mai
 — 
11/12/2024 14:08
De Han
J’avais sauvegardé sur mon serveur avec Han
mel
 — 
11/12/2024 14:10
hahahah
du génie if you ask me
Mois de Mai
 — 
11/12/2024 14:10
🤣🤣
Mois de Mai
 — 
18/12/2024 18:34
Transféré
Coucou !
Je t'envoie des ressources intéressantes pour le push swap :
https://nervous-whip-ce6.notion.site/push-swap-article-perez-v0
https://github.com/misteraioli
N'hésites pas à aller voir mon github pour ce dernier, et si jamais ça te dit de faire fractol au lieu de so_long, j'ai bien structuré le mien je peux prendre un peu de temps à regarder avec toi si besoin !
Tu peux le partager avec le groupe des futurs cercles 3 en devenir, n'hésitez pas à me contacter les prochaines semaines j'aurai du temps contrairement à début janvier !
Voilà voilà je croise les doigts pour ton minitalk courage 😉
Notion de Perez on Notion
final edit fr | Notion
Introduction
final edit fr | Notion
GitHub
misteraioli - Overview
misteraioli has 6 repositories available. Follow their code on GitHub.
Image
mel
 — 
04/01/2025 22:16
Transféré
pour ceux qui savaient pas, on a copilot free : https://github-portal.42.fr/
Dehors Luna  •  25/12/2024
preuve n°1
Transféré
mais depuis que j'ai découvert l'autocomplétion de copilot ma vie a changé
Dehors Luna  •  28/12/2024
evidence number 2
et ce ne sont que les preuves écrites...
Mois de Mai
 — 
04/01/2025 22:17
mdrerrr
c recent un jour de fete
mel
 — 
07/01/2025 15:50
Image
mel
 — 
09/01/2025 01:12
toi quand on va te livrer le cadeau
Image
Mois de Mai
 — 
09/01/2025 02:47
Ptdrrrr on a vraiment le même feed
mel
 — 
Hier à 18:22
https://www.pap.fr/annonces/appartement-saint-denis-r432600426
mel
 — 
Aujourd’hui à 18:20
Transféré

Le Main :

- Le parsing : vérifier que l’input =
    - soit “mandelbrot”
    - soit “julia” avec 2 double
- sinon : afficher un message pour demander d’entrer ça

Afficher plus
message.txt4 Ko
﻿
Mois de Mai
_mai42

Le Main :

- Le parsing : vérifier que l’input =
    - soit “mandelbrot”
    - soit “julia” avec 2 double
- sinon : afficher un message pour demander d’entrer ça
- Lancer les fonctions :
    - init_fractal pour initialiser la bibliothèque MiniLibX et configurer les évènements de façon sécurisée (préparer le terrain)
    - fractal_render pour “faire” la fractale avec les formules en affichant les pixels avec la couleur adéquate  + en gérant les zooms
    - mlx_loop = une fonction de minilibx pour garder la fenetre ouverte tant qu’on l’a pas fermé (au lieu de se fermer dès la fin du main.
    - close_handler pour tout fermer de façon sécurisée.

Le init :

Initialise la fênetre et “récolte” les données nécessaires pour la fractale :

1. init_data

Si c’est julia : récolter les double des arguments avec la fonction atod (atoi pour les double)

Après c’est des données arbitraires pour esc_value (= correspond au point de divergence choisi pour savoir quand il “sort” du cercle) et c’est ce qui determiner la taille du cercle. Je crois que ça correspond à la racine carré du rayon, un truc comme ça.

pareil pour nb_iter, c’est arbitraire

1. init_mlx

c’est pareil sur tous les projets graphiques, c’est pour lancer la fenêtre quoient, je saurais pas expliquer en détail

1. Init event

pour initialiser le fait qu’on va utiliser clavier, souris…

1. init fractal

on initialise le tout et si c’est pas bon on envoie un message d’erreur

Le event :

On gere les input périphérique… voila… facile à comprendre, mais jette un bon coup d’oeil à la derniere fonction

Utils

1. Atod t’as capté
2. map : pour passer d’une échelle à une autre, on va utiliser une formule de proportionnalité. On s’en sert dans la fonction d’apres pour s’adapter à la plage r, v ou b qui sont différentes
3. color_grad : le nom est explicite, pour rouge, vert ou bleu on détermine une valeur min et max possible et ensuite on retourne celle qui correspond à la valeur donnée en paramètre. Donc plus la valeur est élevée, plus l’intensité de la couleur l’est.
4. sum_complex, tres explicite aussi, ça additionne 2 nombres complexes avec leurs parties reelles et imaginaires
5. square complex : t’as capté, carré de complexe

Render :

= le coeur du programme

1. select_fractal : initalise le c de la structure en fonction de la fractale choisie.
2. handle pixel : vrmt la grosse fonction. Elle va trouver la couleur de chaque pixel en fonction du nb de fois que ça rentre dans le cercle
    1. balaie chaque pixel (x,y) et lui assigne une coordonnée z à la place pour obtenir ça, on fait un calcul qui est dur à expliquer mais vrmt pas dur à comprendre, j’aurai du faire un schéma tout à l’heure mais du coup débrouille toi (on va pas te poser de question sur ce point en sah, imo)
    2. cependant, tu remarqueras qu’on prend en compte le zoom en dessous et qu’on le modifie dans la structure en fonction de ça
    3. La boucle while : en fonction du nombre d’itération donné (ici 16 je crois, mais comme j’ai dit, c’est arbitraire), on applique la formule et, si on dépasse le cercle (avec esc_value) alors on a divergé et on colorie en fonction. (s’il ne diverge pas = noir)
