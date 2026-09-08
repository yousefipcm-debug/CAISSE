# Caisse Espèces — I.P.C.M BOUTEMA

Application web mono-utilisateur pour gérer la caisse espèces de l'entreprise, installable sur iPhone comme une vraie app (PWA).

**App en ligne :** https://yousefipcm-debug.github.io/CAISSE/

## Fonctionnalités

- Enregistrement des entrées et sorties de caisse (montant, description, date, personne, motif, référence)
- Solde recalculé automatiquement
- Impression de décharges individuelles (montant en chiffres et en lettres)
- **Paie des ouvriers** : tableau nom + salaire, génère un état de paie imprimable avec case de signature par ouvrier, et enregistre automatiquement chaque paiement comme sortie de caisse
- Rapports mensuels / globaux imprimables
- Export / import des données en JSON (sauvegarde)

## Installation sur iPhone

1. Ouvrir le lien ci-dessus dans **Safari** (pas Chrome)
2. Appuyer sur le bouton Partager → **« Ajouter à l'écran d'accueil »**
3. L'app s'ouvre en plein écran comme une vraie application

## Stockage des données

Toutes les données (mouvements de caisse) sont stockées **uniquement en local sur l'appareil** (localStorage du navigateur) — rien n'est envoyé sur un serveur. Il est donc important d'exporter une sauvegarde régulièrement (bouton *Exporter les données* dans l'onglet Rapports) et de la conserver ailleurs (iCloud Drive, e-mail, etc.).

## Développement

Fichier unique `index.html`, sans dépendance ni étape de build — toute modification se fait directement dans ce fichier.
