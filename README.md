# Hamo Tefess Store

Boutique officielle en ligne des 72 Heures de Hamo Tefess (18–20 septembre 2026).
Site statique en HTML/CSS/JS pur — aucune installation ni build nécessaire.

## Structure du projet

```
.
├── index.html          → la boutique complète (page unique)
└── assets/
    ├── logo-hamo-tefess.png     → logo (repris directement du t-shirt, inchangé)
    ├── tshirt-blanc-face.png
    ├── tshirt-blanc-dos.png
    ├── tshirt-noir-face.png
    └── tshirt-noir-dos.png
```

## Fonctionnalités

- Catalogue avec 2 produits (t-shirt blanc / noir), choix de taille et quantité
- Panier en mémoire (compteur, ajout/suppression, total en FCFA)
- Formulaire de commande (nom, téléphone, quartier, adresse, mode de réception)
- Envoi de la commande directement vers WhatsApp au **77 939 26 35** (numéro configurable dans `index.html`, variable `WHATSAPP_NUMBER`)
- Zoom sur les photos produit
- Menu mobile fonctionnel, site responsive (mobile / tablette / desktop)

## Déployer sur GitHub Pages

1. Crée un nouveau dépôt sur GitHub (ex. `hamo-tefess-store`).
2. Mets `index.html` et le dossier `assets/` à la racine du dépôt (garde exactement cette structure — le HTML référence les images en chemin relatif `assets/...`).
3. Sur GitHub : **Settings → Pages → Source**, choisis la branche `main` et le dossier `/ (root)`, puis **Save**.
4. Après 1-2 minutes, le site est en ligne à l'adresse :
   `https://<ton-nom-utilisateur>.github.io/hamo-tefess-store/`

## Personnalisation rapide

- **Numéro WhatsApp** : dans `index.html`, cherche `WHATSAPP_NUMBER = "221779392635"` et `wa.me/221779392635` (footer + bouton flottant), et remplace par le bon numéro.
- **Prix** : variable `PRICE` en haut du `<script>` (actuellement `5000` FCFA).
- **Date de l'événement** : section `.event-date` dans le HTML.
- **Photos produits / logo** : remplace simplement les fichiers dans `assets/` en gardant les mêmes noms.

## Vérifications effectuées

- JS validé (aucune erreur de syntaxe)
- Toutes les références `id` du JavaScript correspondent bien à des éléments du HTML
- Toutes les balises HTML sont correctement fermées/équilibrées
- Menu mobile, panier, zoom, favoris et commande WhatsApp testés fonctionnellement
