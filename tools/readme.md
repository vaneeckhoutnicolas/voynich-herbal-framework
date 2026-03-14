# 🔮 Voynich Lab — Outil d'analyse interactif à 8 couches
# 🔮 Voynich Lab — 8-Layer Interactive Analysis Tool

---

## 🇫🇷 Français

### Qu'est-ce que c'est ?

`voynich-lab.html` est un outil d'analyse interactif autonome qui permet de **reproduire et vérifier** les 8 couches d'analyse décrites dans le rapport de recherche. Il ne nécessite aucune installation, aucun serveur, aucune dépendance — il suffit d'ouvrir le fichier dans un navigateur web moderne.

Cet outil est le support expérimental du rapport *« Cadre analytique multi-couches pour le Manuscrit de Voynich »* de Nicolas Van Eeckhout & Claude AI.

### Comment l'utiliser

1. **Ouvrir** le fichier `voynich-lab.html` dans un navigateur (Chrome, Firefox, Safari, Edge)
2. **Sélectionner** une page du manuscrit dans le menu déroulant (3 pages disponibles : f2r Plante, f75r Pharmacie, f1r Ouverture)
3. **Cliquer** sur « ▶ Lancer l'analyse complète »
4. **Explorer** chaque couche via les onglets

### Les 8 onglets

| Onglet | Couche | Ce que vous pouvez vérifier |
|--------|--------|---------------------------|
| **Vue d'ensemble** | Toutes | Tableau récapitulatif des 8 couches, métriques clés, résultat principal |
| **① Entropie** | Couche 1 | H1 et H2 mesurés en temps réel sur la page sélectionnée. Comparaison avec 5 langues médiévales (latin, italien, espagnol, français, tchèque). Visualisation de l'écart de ~1.0 bit. |
| **② Transformations** | Couche 2 | 7 transformations mathématiques (Fibonacci, Log φ, Sin(n·φ), Fib+Sin, Log₂, Linéaire k=3) exécutées en temps réel. H2 résultant affiché pour chaque transformation. **Résultat négatif visible** : aucune ne normalise H2 vers 3.0-4.0. |
| **③④ Phonétique** | Couches 3-4 | Table complète des 14 valeurs sonores de Stephen Bax avec niveaux de confiance (haute/moyenne/basse) et sources de dérivation. **Bouton « Écouter »** : synthèse vocale de la page en accent italien via l'API Web Speech du navigateur. |
| **⑤⑥ Traduction** | Couches 5-6 | Traduction mot-à-mot dans l'ordre original du manuscrit — le sens incohérent est visible directement. Explication du résultat négatif de la transposition (9 stratégies testées, aucun pattern). |
| **⑦ Template** | Couche 7 | **LE CŒUR DE L'OUTIL.** Visualisation du flux des phases sémantiques (🌱1→🔍2→⚗️3→💊4) dans l'ordre original des mots. Chaque mot est représenté par un carré coloré selon sa phase. Statistiques de transition (% avant / arrière / même phase). Démontre visuellement que le flux est préservé. |
| **⑧ Préfixes** | Couche 8 | Tableau des familles de préfixes (qok-, sh-, ch-, ot-, cth-, dai-) avec leur phase sémantique dominante. Focus sur « daiin » : nombre d'occurrences, positions dans le texte, compatibilité avec le latin *item*. |
| **Reconstruction** | Synthèse | Texte EVA original + traduction française structurée par phases du template herbier + détail mot par mot en cartes colorées (Voynich → Français → Phase). **Avertissement** : reconstruction hypothétique. |

### Pages du corpus disponibles

