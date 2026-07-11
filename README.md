# TDAH Oculaire — Batterie d'attention & dépistage 👁️

Application web (une seule page, sans build) réunissant plusieurs tests
d'attention et d'impulsivité, plus un questionnaire de dépistage. Chaque
module se lance seul depuis le menu, ou en **parcours complet**, et une
**synthèse** agrège les résultats.

## Modules

1. **Questionnaire ASRS v1.1** — auto-évaluation des symptômes (18 items,
   échelle de dépistage adulte de l'OMS). Scoring officiel de la Partie A
   (≥ 4 marques = dépistage positif). C'est l'indicateur le plus prédictif.
2. **Attention soutenue (Go / No-Go)** — des lettres défilent ; on réagit à
   chacune *sauf* le « X ». Mesure les oublis (inattention), les réactions
   sur le « X » (impulsivité) et la variabilité des temps de réaction.
3. **Test de Stroop** — nommer la *couleur de l'encre* d'un mot de couleur.
   Mesure l'inhibition et le contrôle de l'interférence.
4. **Test Stop-Signal** — répondre au sens d'une flèche, sauf quand un signal
   d'arrêt apparaît. Calcule le **SSRT** (référence de l'inhibition motrice)
   via un escalier adaptatif du délai d'arrêt (SSD).
5. **Suivi oculaire (webcam)** — oculométrie approximative via
   [WebGazer.js](https://webgazer.cs.brown.edu/) : calibration puis mesure de
   la stabilité de fixation et de la précision de poursuite. **La vidéo ne
   quitte jamais l'appareil.**

La synthèse compte le nombre de « signaux évocateurs » parmi les tests
réalisés et fournit une interprétation prudente.

> ⚠️ **Avertissement** — Cet outil est **éducatif et de sensibilisation**. Il
> ne constitue **pas** un diagnostic. Seul un professionnel de santé
> (médecin, psychiatre, neuropsychologue) peut poser un diagnostic de TDAH.
> Le TDAH se manifeste sur la durée, depuis l'enfance et dans plusieurs
> contextes de vie : un test ponctuel ne peut ni le confirmer ni l'exclure.

## Confidentialité

Tout s'exécute **localement dans le navigateur**, y compris la vidéo de la
webcam. Aucune donnée n'est envoyée ni stockée sur un serveur. Seule dépendance
externe : le script WebGazer, chargé depuis un CDN uniquement si tu lances le
module de suivi oculaire.

## Utilisation

Ouvrez le site (voir GitHub Pages ci-dessous), ou ouvrez `index.html` dans un
navigateur. Fonctionne au tactile (mobile/tablette) et à la souris/clavier
(barre **Espace** pour le Go/No-Go, flèches **←/→** pour le Stop-Signal).

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
