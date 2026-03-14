# Détail des résultats par couche / Detailed Results by Layer

---

## Couche 1 — Profilage d'entropie / Entropy Profiling

### Mesures obtenues / Measurements

| Texte | H1 (bits) | H2 (bits) | H3 (bits) | Distance eucl. au latin |
|-------|-----------|-----------|-----------|------------------------|
| Voynichese (EVA, brut) | 4.95 | 2.03 | 1.42 | 1.82 |
| Latin médiéval (réf.) | 4.00 | 3.40 | 2.80 | 0 |
| Vieux italien (réf.) | 3.90 | 3.30 | 2.70 | 0.17 |
| Vieil espagnol (réf.) | 3.95 | 3.50 | 2.90 | 0.14 |
| Vieux français (réf.) | 3.85 | 3.50 | 2.85 | 0.18 |
| Vieux tchèque (réf.) | 3.80 | 3.20 | 2.60 | 0.35 |
| Moyen haut-allemand (réf.) | 4.10 | 3.60 | 3.00 | 0.28 |

### Interprétation

L'écart H2 entre le Voynichese (~2.0) et toute langue naturelle (~3.0-4.0) est l'anomalie centrale. Cet écart de ~1.0 bit signifie que les séquences de caractères Voynich sont **environ deux fois plus prévisibles** que dans une langue naturelle. Cette anomalie est indépendante du système de transcription (confirmée sur EVA, Currier, Frogguy, v101, Takahashi).

Deux explications possibles : (a) le script encode plus d'un caractère source par glyphe Voynich (substitution verbose), ou (b) le script est syllabique/logographique, comprimant naturellement l'entropie au niveau caractère.

---

## Couche 2 — Transformations mathématiques / Mathematical Transformations

### Transformations testées et résultats / Transformations tested

| Famille | Paramètres testés | Meilleur ΔH2 | H2 résultant | Langue cible la plus proche |
|---------|-------------------|-------------|-------------|---------------------------|
| Fibonacci | offsets 0-5 | +0.18 | 2.21 | — |
| Log base φ | — | +0.12 | 2.15 | — |
| Log base 2 | — | +0.09 | 2.12 | — |
| Log base e | — | +0.11 | 2.14 | — |
| Sin(n·φ) | — | +0.22 | 2.25 | — |
| Sin(n·π) | — | +0.15 | 2.18 | — |
| Cos(n·φ) | — | +0.19 | 2.22 | — |
| Linéaire k=1-7 | k=3 meilleur | +0.14 | 2.17 | — |
| Fib + Sin(φ) | — | +0.28 | 2.31 | — |
| n·log(n) k=1-3 | k=2 meilleur | +0.16 | 2.19 | — |
| φ^(n/k) k=1-3 | k=2 meilleur | +0.21 | 2.24 | — |
| Atbash | — | +0.05 | 2.08 | — |
| Atbash + Fib | — | +0.24 | 2.27 | — |
| **Combinaisons doubles** | top 8 × top 8 | **+0.31** | **2.34** | — |

### Conclusion

Le déplacement maximum de H2 obtenu est de **+0.31 bit** (combinaison Fib+Sin(φ) → Log(φ)), portant H2 de 2.03 à 2.34. Cela reste **0.96 bit en dessous** de la cible latin (3.30). Aucune transformation ou combinaison ne comble l'écart. La probabilité que le chiffrement soit une transformation mathématique pure est jugée très faible.

Ce résultat négatif est cohérent avec le modèle de substitution verbose (Greshko 2025) : dans un tel chiffre, l'entropie basse est un artefact de la redondance inhérente au mapping 1-caractère → multi-glyphes, pas d'une transformation mathématique.

---

## Couche 3 — Mapping phonétique Bax / Bax Phonetic Mapping

### Valeurs intégrées / Values integrated

| Glyphe EVA | Son proposé (IPA) | Confiance Bax | Source de dérivation |
|-----------|-------------------|---------------|---------------------|
| k | /k/ | Haute | Coriandre, Centaurée, Hellébore |
| o | /a/ | Haute | Genévrier (OROR = 'arar') |
| r | /r/ | Haute | Genévrier |
| t | /t/ ou /θ/ | Moyenne | Taureau (zodiac f68r) |
| n | /n/ | Moyenne | Centaurée, Taureau |
| sh | /ʃ/ | Moyenne | Par analogie structurelle |
| ch | /x/ ou /tʃ/ | Moyenne | Chiron (f2r), 'char' (f29v) |
| th | /θ/ | Basse | Par analogie |
| a | /a/ | Basse | Contexte vocalique |
| i | /i/ | Basse | Contexte vocalique |
| e | /e/ | Basse | Contexte vocalique |
| y | /j/ | Basse | Contexte semi-vocalique |
| d | /d/ | Basse | Non dérivé par Bax, inféré |
| l | /l/ | Basse | Non dérivé par Bax, inféré |

### Limites documentées

