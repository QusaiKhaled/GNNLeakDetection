Explainable Fuzzy GNNs for Leak Detection in Water Distribution Networks
This repository contains the implementation of an explainable fuzzy graph neural network (FGNN) framework designed for detecting and localizing leaks in water distribution networks (WDNs). By integrating graph neural networks (GNNs) with fuzzy logic, the framework delivers both accurate predictions and interpretable, rule-based explanations. It was developed using the Hanoi Benchmark Network dataset (LeakDB) and serves as the official codebase for the paper "Explainable Fuzzy GNNs for Leak Detection in Water Distribution Networks" by Qusai Khaled et al., submitted to the 2025 IFSA World Congress NAFIPS.
Overview
The project explores various GNN architectures and introduces a fuzzy-enhanced model, combining mutual information and fuzzy logic to enhance explainability. It focuses on two primary tasks:
Leak Detection: Graph-level classification to identify the presence of leaks.

Leak Localization: Node-level classification to pinpoint leak locations.

The fuzzy approach generates human-readable explanations, such as "IF Pressure at Node 1 is high AND Pressure at Node 2 is low, THEN Leak probability at Node 5 is high," making it valuable for domain experts.
Repository Structure
The repository is organized as follows:
Notebooks:
01_Reshape_data.ipynb, 01_Reshape_oldata.ipynb: Data preparation and preprocessing.

05_GCN.ipynb, 06_GAT.ipynb: Experiments with specific GNN architectures (e.g., GCN, GAT).

11_AnomalyDetectionScenario.ipynb: Anomaly detection use case.

12_FeatureExtraction.ipynb: Feature extraction processes.

Explain.ipynb: Generation of fuzzy rule-based explanations.

Python Scripts:
data.py, preprocess.py: Utilities for data loading and preprocessing.

model.py: GNN model definitions, including the fuzzy variant.

train.py, test.py: Scripts for training and evaluating models.

grid.py, Grid search py: Tools for hyperparameter tuning.

loss.py, tracker.py, logger.py: Helpers for loss calculation, performance tracking, and logging.

Other:
.gitignore: Specifies files to exclude from version control.

Setup
To get started:
Clone the repository:
bash

git clone https://github.com/yourusername/GNNLeakDetection.git
cd GNNLeakDetection

Install dependencies:
Use Python 3.8+ and install necessary packages (e.g., PyTorch Geometric) as needed. A requirements.txt file is assumed—create one if it’s not present.

Dataset:
Obtain the Hanoi Benchmark Network dataset (LeakDB) from its source and place it in a suitable directory (e.g., data/). Run the preprocessing notebooks to prepare the data.

Usage
Training and Testing:
Use train.py and test.py to train and evaluate models. Adjust configurations as needed via arguments or files.

Experiments:
Explore GNN implementations in notebooks like 05_GCN.ipynb and 06_GAT.ipynb. Use Explain.ipynb to see fuzzy explanations in action.

Hyperparameter Tuning:
Leverage grid.py or Grid search py to optimize model parameters.

Results
The framework’s performance is detailed in the paper, with the fuzzy-enhanced model providing competitive accuracy and explainability. Results are typically saved in a results/ directory.
Citation
If you use this code, please cite:
bibtex

@article{khaled2025explainable,
  title={Explainable Fuzzy GNNs for Leak Detection in Water Distribution Networks},
  author={Khaled, Qusai and De Marinis, Pasquale and Louati, Moez and Ferras, David and Genga, Laura and Kaymak, Uzay},
  journal={2025 IFSA World Congress NAFIPS},
  year={2025}
}

Acknowledgments
This work is supported by the ILUSTRE project, funded in part by the Dutch Research Council (NWO).
Contact
For inquiries, please open an issue on this repository.

