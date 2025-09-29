project:
  name: "Advanced Persistent Threat (APT) Detection with Graph Neural Networks"
  description: >
    Jupyter Notebook implementation of APT detection using Graph Neural Networks (GNNs),
    specifically a lightweight Graph Attention Network (GAT). The notebook demonstrates
    preprocessing, graph construction, model training, evaluation, explainability,
    and visualization.

features:
  - Data preprocessing and graph construction from PCA-transformed input
  - Lightweight GAT model for classifying attack patterns
  - Training, validation, and testing with performance tracking
  - Metrics: accuracy, confusion matrix, classification report
  - Graph-level and feature-level explainability
  - Subgraph visualization with edge importance
  - Model saving and loading with metadata

repository_contents:
  - apt_gnn_detection.ipynb: "Main Jupyter Notebook"
  - README.md: "Project documentation"

setup:
  clone:
    - command: git clone https://github.com/your-username/apt-gnn-detection.git
    - command: cd apt-gnn-detection

  environment:
    recommended: "Use a Python virtual environment"
    linux_mac: "python -m venv venv && source venv/bin/activate"
    windows: "python -m venv venv && venv\\Scripts\\activate"

  installation:
    pip:
      - torch
      - torchvision
      - torchaudio
      - torch-geometric
      - scikit-learn
      - pandas
      - numpy
      - matplotlib
      - seaborn
      - networkx
      - jupyter

  run_notebook:
    - command: jupyter notebook apt_gnn_detection.ipynb

example_results:
  dataset: "~3000 nodes, ~15k edges"
  model: "Lightweight GAT (~200k parameters)"
  test_accuracy: "~0.93 (depends on dataset)"
  outputs:
    - Graph structure visualizations
    - Degree distribution plots
    - Training/validation loss and accuracy curves
    - Confusion matrices (raw and normalized)
    - Feature importance heatmaps
    - Subgraph explanations with edge importance

requirements:
  python: ">=3.8"
  libraries:
    - torch
    - torch-geometric
    - scikit-learn
    - pandas
    - numpy
    - matplotlib
    - seaborn
    - networkx
    - jupyter

license:
  type: "MIT"
  year: 2025
  author: "Your Name"
