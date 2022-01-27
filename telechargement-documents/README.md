# Téléchargement de documents Gallica

Ce carnet permet de télécharger les pages de documents Gallica au format JPG, ou l'ensemble des documents aux formats PDF ou TXT, à partir des identifiants ark des documents. 

Les identifiants ark des docs à télécharger doivent être listés dans une colonne d'un fichier .xlsx présent sur le drive. 
Le dossier exemple_liste_identifiants contient un exemple de fichier .xlsx listant 5 documents Gallica.

Téléchargement des pages des documents au format JPG ou de l'ensemble du document au format PDF ou TXT.

Ce carnet utilise l'API Document de Gallica (https://api.bnf.fr/fr/api-document-de-gallica)

Nécessite un compte Google et la synchronisation d'un Drive.
## Utilisation

1. Ouvrir le carnet dans l'interface Google Colab et se connecter à un compte Google Drive 

2. Lancer la première cellule "Préparation du script et synchronisation d'un Google Drive" et cliquer sur le lien généré pour synchroniser un compte Drive si demandé.
Cette cellule importe les bibliothèques nécessaires à l'utilisation du carnet, et connecte un compte Drive.

3. Dans le cellule **Téléchargement des pages de documents** :
	- Entrer le chemin vers le fichier .xlsx sur le Drive contenant les identifiants ark des documents à télécharger.
	- Préciser l'indice de la colonne du fichier .xlsx contenant les identifiants.
	- Entrer le chemin de destination où télécharger les documents
	- Préciser le format de téléchargement souhaité (JPG = un fichier par page, TXT ou PDF = l'ensemble du document)
	- Préciser la taille des images à télécharger si le format JPG a été choisi. 
	- Lancer la cellule 
