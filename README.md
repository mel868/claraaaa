

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
