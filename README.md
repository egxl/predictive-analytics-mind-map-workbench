# Predictive Analytics Mind Map Workbench

> An interactive visual workbench and hand-drawing companion for structuring, understanding, and drawing an end-to-end Predictive Analytics mind map on a single sheet of paper.

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![SVG](https://img.shields.io/badge/SVG-Interactive_Canvas-FFB13B?style=flat-square&logo=svg&logoColor=white)](https://www.w3.org/Graphics/SVG/)
[![Zero Dependencies](https://img.shields.io/badge/Dependencies-Zero_Install-success?style=flat-square)](#quick-start)

---

## Table of Contents

- [Overview](#overview)
- [Key Features](#key-features)
- [Taxonomy & Mind Map Architecture](#taxonomy--mind-map-architecture)
  - [1. Kind of Question](#1-kind-of-question)
  - [2. Family of Technique](#2-family-of-technique)
  - [3. Named Algorithms](#3-named-algorithms)
  - [4. Evaluation Metrics](#4-evaluation-metrics)
- [Relational Joins & Cross-Links](#relational-joins--cross-links)
- [Hand-Drawing Blueprint Strategy](#hand-drawing-blueprint-strategy)
- [Interactive Controls & Usage](#interactive-controls--usage)
- [Quick Start](#quick-start)
- [Tech Stack](#tech-stack)

---

## Overview

The **Predictive Analytics Mind Map Workbench** serves as an interactive reference guide and learning companion. It visualizes the core dimensions of predictive modeling—connecting problem formulations, modeling traditions, algorithms, and evaluation metrics into a coherent graph.

Designed specifically to guide learners and practitioners in constructing a comprehensive, hand-drawn mind map on a single sheet of paper, the workbench provides:
- A holistic view of predictive analytics concepts.
- Step-by-step progressive drawing views.
- Cross-cutting relational joins between algorithms, methodological families, and analytical questions.
- Detailed metrics formulas, definitions, and an interactive checklist.

---

## Key Features

- **Step-by-Step Drawing Guide**: Progressively isolate each phase of drawing your map:
  - `All View`: Complete blueprint showing all nodes and joins.
  - `1. 4 Branches`: Central root node and 4 primary branches.
  - `2. Sub-Nodes`: All questions, families, algorithms, and metric nodes.
  - `3. Algo → Family`: Relational links between algorithms and their parent disciplines.
  - `4. Algo → Question`: Connections matching algorithms to problems they solve.
  - `5. Metric → Question`: Links connecting evaluation metrics to compatible question types.
- **Relational Filtering**: Toggle visibility between All Joins, Algorithm $\to$ Family, Algorithm $\to$ Question, and Metric $\to$ Question.
- **Interactive Node Inspector**: Click or hover any node to reveal theoretical definitions, mathematical formulas, and mandatory connection requirements in the sidebar.
- **Dynamic Hover Isolation**: Hovering over any algorithm or metric highlights its active relational lines while dimming non-connected paths.
- **Pan & Zoom Canvas**: Smooth SVG canvas navigation supporting drag-to-pan, mouse-wheel zooming, and instant zoom reset.
- **Hand-Drawing Checklist**: Live interactive 14-item checklist tracking all mandatory elements for submission and study.
- **Zero-Build, Standalone Architecture**: Delivered as a self-contained HTML file running directly in any modern browser.

---

## Taxonomy & Mind Map Architecture

The mind map radiates outward from the central root: **`PREDICTION`**.

```
                           ┌── [Kind of question] ── (Classification, Regression, Time Series)
                           │
                           ├── [Family of technique] ── (Statistics, Machine Learning, Deep Learning)
       [ PREDICTION ] ─────┤
                           ├── [Algorithms] ── (Linear, Trees, Ensembles, Neural Nets, etc.)
                           │
                           └── [Metrics] ── (Accuracy, F1, RMSE, R², MAPE, etc.)
```

### 1. Kind of Question

Defines the predictive objective and target output structure:

| Node | Question Formulation | Example Use Case |
| :--- | :--- | :--- |
| **Classification** | Which discrete category or class does a record belong to? | Customer churn ($yes / no$), fraud detection, disease diagnosis |
| **Regression** | What continuous numerical quantity corresponds to this record? | House pricing, salary estimation, sales volume forecasting |
| **Time Series Forecasting** | What numerical values or patterns emerge next in chronological order? | Quarterly revenue projections, electricity grid demand |

---

### 2. Family of Technique

Classifies algorithms according to their statistical and mathematical lineage:

| Family | Core Philosophy & Characteristics |
| :--- | :--- |
| **Statistics** | Grounded in probability theory, parameter estimation, hypothesis testing, and highly interpretable coefficients. |
| **Machine Learning** | Algorithmic optimization, decision boundaries, rule splitting, regularized loss minimization, and ensemble methods. |
| **Deep Learning** | Multi-layer neural networks learning hierarchical latent representations with non-linear activations. |

---

### 3. Named Algorithms

Each algorithm originates from a technique family and maps to one or more predictive question types:

| Algorithm | Technique Family | Solves Question(s) | Description |
| :--- | :--- | :--- | :--- |
| **Linear Regression** | Statistics | Regression | Fits continuous targets through linear combinations of weighted features ($y = \beta_0 + \sum \beta_i x_i$). |
| **Ridge / Lasso / Elastic Net** | Statistics | Regression | Regularized linear regression applying $L_2$ / $L_1$ penalties to prevent overfitting and encourage feature sparsity. |
| **Logistic Regression** | Statistics | Classification | Applies a sigmoid transformation to log-odds; yields calibrated class probabilities and interpretable coefficients. |
| **Naive Bayes** | Statistics | Classification | Fast probabilistic classifier based on Bayes' Theorem under conditional feature independence assumptions. |
| **ARIMA** | Statistics | Time Series Forecasting | Autoregressive Integrated Moving Average; models temporal autocorrelation, differencing, and moving average errors. |
| **Decision Tree** | Machine Learning | Classification & Regression | Recursively partitions feature space using sequential decision rules ($if\text{-}then$ splits). |
| **Random Forest** | Machine Learning | Classification & Regression | Bagged ensemble of decorrelated decision trees; reduces variance and boosts stability. |
| **Gradient Boosting** | Machine Learning | Classification & Regression | Sequential ensemble minimizing pseudo-residuals iteratively; top benchmark for tabular data. |
| **Support Vector Machine (SVM)** | Machine Learning | Classification & Regression | Maximizes geometric margin between classes with kernel transformations (RBF, polynomial). |
| **k-Nearest Neighbours (k-NN)** | Machine Learning | Classification & Regression | Non-parametric, instance-based method that assigns labels based on Euclidean distance in feature space. |
| **Neural Network** | Deep Learning | Classification, Regression, Time Series | Multi-layer perceptron or deep architectures modeling complex non-linear feature interactions. |

---

### 4. Evaluation Metrics

Metrics assess the generalization fidelity of predictions against ground truth:

#### Classification Metrics

| Metric | Mathematical Formula | Purpose & Interpretation |
| :--- | :--- | :--- |
| **Accuracy** | $\frac{TP + TN}{TP + TN + FP + FN}$ | Overall percentage of correct classifications across all classes. |
| **Precision** | $\frac{TP}{TP + FP}$ | Positive Predictive Value: out of all positive predictions, how many were true positives. |
| **Recall (Sensitivity)** | $\frac{TP}{TP + FN}$ | True Positive Rate: proportion of actual positive instances successfully identified. |
| **Specificity** | $\frac{TN}{TN + FP}$ | True Negative Rate: proportion of actual negative instances correctly identified. |
| **NPV** | $\frac{TN}{TN + FN}$ | Negative Predictive Value: when predicting negative, how frequently is the model correct. |
| **F1-Score** | $2 \cdot \frac{\text{Precision} \cdot \text{Recall}}{\text{Precision} + \text{Recall}}$ | Harmonic mean balancing precision and recall, especially in imbalanced distributions. |

#### Continuous (Regression & Forecasting) Metrics

| Metric | Mathematical Formula | Purpose & Interpretation |
| :--- | :--- | :--- |
| **MAE** | $\frac{1}{n}\sum \|y_i - \hat{y}_i\|$ | Mean Absolute Error: average magnitude of residuals in original target units. |
| **MSE** | $\frac{1}{n}\sum (y_i - \hat{y}_i)^2$ | Mean Squared Error: heavily penalizes larger errors through squaring. |
| **RMSE** | $\sqrt{\text{MSE}}$ | Root Mean Squared Error: retains quadratic error penalties while restoring original units. |
| **MAPE** | $\frac{100\%}{n}\sum \left\|\frac{y_i - \hat{y}_i}{y_i}\right\|$ | Mean Absolute Percentage Error: scale-independent relative error percentage. |
| **$R^2$ (R-Squared)** | $1 - \frac{\sum (y_i - \hat{y}_i)^2}{\sum (y_i - \bar{y})^2}$ | Coefficient of determination: proportion of total variance explained by model features. |

---

## Relational Joins & Cross-Links

In addition to hierarchical tree branches, the workbench visualizes three classes of relational cross-links:

1. **Algorithm $\to$ Family Joins** *(Dashed Amber)*:
   - Traces each specific algorithm back to its foundational tradition (`Statistics`, `Machine learning`, or `Deep learning`).
2. **Algorithm $\to$ Question Joins** *(Dashed Sky Blue)*:
   - Indicates which problem types an algorithm is formulated to solve.
   - Highlights multi-purpose models (e.g., **Decision Trees**, **Random Forests**, **Gradient Boosting**, **SVM**, and **k-NN** serve both Classification and Regression; **Neural Networks** serve all three).
3. **Metric $\to$ Question Joins** *(Dashed Emerald Green)*:
   - Connects appropriate evaluation frameworks to question categories (classification metrics to Classification; continuous error metrics to Regression and Time Series Forecasting).

---

## Hand-Drawing Blueprint Strategy

When transcribing this map onto a single sheet of physical paper:

1. **Landscape Orientation**: Position the sheet horizontally to provide sufficient horizontal clearance between left-hand algorithm blocks and right-hand evaluation metrics.
2. **Central Root Anchor**: Write **`PREDICTION`** in a clean central box with generous padding.
3. **Branch Separation**:
   - Radiate **Kind of question** (top-left) and **Family of technique** (bottom-left).
   - Position **Algorithms** spanning the left-to-center field.
   - Position **Metrics** grouped clearly across the right-hand side.
4. **Visual Encoding**:
   - Use **solid lines** for the primary hierarchy (tree backbone).
   - Use **dashed or colored pens** for relational cross-links (e.g., orange for Family joins, blue for Question joins, green for Metric joins) to avoid visual confusion.

---

## Interactive Controls & Usage

| Control | Action | Function |
| :--- | :--- | :--- |
| **Step Buttons (`All View`, `1`–`5`)** | Click | Progressively isolates drawing stages with contextual instruction prompts. |
| **Join Filters (`All`, `Algo→Fam`, etc.)** | Click | Toggles visibility of specific connection categories. |
| **Pan Canvas** | Click + Drag | Moves the viewport across the infinite workspace canvas. |
| **Zoom Canvas** | Mouse Wheel | Zooms in or out centered at cursor position (bounded $600\text{px} - 3000\text{px}$). |
| **Reset Zoom** | Click Button | Restores default camera viewport ($1600 \times 1000$). |
| **Hover Node** | Mouse Enter | Highlights all incident connections while dimming irrelevant canvas elements. |
| **Inspect Node** | Click Node | Opens the sidebar with node description, formulas, and required joins. |
| **Drawing Guide** | Click Button | Toggles the right-hand reference panel and submission checklist. |

---

## Quick Start

No installation, build tools, or web servers are required.

### Direct Browser Launch

Simply double-click or open the HTML file directly in any modern web browser (Chrome, Edge, Firefox, Safari):

```bash
# Windows PowerShell
Start-Process .\predictive_analytics_mind_map_workbench.html

# macOS
open predictive_analytics_mind_map_workbench.html

# Linux
xdg-open predictive_analytics_mind_map_workbench.html
```

### Local Development Server (Optional)

If preferred, serve the workspace via Python, Node.js, or any static file server:

```bash
# Python 3
python -m http.server 8000

# Node.js (npx serve)
npx serve .
```

Then visit `http://localhost:8000/predictive_analytics_mind_map_workbench.html`.

---

## Tech Stack

- **Markup & Layout**: [HTML5](https://developer.mozilla.org/en-US/docs/Web/HTML) with semantic components.
- **Styling**: [Tailwind CSS](https://tailwindcss.com/) (CDN) with customized dark slate palette tokens and responsive utilities.
- **Typography**: [Inter](https://fonts.google.com/specimen/Inter) & [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono).
- **Graphics**: Hardware-accelerated SVG utilizing cubic Bezier curves (`M x1 y1 C ...`), filter drop shadows, and coordinate transformations.
- **Scripting**: Pure Vanilla JavaScript (ES6+), zero external runtime libraries.
