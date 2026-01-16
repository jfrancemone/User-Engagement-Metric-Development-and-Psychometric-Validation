# 📈 Emotional Dynamics Scale Development & Psychometric Validation

[![Publication](https://img.shields.io/badge/Publication-Media_Psychology_(2023)-blue)](https://doi.org/10.1080/15213269.2023.2215447)
[![Method](https://img.shields.io/badge/Method-Psychometrics_%7C_Survey_Validation_(N%3D2,626)-green)](https://github.com/jfrancemone/User-Engagement-Metric-Development-and-Psychometric-Validation)
[![Tools](https://img.shields.io/badge/Tools-SPSS_%7C_AMOS-orange)](https://github.com/jfrancemone/User-Engagement-Metric-Development-and-Psychometric-Validation)

### **Project Overview**

Can we measure how content moves users, not just whether they liked it? This project demonstrates **Advanced Psychometrics** and **Scale Development** by creating and validating the **Emotional Flow Scale** — a 6-item instrument that captures the trajectory of user emotions during content consumption.

Standard sentiment metrics are static ("Positive" or "Negative"). But engagement is a process. Across 7 studies (N = 2,626), I led the statistical validation of a scale measuring dynamic emotional experience that encapsulates the shifts, peaks, and valleys users feel as they consume content. Research shows this emotional flow correlates with deeper engagement and more positive content evaluation, suggesting potential applications for engagement measurement.

> **📄 Publication:**
> Fitzgerald, K., Francemone, C. J., Green, M. C., Grizzard, M., & Frazer, R. (2023). The Emotional Flow Scale: Validating a measure of dynamic emotional experiences in message reception. *Media Psychology, 26*(6), 668–689.
>
> [**Read the Full Paper (PDF)**](Francemone_Scale_Development_2023.pdf)

*Note: This project uses SPSS and AMOS for statistical modeling. The psychometric approach (CFA, invariance testing) is tool-agnostic and transferable to Python-based workflows (e.g., semopy, factor_analyzer).*

---

### **Key Findings & Strategic Insights**

#### **1. Dynamic Experience Predicts Evaluation**
* **The Finding:** Static enjoyment (how "fun" content was) is a weaker predictor of meaningful engagement than Emotional Flow (how much the content *moved* the user).
* **Implication:** For platforms seeking deeper engagement (e.g., Streaming, EdTech), emotional diversity (ups and downs) may matter more than pure positivity. This scale provides a validated way to measure that dynamic.

#### **2. Cross-Population Stability (Invariance Testing)**
Rigorously tested the metric to ensure the scale works across different content formats and user populations.
* **The Finding:** The scale demonstrated **Measurement Invariance** across text-based vs. audio-visual video content, different age groups, and genders.
* **Implication:** The instrument measures the same construct consistently across contexts, which is a prerequisite for any metric intended for cross-platform or cross-demographic comparison.

#### **3. Sensitivity to Content Manipulation**
* **The Validation:** In a controlled experiment, content was manipulated to have 0, 1, or 2 emotional shifts.
* **The Result:** The metric successfully detected these shifts with linear precision.
* **Implication:** The instrument is sensitive enough to detect real differences in content structure, suggesting potential utility for content testing and optimization.

---

### **The Validated Instrument (Emotional Flow Scale)**
The final 6-item scale (Cronbach's α = .92):
1. "I felt a range of emotions."
2. "Some of my emotions felt intense while others felt less intense."
3. "I felt a series of shifts in my emotions."
4. "I felt like I was on an emotional rollercoaster."
5. "I felt negative emotions at times, while at other times I felt positive emotions."
6. "My feelings changed a lot from the beginning to the end."

<img src="factor_structure_viz.png" alt="CFA Path Diagram" width="75%">

---

### **Methodology**

* **Data Source:** N = 2,626 participants aggregated across 7 independent studies.
* **Psychometric Validation:**
    * **Exploratory Factor Analysis (EFA):** To identify the latent structure of emotional dynamics from an initial 18-item pool.
    * **Confirmatory Factor Analysis (CFA):** Optimized the scale to a concise, high-reliability 6-item instrument.
    * **Measurement Invariance Testing:** Statistically confirmed the scale works equivalently across Gender, Age, Sample Type, and Media Format (Text vs. Video).
* **Tools:**
    * **SPSS:** Initial data management and exploratory factor analyses.
    * **AMOS:** Confirmatory factor analyses, structural equation modeling, and multi-group invariance testing.

---

### **Repository Structure**

```text
/User-Engagement-Metric-Development-and-Psychometric-Validation
│
├── /data
│   ├── EFS_data.csv                              <-- Complete dataset (converted to csv)
│   └── EFS_data.sav                              <-- Original dataset (SPSS format)
│
├── /baseline_model_invariance_tests              <-- Final Model (6-Item Model)
│   ├── baseline_model.amw                        <-- Path diagram & model specification (AMOS)
│   ├── baseline_model.AmosOutput                 <-- Statistical output (Chi-Square, CFI, RMSEA)
│   ├── /age                                      <-- Invariance testing: Younger vs. Older
│   ├── /sex                                      <-- Invariance testing: Male vs. Female
│   ├── /sample                                   <-- Invariance testing: Student vs. General Pop
│   └── /stimuli                                  <-- Invariance testing: Text vs. Video Content
│
├── /model_comparison_invariance_tests            <-- Robustness Checks (9-Item Model)
│   ├── 9_item_comparison_model.amw               <-- Alternative specification for fit comparison
│   ├── 9_item_comparison_model.AmosOutput        <-- Output for comparison
│   └── (Subfolders contain full invariance suite for the 9-item structure)
│
├── Francemone_Scale_Development_2023.pdf         <-- Full publication
└── factor_structure_viz.png                      <-- Model visualization
```

---

### **My Role**
**Lead Statistician (Second Author)**
* Led all psychometric analyses, including exploratory and confirmatory factor analyses.
* Managed data aggregation across 7 distinct sample populations (N = 2,626).
* Conducted all measurement invariance testing to confirm cross-population and cross-platform scale stability.
* Co-authored the peer-reviewed publication in *Media Psychology.*
