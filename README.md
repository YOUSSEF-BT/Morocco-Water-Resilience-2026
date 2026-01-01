# 🌊 Morocco Water Resilience 2026 – Ifrane

## 🎯 Objectif

Analyser le lien entre les précipitations et le niveau des barrages (signal simulé) pour une région climatique clé du Maroc (Ifrane), puis prédire le risque de stress hydrique à l’horizon 2026 à l’aide d’un modèle de séries temporelles (Prophet).  

---

## 📊 Aperçu Visuel des Résultats

### Impact des précipitations sur le niveau des barrages (2020–2025)

![Impact des précipitations](impact_pluie_niveau_barrages_ifrane.png)

Ce graphique montre l’évolution du niveau simulé des barrages (courbe) et des précipitations quotidiennes (barres) pour la zone climatique d’Ifrane entre 2020 et 2025.  

### Prédiction du niveau des barrages – Horizon 2026

![Prédiction 2026](prediction_barrages_ifrane_2026.png)

Le modèle Prophet projette l’évolution du niveau des barrages jusqu’en 2026, avec un **seuil critique de 10 %** matérialisé par une ligne rouge en pointillé.  

---

## 📁 Contenu du Projet

- `Water_Resilience_Morocco_2026.ipynb`  
  Notebook complet : récupération des données météo, construction du signal de niveau de barrage, visualisations, indicateurs et prédiction 2026.  
- `impact_pluie_niveau_barrages_ifrane.png`  
  Graphique pluie vs niveau des barrages (2020–2025).  
- `prediction_barrages_ifrane_2026.png`  
  Graphique de la projection du niveau des barrages jusqu’en 2026.  

---

## 🧪 Méthodologie

1. **Données météo réelles**  
   - Récupération des précipitations quotidiennes et de la température moyenne (2020–2025) pour Ifrane via une API météo ouverte.  
2. **Construction du signal de niveau de barrage**  
   - Composante saisonnière (cycles annuels de remplissage/vidange).  
   - Tendance à la baisse sur plusieurs années (stress hydrique).  
   - Bruit aléatoire pour refléter la variabilité naturelle.  
3. **Analyse exploratoire**  
   - Courbe conjointe pluie / niveau.  
   - Calcul d’indicateurs clés : moyenne, min, max du niveau, cumul des précipitations, corrélation pluie (30 jours cumulés) / niveau.  
4. **Modélisation & prédiction**  
   - Entraînement d’un modèle Prophet sur le niveau simulé.  
   - Projection du niveau des barrages sur 365 jours supplémentaires (année 2026).  
   - Comparaison au seuil critique de 10 %.  

---

## 📈 Indicateurs Clés (Ifrane 2020–2025)

- Niveau moyen des barrages : **37,6 %**  
- Niveau minimum observé : **≈ 15,8 %**  
- Niveau maximum observé : **≈ 59,1 %**  
- Total des précipitations : **≈ 3 253 mm**  
- Corrélation pluie (30 jours cumulés) / niveau : **≈ -0,05**  

Ces résultats illustrent une **tendance générale à la baisse** du niveau des barrages malgré un volume de précipitations significatif, ce qui reflète la pression croissante sur la ressource en eau.  

---

## 🛠️ Stack Technique

- Python  
- Pandas  
- Matplotlib  
- Prophet (modélisation de séries temporelles)  
- API météo (données ouvertes)  

---

## 🚀 Comment Reproduire l’Analyse

1. Cloner le repository :  
   ```
   git clone https://github.com/YOUSSEF-BT/Morocco-Water-Resilience-2026.git
   cd Morocco-Water-Resilience-2026
   
Installer les dépendances principales (exemple) :
   ```
pip install pandas matplotlib prophet requests
   ```
Ouvrir le notebook :

jupyter notebook Water_Resilience_Morocco_2026.ipynb
Exécuter les cellules dans l’ordre pour reconstruire les graphiques et les indicateurs.

👤 Auteur
Youssef Bouzit
Étudiant Cycle Ingénieur Data Science – SUP MTI Rabat
