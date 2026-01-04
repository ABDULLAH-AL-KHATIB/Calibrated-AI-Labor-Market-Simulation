Calibrated AI-Labor Market Simulation Model
  
This repository contains the Python source code for the paper "The Heterogeneous Effects of Artificial Intelligence on Labour Markets: A Calibrated Simulation of Skills, Tasks, and Wages."
This project implements a computational framework for analyzing the heterogeneous effects of Artificial Intelligence on labor markets through a task-based approach. It extends traditional models by incorporating a two-dimensional task space (Cognitive Complexity vs. Codifiability) with a dynamic AI capability frontier.
📋 Table of Contents
	Key Features
	Theoretical Framework
	Installation
	Usage
	Repository Structure
	Citation
	License
✨ Key Features
	Empirical Calibration: Automatically calibrates core parameters (elasticity of substitution \sigma, AI frontier \theta) to match stylized facts, such as a high-skill wage premium of 1.75.
	Dynamic Task Space: Simulates an economy with 2,000 discrete tasks defined by cognitive complexity and codifiability.
	AI Capability Frontier: Models the exogenous expansion of AI capabilities over 30 periods.
	Policy Analysis Engine: Simulates the impact of interventions, including:
	Training Subsidies (Human Capital accumulation)
	AI Taxes (Pace of technological adoption)
	Labor Supply Shocks
	Visualization Suite: Generates publication-quality plots for trajectories, sensitivity analysis, and task space evolution.
🧮 Theoretical Framework
The model is built on a nested Constant Elasticity of Substitution (CES) production function.
Y=\left[\alpha T_A^{\frac{\sigma-1}{\sigma}}+\left(1-\alpha\right)T_H^{\frac{\sigma-1}{\sigma}}\right]^\frac{\sigma}{\sigma-1}
Tasks are allocated based on comparative advantage. The AI capability frontier is defined by 
c\le\theta\left(t\right)k, determining which tasks are automatable at time t.
🛠️ Installation
Prerequisites
	Python 3.8 or higher
	pip package manager
Dependencies
Clone the repository and install the required packages:
bash
git clone https://github.com/ABDULLAH-AL-KHATIB/Calibrated-AI-Labor-Market-Simulation-Model.git 
cd Calibrated-AI-Labor-Market-Simulation-Model
pip install -r requirements.txt
requirements.txt
text
numpy
pandas
matplotlib
seaborn
scipy
scikit-learn
🚀 Usage
To run the full simulation pipeline (including calibration, baseline scenarios, policy analysis, and visualization):
bash
python ai_labor_model.py
Custom Simulation
You can also import the CalibratedAILaborModel class into your own scripts for custom analysis:
python
from ai_labor_model import CalibratedAILaborModel, ModelVisualizer

# 1. Initialize and Calibrate Model
model = CalibratedAILaborModel(n_tasks=2000)

# 2. Run Baseline Simulations
baseline_results = model.run_dynamic_simulation(T_periods=30)

# 3. Visualize Results
visualizer = ModelVisualizer(model)
visualizer.plot_dynamic_trajectories(baseline_results)

# 4. Run Policy Analysis (e.g., AI Tax)
policy_comparison = model.policy_analysis(baseline_results, policy_type='ai_tax')
📂 Repository Structure
.
├── ai_labor_model.py       # Core simulation code & visualization logic
├── README.md                # This file
├── requirements.txt          # List of Python dependencies
└── figures/                 # Output directory (optional, created during run)
📊 Outputs
Upon running the script, the model generates the following visualizations:
	Calibration Validation: Task space distribution and parameter sensitivity.
	Dynamic Trajectories: Evolution of Output, Wages, Wage Ratio, and Automation Share over time.
	Sensitivity Analysis: Final Wage Inequality vs. Elasticity of Substitution (σ).
	Task Space Evolution: Visual representation of the AI frontier expanding over time.
	Policy Analysis: Comparative charts showing the impact of "AI Tax", "Training Subsidy", and "Labor Supply Shock".
📝 Citation
If you use this code or the associated paper for your research, please cite it as follows:
bibtex
@article{Al khatib2026ai,
  title={The Heterogeneous Effects of Artificial Intelligence on Labour Markets: A Calibrated Simulation of Skills, Tasks, and Wages},
  author={Al Khatib, Abdullah Mohammad Ghazi},
  journal={ }, 
  year={2026},
  doi={}
}
📜 License
This project is licensed under the MIT License - see the LICENSE file for details.
📧 Contact
Abdullah Mohammad Ghazi Al Khatib
genius.275@hotmail.com 
________________________________________
Note: The model is calibrated using stylized facts derived from publicly available literature. No new proprietary data was generated for this research.

