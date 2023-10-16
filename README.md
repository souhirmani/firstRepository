# firstRepository
Partie 1: Préparation de l'environnement Git
 1. création de clé SSH
 Dans la premiére etape j'ai installée d'abord git bash pour gérer les commandes.
 Tout d'abord gérer clé SSH par la commande : ssh-keygen -t rsa -b 4096 -C votreadresse@email.com
 pour voir la clé SSH en utilisant la commande :cat ~/.ssh/id_rsa.pub et le copier
 Aprés j'ai connectée sur mon compte github est j'ajoute un nouveau clé dans les paramétres.

 2. Configuration de git
  cette etape pour configurer mon identité globale : 
  avec mon nom d'utilisateur : git config --global user.name "Votre Nom"
  et mon email : git config --global user.email votre@email.com

  3. Connexion SSH aux dépôts distants
  j'ai testé mon connexion SSH par la commande : ssh -T git@github.com

Partie 2: Création d'un nouveau projet
 1. j'ai déja connectée sur mon compte github
 2. j'ai crée un nouveau repository appellée firstRepository avec un clé public et avec README
 3.  Clonez mon projet sur mon pc (local) en utilisant l'URL SSH : git clone git@github.com:votre-nom-utilisateur/mon-projet.git
 4. maintenant mon projet cloné avec succés sur mon pc locale et je l'accédé avec la commande : cd firstRepository

Partie 3 : Concepts de base de Git
 1. Travailler avec les fichiers
   Création du fichier "index.html" : touch index.html
   j'ajoute le contenu dans "index.html" : echo "Contenu de votre fichier" > index.html
   j'ajout le fichier dans mon projet : git add index.html
   Enregistrer mon premiére commit sur local avec un message : git commit -m "Premier commit : ajout de index.html"

 2. Historique des commits
  Pour voir la liste des commit que je fais : git log
  pour afficher les différences entre deux commits : git diff commit_id_1 commit_id_2

Partie 4 : Collaborer sur Git
 1. par defaut il ya la branche MASTER , j'ai crée une nouvelle branche : git branche ma-fonctionnalite
 et switcher sur la nouvelle branche ma-fonctionnalite : git checkout ma-fonctionnalite
 2. j'ai fait des modification sur le fichier index par la commande : echo "Premiere commit:ajout de l'index.html" > index.html
  puis j'ai l'ajoutée : git add .
  et j'ai fait la commit : git commit -m "Modification de ma-fonctionnalite"
  et l'enregistrer : git push origin ma-fonctionnalite
 3. Geston des conflits:
  j'ai changer le contenu du fichier index.html puis j'ai changer le contenu du fichier index2.html et j'ai fait l'ajout avec git add . 
  et puis avec la commande :  git merge ma-fonctionnalite 

Partie 5 : Utilisation de gitFlow
 1. initialisation de gitflow : git flow init
 2. crée d'un nouvel fonctionnalite : git flow feature start ma-fonctionnalite
 3. crée une nouvelle version : git flow release start ma-version
 4. fusionnez la branche de fonctionnalité avec la branche de développement : git flow feature finish ma-fonctionnalite
 5. création d'un correctif : git flow hotfix start mon correctif





 

