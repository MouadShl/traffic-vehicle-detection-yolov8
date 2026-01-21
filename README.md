# 🚦 Système de Gestion de Trafic Urbain Intelligent  
## 🧠 Détection de Voitures & Motos sur Vidéo avec YOLOv8 (Google Colab)

<p align="center">
  <img src="https://img.shields.io/badge/Computer%20Vision-YOLOv8-blue" />
  <img src="https://img.shields.io/badge/Platform-Google%20Colab-orange" />
  <img src="https://img.shields.io/badge/Task-Object%20Detection-green" />
  <img src="https://img.shields.io/badge/Tracking-ByteTrack-purple" />
  <img src="https://img.shields.io/badge/Status-Student%20Project-brightgreen" />
</p>

<p align="center">
  <a href="https://colab.research.google.com/github/<GITHUB_USERNAME>/<REPO_NAME>/blob/main/Trafficproject.ipynb">
    <img src="https://colab.research.google.com/assets/colab-badge.svg" />
  </a>
</p>

---

## 👤 Informations
- 🧑‍🎓 **Auteur :** Mouad Souhal  
- 🏫 **École :** SUP MTI  
- 📅 **Année universitaire :** 2026 – 2027  
- 📌 **Projet :** Vision par ordinateur appliquée à la gestion du trafic urbain

---

## 🎯 Objectif du projet
Ce projet propose un prototype de **gestion intelligente du trafic urbain** basé sur la **Vision par Ordinateur** et l’**Intelligence Artificielle**.

✅ Le système prend une **vidéo** en entrée et détecte automatiquement :  
- 🚗 **Voitures (car)**  
- 🏍️ **Motos (motorcycle)**  

📌 En sortie, le système génère une **vidéo annotée** avec :
- des **bounding boxes** (boîtes)  
- des **labels** (car / motorcycle)  
- un **score de confiance** (confidence)

---

## 🧩 Fonctionnalités
### ✅ Fonctionnalités principales
- 🎥 Import d’une vidéo (upload dans Colab)
- 🔍 Détection d’objets sur vidéo via **YOLOv8**
- 🏷️ Filtrage uniquement sur **voitures** et **motos**
- 💾 Sauvegarde automatique de la vidéo annotée
- 📥 Téléchargement du résultat final

### ⭐ Fonctionnalités optionnelles
- 🧭 **Tracking** des véhicules (ID) via **ByteTrack**
- ⚙️ Ajustement du seuil `conf` pour améliorer la précision

---

## 🛠️ Technologies utilisées
- ☁️ **Google Colab** (GPU)
- 🤖 **Ultralytics YOLOv8** (`yolov8n.pt`)
- 🧾 **COCO Dataset (pré-entraîné)**
- 🎞️ **OpenCV** (outils vidéo)
- 🧭 **ByteTrack** (tracking multi-objets)

📌 **Classes COCO utilisées :**
- 🚗 `car = 2`  
- 🏍️ `motorcycle = 3`

---

## 🧠 C’est quoi YOLO ?
**YOLO** signifie **You Only Look Once**.  
C’est une méthode rapide de **détection d’objets** qui analyse une image en une seule passe et renvoie :
- 📍 la position des objets (**bounding boxes**)
- 🏷️ la catégorie (**classe**)
- ✅ un score de confiance (**confidence score**)

YOLO est très utilisé pour des applications temps réel : surveillance, trafic, sécurité, etc.

---

## 🏗️ Pipeline du système
Voici le workflow du projet :

1. 📤 Upload de la vidéo dans Colab  
2. 🖼️ Extraction des frames (automatique)  
3. 🔍 Détection YOLOv8 : voitures + motos  
4. 🧭 (Optionnel) Tracking ByteTrack (ID véhicule)  
5. 🏷️ Annotation : boîtes + labels + scores  
6. 💾 Export et sauvegarde de la vidéo annotée  
7. 📥 Téléchargement du résultat

**Schéma :**  
🎥 Vidéo → 🖼️ Frames → 🔍 Détection → 🧭 Tracking → 🏷️ Annotation → 💾 Export

---

## 🚀 Démarrage rapide (Google Colab)
### 1) Ouvrir le notebook
Clique sur le bouton ci-dessous :  
👉 **Open in Colab**  
https://colab.research.google.com/github/<GITHUB_USERNAME>/<REPO_NAME>/blob/main/Trafficproject.ipynb

### 2) Activer le GPU
Dans Colab :  
`Runtime → Change runtime type → GPU`

### 3) Exécuter les cellules
Exécute les cellules dans l’ordre :
- installation
- upload vidéo
- détection / tracking
- export + download

---

## 🧪 Commandes principales
### ✅ Détection (FAST)
```bash
yolo task=detect mode=predict model=yolov8n.pt source="VIDEO" classes=2,3 conf=0.25 save=True
