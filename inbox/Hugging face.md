# 🤗 Hugging Face — Guide & Référence

## 📌 Description
**Hugging Face** est la plateforme de référence et le principal écosystème de l'intelligence artificielle open-source (souvent surnommé le *« GitHub de l'IA »*).

Contrairement à un simple moteur d'exécution local (comme Ollama), Hugging Face combine :
- **Un hub centralisé** hébergeant des millions de modèles, jeux de données et démonstrations.
- **Une suite de bibliothèques Python** permettant de télécharger, exécuter, entraîner et optimiser des modèles sur sa propre machine ou dans le cloud.
- **Des services d'hébergement et d'inférence** pour tester ou déployer des applications IA.

---

## 🧩 Les 3 piliers du Hub

| Pilier | Rôle | Ce qu'on y trouve |
| :--- | :--- | :--- |
| **Models** | Catalogue de modèles pré-entraînés | Texte (LLM), vision, génération d'images, audio/voix, vidéo, multimodal, robotique. |
| **Datasets** | Jeux de données prêts à l'emploi | Corpus de texte, images annotées, audio, données structurées (souvent au format Parquet). |
| **Spaces** | Hébergement d'applications et démos | Interfaces web interactives (Gradio, Streamlit, Docker) pour tester les modèles directement dans le navigateur. |

> **💡 Bon à savoir :** Chaque modèle possède une **Model Card** détaillant son architecture, sa licence, ses limites, ses benchmarks et un exemple de code pour le lancer.

---

## 🛠️ Fonctionnalités & Bibliothèques principales

### 1. Exécution et inférence locale
- **`transformers`** : Bibliothèque cœur permettant de charger et d'exécuter presque n'importe quel modèle en quelques lignes de Python (via PyTorch, TensorFlow ou JAX).
- **`diffusers`** : Bibliothèque dédiée aux modèles de génération d'images, d'audio et de vidéo (ex. : Stable Diffusion, Flux).
- **Format `safetensors`** : Format standard sécurisé et ultra-rapide développé par Hugging Face pour stocker les poids des modèles sans risque d'exécution de code malveillant.

### 2. Entraînement, adaptation et optimisation
- **`datasets`** : Téléchargement, streaming et prétraitement rapide de gros volumes de données.
- **`peft` (Parameter-Efficient Fine-Tuning)** : Permet d'adapter (*fine-tuner*) un gros modèle sur du matériel modeste grâce à des techniques comme **LoRA / QLoRA**.
- **`accelerate`** : Simplifie l'exécution du code sur CPU, mono-GPU, multi-GPU ou TPU sans réécrire la logique d'entraînement.
- **`trl` (Transformer Reinforcement Learning)** : Outils pour l'alignement de modèles (SFT, DPO, RLHF).

### 3. Agents & Outils modernes
- **`smolagents`** : Framework minimaliste pour créer des agents IA capables d'exécuter du code Python et d'appeler des outils externes.
- **`huggingface_hub` & CLI (`hf`)** : Outil en ligne de commande et SDK Python pour gérer l'authentification, le téléchargement de modèles, le cache local et le versionnement Git-LFS.
