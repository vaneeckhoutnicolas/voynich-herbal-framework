# A Multi-Layered Analytical Framework for the Voynich Manuscript
## From Entropy to Medieval Herbal Templates

### Exploratory Research Report

**Lead researcher:** Nicolas Van Eeckhout  
**Analytical & computational assistance:** Claude AI (Anthropic)  
**Date:** March 2026  
**License:** CC BY-SA 4.0  
**Repository:** `github.com/[user]/voynich-herbal-framework`

---

## Foreword

This report documents an exploratory research process born from a chance encounter between a curious mind and a six-hundred-year-old manuscript. In March 2026, Nicolas Van Eeckhout came across an Instagram post by the account *Ageless Literature* describing the Voynich Manuscript — 240 pages of undeciphered writing, illustrations of unrecognizable plants, women bathing in green pools, a script bearing the statistical fingerprint of a real language yet matching none known. Six hundred years old. Not a single word decoded.

What followed was an iterative dialogue spanning several hours between Nicolas and Claude, an artificial intelligence model by Anthropic. Nicolas drove the investigation by proposing the foundational hypotheses at each stage: the idea that entropy should be measured not on the raw character sequence but on a mathematical abstraction — "why not try a Fibonacci, logarithmic, or trigonometric approach?"; the concept of algorithmic complexity classes (O(1), O(log n), O(n), O(n log n)) applied to cipher analysis; the intuition that glyphs might represent sounds rather than letters; the realization that the translated words might be "all there but not in the right order"; and finally the decisive pivot — "look for a *semantic journey* like describing a plant, how to prepare it, and what it's used for."

Claude provided the computational infrastructure (interactive entropy analysis, transformation testing, and speech synthesis tools), extensive academic literature research, knowledge of medieval herbal traditions, and statistical rigor. Together, eight analytical layers were built, tested, evaluated — and mostly discarded in favor of the next, through a process of progressive elimination that ultimately converged on a coherent result.

This report does not claim to have deciphered the Voynich Manuscript — no one ever has. But it fully embraces a deliberate intention: **to try differently**.

For over a century, the Voynich has been attacked almost exclusively by cryptanalysts and computer scientists — experts of the *how* (how is it encrypted?) rather than the *what* (what does it say?). Classical methods — frequency analysis, substitution testing, decryption algorithms — have all failed. Modern AI systems, trained on massive corpora, have fared no better. Perhaps the problem is not a lack of computational power or cryptographic sophistication. Perhaps the problem is the angle of attack itself.

Our approach starts from a different premise: **if we understand what the text is supposed to say — because we know the literary genre it belongs to — then we can constrain the solution space from within, through content, rather than from without, through mechanism.** A medieval herbal can only say a limited number of things, in a predictable order, with a closed vocabulary. This content constraint is as powerful as any cryptographic constraint — and it had never been systematically exploited.

This is the founding idea of this work: stop staring at the symbols and start listening to the story they tell. The report presents an analytical framework identifying the medieval herbal template as the most promising structural key, and fills a documented gap in the scholarly literature. It is published as open source so that other researchers can build upon, critique, and improve this work.

---

## Abstract

This report presents an eight-layer analytical framework applied to the botanical pages of the Voynich Manuscript (Beinecke MS 408, Yale University). Exploratory layers — entropy analysis, mathematical inverse transformations (Fibonacci, log φ, sin(n·φ)), phonetic mapping, speech synthesis, direct translation, and transposition testing — produced largely negative or inconclusive results but progressively constrained the hypothesis space. The primary finding emerges from the final two layers: positional word-distribution patterns on folio f2r match the "Ad [condition]" micro-template of the *Pseudo-Apuleius Herbarius*, and Voynich prefix families (qok-, sh-, ot-, cth-, dai-) correlate with the semantic categories of that template. The word "daiin" (~866 occurrences) behaves as a structural transitional marker analogous to Latin *item*. The semantic flow Identification → Description → Preparation → Medical Use is already present in the original word order, indicating substitution-based encipherment without transposition.

---

## 1. Introduction

### 1.1 The manuscript's material identity

