# ProjetVagrant
Vagrantfile pour Soutenance Projet3
PROJET VALIDÉ
Créez votre environnement de travail local
50 heures
Mis à jour le mardi 7 juillet 2020
Docker
Docker
La démarche DevOps est constituée de nombreuses tâches, au service des différent pôles informatiques, développeurs, exploitation, testing, etc. L'une d'entre elles, est la mise en place d'environnements de développement, en local, pour les Développeurs.

Cet environnement, à l’image des serveur cibles, permet aux développeurs de travailler sur un environnement qui reproduit les conditions dans lesquelles leur code fonctionnera.

Dans le même esprit, vous allez mettre en place un environnement de travail en local pour vos besoins. En effet, vous aussi, vous allez avancer pas à pas, et vous devrez régulièrement tester vos scripts et déployer des outils pour les essayer avant de les installer en production.

Votre environnement local doit vous permettre de tester, bricoler, installer, sans risquer d'abimer un serveur, et surtout gratuitement. Il vous sera utile tout au long de votre parcours d’Expert DevOps, et bien sur, il vous sera utile ultérieurement, pour vos propres besoins, ou pour les besoins de vos clients, de vos collègues, tout au long de vos missions.

Cet environnement de travail sera dans une machine virtuelle, vous pourrez donc le déplacer facilement, et vous testerez vos scripts sur un environnement proche de celui de vos serveurs. Il sera mis en place via l’outil d’automatisation Vagrant. Votre machine virtuelle sera décrite dans un fichier propre à Vagrant, le Vagrantfile, que vous pourrez versionner afin de le réutiliser et de le modifier ultérieurement.


Instructions 
Étape 1
Si vous n’en avez pas encore, vous allez vous créer un compte sur Github. Prenez le temps de découvrir l’outil : vous allez travailler tout au long du parcours avec des dépôts de source Git. D’ailleurs, ça commence maintenant  !

Étape 2
Afin de mettre en place cette machine virtuelle, vous utiliserez l'outil Vagrant, qui permet de décrire et de manipuler très facilement les différents éléments de votre environnement.

Assurez-vous d'avoir la place nécessaire pour télécharger des ISO et pour stocker votre machine virtuelle, car une ISO peut faire entre 500 et 800Mo, et une machine virtuelle entre 2 et 16Go.

Installez d’abord votre outil de virtualisation, VirtualBox ou VMWare.

Installez ensuite Vagrant, et faites un premier Vagrantfile avec l'OS Linux avec lequel vous êtes le plus à l'aise, Debian, CentOS, Ubuntu.

N’oubliez pas de “commit” votre travail régulièrement dans votre premier dépôt.

Étape 3
Vous allez maintenant installer des outils dans votre VM Vagrant. Faites évoluer votre Vagrantfile, et ajoutez les lignes nécessaires pour ajouter :

Un éditeur de texte.
Ansible dans sa version la plus récente.
Docker Community Edition dans sa version la plus récente.

Étape 4
Votre environnement de travail contient maintenant tout ce qu’il faut, mais vous aimeriez pouvoir simuler un serveur cible pour tester les différents outils que vous allez utiliser tout au long de ce parcours.

Pour ce faire, nous allons tirer partie du Docker Engine que vous avez installé. Vous configurez une première image qui contiendra un OS Debian, avec les ports SSH mappés correctement. Votre image contiendra un serveur nginx, et devra donc également être accessible en HTTP

 

Livrables attendus
Dans un dossier nommé “Projet_03_Nom_Prenom”, vous mettrez à disposition de votre mentor :

Un Vagrantfile permettant l'installation de l’environnement de travail décrit ci-dessus
Un Dockerfile de provisionnement de container
Un fichier texte nommé “github.txt” qui contiendra l’URL de votre compte Github
Note : Votre compte Github devra contenir un projet pour Vagrant, et un autre pour Docker.

 

A l'oral en condition réelle, vous présenterez vos différents fichiers. Le mentor jouera le rôle d’un développeur que vous guidez dans la mise en place de son environnement de travail. Il exécutera vos différents scripts à l’aide des directives que vous lui indiquerez. Une fois que tout sera en place, il validera la présence des différents éléments.

La soutenance se déroule comme suit :

La présentation de vos fichiers et le lancement des scripts : 20 minutes
Un moment questions/réponses : 10 minutes
Votre mentor reprendra son rôle à la fin de votre "rendez-vous avec le développeur" pour débriefer avec vous pendant 5 minutes.
Compétences évaluées
Mettre en place et utiliser un outil de gestion des environnements de travail
Versionner le code et les configurations
Containeriser une application
