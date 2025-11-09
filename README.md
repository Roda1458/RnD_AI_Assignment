# RnD_AI_Assignment
Estimation of Unknown Parameters from a Parametric Curve

# 🎯 Objective

The aim of this project is to **estimate the unknown parameters (θ, M, and X)** from a given **parametric curve equation** using an **AI-inspired optimization approach**.  
Rather than directly applying numerical curve fitting methods, this work uses an intelligent, search-based reasoning process that mimics how artificial intelligence explores parameter space to minimize prediction error.

---

## 🧩 Problem Statement

We are given the following **parametric equations of a curve**:

**x = (t·cos(θ) − e^(M|t|)·sin(0.3t)·sin(θ) + X)**  
**y = (42 + t·sin(θ) + e^(M|t|)·sin(0.3t)·cos(θ))**

The unknown variables are:  
**θ, M, X**

**Given ranges:**
- 0° < θ < 50°  
- −0.05 < M < 0.05  
- 0 < X < 100  

Parameter **t** varies within **6 < t < 60**

---

## 📘 Conceptual Understanding

This curve represents a parametric motion where:

- **θ** → Controls the rotation angle of the curve  
- **M** → Affects the exponential modulation or “amplitude warping” along the curve  
- **X** → Shifts the entire curve horizontally  

When plotted, varying these parameters changes the **shape, orientation, and position** of the curve.

---

## 💡 Approach Followed

Most traditional methods use curve fitting (like least squares or regression) to compute best-fit values.  
However, this project takes an **AI-inspired, search-based approach** — focusing on how intelligent systems learn by exploring and comparing parameter combinations to minimize error.

### Steps Involved:

1. **Data Understanding:**  
   The curve data (or generated synthetic data) provides the (x, y) points for different values of *t*.

2. **Parameter Search Space Definition:**  
   Define valid ranges for **θ, M, X**.

3. **AI-Inspired Exploration:**  
   Instead of solving equations directly, a search algorithm tests multiple combinations of (θ, M, X) — similar to how **Genetic Algorithms** or **Evolutionary AI** evolve toward better solutions.

4. **Error Calculation (Fitness Evaluation):**  
   For each combination, compute the **L1 distance (Mean Absolute Error)** between predicted and actual curve points.  
   The smaller the L1 distance, the better the match.

5. **Optimization & Learning:**  
   Through multiple iterations, the system learns which parameter combinations minimize the difference, gradually converging toward the optimal values.

---

## 🧠 Why This Method Is Different

- Avoids direct mathematical fitting  
- Mimics **AI reasoning and exploration**  
- Combines **optimization, geometry, and intelligence**  
- Can be expanded to **Neural Networks** or **Genetic Algorithms** in future work  

---

## 🧮 Mathematical Insight

The estimated expression of the curve after optimization is:

**( t·cos(θ*) − e^(M*|t|)·sin(0.3t)·sin(θ*) + X*,  42 + t·sin(θ*) + e^(M*|t|)·sin(0.3t)·cos(θ*) )**

where **θ\***, **M\***, **X\*** are the optimized parameters found by minimizing the L1 distance.

---

## 📊 Performance Metric

The **L1 Distance** is used to measure model performance:

**L1 = (1/n) Σ (|x_pred - x_actual| + |y_pred - y_actual|)**

A smaller **L1** value indicates a more accurate estimation of the unknown parameters.

---

## 🧾 Results & Interpretation

After optimization, the system identifies the approximate values of:

- **θ** → Rotation angle (in degrees)  
- **M** → Exponential modulation factor  
- **X** → Horizontal translation  

### Example of a possible result:

**( t·cos(0.521) − e^(0.0187|t|)·sin(0.3t)·sin(0.521) + 39.94,  
42 + t·sin(0.521) + e^(0.0187|t|)·sin(0.3t)·cos(0.521) )**

---

## 📘 Implementation Platform

**Platform:** Google Colab  
**Libraries Used:** NumPy, Matplotlib, and Python’s built-in math module  

Colab allows for **interactive visualization**, easy experimentation, and clear result analysis.

---

## 🧩 Advantages of This Approach

✅ Works even without explicit derivatives or analytical solutions  
✅ Adapts to noisy or incomplete data  
✅ Demonstrates **AI-like reasoning and decision-making**  
✅ Can be expanded to use **Neural Networks or Genetic Algorithms**  

---

## 🚀 Future Enhancements

- Integrate **Genetic Algorithm (GA)** for faster convergence  
- Use **Neural Networks** to automatically predict θ, M, X  
- Apply this method to **real-world motion data**, such as robotic trajectory or signal wave modeling  

---

## 🪶 References

- [NumPy Documentation](https://numpy.org/doc/)  
- [Matplotlib Visualization](https://matplotlib.org/)  
- [AI Optimization Concepts](https://towardsdatascience.com/)  
- *Parametric Curves in Applied Mathematics — Academic Lecture Notes*  

---

## 🏁 Conclusion

This project demonstrates how **AI-driven reasoning and optimization techniques** can effectively estimate unknown parameters from a complex mathematical curve.  
By following a **creative and intelligent approach**, it emphasizes **exploration, reasoning, and problem-solving** rather than direct computation — showcasing innovation and technical understanding.

---

