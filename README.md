# GNN vs CNN for Domination Number Prediction

**A Comparative Study of Graph Neural Networks and Convolutional Neural Networks for Predicting NP-Hard Graph Properties**

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://python.org)
[![PyTorch](https://img.shields.io/badge/PyTorch-1.9+-red.svg)](https://pytorch.org)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

## 🎯 **Project Overview**

This repository contains a comprehensive comparison between **Graph Neural Networks (GNNs)** and **Convolutional Neural Networks (CNNs)** for predicting the **domination number** of graphs - an NP-hard combinatorial optimization problem. The study demonstrates that GNNs significantly outperform CNNs in both accuracy and efficiency, achieving **200x speedup** over exact algorithms while maintaining high prediction accuracy.

## 📁 **Repository Structure**

```
├── main_code/                          # 🎯 Main Research Code
│   └── domination number GNN vs CNN.ipynb    # Complete GNN vs CNN comparison
│
├── helper_code/                        # 🔧 Supporting Analysis Code  
│   ├── CNN_Combinatorial_Graph_Properties.ipynb
│   ├── domination number CNN vs graphcalc.ipynb
│   └── domination number GNN vs graphcalc.ipynb
│
├── results/                           # 📊 Results and Visualizations
│   └── images/
│       ├── domination_number_prediction_comparison.png
│       ├── domination_number_prediction_comparison_test_set.png
│       └── stability_number_prediction_comparison.png
│
└── README.md                          # 📖 This file
```

### **Quick Start Guide:**
1. **Start here:** `main_code/domination number GNN vs CNN.ipynb` - Complete analysis
2. **Helper files:** `helper_code/` - Individual model comparisons and validation
3. **Results:** `results/images/` - All visualizations and performance plots

## 🚀 **Key Findings**

| Graph Type | Model | R² Score | MAE | Speedup |
|------------|-------|----------|-----|---------|
| **Erdős-Rényi** | GNN | **0.987** | 0.372 | **208.9×** |
| **Erdős-Rényi** | CNN | 0.955 | 0.500 | 7.4× |
| **Barabasi-Albert** | GNN | **0.981** | 0.395 | **208.9×** |
| **Barabasi-Albert** | CNN | 0.908 | 0.797 | 7.4× |

### **Research Highlights:**
- **GNNs achieve 26% lower MAE** and **47% lower RMSE** compared to CNNs
- **200x speedup** over exact algorithms (GraphCalc) while maintaining 98.7% accuracy
- **Real-world applicability** demonstrated on Barabasi-Albert (scale-free) graphs
- **Robust performance** across different graph topologies and sizes

## 🧠 **Graph Types Studied**

- **Erdős-Rényi (ER) Graphs**: Random graphs with uniform edge probability
- **Barabasi-Albert (BA) Graphs**: Scale-free networks modeling real-world systems
  - Social networks, internet topology, biological systems
  - Addresses reviewer concerns about real-world applicability

## 🔬 **Methodology**

### **Models Compared:**
1. **Graph Isomorphism Network (GIN)**: Graph-native processing with message passing
2. **Convolutional Neural Network (CNN)**: Image-based processing of adjacency matrices

### **Evaluation Metrics:**
- **R² Score**: Coefficient of determination
- **MAE**: Mean Absolute Error  
- **RMSE**: Root Mean Squared Error
- **Runtime**: Computational efficiency
- **Speedup**: Performance gain over exact algorithms

### **Datasets:**
- **Training**: 1,600 graphs (800 ER + 800 BA)
- **Testing**: 400 graphs (200 ER + 200 BA)
- **Graph sizes**: 10-50 nodes
- **Ground truth**: Exact domination numbers computed using GraphCalc

## 📊 **Key Results Summary**

### **Overall Performance:**
- **GNNs dominate** across all metrics and graph types
- **Consistent superiority** on both random and real-world graph topologies
- **Scalable approach** for NP-hard combinatorial problems

### **Real-world Graph Analysis:**
- **Domain-specific training** required for optimal performance
- **Limited cross-domain generalization** (ER→BA: R² = -0.237 for GNNs)
- **GNNs maintain advantage** even on scale-free networks (R² = 0.981 vs 0.908)

### **Computational Efficiency:**
- **GNNs**: 208.9× speedup over exact algorithms
- **CNNs**: 7.4× speedup over exact algorithms
- **Practical deployment** feasible for large-scale graph analysis

## 🛠 **Installation & Usage**

### **Requirements:**
```bash
pip install torch torch-geometric networkx graphcalc matplotlib numpy pandas scikit-learn
```

### **Running the Analysis:**
1. **Main Analysis**: Open `main_code/domination number GNN vs CNN.ipynb`
2. **Helper Analysis**: Explore files in `helper_code/` for specific comparisons
3. **Results**: View visualizations in `results/images/`

## 📈 **Research Significance**

This work demonstrates that **Graph Neural Networks are superior to CNNs** for graph-native tasks, providing:

- **Higher accuracy** on combinatorial optimization problems
- **Better efficiency** with 200x speedup over exact methods
- **Real-world applicability** across diverse graph topologies
- **Scalable solutions** for NP-hard problems

## 🎓 **Academic Context**

- **Conference**: NeurIPS 2025 MATH-AI Workshop
- **Problem**: NP-hard domination number prediction
- **Contribution**: First comprehensive GNN vs CNN comparison for graph invariants
- **Impact**: Enables practical deployment of ML for combinatorial optimization

## 🔮 **Future Work**

- Extension to other NP-hard graph properties (chromatic number, independence number)
- Investigation of different GNN architectures (GraphSAGE, GAT, Graph Transformer)
- Analysis of generalization across graph families
- Real-world deployment on large-scale networks

## 📄 **Citation**

```bibtex
@article{gnn_vs_cnn_domination,
  title={Graph Neural Networks vs Convolutional Neural Networks for Domination Number Prediction},
  author={Ispir, Beyza},
  journal={NeurIPS 2025 MATH-AI Workshop},
  year={2025}
}
```

## 📞 **Contact**

- **Author**: Beyza Ispir
- **Repository**: [https://github.com/beyzaispiir/CNN-vs-GNN-domination-number](https://github.com/beyzaispiir/CNN-vs-GNN-domination-number)
- **Paper**: NeurIPS 2025 MATH-AI Workshop Submission

---

*This research demonstrates the power of graph-native neural architectures for solving combinatorial optimization problems at scale.*