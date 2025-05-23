# 📩 Détection de SMS Spam avec le Machine Learning

Ce projet a été réalisé dans le cadre du **Master SSD (Statistiques et Sciences des Données)**. Il consiste à construire un pipeline de classification de messages SMS en **spam** ou **ham** (non spam), avec une prise en charge des messages **en langue arabe ou francais... -> traduits en anglais**.

---

## 🎯 Objectifs du projet

- Construire un modèle de classification de texte à l’aide de :
  - Naive Bayes Gaussien
  - Naive Bayes Multinomial
  - Régression Logistique
  - K-Nearest Neighbors (KNN)
- Prétraitement des messages avec la **vectorisation TF-IDF**
- Support des messages en **arabe ,francais ,....**, traduits automatiquement en anglais
- Comparaison des performances des modèles à l’aide de métriques classiques

---

## 📁 Jeu de données

- **Source** : SMS Spam Collection Dataset
- Contenu :
  - `ham` : message normal
  - `spam` : message indésirable

---

## 🛠️ Technologies utilisées

- Python
- Scikit-learn (`sklearn`)
- Pandas, NumPy
- Matplotlib / Seaborn (pour les visualisations)
- `deep-translator` (pour la traduction  vers l’anglais)

---

## 📊 Performances des modèles

| Modèle                    | Accuracy |
|---------------------------|----------|
| Régression Logistique     | 97.96%   |
| Naive Bayes Multinomial   | 98.94%   |
| Naive Bayes Gaussien      | 96.86%   |
| KNN                       | 92.83%   |

La **Naive Bayes Multinomial** a obtenu les meilleures performances sur le jeu de test.

---

## 🌐 Traduction automatique

Pour prendre en charge les SMS en arabe,francais .... , la bibliothèque `deep_translator` a été utilisée :

```python
from deep_translator import GoogleTranslator

msg_ar = "لقد ربحت جائزة، اضغط على هذا الرابط"
msg_en = GoogleTranslator(source='ar', target='en').translate(msg_ar)
