# 🔮 Voynich Herbal Framework

## Cadre analytique multi-couches pour le Manuscrit de Voynich / Multi-Layered Analytical Framework for the Voynich Manuscript

[![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-sa/4.0/)
[![Language: FR/EN](https://img.shields.io/badge/Language-FR%20%2F%20EN-blue.svg)](https://github.com/vaneeckhoutnicolas/voynich-herbal-framework/blob/main)

---

> ⚠️ **Avertissement / Disclaimer**
>
> 🇫🇷 Ce travail est **exploratoire et hypothétique**. Le Manuscrit de Voynich n'a jamais été officiellement déchiffré. Ce rapport propose un cadre d'analyse, pas une solution définitive. Les hypothèses et conclusions présentées ici sont celles de l'auteur (Nicolas Van Eeckhout) ; Claude AI (Anthropic) a été utilisé comme **outil d'exploration et de structuration**, pas comme source de vérité.
>
> 🇬🇧 This work is **exploratory and hypothetical**. The Voynich Manuscript has never been officially deciphered. This report proposes an analytical framework, not a definitive solution. The hypotheses and conclusions presented here are those of the author (Nicolas Van Eeckhout); Claude AI (Anthropic) was used as an **exploration and structuring tool**, not as a source of truth.

---

### 🇫🇷 Français

Ce dépôt contient le rapport de recherche et les outils développés lors d'une exploration menée par **Nicolas Van Eeckhout**, avec **Claude AI (Anthropic)** utilisé comme assistant pour structurer et élargir la réflexion analytique sur le Manuscrit de Voynich (Beinecke MS 408, Yale University).

#### Le problème

Le Manuscrit de Voynich est un codex illustré du XVe siècle (~1404-1438) de 240 pages, rédigé dans un script inconnu que personne n'a jamais déchiffré — ni les cryptanalystes de la Seconde Guerre mondiale, ni les linguistes de Yale, ni les systèmes d'IA modernes.

#### Notre approche

Huit couches d'analyse progressives, de l'entropie aux herbiers médiévaux :

| # | Couche | Résultat |
| --- | --- | --- |
| 1 | Profilage d'entropie (H1, H2, H3) | ✅ Baseline établie |
| 2 | Transformations mathématiques (Fibonacci, log φ, sin(n·φ)) | ❌ Pas de normalisation |
| 3 | Mapping phonétique (Bax) | 🔶 Exploratoire |
| 4 | Synthèse vocale | 🔶 Exploratoire |
| 5 | Traduction directe français | ❌ Sens incohérent |
| 6 | Hypothèse de transposition | ❌ Pas de pattern |
| 7 | **Template d'herbier médiéval** | **✅ Flux sémantique préservé** |
| 8 | **Analyse sémantique positionnelle** | **✅ Préfixes ↔ sémantique** |

#### Résultat principal

La distribution des mots sur les pages botaniques correspond au template « Ad [condition] » du *Pseudo-Apuleius Herbarius*. Le flux sémantique **Identification → Description → Préparation → Usage médical** est déjà présent dans l'ordre original des mots, indiquant un chiffrement par substitution (pas de transposition). Le mot « daiin » (~866 occurrences) se comporte comme le latin *item* — un marqueur de transition entre recettes.

---

### 🇬🇧 English

This repository contains the research report and tools developed by **Nicolas Van Eeckhout**, with **Claude AI (Anthropic)** used as an assistant to help structure and broaden the analytical exploration of the Voynich Manuscript (Beinecke MS 408, Yale University).

#### The problem

The Voynich Manuscript is a 240-page illustrated codex from the 15th century (~1404-1438), written in an unknown script that no one has ever deciphered — not WWII codebreakers, not Yale linguists, not modern AI systems.

#### Our approach

Eight progressive analytical layers, from entropy to medieval herbals. The key finding is that word-distribution patterns on botanical pages match the "Ad [condition]" micro-template of the *Pseudo-Apuleius Herbarius*, with the semantic flow **Identification → Description → Preparation → Medical Use** already preserved in the original word order.

---

## 📁 Structure du dépôt / Repository Structure

```
voynich-herbal-framework/
├── README.md                          ← Ce fichier / This file
├── LICENSE                            ← CC BY-SA 4.0
├── CONTRIBUTING.md                    ← Guide de contribution
├── rapport/
│   ├── rapport-FR.md                  ← Rapport complet (français)
│   └── report-EN.md                   ← Full report (English)
├── data/
│   ├── voynich-word-frequencies.csv   ← Fréquences des mots
│   ├── prefix-families.csv            ← Familles de préfixes
│   └── f2r-semantic-mapping.csv       ← Mapping sémantique f2r
├── results/
│   ├── f2r-reconstruction-FR.md       ← Reconstruction de f2r
│   ├── summary-table.md               ← Tableau récapitulatif
│   └── layer-results.md               ← Détail par couche
└── references/
    └── bibliography.md                ← Bibliographie complète
```

## 🚀 Comment contribuer / How to Contribute

Voir / See [contributing.md](https://github.com/vaneeckhoutnicolas/voynich-herbal-framework/blob/main/contributing.md)

## 📖 Citer ce travail / Citing This Work

```
Van Eeckhout, N. (2026). Cadre analytique multi-couches 
pour le Manuscrit de Voynich : de l'entropie aux templates d'herbiers 
médiévaux. GitHub: voynich-herbal-framework. CC BY-SA 4.0.
(Exploration menée avec l'assistance de Claude AI, Anthropic)
```

## 📄 Licence / License

Ce travail est publié sous licence [Creative Commons Attribution-ShareAlike 4.0 International](https://creativecommons.org/licenses/by-sa/4.0/).

---

*Nicolas Van Eeckhout — Mars / March 2026*  
*Exploration réalisée avec l'assistance de Claude AI (Anthropic)*
