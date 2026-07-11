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

Le site est un simple `index.html` à la racine, servi directement par GitHub
Pages. Pour l'activer (une seule fois) :

1. Le dépôt doit être **public** (Pages sur dépôt privé nécessite un forfait
   GitHub Pro).
2. **Settings → Pages → Build and deployment → Source : « Deploy from a
   branch »**.
3. Branche : **`main`**, dossier : **`/ (root)`** → **Save**.

Après une minute, le site est disponible à l'adresse :

```
https://ckartier.github.io/TDAH/
```

## Développement

Aucune installation nécessaire — c'est du HTML/CSS/JS pur dans `index.html`.
Pour tester localement :

```bash
python3 -m http.server 8000
# puis ouvrir http://localhost:8000
```
