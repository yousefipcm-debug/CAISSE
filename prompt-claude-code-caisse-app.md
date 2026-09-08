# PROMPT POUR CLAUDE CODE — Application "Caisse Espèces" IPCM BOUTEMA

## Qui je suis

Je suis Youcef Boutema, gérant de **IPCM BOUTEMA**, une entreprise de sous-traitance de main-d'œuvre spécialisée en construction métallique (centres commerciaux, hangars), basée à Blida, Algérie. J'ai moins de 2 ans d'expérience en gestion. Je gère l'entreprise avec une petite équipe administrative (RH, DFC, Juridique, Secrétariat) et une sœur qui assure la liaison/coordination sur le terrain. L'entreprise n'a pas encore de vrais systèmes internes — je construis ces outils un par un.

## L'entreprise (infos légales pour l'en-tête des documents imprimés)

- Raison sociale : I.P.C.M BOUTEMA
- Adresse : Rue des Frères Djennadi, 3ème étage, Lot 35 Div 96, Blida
- RC : 09/00-4108712A23
- NIF : 16922040023019500900
- NIS : 196922040023050
- BP : 1001369786
- Tél : 0550700196
- Email : direction.ipcmboutema@gmail.com

## Contexte financier

- Une seule caisse espèces + un compte bancaire, en dinars algériens (DZD) uniquement
- Les ouvriers sont payés en partie par virement/fixe, en partie en espèces
- Je suis le **seul utilisateur** de cette application

## Objectif de l'application

Construire une web app simple, **utilisable sur iPhone comme une vraie app** (PWA installable via "Ajouter à l'écran d'accueil" depuis Safari), dont le SEUL rôle est de gérer ma **Caisse Espèces** de l'entreprise — rien d'autre (pas de gestion de projets, pas de RH).

## Fonctionnalités obligatoires

### 1. Entrées et sorties de caisse
- Bouton rapide pour ajouter une **Entrée** (argent reçu) ou une **Sortie** (argent donné/dépensé)
- Champs par mouvement :
  - Date (par défaut aujourd'hui)
  - Type : Entrée / Sortie
  - Montant (DZD)
  - Motif / description
  - Partie concernée (nom de la personne qui a donné ou reçu l'argent)
  - Numéro de pièce/référence (optionnel)
- Le solde de caisse se recalcule automatiquement après chaque mouvement
- Liste des mouvements récents, triable/filtrable par date

### 2. Impression de décharge
- Depuis n'importe quel mouvement, bouton "Imprimer décharge"
- Document PDF/imprimable propre contenant :
  - En-tête entreprise (raison sociale, adresse, RC, NIF, NIS, tél, email — voir infos ci-dessus)
  - Titre "DÉCHARGE"
  - Numéro et date
  - Montant en chiffres ET en toutes lettres (en français, ex : "trente mille dinars algériens (30 000 DA)")
  - Motif
  - Nom de la partie (remis à / reçu de)
  - Deux zones de signature : "Remis par" et "Reçu par"
- Doit s'imprimer correctement au format A4 depuis l'aperçu d'impression natif de Safari iPhone

### 3. Rapports
- Rapport mensuel : mouvements du mois sélectionné + total entrées, total sorties, solde
- Rapport total/global : tous les mouvements depuis le début + solde actuel
- Les deux imprimables/exportables en PDF

## Langue et style
- Toute l'interface et tous les documents imprimés en **français**
- Design simple, sobre, professionnel — priorité à la clarté et à la rapidité de saisie sur mobile, pas besoin d'être flashy

## Contraintes techniques
- Doit très bien fonctionner sur iPhone (Safari), en mode "app" via PWA (manifest + icône + mode standalone)
- Utilisateur unique (moi) — pas besoin de système de comptes/login complexe, mais les données doivent être persistantes et fiables (aucune perte de données en fermant l'app)
- Propose la solution de stockage la plus simple et fiable pour un seul utilisateur (stockage local fiable + export/sauvegarde des données, ou petite base de données si tu juges que c'est plus sûr) — explique-moi ton choix
- Génère les PDF (décharge + rapports) côté app, sans dépendance externe compliquée

## Ce que j'attends de toi
1. Propose une architecture simple adaptée à ce besoin (mono-utilisateur, mobile-first, PWA)
2. Construis l'application avec toutes les fonctionnalités ci-dessus
3. Explique-moi comment l'installer sur mon iPhone une fois prête
4. Explique-moi comment sauvegarder/exporter mes données régulièrement (par sécurité)
