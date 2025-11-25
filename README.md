<p align="center">
  <img src="assets/logo/R-SIT_v1_logo.png" width="200" alt="R-SIT Logo"/>
</p>

# **R-SIT v1 — Robotic Social Interaction Taxonomy**

## 🔍 **What is R-SIT?**

**R-SIT (Robotic Social Interaction Taxonomy)** is a structured, extensible taxonomy for representing human social interactions from a robot’s point of view. It provides a unified vocabulary and conceptual framework for building datasets, benchmarks, and models that perform robot-centric social scene understanding.

This repository contains the first public release (v1) of the taxonomy.

R-SIT defines a set of interpretable, perceptually grounded dimensions describing social situations as seen by a robot-mounted camera, focusing exclusively on features that can be visually inferred—including pose, proximity, gaze, facial expression, group structure, and contextual cues.

---

## 🧠 **Why create a new taxonomy?**

Despite extensive research in social psychology and HRI, **no existing taxonomy describes social interactions specifically for robot perception**.
Robots operate under unique constraints:

* monocular or RGB-D cameras
* partial views / occlusions
* limited field of view
* real-time inference requirements
* absence of linguistic context

R-SIT fills this gap by offering a taxonomy that is:

* **grounded in psychological theory**,
* **designed for robot vision**,
* **extensible for future research**,
* **simple enough for dataset generation**,
* **structured for machine learning pipelines**.


---

## 📚 **Scientific Foundations**

R-SIT v1 is grounded in a multidisciplinary set of theories and empirical findings:

### **F-Formation & Spatial Interaction**

* Kendon, A. *Conducting Interaction*
* Setti et al. (2015). *F-Formation Detection*
* Hall, E. *The Hidden Dimension* (proxemics)

### **Robot-Centric Perception**

* Webb, N., Giuliani, M., & Lemaignan, S. *Measuring Visual Social Engagement from Proxemics and Gaze*
* Repiso et al. (2020). *Adaptive Social Robot Navigation*

### **Social Cognition & Commonsense Reasoning**

* Sap et al. (2019). *Social IQa Dataset*
* Bartlett et al. (2019). *Inferring Internal States from Movement*

### **General Social & Cognitive Psychology**

* Goffman, E. *The Interaction Order*
* Fiske, A. *Relational Models Theory*

These works collectively justify the dimensions selected for R-SIT v1.

---

## 📁 **Repository Structure**

```
R-SIT/
│
├── README.md
├── taxonomy/
│   ├── R-SIT_v1.json
│   └── R-SIT_v1.md
│
├── sources/
│   ├── F-Formation.pdf
│   ├── Measuring_Visual_Social_Engagement.pdf
│   ├── SOCIAL_IQA.pdf
│   └── reference_list.md
│
├── dataset_spec/
│   ├── combinations_v1.json
│   └── annotation_guidelines.md
│
└── examples/
    ├── sample_annotations.json
    └── images/
```


---

## 🔖 **How to Cite R-SIT**

```bibtex
@misc{pallonetto2025rsit,
  title={R-SIT: Robotic Social Interaction Taxonomy},
  author={Pallonetto, Luca and Lemaignan, Severin},
  year={2025},
  publisher={GitHub},
  howpublished={\url{https://github.com/lulilac/R-SIT}}
}
```


