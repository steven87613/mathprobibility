## 🎲 Pragmatic Play – The Bingo Spot: Math Model & Simulation

### 📝 Project Overview
This project presents an independent mathematical analysis and simulation study of Pragmatic Play’s live game show, **The Bingo Spot**. The objective is to evaluate the structural payout mechanics by combining theoretical probability modeling with large-scale Monte Carlo simulations to validate payout convergence and volatility characteristics.

**Key Objectives:**
* Model the structural payout mechanics.
* Estimate Base RTP (Return to Player).
* Analyze hit frequency distribution.
* Evaluate volatility behavior under multiplier compounding.
* Measure the mathematical impact of the Wild Ball extra draw feature.

### 🧮 Game Mechanics Analyzed

* **1. Base Bingo Structure:** Simulates standard bingo-style ball drawing logic with a fixed base draw count. Incorporates line completion detection (horizontal & vertical) up to a maximum 6-line configuration.
* **2. Wild Ball (Extra Draw Feature):** The Wild acts purely as a trigger (not present on player cards). When drawn, weighted additional balls are awarded, increasing effective hit frequency, shifting mid-tier payout probabilities, and raising the average draw count per round.
* **3. Lucky Numbers & Dynamic Multipliers:** 5 Lucky Numbers are selected independently each round with a weighted multiplier distribution (e.g., 2x, 3x, 5x). Multipliers apply only if the Lucky Number contributes to a completed line.
* **4. Multiplier Compounding:** When multiple multipliers are hit within the same round, they compound multiplicatively. This drives extreme outcome probabilities and significantly increases the overall Volatility Index (VI).

### 📐 Mathematical Evaluation Scope
The simulation and theoretical models strictly measure:
* **RTP & Hit Rate**
* **Line Frequency Distribution** (0–6 lines) & Multi-line frequency (2+ lines)
* **Full Board Probability**
* **Standard Deviation & Coefficient of Variation (CV)**
* **Return distribution** across payout ranges, with a special focus on volatility amplification via multiplier stacking.

### 🛠️ Technical Implementation

**1️⃣ Theoretical Probability Model (Excel)**
* **File:** `pragmatic play bingo spot.xlsx`
* **Features:** Combinatorial line completion modeling, Multiplier Expected Value (EV) estimation, structural RTP framework, and contribution analysis per payout tier.

**2️⃣ Monte Carlo Simulation (Python + Numba)**
* **File:** `pragmatic play bingo spot simulate.ipynb`
* **Features:** High-volume simulation (10M+ rounds tested), **parallelized using Numba JIT** for extreme performance. Validates empirical RTP convergence and measures volatility through distribution analysis.

### 📈 Key Observations
* **Volatility Profile:** Medium-to-high volatility.
* **Extreme Payout Driver:** Multiplier compounding is the primary engine for extreme payouts.
* **Wild Feature Impact:** Meaningfully increases mid-frequency hit probability and shifts the RTP distribution.

### 🧠 Skills Demonstrated
`Probability Modeling` | `Combinatorics` | `Monte Carlo Simulation` | `Volatility Analysis` | `Performance Optimization (Numba JIT)` | `Game Math Structural Analysis`

> **⚠ Disclaimer:** This project is an independent mathematical research and modeling exercise based on publicly observable mechanics and statistical inference. It does not reproduce or represent any proprietary source code or internal systems of Pragmatic Play. All results are statistical estimations derived from modeling assumptions.
