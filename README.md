# 🚦 Système de Gestion de Trafic Urbain Intelligent  
## 🧠 Détection de Voitures & Motos sur Vidéo avec YOLOv8

<p align="center">
  <img src="https://img.shields.io/badge/AI-Computer%20Vision-blue" />
  <img src="https://img.shields.io/badge/Model-YOLOv8-green" />
  <img src="https://img.shields.io/badge/Application-Traffic%20Management-orange" />
  <img src="https://img.shields.io/badge/Level-Student%20Project-brightgreen" />
</p>

---

## 👤 Informations Générales
- 🧑‍🎓 **Auteur :** Mouad Souhal  
- 🏫 **École :** SUP MTI  
- 📅 **Année universitaire :** 2026 – 2027  
- 📚 **Matière :** Vision par Ordinateur / Intelligence Artificielle  

---

## 🎯 Objectif du Projet
Ce projet vise à concevoir un **prototype intelligent de gestion du trafic urbain** basé sur la **vision par ordinateur**.

🎥 À partir d’une **vidéo**, le système est capable de :
- détecter automatiquement les **voitures** 🚗  
- détecter automatiquement les **motos** 🏍️  
- générer une **vidéo annotée** (boîtes, labels, score de confiance)

L’objectif principal est de démontrer comment l’IA peut être utilisée pour **analyser le trafic routier de manière automatique**.

---

## 🚗 Pourquoi la gestion du trafic ?
Les villes modernes font face à plusieurs défis :
- 🚦 congestion routière  
- ⚠️ accidents  
- 📈 augmentation du nombre de véhicules  
- 🧍 surveillance manuelle coûteuse et limitée  

👉 La **vision par ordinateur** permet d’automatiser l’analyse des flux de véhicules à partir de caméras existantes.

---

## 🧠 C’est quoi YOLO ?
**YOLO (You Only Look Once)** est une famille de modèles de **détection d’objets**.

Contrairement aux méthodes classiques :
- YOLO analyse l’image **en une seule passe**
- il prédit directement :
  - 📍 la position (bounding box)
  - 🏷️ la classe de l’objet
  - ✅ un score de confiance

YOLO est très utilisé pour des applications **temps réel** :
- vidéosurveillance  
- trafic routier  
- drones  
- véhicules autonomes  

---

## 🤖 Modèle utilisé : YOLOv8
Dans ce projet, nous utilisons **YOLOv8** (Ultralytics), une version moderne et optimisée.

### Pourquoi YOLOv8 ?
- ⚡ rapide
- 🎯 bonne précision
- 🧩 facile à intégrer
- 🚀 adapté aux projets étudiants et prototypes

Le modèle utilisé est **YOLOv8n (nano)** :
- léger
- rapide
- idéal pour des tests sur vidéo

---

## 🧾 Dataset & Classes
Le modèle est **pré-entraîné** sur le dataset **COCO**.

📌 Classes utilisées dans ce projet :
- 🚗 **car = 2**
- 🏍️ **motorcycle = 3**

Les autres classes sont volontairement ignorées afin de se concentrer sur le trafic routier.

---

## 🛠️ Technologies Utilisées
- 🤖 **YOLOv8 (Ultralytics)**
- ☁️ **Google Colab (GPU)** pour l’exécution
- 🎞️ **OpenCV** pour la gestion vidéo
- 🧭 **ByteTrack** (optionnel) pour le tracking
- 🐍 **Python**

⚠️ Le notebook Colab **n’est pas partagé** dans ce dépôt.  
Ce repository présente la **méthodologie, l’architecture et les résultats**.

---

## 🏗️ Architecture du Système
Le pipeline du système est le suivant :

1. 📤 Import de la vidéo  
2. 🖼️ Traitement image par image  
3. 🔍 Détection des véhicules avec YOLOv8  
4. 🏷️ Annotation (boîtes + labels + score)  
5. 🎞️ Génération d’une vidéo annotée  
6. 📥 Export du résultat final  

**Schéma simplifié :**  
🎥 Vidéo → 🖼️ Frames → 🔍 Détection → 🏷️ Annotation → 🎞️ Vidéo annotée

---

## 🧭 Tracking des véhicules (Optionnel)
Le projet inclut une fonctionnalité optionnelle de **tracking multi-objets**.

📌 Grâce à **ByteTrack**, chaque véhicule reçoit :
- un **identifiant unique (ID)**
- un suivi stable sur plusieurs frames

🎯 Le tracking est utile pour :
- comptage des véhicules  
- analyse des trajectoires  
- estimation de vitesse (future amélioration)

---

## 📊 Résultats Obtenus
Le système permet d’obtenir :
- 🎞️ une vidéo annotée
- 🚗 détection fiable des voitures
- 🏍️ détection fiable des motos
- 🏷️ labels + score de confiance visibles

📸 Les résultats sont validés visuellement à partir des vidéos générées.

---

## ⚠️ Limites du Système
Comme tout prototype basé sur la vision par ordinateur :
- 🌙 performances réduites la nuit
- 🌧️ pluie, reflets et flou de mouvement
- 🚙 occlusion entre véhicules
- 📷 difficulté avec objets très éloignés

---

## 🔮 Améliorations Futures
Plusieurs extensions sont possibles :
- 🔢 comptage automatique (ligne virtuelle)
- 🏎️ estimation de vitesse
- 🚧 détection de congestion
- 🪪 reconnaissance de plaques (ALPR)
- 🏋️ entraînement sur un dataset local (caméras réelles)

---

## 🏁 Conclusion
Ce projet démontre qu’il est possible de construire un **système intelligent de détection de trafic** à partir d’une simple vidéo.

Grâce à **YOLOv8**, la détection est :
- rapide
- automatisée
- visuellement exploitable

Ce prototype constitue une **base solide** pour des systèmes avancés de gestion du trafic urbain.

---

## 📩 Contact
**Mouad Souhal**  
SUP MTI — 2026–2027  