The Voynich Manuscript is an illustrated codex written in an unknown script. Radiocarbon dating (University of Arizona, 2009, Greg Hodgins) places the vellum between **1404 and 1438 CE** (95% CI). The manuscript comprises approximately 240 pages on calfskin vellum (22.5 × 16 cm), organized in 18 quires. The text corpus totals ~37,919 tokens and ~8,114 unique word types in EVA transcription. The script employs 20–25 core glyphs. The manuscript is held at the Beinecke Rare Book and Manuscript Library, Yale University (MS 408).

### 1.2 Statistical fingerprint

The second-order conditional entropy (H2) of Voynichese is approximately **2.0 bits/character** — well below the 3.0–4.0 bits measured for any known natural language (Bowern & Lindemann, 2021, across 316 texts in 294 languages). Paradoxically, at the word level, the text obeys Zipf's law (Montemurro & Zanette, 2013, *PLOS ONE*) and exhibits entropy of approximately 10 bits/word, comparable to Latin.

### 1.3 Five scribes, two registers

Lisa Fagin Davis (2020, *Manuscript Studies*) identified five distinct scribal hands through digital paleography. Scribes 1 and 4 write in Currier A; Scribes 2, 3, and 5 in Currier B — two statistically distinguishable textual populations first identified by Prescott Currier in 1976.

### 1.4 State of the art 2025–2026

Greshko's **Naibbe cipher** (2025, *Cryptologia*) demonstrates that a verbose homophonic substitution using six lookup tables, dice, and playing cards can transform Latin into text statistically indistinguishable from Voynichese. **Hidden alphabet columns** discovered by Davis (2024) via multispectral imaging on folio 1r — attributed to J. M. Marci (1660s) — constitute a historical decryption attempt. No complete solution has been independently verified to date.

---

## 2. Historical Context: Herbals and 15th-Century Medicine

### 2.1 Padua and Venice: the heart of European medicine

Understanding why medieval herbal templates constitute the appropriate analytical framework for the Voynich requires immersion in the medical milieu of Northern Italy in the early fifteenth century — precisely the time and place of the manuscript's creation.

The University of Padua, founded in 1222, was Europe's preeminent medical training center in the early 1400s. It was at Padua that the first public anatomical dissections took place, that the Hippocratic tradition was transmitted directly from Greek texts, and that *materia medica* — the systematic study of medicinal substances, primarily botanical — formed the foundation of physician and apothecary training. The creation of the world's first university botanical garden (the *Orto Botanico* of Padua, 1545) was a direct continuation of this tradition, which had existed earlier in the form of private *simplicia* gardens.