- **Problème des gallows :** ~108 pages botaniques commencent par un des 4 gallows characters. Si tous = /k/ ou /t/, presque tous les noms de plantes commenceraient par K — improbable.
- **Trois /r/ :** Trois glyphes distincts mappés à des variantes de /r/ — typologiquement inhabituel.
- **Couverture :** 14 glyphes sur ~25, 10 mots sur ~38 000 (0,03 %).

---

## Couches 5-6 — Traduction et transposition / Translation and Transposition

### Couche 5 : Exemple de traduction incohérente (f2r, ordre original)

> « cette-mixture verser terre-sève moment mélange soleil plante-racine du-temps soigner lotion préparation soleil sève-huile moment terre baume-agit soin-branche plante racine du-temps soleil onguent-fort herbe-séchée de-la branches pousse moment feuilles herbe-séchée sève du-temps préparation sève-épaisse baume de-la fleur-eau huile du-temps baume feuilles herbe-séchée baume branches du-temps remède soleil plante herbe-séchée »

**Observation :** Les mots individuels sont plausibles dans un contexte d'herbier (plante, racine, sève, onguent, baume, remède, feuilles) mais leur enchaînement ne forme pas de phrases cohérentes. C'est ce constat qui a conduit Nicolas à formuler l'hypothèse de transposition.

### Couche 6 : Scores de transposition

| Stratégie | Score autocorrélation (lag 1) | Pattern constant ? | Score Fibonacci | Score colonnes 5 | Score colonnes 7 |
|-----------|------------------------------|-------------------|----------------|-----------------|-----------------|
| Grammaire SVO | -0.12 | Non | 18 % | 12 % | 8 % |
| Inversé | +0.03 | Oui (=-1) | 0 % | 0 % | 0 % |
| Boustrophédon 5 | +0.08 | Non | 5 % | 22 % | 4 % |
| Boustrophédon 7 | -0.05 | Non | 3 % | 6 % | 19 % |
| Colonnes 5 | +0.15 | Non | 7 % | 28 % | 5 % |
| Colonnes 7 | +0.11 | Non | 4 % | 5 % | 25 % |
| Spirale | -0.09 | Non | 6 % | 9 % | 7 % |
| Fibonacci | +0.04 | Non | 32 % | 8 % | 6 % |
| Nombre d'or | -0.02 | Non | 14 % | 10 % | 9 % |

**Aucun score ne dépasse le seuil de significativité** (>50 % pour les patterns structurels, >0.3 pour l'autocorrélation). Conclusion : si transposition il y a, elle ne suit pas un pattern mathématique régulier. Le paradigme doit changer.

---

## Couches 7-8 — Template herbier et analyse positionnelle / Herbal Template and Positional Analysis

### Distribution des phases dans l'ordre original de f2r

```
Mot:    1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18
Phase:  1  3  2  3  3  2  1  T  4  4  4  2  2  3  2  4  4  1

Mot:   19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36
Phase:  2  T  2  4  1  3  2  1  3  2  1  2  T  4  2  4  3  1

Mot:   37 38 39 40 41 42 43 44 45 46 47 48
Phase:  3  T  4  2  1  4  2  T  4  2  1  1

T = Transitionnel (daiin)
```

### Statistiques clés

| Métrique | Valeur | Interprétation |
|----------|--------|----------------|
| Transitions avant (n → n+k) | 55,3 % | Flux globalement directionnel ✅ |
| Transitions arrière (n → n-k) | 19,1 % | Retours limités |
| Même phase (n → n) | 25,5 % | Regroupement intra-phase |
| Position moy. Phase 4 (Médical) | 63 % du texte | Concentration en fin ✅ |
| Position de « otar » (remède) | 94 % du texte | Conclusion thérapeutique ✅ |
| Occurrences « daiin » dans f2r | 5 sur 48 mots (10,4 %) | Cohérent avec densité *item* en Currier A |

### Correspondance avec le template Pseudo-Apuleius

| Élément du template | Position attendue | Position observée dans f2r | Correspondance |
|--------------------|--------------------|---------------------------|---------------|
| « Herba [nom] » | Tout début | Mot 1 (kchor) = hapax | ✅ |
| Description/synonymes | Début | Mots 2-7 : cth-, sh- (terre, soleil) | ✅ |
| « Ad [condition] » + recette | Milieu | Mots 8-18 : mélange ot-, ok-, ch- | ✅ |
| *Item* (transition) | Entre recettes | « daiin » en pos. 8, 20, 31, 38, 44 | ✅ |
| Conclusion thérapeutique | Fin | « otar » en pos. 45 (94 %) | ✅ |
| Clôture par nom de plante | Toute fin | qokain + qokeedy en pos. 47-48 | ✅ |

**6 correspondances sur 6 éléments testés.** Ce score n'est pas une preuve de déchiffrement mais une indication forte de compatibilité structurelle avec le template Pseudo-Apuleius.

---

*Nicolas Van Eeckhout & Claude AI — Mars 2026 — CC BY-SA 4.0*
