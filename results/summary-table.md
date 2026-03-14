# Tableau récapitulatif des 8 couches d'analyse
# Summary Table of the 8 Analytical Layers

---

## 🇫🇷 Version française

| # | Couche | Initiée par | Approche | Résultat clé | Verdict | Contribution à l'investigation |
|---|--------|------------|----------|-------------|---------|-------------------------------|
| 1 | Profilage d'entropie | Nicolas (« l'entropie doit être calculée sur une abstraction ») | Mesure H1, H2, H3 sur EVA. Comparaison avec 8 langues médiévales | H2 ≈ 2,0 confirmé (cible : 3,0-4,0) | ✅ Positive | Baseline quantitative établie |
| 2 | Transformations mathématiques | Nicolas (complexité O(1), O(log n), O(n)) | 50+ transformations : Fibonacci, log φ, sin(n·φ), combinaisons | Déplacement max H2 ≈ 0,3 bit. Pas de normalisation | ❌ Négative | Exclut les chiffres à transformation math pure |
| 3 | Mapping phonétique Bax | Nicolas (« et si on essayait avec les sons ? ») | 14 valeurs sonores de Bax. Conversion EVA → IPA | Lectures plausibles mais 14/25 glyphes, 10/38000 mots | 🔶 Exploratoire | Hypothèses testables mais non vérifiées |
| 4 | Synthèse vocale | Suite de la couche 3 | Écoute multi-mappings (Bax, Cheshire, syllabique) + sonification | Pas de langue reconnue | 🔶 Exploratoire | Pivot conceptuel : contenu > mécanisme |
| 5 | Traduction directe FR | Suite logique | Lexique EVA → médiéval → français. 4 stratégies | Mots plausibles, sens incohérent dans l'ordre original | ❌ Négative | Génère l'hypothèse de transposition |
| 6 | Transposition | Nicolas (« les mots sont là mais pas dans le bon ordre ») | 9 stratégies de réordonnancement. Analyse de permutation | Pas de pattern mathématique de transposition | ❌ Négative | Conduit au changement de paradigme |
| 7 | **Template herbier** | **Nicolas (« cherche un semantic journey : plante → préparation → usage »)** | **Pseudo-Apuleius sur f2r. Classification en 4 phases** | **Flux sémantique 1→2→3→4 préservé dans l'ordre original (55 % transitions avant)** | **✅ Positive** | **Résultat principal** |
| 8 | **Analyse sém. positionnelle** | Suite de la couche 7 | **Préfixes × position × catégorie sémantique** | **Corrélation préfixes/sémantique. « daiin » = *item*** | **✅ Positive** | **Corroboration** |

---

## 🇬🇧 English version

| # | Layer | Initiated by | Approach | Key result | Verdict | Contribution |
|---|-------|-------------|----------|-----------|---------|-------------|
| 1 | Entropy profiling | Nicolas ("entropy should be calculated on an abstraction") | H1, H2, H3 on EVA. Comparison with 8 medieval languages | H2 ≈ 2.0 confirmed (target: 3.0–4.0) | ✅ Positive | Quantitative baseline |
| 2 | Math transformations | Nicolas (complexity O(1), O(log n), O(n)) | 50+ transforms: Fibonacci, log φ, sin(n·φ), combos | Max H2 shift ≈ 0.3 bits. No normalization | ❌ Negative | Rules out pure math ciphers |
| 3 | Bax phonetic mapping | Nicolas ("what if we tried with sounds?") | 14 Bax sound values. EVA → IPA conversion | Plausible readings but 14/25 glyphs, 10/38000 words | 🔶 Exploratory | Testable but unverified hypotheses |
| 4 | Speech synthesis | Follow-up to layer 3 | Multi-mapping listening (Bax, Cheshire, syllabic) + sonification | No recognized language | 🔶 Exploratory | Conceptual pivot: content > mechanism |
| 5 | Direct FR translation | Logical follow-up | EVA → medieval → French lexicon. 4 strategies | Plausible words, incoherent meaning in original order | ❌ Negative | Generates transposition hypothesis |
| 6 | Transposition | Nicolas ("the words are all there but not in the right order") | 9 reordering strategies. Permutation analysis | No mathematical transposition pattern | ❌ Negative | Leads to paradigm shift |
| 7 | **Herbal template** | **Nicolas ("look for a semantic journey: plant → preparation → use")** | **Pseudo-Apuleius on f2r. 4-phase classification** | **Semantic flow 1→2→3→4 preserved in original order (55% forward transitions)** | **✅ Positive** | **Primary result** |
| 8 | **Positional semantic** | Follow-up to layer 7 | **Prefixes × position × semantic category** | **Prefix/semantic correlation. "daiin" = *item*** | **✅ Positive** | **Corroboration** |

---

## Synthèse visuelle / Visual summary

```
Couche 1  [Entropie]        ──→ ✅ Baseline H2 ≈ 2.0
     │
Couche 2  [Fibonacci/Trig]  ──→ ❌ Pas de normalisation H2
     │                            ↓ Conclusion: pas de chiffre math pur
Couche 3  [Sons/Bax]        ──→ 🔶 Plausible mais non vérifié
     │
Couche 4  [Synthèse vocale] ──→ 🔶 Pivot vers le contenu
     │
Couche 5  [Traduction FR]   ──→ ❌ Sens incohérent
     │                            ↓ « Les mots sont là mais pas dans le bon ordre »
Couche 6  [Transposition]   ──→ ❌ Pas de pattern
     │                            ↓ CHANGEMENT DE PARADIGME
Couche 7  [TEMPLATE HERBIER] ──→ ✅ FLUX SÉMANTIQUE PRÉSERVÉ
     │
Couche 8  [ANALYSE PRÉFIXES] ──→ ✅ CORRÉLATION PRÉFIXES ↔ SÉMANTIQUE
     │
     └──→ CONCLUSION: Substitution verbose, pas de transposition.
           Le manuscrit est probablement un herbier pharmaceutique chiffré.
```

---

*Nicolas Van Eeckhout & Claude AI — Mars 2026 — CC BY-SA 4.0*
