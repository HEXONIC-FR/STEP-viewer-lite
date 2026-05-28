# STEP-viewer-lite

Version allégée de la visionneuse 3D Hexonic (clone de `step_viewer`), destinée à la
**consultation seule**.

Cette version reprend le catalogue et le visualiseur 3D STEP, mais **retire les outils
d'édition** présents dans la version d'origine :

- 🔧 **Outils avancés** (clé à molette) — presets matériaux, sliders lumière / ambiance /
  miroir, sélection de groupe ;
- 💾 **Disquette** — export du message de renommage des groupes vers Claude Code ;
- 🪄 **Iso** (baguette d'isolation 3D) ;
- **Menu de gauche des groupes** (liste des groupes / isolation / filtres).

L'outil de **mesure** (📏) reste disponible.

> Note technique : les éléments masqués restent présents dans le DOM (leurs valeurs par
> défaut d'éclairage pilotent toujours le rendu 3D) mais sont cachés via CSS `!important`
> dans le bloc « VERSION LITE » de `index.html`. La logique de rendu est identique à
> l'original — seule l'interface est simplifiée.

## Lancer en local

```
python -m http.server 8099
# puis ouvrir http://localhost:8099/index.html
```

## Contenu

- `index.html` — visionneuse + catalogue
- `data.json`, `data_pj.json`, `data_tubulaires.json` — données produits
- `libs/` — Online3DViewer (`o3dv`) + import OCCT (WASM)
- `hexonic_blueprint.png`, `hexonic2.png`, `logo.png` — visuels
