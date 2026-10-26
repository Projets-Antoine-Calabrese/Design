# Design — boîte à outils de Claude

Ressources que Claude utilise pour concevoir les interfaces de tous les projets.
Provenance exacte et commits dans `SOURCES.md`.

| Dossier | Contenu |
|---|---|
| `.claude/skills/` | 34 compétences |
| `.claude/agents/` | 5 sous-agents design |
| `references/composants.md` | Bibliothèques de composants (non copiées) |
| `licenses/`, `scripts/` | Licences ; `sources.txt` + `sync.sh` pour mettre à jour |

## Compétences automatiques
| Famille | Compétences |
|---|---|
| Direction artistique (design-taste) | `design-taste` (point d'entrée), `taste-typography`, `taste-color`, `taste-motion`, `taste-gsap`, `taste-design-system`, `taste-design-review`, `taste-code-review`, `taste-code-craft`, `taste-accessibility`, `taste-ux-copy`, `taste-landing-page`, `taste-brand-identity`, `taste-web-performance` |
| Styles prêts à l'emploi (design-taste) | `editorial-minimal`, `quiet-luxury`, `japanese-minimal`, `corporate-trust`, `dark-tech`, `playful-color`, `neo-brutalism`, `brutalist-industrial`, `retro-print`, `cinematic-motion` |
| Officiel Anthropic | `frontend-design`, `theme-factory` |
| Données de design | `ui-ux-pro-max` (base consultable : styles, palettes, typos, graphiques, icônes) |
| Interface et tableaux de bord | `responsive-design`, `interaction-design`, `kpi-dashboard-design`, `data-storytelling` |

## Compétences sur demande (mode manuel)
Claude ne les déclenche pas seul, pour éviter qu'elles se concurrencent ; les appeler par leur nom.
| Commande | Usage |
|---|---|
| `/impeccable` | Auditer, critiquer, peaufiner, animer une interface **existante** |
| `/hallmark` | Créer une **nouvelle** page au rendu « fait main » (48 thèmes, relecture à froid) |
| `/design-taste-frontend` | Direction artistique inspirée de 247 sites primés, contrôle visuel en navigateur |

Sous-agents : `design-ui-designer`, `design-ux-architect`, `design-ui-finish-gate-reviewer` (contrôle final), `design-whimsy-injector`, `design-persona-walkthrough`.

## Sécurité
Chaque source a été vérifiée avant ajout (octobre 2026) : licence libre (MIT, Apache 2.0, domaine public), auteur identifié, projet actif.
Le code exécutable a été relu : pas de lecture de secrets, pas de consignes cachées, connexions réseau limitées à des CDN connus et à des banques d'images publiques.
Règle pour toute nouvelle source : même vérification avant de l'ajouter à `scripts/sources.txt`.

## Mise à jour
`bash scripts/sync.sh` puis commit.
