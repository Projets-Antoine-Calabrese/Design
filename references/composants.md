# Bibliothèques de composants — catalogue

Ces bibliothèques ne sont **pas copiées** ici (trop lourdes, et conçues pour React / Next / Tailwind).
Nos applications sont des pages HTML autonomes : on s'en sert comme **modèles à transposer** en HTML/CSS/JS natif.
Pour lire le code d'un composant : `git clone --depth 1 <lien>` dans un dossier temporaire.

| Bibliothèque | Ce qu'elle apporte | Composants notables | Pile | Licence | Utilisable tel quel ? |
|---|---|---|---|---|---|
| [paper-design/shaders](https://github.com/paper-design/shaders) | Fonds animés WebGL (dégradés, textures, bruit) | mesh-gradient, grain-gradient, dot-grid, paper-texture, waves, liquid-metal, halftone-dots, god-rays, water | **Vanilla JS sans dépendance** (`@paper-design/shaders`) + version React | Apache-2.0 | **Oui** — import ESM depuis jsDelivr, version épinglée |
| [ibelick/motion-primitives](https://github.com/ibelick/motion-primitives) | Micro-animations d'interface | animated-number, sliding-number, text-effect, text-shimmer, border-trail, progressive-blur, in-view, morphing-dialog, transition-panel, tilt, magnetic | React + motion + Tailwind | MIT | Non — transposer en CSS / Web Animations API |
| [DavidHDev/canvas-ui](https://github.com/DavidHDev/canvas-ui) | Effets visuels dessinés sur `<canvas>` | particle-reveal, decrypt-reveal, ripple, glass, liquid, frost, glitch, retro-dither, ascii | React/Next (moteur canvas réutilisable) | MIT + Commons Clause (usage OK dans une appli, revente interdite) | Partiellement — la logique canvas se porte bien |
| [ui-layouts/uilayouts](https://github.com/ui-layouts/uilayouts) | Composants et mises en page créatifs | animated-beam, spotlight-cards, marquee, drawer, timeline-animation, motion-number, liquid-glass, image-reveal, color-picker | React + Tailwind + framer-motion | MIT | Non — transposer |
| [ui-layouts/cursify](https://github.com/ui-layouts/cursify) | Curseurs animés | blob-cursor, neoncursor, fairydust, neural-glow, text-flag | React + Tailwind | aucune déclarée → **inspiration seulement, ne pas copier** | Non |

## Quand y penser
- **Chiffres qui évoluent** (soldes, poids, kcal) → motion-primitives `animated-number` / `sliding-number`.
- **Fond d'écran d'accueil ou en-tête** → paper-shaders `mesh-gradient` / `grain-gradient` (discret, respecter `prefers-reduced-motion`).
- **Apparition au défilement** → motion-primitives `in-view`, uilayouts `timeline-animation`.
- **Révélation d'un résultat** (bilan, objectif atteint) → canvas-ui `particle-reveal`, `decrypt-reveal`.
- Curseurs : gadget sur ordinateur, inutile sur mobile — à éviter dans des outils du quotidien.

## Sources écartées
Voir `references/veille.md` du dépôt Pilotage.
