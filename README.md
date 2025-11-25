# MCU-Order
MCU


**Commandes Git Essentielles**

git init	Initialisation. Transforme le dossier courant en dépôt Git local. (À faire une seule fois par projet.)	"git init"

git status	Vérification. Affiche l'état des fichiers (modifiés, ajoutés, non suivis).	"git status"

git add .	Staging. Ajoute tous les fichiers modifiés/nouveaux à la zone de préparation pour le commit.	"git add ."

git commit -m "message"	Sauvegarde Locale. Enregistre officiellement les changements dans l'historique local. Le message doit décrire la modification.	"git commit -m "feat: ajout du formulaire de contact""

git push origin main	Sauvegarde Distante. Envoie les commits locaux de la branche main vers le dépôt GitHub (origin).	"git push origin main"

git pull origin main	Mise à Jour. Télécharge et fusionne les dernières modifications depuis GitHub vers votre dépôt local.	"git pull origin main"

git branch	Branche. Affiche toutes les branches locales.	"git branch"

git checkout -b <nom>	Nouvelle Branche. Crée une nouvelle branche de travail et bascule immédiatement dessus.	"git checkout -b feature-nouvelle-page"

git checkout <nom>	Changement de Branche. Bascule vers une branche existante.	"git checkout main"

git merge <branche>	Fusion. Intègre les changements d'une branche dans la branche actuelle (par exemple, fusionner la branche de fonctionnalité dans main).	"git merge feature-contact"


**Le Workflow de Branche**

Démarrer	git checkout main puis git pull origin main	Assurez-vous d'avoir la version la plus récente de la branche stable.
2. Isoler	git checkout -b feature-nom-de-la-tache	Créez un bac à sable sécurisé pour votre nouvelle fonctionnalité/correction.
3. Coder/Commit	git add . & git commit -m "..."	Travaillez et enregistrez vos progrès localement.
4. Préparer le Test	git push origin feature-nom-de-la-tache	Envoie la branche de travail sur GitHub pour créer un Aperçu de Déploiement Vercel.
5. Finaliser	(Sur GitHub :) Créez une Pull Request, demandez une revue, puis fusionnez dans main.	
6. Déploiement	git push origin main	Vercel s'occupe de la mise en production.


**Vercel**

Déploiement Continu (CI/CD)	Vercel surveille votre dépôt GitHub. Chaque git push sur la branche main déclenche un déploiement et met le site à jour automatiquement en production.
Production URL	L'adresse finale et stable du site (ex: mcu-order.vercel.app). Mise à jour uniquement par les commits sur la branche main.
Preview URL	Une adresse temporaire et unique générée pour chaque branche ou Pull Request.
Utilité Client	Permet aux clients ou aux testeurs de voir et de valider les nouvelles fonctionnalités (ex: le formulaire de contact) sur une URL dédiée avant que ces changements n'arrivent sur le site principal.
Configuration	Une fois Vercel lié à GitHub, la configuration pour un site statique est automatique.
