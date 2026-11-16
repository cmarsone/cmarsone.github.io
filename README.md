# Clément Marsone — site personnel

Site personnel en français, généré avec Jekyll et publié sur GitHub Pages. Le design reprend les codes des portfolios éditoriaux et académiques, avec des gabarits locaux pour garder une configuration simple et compatible avec Pages.

## Pages

- `index.md` : présentation et notes récentes
- `notes.md` : archive des articles de `_posts/`
- `about.md` : parcours et contact
- `cycling.md` : dernières sorties Strava

## Développement local

Les dépendances Ruby sont déclarées dans `Gemfile`. Pour lancer le site localement :

```sh
bundle install
bundle exec jekyll serve
```

Les styles du site sont dans `assets/css/style.scss`; les gabarits partagés sont dans `_layouts/` et `_includes/`.
