# Telechargement de périodiques sur Gallica


Ce carnet permet de télécharger les pages des parutions de périodiques Gallica au format JPG, ou l'ensemble des parutions aux formats PDF ou TXT, à partir des identifiants ark des documents. 

Téléchargement des pages des documents au format JPG ou de l'ensemble du document au format PDF ou TXT.

Les périodiques sont définis par leur identifiant ark (ex : cb32701734b).

Il est possible de télécharger pour chaque périodique une ou plusieurs année(s) en définissant un intervalle :

Intervalles possibles :

une année = 1894

un intervalle d'années = 1894-1902 (9 années)

certaines années = 1894;1897;1911;1878 (pas de nombre maximum d'années)

Laisser vide signifie la totalité des parutions

Télécharger plusieurs périodiques à partir d'un fichier tableur :

Pour télécharger plusieurs périodiques, spécifier dans la dernière cellule le chemin absolu vers un fichier xls contenant au minimum une colonne sans titre listant les liens Gallica des documents, et une colonne sans titre contenant les indications d'intervalles temporels à télécharger.

Les colonnes sont ensuite précisées par leur indice (ex : A)

Ce carnet utilise l'API Document de Gallica (https://api.bnf.fr/fr/api-document-de-gallica)

Il carnet nécessite un compte Google Drive.

## Utilisation


1. Ouvrir le carnet dans l'interface Google Colab et se connecter à un compte Google Drive 

2. Lancer la première cellule "Préparation du script et synchronisation d'un Google Drive" et cliquer sur le lien généré pour synchroniser un compte Drive si demandé.
Cette cellule importe les bibliothèques nécessaires à l'utilisation du carnet, et connecte un compte Drive.

### Pour télécharger un seul périodique Gallica :

3. Dans la cellule **Télécharger un seul périodique** :
	- Spécifier l'identifiant ark d'un périodique Gallica
	- Spécifier un intervalle d'années en fonction des instructions dans le script
	- Spécifier un chemin de destination où télécharger le périodique
	- Spécifier le format de téléchargement souhaité
	- Réduire la taille des images téléchargées si besoin (si téléchargement des pages au format JPG uniquement)
	- Lancer la cellule


### Pour télécharger plusieurs périodiques Gallica : 

3. Dans la cellule **Télécharger plusieurs périodiques référencés dans un fichier tableur** :
	- Spécifier le chemin vers un fichier .xlsx sur le Drive comprenant les identifiants ark dans une colonne et les intervalles dans une autre.
	- Spécifier l'indice de la colonne du fichier contenant les identifiants ark.
	- Spécifier l'indice de la colonne du fichier contenant les intervalles.
	- Spécifier un dossier de destination où télécharger les périodiques
	- Spécifier le format de téléchargement souhaité
	- Réduire la taille des images téléchargées si besoin (si téléchargement des pages au format JPG uniquement)
	- Lancer la cellule
