# Caisse Espèces — I.P.C.M BOUTEMA

Application web mono-utilisateur (PWA) pour gérer la caisse espèces de l'entreprise.
Interface refondue en septembre 2026 : composants natifs iOS (listes groupées, feuilles
modales glissables, pavé numérique, barre d'onglets translucide, glisser-pour-supprimer).

## Contenu

- `index.html` — l'application entière (HTML + CSS + JS, aucune dépendance)
- `manifest.json` — manifeste PWA
- `icons/` — icônes 180px et 512px

## Installation sur iPhone

1. Publier le dossier (GitHub Pages, ou tout hébergement HTTPS).
2. Ouvrir l'adresse dans Safari.
3. Partager → « Sur l'écran d'accueil ».

L'app s'ouvre alors en plein écran, sans barre Safari.

## Fonctions

- **Registre** — solde, totaux entrées/sorties, mouvements groupés par jour ; glisser une ligne vers la gauche pour supprimer.
- **Nouveau mouvement** — pavé numérique, montant en toutes lettres, description, date, personne, motif, référence.
- **Décharge** — document A4 imprimable (en-tête société, montant en lettres, deux signatures).
- **Paie** — saisie ouvrier par ouvrier ; enregistre une sortie par ligne et imprime l'état de paie à signer.
- **Rapports** — filtre par mois, entrées/sorties/solde net, rapport A4 avec solde courant.
- **Sauvegarde** — export et import JSON. Les données restent sur l'appareil (localStorage).

## Données

Tout est stocké dans le `localStorage` du navigateur, clé `ipcm_caisse_espece_v1`.
Exportez une sauvegarde régulièrement : effacer les données Safari efface le registre.
