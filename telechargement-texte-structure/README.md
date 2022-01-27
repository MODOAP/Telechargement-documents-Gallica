# ModOAP Téléchargement des blocs de texte de documents Gallica en format structuré

Ce carnet propose de télécharger les blocs de texte de documents sur Gallica, dans un format structuré au sein d'un fichier json.
Ce type de téléchargement conserve en plus du texte de chaque bloc le numéro de la page correspondante et la position du bloc dans la page.

Les documents dont on souhaite télécharger le texte doivent avoir subi un traitement de reconnaissance de caractères (OCR), c'est à dire qu'ils doivent être disponibles "en mode texte" sur Gallica. 
Ces documents sont spécifiés par leur identifiant unique ARK.

Le script télécharge les blocs de texte de chaque document dans un fichier structuré au format .json Ce fichier .json n'est pas destiné à être lu : il est utilisé par d'autres scripts ModOAP pour des traitements textuels ultérieurs.

L'utilisateur peut au choix télécharger les blocs de texte d'un seul document Gallica en renseignenant directement un identifiant ark, ou télécharger les blocs de texte d'une liste d'identifiants ark dans un fichier tableur. 

Ce carnet nécessite de synchroniser un compte Google Drive.

Il repose sur l'API Document de Gallica : https://api.bnf.fr/fr/api-document-de-gallica#/


## Utilisation

1. Ouvrir le carnet dans l'interface Google Colab et se connecter à un compte Google Drive 

2. Lancer la première cellule et cliquer sur le lien généré pour synchroniser un compte Drive si demandé.
Cette cellule importe les bibliothèques nécessaires à l'utilisation du carnet, et connecte un compte Drive.

#### Pour télécharger les blocs de texte d'un seul document Gallica :

3. Renseigner les paramètres de la seconde cellule "A partir d'un identifiant ARK" :
	- Spécifier l'identifiant ark dans le champ "ark" :
	- Spécifier le chemin d'un dossier sur le Drive où télécharger le fichier
	- Lancer la cellule

#### Pour télécharger les blocs de texte d'une liste de documents Gallica :

3. Importer sur le Drive un fichier tableur au format .xlsx ou .xlsm dont une colonne contient les identifiants ark des docs à télécharger (un id ark par ligne)

4. Renseigner les paramètres de la troisième cellule "A partir d'une liste d'identifiants ARK" :
	- Spécifier le chemin vers le fichier tableur (.xlsx) contenant les identifiants ark
	- Spécifier l'indice de la colonne contenant les identifiants ARK 
	- Spécifier le chemin d'un dossier sur le Drive où télécharger les fichiers
	- Lancer la cellule
