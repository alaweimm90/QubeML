# QubeML

Educational notebooks for quantum computing and materials informatics. Six tool modules: Qiskit/Cirq/PennyLane for quantum algorithms, PyTorch/sklearn/Kwant for materials modeling.

[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)
[![MIT License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

## Overview

Hands-on tutorials covering quantum algorithms for chemistry (VQE, quantum circuits) and ML for materials science (graph neural networks, property prediction). Built for grad students and researchers.

## Modules

**Quantum Computing**
- Qiskit: VQE for H2, HeH+ molecules
- Cirq: Custom gates, noise simulation
- PennyLane: Quantum kernels, variational classifiers

**Materials Informatics**
- PyTorch: Crystal graph convolution networks
- Scikit-learn: PCA on materials datasets, property regression
- Kwant: 2D material transport, spin-orbit coupling

## Topics Covered

| Module | Key Implementations |
|--------|-----------------------|
| Qiskit | VQE ground states, ansatz comparison, basis set effects |
| PyTorch | CGCNN for band gaps, descriptor engineering |
| Scikit-learn | Materials Project queries, feature importance |
| Kwant | Graphene ribbons, MoS2 transistors |
| Cirq | Error mitigation, qubit calibration |
| PennyLane | Quantum embeddings, kernel methods |

## Structure

```
quantum_computing/
  qiskit/          # VQE tutorials, molecule examples
  cirq/            # Gate decomposition, error models  
  pennylane/       # Quantum ML demos
materials_informatics/
  pytorch/         # GNN implementations
  scikit_learn/    # Classical ML pipelines
  kwant/           # Transport simulations
src/               # Utilities (descriptors, plotting)
tests/             # Unit tests
```

## Setup

```bash
git clone https://github.com/meshalawein/QubeML.git
cd QubeML
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
```

**Google Colab**: Notebooks work in Colab's free tier. Upload and run.

## Notebooks

**Quantum Chemistry** (`quantum_computing/qiskit/`):
- Build H2 molecule, run VQE with UCCSD ansatz
- Compare to exact diagonalization
- Basis set convergence study

**Graph Neural Networks** (`materials_informatics/pytorch/`):
- Load crystal structures from CIF
- Build graph representation 
- Train CGCNN on Materials Project data

**Transport** (`materials_informatics/kwant/`):
- Graphene nanoribbon conductance
- MoS2 field-effect transistor
- Strain effects on band structure

**ML Pipelines** (`materials_informatics/scikit_learn/`):
- Query MP API for oxide band gaps
- Feature engineering from composition
- Random forest vs gradient boosting comparison

## Applications

These notebooks connect to active research areas:
- Quantum advantage for strongly correlated molecules
- ML-accelerated materials screening
- Topological phases in 2D materials
- Interpretable models for experimental validation

## Testing

```bash
python -m pytest tests/ -v
python tests/test_quantum_utils.py::TestQuantumUtils::test_bell_states
```

## Contributing

Contributions welcome. See open issues or add examples/fixes via PR.

## References

- Qiskit Textbook: https://qiskit.org/textbook/
- Materials Project: https://materialsproject.org/
- CGCNN paper: Xie & Grossman, Phys. Rev. Lett. 120, 145301 (2018)

## License

MIT License. See [LICENSE](LICENSE).

## Author

Dr. Meshal Alawein  
UC Berkeley  
meshal@berkeley.edu
