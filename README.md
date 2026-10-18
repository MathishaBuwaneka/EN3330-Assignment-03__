# EN3330 — Assignment 03: Engineering Optimization

Python implementations and visualizations for **Assignment 03** of **EN3330 — Introduction to Engineering Optimization**, Department of Electronic and Telecommunication Engineering, University of Moratuwa.

The repository contains **three Jupyter notebooks**, one for each question. Each notebook includes the necessary mathematical background, Python calculations, plots, and short interpretations of the results.

## Repository structure

```text
EN3330-Assignment-03/
├── Q_1_Lagrangian_Duality.ipynb
├── Q_2_Saddle_Point.ipynb
├── Q_3_Weak_Duality.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

## Contents

| Notebook | Topics covered | Visualizations |
| --- | --- | --- |
| [Question 1 — Lagrangian Duality](Q_1_Lagrangian_Duality.ipynb) | Lagrangian minimizers, dual function, optimal multiplier, primal function, and duality gap | Lagrangian curves for four multipliers; dual-function curve; primal-function plot |
| [Question 2 — Saddle Point](Q_2_Saddle_Point.ipynb) | Saddle-point inequalities, primal optimality, complementary slackness, and a modified constraint | Two plots verifying the saddle-point inequalities |
| [Question 3 — Weak Duality](Q_3_Weak_Duality.ipynb) | Proof and numerical check of weak duality, lower envelope, and concavity of the dual function | Three Lagrangian lines and their lower envelope, compared with the exact dual |

## Problem setup

Questions 1 and 2 use the constrained minimization problem

$$
\min_x x^2 \quad \text{subject to } x\geq 1.
$$

With $h(x)=1-x\leq0$, the Lagrangian is

$$
L(\mu,x)=x^2+\mu(1-x),\qquad \mu\geq0.
$$

The main analytical results are

$$
x(\mu)=\frac{\mu}{2},\qquad
 d(\mu)=\mu-\frac{\mu^2}{4},
$$

$$
x^*=1,\qquad \mu^*=2,\qquad p^*=d^*=1.
$$

Question 3 develops the general weak-duality argument and illustrates the concavity of the dual function using the same Lagrangian.

## Requirements

- Python 3.9 or newer
- NumPy
- Matplotlib
- Jupyter Notebook

Install the packages listed in [`requirements.txt`](requirements.txt):

```bash
python -m pip install -r requirements.txt
```

## How to run

**Option 1 — Locally (Jupyter Notebook)**

1. Clone or download this repository.
2. Open a terminal in the repository folder.
3. Install the dependencies with the command above.
4. Start Jupyter:

   ```bash
   jupyter notebook
   ```

5. Open any of the three `.ipynb` files and select **Run All** to reproduce the results and figures.

**Option 2 — Google Colab**

Upload a notebook to [Google Colab](https://colab.research.google.com/) and run the cells. The notebooks can be run independently.

## Notes on the plots

- In **Q1(c)**, the exact primal function is $+\infty$ for $x<1$. The plot identifies this region rather than assigning an artificial finite value to infinity.
- In **Q3(b)**, the lower envelope of the three selected lines is an **upper approximation** of the exact dual function, since it minimizes over only $x\in\{0,1,2\}$ instead of all real $x$.
- The code generates the figures from the equations; it does not require a numerical optimization solver.

## Submission note

These notebooks provide reproducible computational support for a separately prepared written assignment. If referring to the generated plots in a submitted report, include a link to this source-code repository as required by the assignment instructions.
