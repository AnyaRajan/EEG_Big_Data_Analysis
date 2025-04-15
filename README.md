# EEG and Decision Game-Based Prediction of Trait Anxiety

**Team Members:**
- Ahmad Raza (220088)  
- Anya Rajan (220191)  
- Debarpita Dash (220328)  
- Manasvi Nidugala (220613)  
- Nischay Patel (220721)  
- Poojal Katiyar (220770)  

---

## 🧠 Project Overview

This project aims to **predict trait anxiety levels** using a combination of **behavioral patterns** and **EEG signals** collected during a decision-making game. By leveraging **machine learning (ML)** and **deep learning (DL)** techniques, we seek to build **computational models** that provide a more objective understanding of anxiety—beyond traditional self-report tools.

---

## 🔍 Problem Statement

Trait anxiety significantly impacts cognitive processes like decision-making, attentional control, and emotional regulation. While tools like the **State-Trait Anxiety Inventory (STAI)** offer psychological insight, they lack the neurophysiological depth needed for computational psychiatry.

This study integrates **EEG data**, **game-based behavior**, and **neurophysiological signals** (e.g., cortisol, norepinephrine) to build models capable of **distinguishing trait anxiety patterns** in naturalistic settings.

---

## 📚 Background & Significance

### 1. Trait vs. State Anxiety
- **Trait Anxiety:** Chronic tendency to feel anxious; stable across situations.
- **State Anxiety:** Transient anxiety response to specific events or stressors.

> Our focus is on **trait anxiety**, as it provides more consistent neural and behavioral markers.

### 2. Why Foraging Tasks?
- Foraging tasks simulate **real-world decisions under uncertainty**, ideal for studying anxiety-related cognitive mechanisms.
- Based on neuroscience findings on **theta-phase precession**, foraging tasks reflect natural decision-making circuits.

### 3. EEG as a Neurophysiological Marker
EEG frequency bands and their functions under anxiety:

| Wave Type | Frequency | Function | Effect in Anxiety/Stress |
|-----------|-----------|----------|---------------------------|
| **Delta** | 0.5–4 Hz  | Deep sleep, healing | ↓ Decreases |
| **Theta** | 4–8 Hz    | Emotion, memory | ↑ Increases |
| **Alpha** | 8–12 Hz   | Relaxation, clarity | ↓ Decreases |
| **Beta**  | 12–30 Hz  | Focus, alertness | ↑ Increases |
| **Gamma** | 30–50 Hz  | Cognition, fear response | ↑ Spikes in PTSD/trauma |

**Additional features extracted:**
- Theta/Beta ratio
- Sample Entropy
- ERP components (N200, P300, FRN)
- PAC (Phase-Amplitude Coupling)
- Alpha-band coherence in frontal channels

---

## 🧪 Physiological & Neuromodulatory Data

### 1. Stress Pathways:
- **HPA Axis:** Cortisol regulation → Mood, energy, and anxiety modulation
- **SAM Axis:** Norepinephrine release → Heightened alertness (fight or flight)

### 2. Biomarkers:
- **Salivary cortisol** (pre- and post-game)
- **Salivary alpha-amylase (sAA)** for norepinephrine activity
- Ensured no significant increase in **state anxiety**, isolating trait anxiety effects

---

## 🎮 Decision-Making Task Design

Data collected during 3 key windows:

### 🧠 Tonic Epoch
- EEG recorded **1000 ms before decision**
- Captures brain activity during deliberation

### ⏳ Decision Window
- Participant moves to center before choosing to **explore** (switch tree) or **exploit** (stay)
- Longer deliberation = greater hesitation

### 🖱️ Execution Window
- Time taken to **move mouse and click**
- Faster response = confidence  
- Slower response = hesitation or reconsideration

---

## 👥 Participants & Trials

- **N = 55 participants** (18 females)
- Each performed **~200–250 trials**
- Each trial = a single decision (explore/exploit)

---

## 💡 Contributions

This project:
- Demonstrates the **power of EEG** and **behavioral features** for anxiety modeling
- Provides an **interpretable and non-invasive tool** for trait anxiety detection
- Encourages use of **computational psychiatry** for understanding emotional and cognitive health

---

## 📌 Tools & Methods Used

- **EEG Preprocessing & Feature Extraction:** MNE-Python, NumPy, SciPy
- **Behavioral Analysis:** Custom Python scripts for mouse-tracking and timing
- **Machine Learning:** Scikit-learn, XGBoost, CatBoost
- **Deep Learning:** PyTorch, TensorFlow
- **Visualization:** Matplotlib, Seaborn

---

## 📂 Folder Structure (Recommended)

```bash
project-root/
│
├── data/
│   ├── eeg_raw/
│   ├── behavioral/
│   └── processed/
│
├── notebooks/
│   ├── ERP_Coherence.ipynb
│   ├── PAC_Analysis.ipynb
│   └── SampleEntropy_Feature.ipynb
│
├── models/
│   └── model_training_scripts/
│
├── results/
│   ├── plots/
│   └── metrics/
│
├── README.md
└── requirements.txt
