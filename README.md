# SIGGRAPH17 Image Colorization (PyTorch)

This repository is the **automatic image colorization** task using a **SIGGRAPH17-based architecture combined with a GAN framework (Generator / Discriminator)**

The model learns to predict color information (**ab channels**) from a grayscale image (**L channel**) in the **Lab color space**.

---

## 1. Overview

* **Task**: Automatic image colorization
* **Color Space**: Lab
* **Input**:

  * L channel (Lightness – grayscale image)
* **Output / Target**:

  * ab channels (color information)

### Model Architecture

* **Generator**: `SIGGRAPHGenerator`
* **Discriminator**: `NLayerDiscriminator` (PatchGAN-style)


---

## 2. Dataset

* **Dataset**: **COCO 2017**
* Images are loaded in **RGB** format and converted to **Lab** during preprocessing.
* Training objective: learn a mapping from **L → ab**.

---

## 3. Technologies Used

* **Programming Language**: Python
* **Notebook Environment**: Jupyter Notebook (`.ipynb`)
* **Python Version**: 3.8 or higher
* **Deep Learning Framework**: PyTorch
* **Key Libraries**:

  * torchvision
  * numpy, pandas
  * pillow (PIL)
  * scikit-image
  * opencv-python
  * matplotlib
  * tqdm
* **Operating Systems**: Windows, macOS

---

## 4. Installation Guide

### 4.1 Set Up Virtual Environment

Create a virtual environment to isolate dependencies:

```bash
python -m venv venv
```

Activate the virtual environment:

```bash
# macOS / Linux
source venv/bin/activate

# Windows
venv\Scripts\activate
```

### 4.2 Install Required Libraries

Install all dependencies using `requirements.txt`:

```bash
pip install -r requirements.txt
```
