# Hidden Markov Model — Baum–Welch Algorithm Visualization

## 👩‍🎓 Name: Pavithra S  
## 🆔 University Registration Number: TCR24CS055

---

## 📌 Project Description

This project implements a **Hidden Markov Model (HMM)** using the **Baum–Welch Algorithm**, which is an Expectation–Maximization (EM) method used to estimate model parameters from observation sequences.

The project includes a fully interactive **Streamlit web application** that allows users to:

- Input an observation sequence
- Train the HMM using Baum–Welch
- Visualize parameter updates
- Observe convergence behavior
- View transition probability evolution
- Display a dynamic state transition diagram

---

## 🧠 Model Details

### Hidden States:
- S0 (Rainy)
- S1 (Sunny)

### Observations:
- 0 → Walk
- 1 → Shop

### Model Parameters:
- Transition Matrix (A)
- Emission Matrix (B)
- Initial State Probabilities (π)

The HMM is defined as:

λ = (A, B, π)

---

## ⚙️ Algorithm Used

### Baum–Welch Algorithm (Expectation–Maximization)

The algorithm iteratively updates the HMM parameters using:

1. **Forward Algorithm**  
   Computes α (forward probabilities)

2. **Backward Algorithm**  
   Computes β (backward probabilities)

3. **Compute γ (gamma)**  
   State responsibility:
   γₜ(i) = P(qₜ = i | O, λ)

4. **Compute ξ (xi)**  
   Transition responsibility:
   ξₜ(i,j) = P(qₜ = i, qₜ₊₁ = j | O, λ)

5. **Update Parameters**
   - π ← γ₁
   - A ← normalized expected transitions
   - B ← normalized expected emissions

6. **Repeat Until Convergence**

The log-likelihood increases at every iteration until convergence.

---

## 📊 Visualizations Included

The application displays:

- ✅ Log-Likelihood Convergence  
- ✅ Negative Log-Likelihood (Optimization Loss)  
- ✅ Observation Probability P(O | λ)  
- ✅ Probability Complement  
- ✅ Parameter Evolution of Transition Matrix A[i][j]  
- ✅ State Transition Diagram  

These visualizations demonstrate how parameters stabilize over iterations.

---

## 🚀 How to Run the Project

### 1️⃣ Clone the Repository
