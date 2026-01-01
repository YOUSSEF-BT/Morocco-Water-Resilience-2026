# 🌊 Morocco Water Resilience 2026 – Ifrane

## 🎯 Objectif
Analyser le lien entre précipitations et niveau des barrages (signal simulé) pour une région climatique clé du Maroc (Ifrane), puis prédire le risque de stress hydrique à l’horizon 2026 avec un modèle de séries temporelles (Prophet).

## 📁 Contenu

- `Water_Resilience_Morocco_2026.ipynb` : notebook complet (données météo, simulation du niveau, visualisations, prédiction).
- `impact_pluie_niveau_barrages_ifrane.png` : graphique pluie vs niveau des barrages.
- `prediction_barrages_ifrane_2026.png` : projection du niveau des barrages jusqu’en 2026.

## 🧪 Méthodologie

1. Récupération des données météo quotidiennes (pluie, température) 2020–2025 pour Ifrane via une API météo ouverte.
2. Construction d’un signal de niveau de barrage avec :
   - composante saisonnière (remplissage/vidange annuelle),
   - tendance à la baisse (stress hydrique),
   - bruit aléatoire.
3. Analyse exploratoire :
   - courbe conjointe pluie / niveau,
   - indicateurs clés (minimum, maximum, moyenne, cumul de pluie).
4. Modélisation et prédiction :
   - entraînement d’un modèle Prophet,
   - projection du niveau de barrage sur l’année 2026,
   - comparaison au seuil critique de 10 %.

## 📈 Résultats

- Niveau moyen simulé : **37,6 %** (min ~ **15,8 %**, max ~ **59,1 %**).
- Cumul de précipitations : **3253,4 mm** sur 2020–2025.
- Le scénario projeté montre un risque de passage sous le **seuil critique de 10 %** en 2026, illustrant un contexte de stress hydrique sévère.

## 🛠️ Stack

Python · Pandas · Matplotlib · Prophet · API météo (données ouvertes).

## 👤 Auteur

Youssef Bouzit – Étudiant Cycle Ingénieur Data Science (SUP MTI Rabat).
