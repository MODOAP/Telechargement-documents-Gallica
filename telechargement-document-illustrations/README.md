# Telechargement des illustrations de documents Gallica

Ce carnet propose de télécharger les illustrations de documents Gallica.

Les illustrations sont repérées par le processus d'OCR utilisé par Gallica. Les documents doivent donc être disponibles "en mode texte" sur Gallica.

Le carnet télécharge les illustrations du document au format JPG, et référence les informations des illustrations dans un fichier structuré au format JSON.

Les identifiants ark des docs à télécharger peuvent être listés dans une colonne d'un fichier .xlsx présent sur le drive. 
Le dossier exemple_liste_identifiants contient un exemple de fichier .xlsx listant 5 documents Gallica.

Ce carnet utilise l'API Document de Gallica (https://api.bnf.fr/fr/api-document-de-gallica)

Nécessite un compte Google et la synchronisation d'un Drive.

## Utilisation


1. Ouvrir le carnet dans l'interface Google Colab [![Open In Colab](colab.svg)](https://colab.research.google.com/github/paulbin501/t1/blob/main/t1.ipynb) et se connecter à un compte Google Drive ?????????????????????

2. Lancer la première cellule "Préparation du script et synchronisation d'un Google Drive" et cliquer sur le lien généré pour synchroniser un compte Drive si demandé.
Cette cellule importe les bibliothèques nécessaires à l'utilisation du carnet, et connecte un compte Drive.

### Pour télécharger les illustrations d'un seul document Gallica :

3. Dans la cellule **A partir d'un identifiant ARK** :
	- Spécifier l'identifiant ark d'un document Gallica disponible en mode texte et comprenant des illustrations.
	- Spécifier un dossier de sortie où télécharger les illustrations
	- Réduire la taille des images téléchargées si besoin (laisser 100% pour ne pas réduire)
	- Lancer la cellule


### Pour télécharger les illustrations de plusieurs documents Gallica : 

3. Dans la cellule **A partir d'un fichier tableur** :
	- Spécifier le chemin vers un fichier .xlsx sur le Drive comprenant les identifiants ark dans une colonne
	- Spécifier l'indice de la colonne du fichier contenant les identifiants ark.
	- Spécifier un dossier de sortie où télécharger les illustrations
	- Réduire la taille des images téléchargées si besoin (laisser 100% pour ne pas réduire)
	- Lancer la cellule
	
	
Consulter un tutoriel sur l'utilisation générale des carnets Colab (?????????????????????????)
