# 420-D62-BDEB
# 📊 Analyse de Churn & Rétention Client
**Online Retail II Dataset (2009–2011)**
## **Dataset source :** https://archive.ics.uci.edu/dataset/502/online+retail+ii

## 👥 Auteurs
- Malik Hamza Kouotou  
- Pierre Hubertin Andrianirina  

## 📅 Date
Mai 2026

---

## 📌 Objectif du projet

Ce projet vise à **identifier, prédire et segmenter les clients à risque de churn** dans un contexte e-commerce transactionnel, afin de permettre la mise en place de **stratégies de rétention ciblées et efficaces**.

---

## 🧠 Contexte business

- Dataset e-commerce britannique (UCI Machine Learning Repository)
- Pas de système d’abonnement → churn défini comportementalement
- **Définition du churn :**
  > Client sans achat depuis **plus de 90 jours**   

- Pourquoi c’est important :
  - Coût d’acquisition > coût de rétention (×5 à ×7)   
  - Besoin de ciblage data-driven pour éviter les campagnes inefficaces  

---

## 📂 Données

- **1 067 371 lignes** initiales  
- **805 549 lignes** après nettoyage   
- **5 878 clients identifiés**   

### 🔧 Nettoyage effectué
- Suppression des `CustomerID` manquants (~22,8%)
- Suppression des factures annulées
- Suppression des quantités/prix négatifs

---

## 🔍 Feature Engineering (RFM)

Variables principales construites :

- **Recency (R)** : jours depuis dernier achat  
- **Frequency (F)** : nombre de commandes  
- **Monetary (M)** : valeur totale dépensée  

Variables enrichies :
- AvgOrderValue  
- CustomerLifespan  
- PurchaseFreqPerMonth  
- NumCountries  

---

## 🤖 Modélisation

Trois modèles testés :

| Modèle                | Rôle |
|---------------------|------|
| Régression Logistique | Baseline |
| Random Forest        | ✅ Modèle principal |
| Gradient Boosting    | Modèle complémentaire |

### 📊 Résultats (Random Forest)
- ROC-AUC : **~0,95**
- Recall : **~0,91**
- Precision : **~0,92**   

👉 Excellente capacité à détecter les churners

---

## 📈 Variables les plus importantes

1. **Recency (42%)** ← facteur dominant  
2. Frequency (22%)  
3. Monetary (15%)   

👉 L’inactivité récente est le signal le plus fort de churn

---

## 👥 Segmentation client

4 segments de risque définis :

| Segment     | Probabilité | Action |
|------------|-------------|--------|
| 🔴 Critique | ≥ 75% | Appel + offre personnalisée |
| 🟠 À risque | 50–75% | Email ciblé |
| 🟡 Attention | 25–50% | Newsletter + fidélisation |
| 🟢 Fidèle | < 25% | Cross-sell & récompenses  

---

## 📉 Résultats clés

- **Taux de churn : 50,9%**  
- **~1 950 clients ciblés**  
- **91% des churners détectés**   

---

## Recommandations

### Court terme (0–30 jours)
- Cibler les clients critiques (~750)
- Offres de réactivation immédiates

### Moyen terme (1–3 mois)
- Mise à jour mensuelle des scores
- Intégration automatique dans le CRM

### Long terme
- Ajouter :
  - Catégorie produit
  - Saisonnalité
  - Customer Lifetime Value (CLV)

---

## Technologies utilisées

- Python (pandas, numpy)
- Scikit-learn
- Modèles ML :
  - Logistic Regression
  - Random Forest
  - Gradient Boosting
- Visualisation & analyse exploratoire

---

## Compétences développées

### Techniques
- Pipeline data science complet
- Feature engineering (RFM)
- Modélisation supervisée
- Évaluation multi-métriques

### Business
- Traduction besoin métier → ML
- Définition du churn
- Segmentation CRM actionnable

---

## 📁 Livrables

- 📊 Présentation finale
- 🧾 Code Python complet (~544 lignes)
- 📈 Modèle de prédiction du churn
- 👥 Segmentation client exploitable

---

## ✅ Conclusion

Ce projet démontre qu’une approche data-driven permet de :

- Prédire efficacement le churn
- Identifier les clients à risque
- Déployer des actions CRM ciblées

👉 Impact direct : optimisation des campagnes marketing et augmentation de la rétention client.

---

## 📬 Contact

Pour toute question ou collaboration, n'hésitez pas à nous contacter.
