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
- Display a state transition diagram

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

## Media

<img width="907" height="820" alt="image" src="https://github.com/user-attachments/assets/396862ee-8081-4dcc-a634-56664aca272a" />
<img width="978" height="752" alt="image" src="https://github.com/user-attachments/assets/4ccfa395-61b8-4082-a99b-3f0d1bbb844e" />
<img width="962" height="651" alt="image" src="https://github.com/user-attachments/assets/0c316f65-7c54-4cff-b39a-c15ada7a9d96" />
<img width="948" height="582" alt="image" src="https://github.com/user-attachments/assets/fb524725-8175-49f3-9ca9-812782081ae9" />
<img width="957" height="686" alt="image" src="https://github.com/user-attachments/assets/3091925e-e8de-4961-8aaa-bef483b35841" />

---

## 🚀 How to Run the Project

Clone the Repository:
git clone https://github.com/Pavithra-S-hub/HMM-BaumWelch-Visualization.git 

cd HMM-BaumWelch-Visualization  

pip install -r requirements.txt  

python -m streamlit run app.py  

The Streamlit application will open automatically in your browser.

---

## 📂 Project Structure

HMM-BaumWelch-Visualization/  
│  
├── app.py  
├── hmm_baum_welch.py  
├── requirements.txt  
└── README.md  

---

## 🎯 Objective

The objective of this project is to:

- Understand Hidden Markov Models
- Implement the Baum–Welch Algorithm from scratch
- Visualize parameter convergence
- Analyze transition probability evolution
- Build an interactive AI-based visualization tool

---

## 📚 References

- Rabiner, L. R. (1989). “A Tutorial on Hidden Markov Models”
- Hidden Markov Model Theory
- Baum–Welch Algorithm (EM Method)

---

## ✅ Conclusion

This project successfully demonstrates how Hidden Markov Model parameters can be learned from observation data using the Baum–Welch algorithm.  



