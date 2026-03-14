# Contribuer à ce projet / Contributing to this project

## 🇫🇷 Français

Merci de votre intérêt pour ce projet ! Ce dépôt est ouvert aux contributions de chercheurs, linguistes, cryptanalystes, historiens de la médecine médiévale, et toute personne passionnée par le Manuscrit de Voynich.

### Comment contribuer

#### 1. Étendre l'analyse à d'autres folios
Notre analyse se concentre sur le folio f2r. La priorité est d'étendre le template matching aux **113 folios botaniques** complets. Pour chaque folio :
- Récupérer la transcription EVA (source : voynich.nu ou le Takahashi transcription file)
- Classifier chaque mot par famille de préfixe (qok-, sh-, ch-, ot-, cth-, dai-, autre)
- Assigner une phase du template (Identification, Description, Préparation, Usage)
- Mesurer le pourcentage de transitions « vers l'avant » (phase n → n+1)
- Documenter le résultat dans `results/`

#### 2. Améliorer le lexique sémantique
Le mapping mot → signification dans `data/f2r-semantic-mapping.csv` est hypothétique. Vous pouvez :
- Proposer des correspondances alternatives basées sur d'autres identifications botaniques
- Croiser avec le vocabulaire pharmaceutique latin/italien vernaculaire documenté
- Tester la cohérence avec d'autres pages où le même mot apparaît

#### 3. Tester d'autres templates d'herbier
Nous avons principalement testé le template Pseudo-Apuleius. D'autres templates méritent un test systématique :
- Dioscoride (séquence à 8 éléments)
- Tacuinum Sanitatis (format tabulaire à 5 champs)
- Antidotarium Nicolai (format de recette)
- Herbiers vernaculaires nord-italiens

#### 4. Développer les outils computationnels
Les outils dans `tools/` sont des prototypes. Contributions bienvenues pour :
- Automatiser le template matching sur le corpus complet
- Implémenter des tests statistiques de significativité
- Créer des visualisations du flux sémantique
- Construire un outil de comparaison inter-folios

### Règles de contribution
- Forkez le dépôt et créez une branche pour votre contribution
- Documentez clairement votre méthodologie
- Distinguez toujours les **résultats vérifiés** (statistiques, distributions) des **hypothèses** (traductions, mappings)
- Soumettez une Pull Request avec une description détaillée

### Code de conduite
Ce projet adopte le [Contributor Covenant](https://www.contributor-covenant.org/). Toute contribution doit respecter un échange scientifique courtois et constructif.

---

## 🇬🇧 English

Thank you for your interest! This repository welcomes contributions from researchers, linguists, cryptanalysts, historians of medieval medicine, and anyone passionate about the Voynich Manuscript.

### How to contribute

#### 1. Extend analysis to other folios
Our analysis focuses on folio f2r. The priority is extending template matching to all **113 botanical folios**:
- Retrieve the EVA transcription (source: voynich.nu or the Takahashi transcription file)
- Classify each word by prefix family (qok-, sh-, ch-, ot-, cth-, dai-, other)
- Assign a template phase (Identification, Description, Preparation, Use)
- Measure the percentage of "forward" transitions (phase n → n+1)
- Document results in `results/`

#### 2. Improve the semantic lexicon
The word → meaning mapping in `data/f2r-semantic-mapping.csv` is hypothetical. You can:
- Propose alternative correspondences based on other botanical identifications
- Cross-reference with documented Latin/Italian vernacular pharmaceutical vocabulary
- Test consistency across pages where the same word appears

#### 3. Test other herbal templates
We primarily tested the Pseudo-Apuleius template. Other templates deserve systematic testing:
- Dioscorides (8-element sequence)
- Tacuinum Sanitatis (5-field tabular format)
- Antidotarium Nicolai (recipe format)
- Northern Italian vernacular herbals

#### 4. Develop computational tools
Tools in `tools/` are prototypes. Contributions welcome to:
- Automate template matching across the full corpus
- Implement statistical significance tests
- Create semantic flow visualizations
- Build cross-folio comparison tools

### Contribution guidelines
- Fork the repository and create a branch for your contribution
- Clearly document your methodology
- Always distinguish **verified results** (statistics, distributions) from **hypotheses** (translations, mappings)
- Submit a Pull Request with a detailed description

---

*Ce projet est sous licence CC BY-SA 4.0*
