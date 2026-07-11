# TDAH Oculaire — Test d'attention visuelle 👁️

Petite application web (une seule page, sans dépendance) qui propose deux
mini-tests d'attention visuelle inspirés des tests de performance continue
(CPT) utilisés en neuropsychologie :

1. **Attention soutenue (Go / No-Go)** — des lettres défilent ; on réagit à
   chacune *sauf* le « X ». Mesure les oublis (inattention) et les réactions
   sur le « X » (impulsivité).
2. **Poursuite oculaire** — un point se déplace ; on le suit des yeux et on
   réagit quand il change de couleur.

À la fin, un **score global sur 100** est calculé avec le détail :
attention soutenue, contrôle des impulsions, régularité et vitesse de réaction.

> ⚠️ **Avertissement** — Cet outil est **éducatif et de sensibilisation**. Il
> ne constitue **pas** un diagnostic. Seul un professionnel de santé
> (médecin, psychiatre, neuropsychologue) peut poser un diagnostic de TDAH.

## Confidentialité

Tout s'exécute **localement dans le navigateur**. Aucune donnée n'est envoyée
ni stockée sur un serveur.

## Utilisation

Ouvrez simplement le site (voir GitHub Pages ci-dessous), ou ouvrez
`index.html` dans un navigateur. Fonctionne au tactile (mobile/tablette) et à
la souris/clavier (barre **Espace** pour répondre).

## Publication en ligne (GitHub Pages)

Le dépôt inclut un workflow (`.github/workflows/deploy-pages.yml`) qui publie
automatiquement le site à chaque push sur `main`.

Pour l'activer une première fois :

1. Fusionnez cette branche dans `main`.
2. Allez dans **Settings → Pages** du dépôt.
3. Dans **Build and deployment → Source**, choisissez **GitHub Actions**.

Le site sera alors disponible à l'adresse :

```
https://ckartier.github.io/TDAH/
```

*(Alternative sans workflow : Settings → Pages → « Deploy from a branch » →
branche `main`, dossier `/root`.)*

## Développement

Aucune installation nécessaire — c'est du HTML/CSS/JS pur dans `index.html`.
Pour tester localement :

```bash
python3 -m http.server 8000
# puis ouvrir http://localhost:8000
```
