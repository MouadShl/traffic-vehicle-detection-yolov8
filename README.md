# Système de Gestion de Trafic Urbain Intelligent (YOLOv8)

**Auteur:** Mouad Souhal  
**École:** SUP MTI  
**Année:** 2026–2027  

## Description
Ce projet détecte automatiquement les **voitures** et **motos** à partir d'une **vidéo** et génère une **vidéo annotée** (bounding boxes + labels) en utilisant **YOLOv8** sur **Google Colab**.

- Classes COCO utilisées : `car = 2`, `motorcycle = 3`
- Option : Tracking (ByteTrack)

## Exécution (Google Colab)
1. Ouvrir le notebook `Trafficproject.ipynb` dans Google Colab.
2. Activer GPU: Runtime → Change runtime type → **GPU**
3. Exécuter les cellules dans l’ordre.
4. Importer une vidéo via `files.upload()`.
5. Télécharger la vidéo annotée générée dans `runs/detect/...`.

## Commande principale
```bash
yolo task=detect mode=predict model=yolov8n.pt source="VIDEO" classes=2,3 conf=0.25 save=True