| Page | Section | Registre | Mots | Intérêt |
|------|---------|----------|------|---------|
| **f2r — Plante 1** | Botanique (Cahier 1) | Currier A | ~48 | Page de référence. Illustration de plante (Centaurea ?). Premier mot unique (hapax). Meilleur candidat pour le template matching. |
| **f75r — Pharmacie** | Pharmaceutique | Currier A | ~30 | Page plus courte. Contenu orienté recette/préparation. Bon test de cohérence du template sur une section différente. |
| **f1r — Ouverture** | Introduction | Currier A | ~83 | Première page du manuscrit. Texte plus long. Contient les colonnes alphabétiques cachées de Marci (non visibles dans l'outil, mais mentionnées dans le rapport). |

### Fonctionnalité de synthèse vocale

L'onglet ③④ Phonétique dispose d'un bouton **« ▶ Écouter la page »** qui utilise l'API Web Speech du navigateur pour prononcer le texte EVA avec un accent italien. Les substitutions phonétiques appliquées sont :

- `qo` → `ko` (suppression du caractère muet `q`)
- `cth` → `st` (approximation de la gallows character)
- `sh` → `ʃ` (chuintante, valeur Bax)
- `ch` → `k` (approximation vélaire, valeur Bax)

Pour arrêter la lecture : bouton **« ■ Stop »**.

**Note :** La synthèse vocale nécessite que votre navigateur dispose d'une voix italienne installée. Sur Chrome, les voix sont chargées de manière asynchrone — si la première tentative est silencieuse, attendez 2 secondes et réessayez.

### Détails techniques

| Propriété | Valeur |
|-----------|--------|
| Format | HTML5 + CSS + JavaScript vanilla |
| Dépendances | **Aucune** (pas de React, pas de framework, pas de CDN) |
| Taille | ~30 Ko |
| Navigateurs testés | Chrome 120+, Firefox 120+, Safari 17+, Edge 120+ |
| Fonctionnement | 100% côté client (pas de serveur, pas de requête réseau) |
| API externe | Web Speech API (synthèse vocale, optionnelle) |

### Ce que l'outil prouve / ne prouve pas

**Ce qu'il permet de vérifier :**
- ✅ L'anomalie entropique (H2 ≈ 2.0) est réelle et mesurable
- ✅ Aucune transformation mathématique testée ne normalise H2
- ✅ Le flux sémantique 1→2→3→4 est visible dans l'ordre original des mots
- ✅ Les familles de préfixes se concentrent dans des positions spécifiques
- ✅ « daiin » apparaît en positions compatibles avec un marqueur *item*

**Ce qu'il ne prouve PAS :**
- ❌ Que les traductions mot-à-mot sont correctes (elles sont hypothétiques)
- ❌ Que le template Pseudo-Apuleius est le bon template (c'est le plus compatible parmi ceux testés)
- ❌ Que le manuscrit a été déchiffré (il ne l'a pas été)

---

## 🇬🇧 English

### What is this?

`voynich-lab.html` is a standalone interactive analysis tool that allows anyone to **reproduce and verify** the 8 analytical layers described in the research report. No installation, no server, no dependencies required — just open the file in a modern web browser.

This tool is the experimental support for the report *"A Multi-Layered Analytical Framework for the Voynich Manuscript"* by Nicolas Van Eeckhout & Claude AI.

### How to use

1. **Open** `voynich-lab.html` in a browser (Chrome, Firefox, Safari, Edge)
2. **Select** a manuscript page from the dropdown (3 pages: f2r Plant, f75r Pharmacy, f1r Opening)
3. **Click** "▶ Lancer l'analyse complète" (Run full analysis)
4. **Explore** each layer via tabs

### The 8 tabs

| Tab | Layer | What you can verify |
|-----|-------|-------------------|
| **Vue d'ensemble** | All | Summary table of all 8 layers, key metrics, primary finding |
| **① Entropie** | Layer 1 | H1 and H2 measured in real-time. Comparison with 5 medieval languages. The ~1.0 bit gap is visible. |
| **② Transformations** | Layer 2 | 7 mathematical transformations executed in real-time. H2 shown for each. **Negative result visible**: none normalizes H2 toward 3.0–4.0. |
| **③④ Phonétique** | Layers 3–4 | Bax's 14 sound values with confidence levels. **"Listen" button**: Italian speech synthesis of the page text. |
| **⑤⑥ Traduction** | Layers 5–6 | Word-by-word translation in original order — incoherent meaning directly visible. Transposition negative result explained. |
| **⑦ Template** | Layer 7 | **THE CORE.** Visualization of semantic phase flow (🌱1→🔍2→⚗️3→💊4) in original word order. Each word = colored square by phase. Transition statistics. Visually demonstrates preserved flow. |
| **⑧ Préfixes** | Layer 8 | Prefix family table with dominant semantic phase. Focus on "daiin" as *item* marker. |
| **Reconstruction** | Synthesis | Original EVA + French translation structured by herbal template phases + word-by-word colored cards. **Warning**: hypothetical reconstruction. |

### Technical specifications

| Property | Value |
|----------|-------|
| Format | HTML5 + CSS + vanilla JavaScript |
| Dependencies | **None** (no React, no framework, no CDN) |
| Size | ~30 KB |
| Browsers | Chrome 120+, Firefox 120+, Safari 17+, Edge 120+ |
| Execution | 100% client-side (no server, no network requests) |
| External API | Web Speech API (speech synthesis, optional) |

### What the tool proves / does not prove

**What it verifies:**
- ✅ The entropy anomaly (H2 ≈ 2.0) is real and measurable
- ✅ No tested mathematical transformation normalizes H2
- ✅ The semantic flow 1→2→3→4 is visible in original word order
- ✅ Prefix families cluster in specific positions
- ✅ "daiin" appears in positions consistent with an *item* marker

**What it does NOT prove:**
- ❌ That word-by-word translations are correct (they are hypothetical)
- ❌ That the Pseudo-Apuleius template is the right template (it's the most compatible among those tested)
- ❌ That the manuscript has been deciphered (it has not)

---

## Structure des fichiers / File structure

```
tools/
├── README.md            ← Ce fichier / This file
└── voynich-lab.html     ← L'outil interactif / The interactive tool
```

## Contribuer / Contributing

L'outil peut être étendu de plusieurs façons :
- **Ajouter des pages** : éditer le dictionnaire `PAGES` dans le JavaScript pour inclure d'autres folios (transcription EVA disponible sur voynich.nu)
- **Enrichir le lexique** : éditer `WORD_DATA` pour ajouter de nouvelles correspondances mot → traduction → phase
- **Ajouter des transformations** : ajouter de nouvelles entrées dans la fonction `transform()` pour tester d'autres hypothèses mathématiques
- **Nouvelles langues de synthèse** : modifier la fonction `speakText()` pour tester d'autres accents (espagnol, français, tchèque)

Voir [CONTRIBUTING.md](../CONTRIBUTING.md) pour les guidelines générales.

---

*Nicolas Van Eeckhout & Claude AI — Mars 2026 — CC BY-SA 4.0*