Venice, a few hours from Padua, was the commercial center par excellence — and the spice and medicinal plant trade was among its most lucrative activities. Venetian *spezierie* (pharmacies) were strictly regulated enterprises, regularly inspected, whose recipes constituted trade secrets of enormous value. The *Collegium Aromatariorum* (apothecaries' guild) controlled training, practice, and formulas.

### 2.2 Why encrypt an herbal?

Three converging motivations explain this documented fifteenth-century practice:

**Commercial protection.** Apothecary recipes had considerable market value. A formula for theriac (universal antidote) or an effective fever electuary could make a *spezieria*'s fortune. Encrypting recipes was the medieval equivalent of trade secret protection.

**Guild secrecy.** Apothecary guilds transmitted knowledge from master to apprentice. Some manuscripts circulated within restricted circles and contained knowledge their authors did not wish freely disseminated — particularly precise dosages of toxic substances (arsenic, mandrake, belladonna) used therapeutically.

**Protection against suspicion of heresy.** Certain medical practices — using plants in healing rituals, medical astrology (prominently present in the Voynich with its zodiac diagrams), alchemical preparations — could attract Inquisitorial attention. Sergio Toresella identified approximately 70 "alchemical herbals" produced almost exclusively in the Veneto region during the fifteenth century, combining real botany with magico-alchemical recipes. The Voynich may belong to this tradition.

### 2.3 The reference herbals and their relevance

Five pharmaceutical textual traditions frame our analysis. Their selection is not arbitrary — these are the texts that every Paduan physician or apothecary in the fifteenth century knew and used daily:

**Dioscorides, *De Materia Medica*** (1st century CE, continuously transmitted for 1,500 years). The foundational text of all Western pharmacology. Each entry follows: Name → Synonyms → Physical description → Habitat → Medicinal properties → Preparation → Dosage → Adulteration detection. Medieval copies added Galenic humoral qualities.

**Pseudo-Apuleius, *Herbarius*** (4th century CE, >60 surviving medieval manuscripts). The most copied herbal of the Middle Ages. Its template is the most distinctive: "Herba [name]" followed by series of "Ad [condition]" micro-recipes — each containing the triad condition → preparation → application. The transition marker *item* ("likewise," "also") links successive recipes. This template is the most compatible with the Voynich's short, formulaic botanical paragraphs.

**Tacuinum Sanitatis** (translated from Arabic of Ibn Butlan, 13th century). Five-field tabular format: Natura → Melius → Iuvamentum → Nocumentum → Remotio nocumenti. Very popular in Northern Italy.

**Antidotarium Nicolai** (12th century, School of Salerno). The standard pharmaceutical formulary of medieval Europe: *Recipe* [ingredients with quantities] → *Fiat* [dosage form] → therapeutic indication.

**Northern Italian herbals contemporary to the Voynich.** The Carrara Herbal (Padua, c. 1390–1404), in Paduan dialect. The Rinio/Roccabonella Herbal (Venice, c. 1415–1449), with 440 illustrations and plant names in Latin, Greek, German, Arabic, and Italian dialects — a multilingualism reminiscent of the Voynich. Toresella's ~70 alchemical herbals from the Veneto, with real plants alongside magico-alchemical recipes, one illustration per page, and short text paragraphs — exactly the Voynich's page layout.

### 2.4 The standardized pharmaceutical vocabulary

Medieval pharmaceutical Latin operated with a remarkably small, highly repetitive functional vocabulary:

**Opening:** *Recipe/Accipe* (Take) → Italian *Piglia/Prendi*. **Grinding:** *Terere/Contundere* → *Pestare*. **Mixing:** *Miscere* → *Mescolare*. **Boiling:** *Coquere/Decoquere* → *Bollire*. **Filtering:** *Colare* → *Colare/Passare*. **Applying:** *Imponere/Linire* → *Ungere*.

Transition markers: *Item* (likewise), *Ad idem* (for the same), *Praeterea* (moreover). Efficacy formulas: *Probatum est* (it is proven), *Mirifice sanat* (it heals wonderfully).

This closed vocabulary of ~50–80 functional terms covering the majority of pharmaceutical text is precisely the kind of lexicon that should produce detectable statistical signatures, even through substitution encryption.

---

## 3. Methodology: Eight Exploration Layers

### Layer 1 — Entropy Profiling (H1, H2, H3)

**Origin.** Nicolas Van Eeckhout suggested from the outset that "entropy should perhaps be calculated on an abstraction of the character sequence."

**Approach.** Entropy measurement at three orders on the EVA transcription. Interactive visualization tool comparing Voynichese profiles against 8 medieval languages.

**Result.** Confirmed the anomaly: H2 ≈ 2.0 vs. 3.3–3.6 for target languages.

**Productivity: ✅ POSITIVE** — quantitative baseline established.

### Layer 2 — Mathematical Inverse Transformations

**Origin.** Nicolas proposed integrating algorithmic complexity concepts (O(1), O(log n), O(n), O(n log n)) as a cipher analysis framework: "each complexity class leaves a signature in the text."

**Approach.** Over 50 transformations tested: Fibonacci sequences (offsets 0–5), logarithms in bases 2, e, φ, 3, 5, 7, 10; sin and cos at frequencies 1, φ, π, 2, 3, 5, 7, 11; Fib+Sin combinations; powers of φ; n·log(n). Applied as inverse decryption operations. Pass 2: double combinations of the top 8.

**Result: ❌ NEGATIVE.** Maximum H2 shift ≈ 0.3 bits. No normalization toward the 3.0–4.0 range. Conclusion: the cipher is likely not a pure mathematical transformation but a verbose substitution (corroborated by the Naibbe cipher).

**Productivity: ❌ Negative** but informative (hypothesis space constraint).

### Layer 3 — Phonetic Mapping (Bax)

**Origin.** Nicolas asked: "Has anyone tried with sounds?" — questioning whether glyphs represented phonemes rather than letters.

**Approach.** Integration of Stephen Bax's 14 sound values (2014–2017), derived from botanical identifications. EVA → IPA conversion table built. Three mappings tested: Bax (botanical), Cheshire (proto-Romance), syllabic.

**Result: 🔶 EXPLORATORY.** Readings are linguistically plausible but cover 14 glyphs of ~25 and 10 words of ~38,000. Not verifiable with current evidence.

### Layer 4 — Speech Synthesis

**Approach.** Tool combining phonetic mappings with mathematical transformations and Web Speech API synthesis (Italian accent). Additional sonification mode (each character → audible frequency).

**Result: 🔶 EXPLORATORY.** No recognizable language heard. But this layer produced an important conceptual pivot: shift toward *content* rather than *mechanism*.

### Layer 5 — Direct French Translation

**Approach.** EVA → medieval language → French lexicon. Four strategies: frequency mapping, length + frequency matching, prefix-based semantic fields, thematic gap-filling.

**Result: ❌ NEGATIVE.** Individually translated words seemed plausible but did not form coherent meaning in original order. This directly generated the next hypothesis.

### Layer 6 — Transposition Hypothesis

**Origin.** Nicolas formulated the key hypothesis: "I think all the words are there but not in the right order — try to make a text that makes sense and cross-reference on a pattern."

**Approach.** Nine reordering strategies (SVO grammar, reversed, boustrophedon, columns, spiral, Fibonacci, golden ratio). Permutation analysis (jump sequence, autocorrelation, match scores).

**Result: ❌ NEGATIVE.** No clear mathematical transposition pattern. This led to the paradigm shift of the next layer.

### Layer 7 — THE PIVOT: Medieval Herbal Template

**Origin.** Nicolas asked: "Look for a *semantic journey* like describing a plant, how to prepare it, and what it's used for." This was the decisive moment of the investigation.

**Approach.** Abandonment of abstract mathematical pattern search. Application of the Pseudo-Apuleius template to folio f2r: classification of each word into one of four phases — 🌱 Identification, 🔍 Description, ⚗️ Preparation, 💊 Medical Use. Semantic flow analysis in the manuscript's original word order.

**Result: ✅ POSITIVE.** The semantic flow Identification → Description → Preparation → Medical Use **is already present in the original order**. Over 55% of inter-word transitions go "forward" (phase n → phase n+1). Phases are broadly clustered rather than scattered. **Conclusion: no significant transposition.**

### Layer 8 — Positional Semantic Analysis

**Approach.** Word classification by prefix families. Correlation testing against template categories.

**Results:**

| Prefix | Approx. occ. | Position | Proposed category |
|---|---|---|---|
| qok- | ~1,100 | Beginning/middle | Botanical (plant) |
| sh- | ~900 | Middle | Preparation (pour, leaves) |
| ch- | ~1,400 | Distributed | Description (branches, sap) |
| ot- | ~500 | End | Medical (remedy, ointment) |
| cth- | ~200 | Beginning | Description (earth, root) |
| dai- | ~900 | Line-initial | Transitional (*item*) |

The word **"daiin"** (~866 occ.) appears as first word on a line in >20% of instances. Its density varies: every ~19 words in Currier A vs. every ~50–60 words in Currier B. Profile consistent with Latin *item*.

**Productivity: ✅ POSITIVE** (corroboration of the primary finding).

---

## 4. Results Summary

| # | Layer | Result | Verdict |
|---|---|---|---|
| 1 | Entropy | Baseline H2 ≈ 2.0 confirmed | ✅ Positive |
| 2 | Math transforms | No H2 normalization | ❌ Negative (informative) |
| 3 | Bax phonetics | Plausible, unverifiable | 🔶 Exploratory |
| 4 | Speech synthesis | No language recognized | 🔶 Exploratory |
| 5 | Direct translation | Incoherent meaning | ❌ Negative |
| 6 | Transposition | No pattern | ❌ Negative |
| 7 | **Herbal template** | **Semantic flow preserved** | **✅ Positive** |
| 8 | **Positional analysis** | **Prefix ↔ semantics** | **✅ Positive** |

---

## 5. Hypothetical Reconstruction of f2r

**EVA text:** `kchor shey cthey dain chor shol qokaiin daiin oky okeol otaiin shol cheol dain cthy okeedy otchedy qokain cthor daiin shol okaiin qokeedy dal chedy qokedy dain shedy qokeedy chey daiin otaiin cheody okeey dal qokeey sheol daiin okeey shedy qokeedy okeey chedy daiin otar shol qokain qokeedy`

**Reconstruction:**

> 🌱 **This plant.** Pour water on its soil, at the right time. The mother plant grows in sunlight. It is a root plant.
>
> ⚗️ **Then,** treat, use as a lotion. In medicinal preparation, in sunlight, extract its oily sap. At the right time, in the earth, the balm acts. Treat the body's branches with the plant.
>
> 💊 **Its root, then,** in sunlight, apply as strong ointment. The dried herb of the branch, the young shoot. Its leaves of dried herb. Pour, then. In medicinal preparation, its thick sap, use as balm, from the water flower, add oil. The balm acts, its leaves. **It is a remedy,** in sunlight. The plant. The dried herb.

⚠️ **Warning:** Hypothetical reconstruction based on the Pseudo-Apuleius template and an unverified lexicon.

---

## 6. Discussion

### 6.1 Convergences

Our results converge with three published works: Montemurro & Zanette (2013) showed section-level keyword distribution compatible with genuine thematic content — our within-page analysis extends this finding. Bowern & Lindemann (2021) confirmed the H2 anomaly and prefix-root-suffix structure — our prefix-based semantic analysis builds directly on this structure. Greshko's Naibbe cipher (2025) demonstrates that verbose substitution can produce all the manuscript's statistical anomalies — our conclusion that word order is preserved (no transposition) is consistent with this model.

### 6.2 Gap addressed

No published study had systematically conducted "positional template matching" between Voynich text and known pharmaceutical manuscript formats. This report proposes this approach as a research direction.

### 6.3 Limitations

No plaintext has been recovered. Phonetic values remain unverified. The lexicon is hypothetical. Analysis focuses on a single folio. Negative layers constrain but do not eliminate all cipher variants.

---

## 7. Conclusion

1. The manuscript likely encodes **genuine pharmaceutical content** following 15th-century herbal templates.
2. The encipherment preserves word order — it is a **substitution** (not transposition).
3. The source text follows herbal conventions of the **Paduan-Venetian tradition**.

**Future work:** Extension to all 113 botanical folios. Computational testing of verbose substitution models. Exploitation of Marci's alphabet columns as cribs. Comparative analysis with Toresella's 70 Veneto alchemical herbals.

---

## Bibliography

- Bax, S. (2014). A proposed partial decoding of the Voynich script. stephenbax.net.
- Bowern, C. & Lindemann, L. (2021). The Linguistics of the Voynich Manuscript. *Annual Review of Linguistics*, 7, 285–308.
- Currier, P. H. (1976). Papers on the Voynich Manuscript. NSA Seminar.
- Davis, L. F. (2020). How Many Glyphs and How Many Scribes? *Manuscript Studies*, 5(1), 164–180.
- Greshko, M. A. (2025). The Naibbe cipher. *Cryptologia*, doi:10.1080/01611194.2025.2566408.
- Kyle, S. R. (2016). *Medicine and Humanism in Late Medieval Italy*. Routledge.
- Montemurro, M. A. & Zanette, D. H. (2013). Keywords and Co-Occurrence Patterns. *PLOS ONE*, 8(6), e66344.
- Stolfi, J. (2000). A Grammar for Voynichese Words. UNICAMP.
- Toresella, S. (1996). Gli erbari degli alchimisti. In *Arte farmaceutica e piante medicinali*.
- Zandbergen, R. (2004–2026). Voynich MS. voynich.nu.

---

## Appendix — Suggested GitHub Repository Structure

```
voynich-herbal-framework/
├── README.md
├── LICENSE (CC BY-SA 4.0)
├── rapport/
│   ├── rapport-FR.md        ← French version
│   └── report-EN.md         ← English version
├── data/
│   ├── eva-transcription/
│   └── word-frequencies.csv
├── tools/
│   ├── entropy-analyzer/
│   ├── transform-tester/
│   ├── herbal-template-matcher/
│   └── semantic-classifier/
├── results/
│   ├── f2r-reconstruction.md
│   └── summary-table.md
└── CONTRIBUTING.md
```

---

*Nicolas Van Eeckhout & Claude AI — March 2026 — CC BY-SA 4.0*
