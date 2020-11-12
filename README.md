# INFOH500
Project
Commentaire du Watermark Project :

Etape1 : Extraire les pixels d’intérêts dans l’image du logo

En utilisant la librairie PIL, l’image ouverte ne peut fournir directement les pixels qui la constituent.(Pas de comparaison numérique possible pour trier). On va donc convertir l’image en mode RGBA pour ensuite extraire sous forme de tuples les valeurs de l’image avec getdata().
Une fois l’accès à l’information de la valeur des pixels possible, on peut trier en parcourant  l’image et ajouter à une liste composées  des tuples désirées. 
Ici, les blancs. Aussi puisqu’il s’agit d’une image binaire, les critères sont simples ( tuple RGBA nul ou R< 150)

2eme étape : Coller le logo sur une image de fond et position

La fonction watermark_picture regroupe les opérations entre les 2 images d’entrées et ainsi construire une image de sortie (output_image) et ce à la position entrée dans la fonction de la librairie PIL , paste(self,box,watermark).

Rmq : Pour afficher l’image finale dans la console jupyter notebook, on utilise la  fontion  show de Matplotlib. (display) plt.imshow(im)

3eme étape :

La transparence du logo se fait grâce au paramètre texture du mode RGBA. En lui assignant une valeur (0 : totalement transparent- 255 : opaque)
