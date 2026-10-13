# Nina Carducci — Optimisation d'un site de photographe

Optimisation du site de Nina Carducci, une photographe fictive installée à Bordeaux. Le site existait déjà, mais il était lent, mal référencé et sa galerie comportait des bugs : je l'ai amélioré sans le refaire.

Projet de la formation Développeuse web d'OpenClassrooms.

**Site en ligne : <https://oudin-deborah.github.io/p4_optimisation/>**

![Aperçu du site de Nina Carducci](https://oudin-deborah.github.io/Portfolio/Nina_Carducci.webp)

## Ce qui a été optimisé

- **Performance** : images converties en WebP, fichiers CSS et JavaScript minifiés.
- **Référencement** : titre et description de page rédigés autour de l'activité et de la ville, données structurées Schema.org pour le référencement local.
- **Accessibilité** : texte alternatif décrivant chaque photo, libellés sur les commandes du carrousel.
- **Corrections de bugs** : filtres de la galerie et navigation dans la modale d'agrandissement.

## Technologies

| Rôle | Outil |
|---|---|
| Structure | HTML5 |
| Mise en page | Bootstrap 5 et feuille de style du site |
| Galerie | Plugin jQuery `mauGallery` (fourni, puis corrigé) |
| Images | Format WebP |
| Référencement | Balises `meta`, données structurées JSON-LD (Schema.org) |
| Mesure | Lighthouse |
| Hébergement | GitHub Pages |

## Installation

Aucune dépendance à installer.

```bash
git clone https://github.com/Oudin-Deborah/p4_optimisation.git
cd p4_optimisation
```

Ouvrir ensuite `index.html` dans un navigateur, ou lancer l'extension Live Server de VS Code.

## Structure du projet

```
├── assets/
│   ├── bootstrap/          Bootstrap (CSS et JavaScript)
│   ├── images/             Photos du carrousel et de la galerie, en WebP
│   ├── maugallery.js       Galerie filtrable : version lisible
│   ├── maugallery.min.js   Galerie filtrable : version minifiée, chargée par la page
│   ├── scripts.js          Initialisation de la galerie
│   ├── scripts.min.js
│   ├── style.css           Styles du site
│   └── style.min.css
└── index.html
```

Chaque fichier minifié est conservé à côté de sa version lisible : la page charge la version minifiée, le développement se fait sur l'autre.

## Choix techniques

- **Mesurer avant et après** : les audits Lighthouse ont servi à repérer ce qui ralentissait la page, puis à vérifier l'effet de chaque optimisation.
- **WebP pour toutes les photos** : sur un site de photographe, les images représentent l'essentiel du poids de la page.
- **Données structurées de type `LocalBusiness` et `Photographer`** : elles indiquent aux moteurs de recherche l'adresse, les horaires et le métier, ce qui compte pour une activité locale.
- **Corriger plutôt que remplacer** : les bugs de la galerie ont été réglés dans le plugin existant, sans changer de bibliothèque.

## Pistes d'amélioration

- Mettre à jour les adresses contenues dans les données structurées, qui pointent encore vers un ancien compte GitHub.
- Héberger les polices avec le site plutôt que de les charger depuis Google Fonts.
- Remplacer la bibliothèque Bootstrap complète par les seuls composants utilisés.
- Ajouter les balises Open Graph pour un meilleur aperçu lors d'un partage sur les réseaux sociaux.

## Crédits

- Site d'origine, photos et plugin de galerie : OpenClassrooms.
- Optimisation : Déborah Oudin — [Portfolio](https://oudin-deborah.github.io/Portfolio/) · [LinkedIn](https://www.linkedin.com/in/oudin-deborah/) · [GitHub](https://github.com/Oudin-Deborah)
