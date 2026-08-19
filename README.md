# CATRANS Transportation Fees

Manifeste journalier des frais de transport (CATRANS) — application web statique
(HTML + JS, sans framework, sans étape de build) avec :
- écran de connexion (admin / mot de passe, changeable, "mot de passe oublié")
- saisie en ligne avec suggestion automatique
- sauvegarde automatique
- export Excel (téléchargement ou préparation d'email)

## Déploiement

Ce projet est un site 100% statique : un seul fichier `index.html`.
Aucune commande de build n'est nécessaire — il suffit de déployer le dossier tel quel.

## Important

- Les identifiants de connexion et les données du manifeste sont stockés via l'API
  `window.storage`, spécifique à l'environnement Claude.ai. Une fois déployée sur
  Vercel (ou tout autre hébergeur), l'application ne dispose plus de cette API : la
  sauvegarde bascule automatiquement sur une variable en mémoire, valable uniquement
  le temps de la session ouverte dans l'onglet (rien n'est conservé après fermeture
  ou rechargement de la page).
- Pour une persistance réelle une fois en ligne (comptes, données), il faut brancher
  une base de données externe (Supabase, Firebase, etc.).
