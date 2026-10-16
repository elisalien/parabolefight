# parabolefight

> Générateur de fiches portraits de personnages animées, au format 16:9 ↔ portrait, avec prévisualisation sur un mur d'écrans Resolume.

![Platform](https://img.shields.io/badge/platform-Web-informational) ![Stack](https://img.shields.io/badge/stack-HTML%20%2F%20CSS%20%2F%20JS-orange)

## À propos

Page web mono-fichier (« Portraits · Pièce ») qui compose une fiche d'identité de personnage au style cyberpunk : nom, titre, signe astro, doctrine, ennemi, arme, citation et jauges de stats. La fiche bascule avec une animation entre un format paysage 16:9 et un format portrait 32:45, et peut être projetée à l'échelle d'un mur d'écrans décrit par un preset Resolume.

## Fonctionnalités

- Formulaire « Fiche d'identité » mis à jour en direct : ID, statut, nom/pseudo, titre/surnom, pronoms, signe astro, âge, aura, territoire, doctrine, ennemi, arme, actes, citation.
- Trois jauges de stats réglables de 0 à 100 : **SEUM**, **FOI**, **CHAOS**.
- Bouton lecture pour basculer la fiche entre 16:9 et 32:45 (transition animée).
- Taille du nom ajustée automatiquement pour tenir dans la carte.
- Valeurs par défaut tirées au hasard à chaque chargement.
- Export / import d'une fiche au format JSON (`portrait-<nom>.json`) et bouton de remise à zéro.
- **Mur d'écrans** : chargement d'un preset Resolume (`.xml`) ; les slices (`Slice`, `PolygonSlice`, `LEDSlice`) sont lues pour afficher le mur, choisir l'écran de départ et faire passer la fiche d'un écran au mur complet.
- Mode plein écran 16:9 (disponible sans preset XML), sortie avec **Échap** ou le bouton « ✕ SORTIR ».

## Installation

Aucune installation : ouvre `index.html` dans un navigateur. Les polices sont chargées depuis Google Fonts (connexion internet requise pour leur affichage).

## Utilisation

1. Remplis les champs de la colonne **Fiche d'identité** et règle les stats : la carte se met à jour en direct.
2. Clique sur le bouton lecture sous la carte pour basculer entre 16:9 et 32:45.
3. **EXPORT** enregistre la fiche en JSON, **IMPORT** recharge un fichier JSON, **RESET** vide tous les champs.
4. Section **Mur d'écrans** : **CHARGER XML** pour importer un preset Resolume, puis choisis l'**écran de départ** ; le bouton lecture fait alors passer la fiche de cet écran au mur complet.
5. Sans preset, **PLEIN ÉCRAN 16:9** affiche la carte seule en plein écran.

Format d'une fiche JSON :

```json
{
  "id": "SEUM-ΔIDEO",
  "status": "LAGGING",
  "name": "Ellie",
  "title": "Alien",
  "pronouns": "iel",
  "sign": "Cancer ♋",
  "age": "29",
  "mass": "inconnue",
  "origin": "Tatami Galaxy",
  "doctrine": "Une chose à la fois ",
  "enemy": "Erreur 404",
  "weapon": "Ordinateurs",
  "acts": "",
  "quote": "Coucou les amis",
  "stats": { "seum": 100, "foi": 0, "chaos": 88 }
}
```

## Structure du projet

| Fichier | Rôle |
|---|---|
| `index.html` | L'application complète (HTML, CSS et JavaScript). |
| `New folder/` | Exemples de fiches exportées (`portrait-*.json`) à réimporter. |

## Stack technique

HTML, CSS, JavaScript vanilla (View Transitions, DOMParser pour les XML Resolume), Google Fonts (DM Serif Display, Share Tech Mono, Space Grotesk).

## Crédits & licence

Polices : DM Serif Display, Share Tech Mono et Space Grotesk via Google Fonts.

Aucune licence n'est spécifiée — tous droits réservés.

---

<p align="center">
  Fait par <a href="https://github.com/elisalien">Élisalien</a> ·
  <a href="https://gitlab.com/elisalien/catalog">Catalogue des shaders, sources & logiciels</a>
</p>
