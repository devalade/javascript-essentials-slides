# JavaScript Essentials - Slides

Slides de présentation interactive sur les fondamentaux JavaScript.

## Présentation

Ce projet contient une présentation interactive créée avec [Slidev](https://sli.dev/) couvrant les concepts essentiels de JavaScript.

## Démarrage rapide

### Prérequis

- [Node.js](https://nodejs.org/) (version 18 ou supérieure)
- [pnpm](https://pnpm.io/) (recommandé)

### Installation

```bash
# Cloner le repository
git clone https://github.com/devalade/javascript-essentials-slides.git
cd javascript-essentials-slides

# Installer les dépendances
pnpm install

# Lancer le serveur de développement
pnpm dev
```

L'application sera accessible à l'adresse : http://localhost:3030

### Commandes disponibles

| Commande | Description |
|----------|-------------|
| `pnpm dev` | Lancer le serveur de développement |
| `pnpm build` | Générer la version de production |
| `pnpm export` | Exporter les slides en PDF |

## Structure du projet

```
.
├── components/          # Composants Vue personnalisés
├── pages/              # Pages additionnelles
├── snippets/           # Extraits de code réutilisables
├── slides.md           # Contenu principal des slides
├── package.json        # Configuration du projet
└── README.md           # Ce fichier
```

## Technologies

- [Slidev](https://sli.dev/) - Framework de présentation basé sur Vue
- [Vue.js 3](https://vuejs.org/) - Framework JavaScript progressif
- [Vite](https://vitejs.dev/) - Build tool rapide

## Licence

Ce projet est sous licence [CC BY 4.0](LICENSE) - Creative Commons Attribution 4.0 International.

## Auteur

Créé avec ❤️ par [@devalade](https://github.com/devalade)

---

**Note** : Pour modifier le contenu des slides, éditez le fichier [`slides.md`](./slides.md).

En savoir plus sur Slidev dans la [documentation officielle](https://sli.dev/).
