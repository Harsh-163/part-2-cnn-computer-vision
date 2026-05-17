# Part 2: Computer Vision Problem Formulation and CNN Prototype

## Overview

This part formulates an **image classification** problem using a synthetic manufacturing defect dataset. A CNN-based prototype is built to classify product surface images into four categories: `normal`, `scratch`, `dent`, and `stain`. The work covers CNN concepts, preprocessing, model training, evaluation, and a business use case mapping.

---

## Directory Structure

```
part-2-cnn-computer-vision/
│
├── notebook.ipynb                        # Main Jupyter Notebook (all tasks)
├── requirements.txt                      # Python dependencies
├── README.md                             # This file
│
├── sample_predictions/
│   └── prediction_outputs.png            # Sample images from each defect class
│
└── results/
    ├── accuracy_loss_curves.png          # Training loss + accuracy plots
    └── confusion_matrix.png              # Confusion matrix (4-class)
```

---

## Dataset

**Source:** Synthetic Manufacturing Defect Image Dataset  
**Classes:** 4 (normal, scratch, dent, stain)  
**Images per class:** 120  
**Total images:** 480  
**Image dimensions:** 96×96 pixels, RGB

| Class | Description |
|---|---|
| `normal` | Product surface with no visible defect |
| `scratch` | Surface with scratch-like linear marks |
| `dent` | Circular dent-like depressions |
| `stain` | Colored stain marks on the surface |

---

## Setup & Execution

```bash
pip install -r requirements.txt
jupyter notebook notebook.ipynb
```

Run all cells in order. Output images are saved automatically to `results/` and `sample_predictions/`.

---

## CNN Concept Summary

| Concept | Purpose |
|---|---|
| **Convolution** | Learns spatial features (edges, textures, shapes) via sliding filters |
| **Pooling** | Reduces spatial size, improves translation invariance |
| **ReLU** | Introduces non-linearity, avoids vanishing gradients |
| **Flatten → Dense** | Converts feature maps to class probabilities |

---

## Business Use Case

**Domain: Manufacturing — Visual Defect Inspection**  
This system can be integrated into a production line camera to inspect 100% of products in real time, replacing slow and error-prone manual sampling checks.
