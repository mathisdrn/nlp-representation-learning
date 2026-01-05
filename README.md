# Representation learning for NLP

### Projet: Inférer automatiquement la relation entre deux phrases 

**Adrien Guille - M2 MALIA & MIASH - Université Lumière Lyon 2** 

---

## Tâche 

On se propose de mettre au point un système pour déterminer la relation entre deux phrases rédigées en français. 

La relation peut-être : 
* **Conséquence** 
* **Contradiction** 
* **Neutre** 

---

## Méthodologie 

On considérera plusieurs options: 

* Ajuster par apprentissage supervisé les encodeurs **CamemBERT 2.0** et **CamemBERTa 2.0** avec la méthode **LoRA** 
* Ajuster par apprentissage supervisé un décodeur de la série **Llama 3**, soit le modèle 1B soit le modèle 3B avec la méthode **LoRA** 
* Ajuster par apprentissage en contexte un décodeur **Llama 3 3B ou 8B** 
    * En mode 0-shot 
    * En mode few-shot 
    * En mode « Chain-of-Thought » 

**Évaluation :** Évaluer les performance de toutes ces approches en généralisation 

> **Conseil:** travailler avec des notebook sur kaggle.com, qui garantit 30h de GPU par semaine renouvelables (nécessite de vérifier son compte kaggle avec un numéro de téléphone) ainsi que la persistances des notebooks hors connexion. 

---

## Objectif pédagogique 

On vise à travers la réalisation de ce projet : 

* La compréhension de ce qui distingue CamemBERTa de CamemBERT 
* La compréhension de la technique LoRA pour l'ajustement efficace de grands modèles de langue 
* La compréhension du « Chain-of-Thought Prompting » 

---

### Usage

To run the code in this repository, you will need to create a Python environment with the dependencies specified in the `pyproject.toml`.
You can do so by installing `uv` (instructions [here](https://docs.astral.sh/uv/getting-started/installation/#standalone-installer)) and running `uv sync` in the repository root.

You can then run the notebooks using Jupyter or serve the markdown documents using `myst start`.