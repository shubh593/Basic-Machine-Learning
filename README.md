# Jupyter Learning Lab: Python, Machine Learning & Quantum Computing

A structured, clean, and comprehensive repository containing curated learning tracks for **Python Core Programming**, **Data Analysis & Machine Learning**, and **Quantum Computing with Qiskit**.

---

## Table of Contents

- [Project Overview](#project-overview)
- [Repository Structure](#repository-structure)
- [File Mapping & Renaming Log](#file-mapping--renaming-log)
- [Learning Tracks & Notebook Guides](#learning-tracks--notebook-guides)
  - [Track 1: Python & Machine Learning](#track-1-python--machine-learning)
  - [Track 2: Quantum Computing (Qiskit)](#track-2-quantum-computing-qiskit)
- [Summary of Code Fixes & Completions](#summary-of-code-fixes--completions)
- [Data Assets](#data-assets)
- [Setup & Installation](#setup--installation)
- [How to Run](#how-to-run)

---

## Project Overview

This repository organizes previously scattered notebooks and datasets into two distinct, sequential learning tracks:
1. **Python & Machine Learning Track**: Starts from fundamental syntax, data structures, and hackathon basics, progresses through data manipulation and visualization with Pandas and Matplotlib, and concludes with an introduction to Machine Learning and predictive modeling.
2. **Quantum Computing Track (Qiskit Fall Fest)**: Guides learners through quantum circuit construction, quantum entanglement, Bell states, the CHSH inequality, quantum noise simulation, arithmetic circuits (quantum half-adder), local backend simulators, and Grover's search algorithm.

---

## Repository Structure

```
jupyter/
├── data/
│   └── data_collection.csv                       # Cleaned dataset: 75 vehicle sighting observations
├── notebooks/
│   ├── python_and_ml/
│   │   ├── 01_python_basics_hackathon.ipynb     # Python basics, data types, and functions
│   │   ├── 02_python_core_fundamentals.ipynb    # Slicing, operators, dictionary methods
│   │   ├── 03_data_analysis_pandas.ipynb        # Pandas DataFrames and data cleaning
│   │   ├── 04_data_visualization.ipynb          # Matplotlib charts on traffic observation data
│   │   └── 05_intro_to_machine_learning.ipynb   # ML lifecycle, paradigms & Linear Regression model
│   └── quantum_computing/
│       ├── 01_first_steps_quantum_circuits.ipynb   # Qiskit Fall Fest Notebook A: Circuits & Bell state
│       ├── 02_chsh_inequality.ipynb                # Qiskit Fall Fest Notebook B: CHSH test & Estimator
│       ├── 03_quantum_workshop_noise_and_adder.ipynb # Workshop 1: Barrier, noise models & half adder
│       ├── 04_half_adder_and_noise_models.ipynb    # Unitary gates, Pauli/Kraus noise & resilience
│       ├── 05_quantum_simulation_methods.ipynb     # AerSimulator & FakeManilaV2 local simulations
│       └── 06_grover_oracle_basics.ipynb           # Grover search oracle & Bloch multivector plot
├── src/
│   └── jupyter/
│       └── __init__.py                           # Source package entry point
├── .gitignore                                    # Git ignore rules including .ipynb_checkpoints
├── .python-version                               # Python environment configuration
├── pyproject.toml                                # Project metadata and dependencies
└── README.md                                     # Main repository documentation
```

---

## File Mapping & Renaming Log

All files with ambiguous, unstructured, or misspelled names have been renamed and organized in chronological and logical sequence:

| Original Name | New Path | Reason & Changes Applied |
| :--- | :--- | :--- |
| `data collection.csv` | `data/data_collection.csv` | Moved to dedicated `data/` folder; removed whitespace from filename for clean programmatic importing. |
| `practicehackathon.ipynb` | `notebooks/python_and_ml/01_python_basics_hackathon.ipynb` | Renamed with sequence prefix; fixed syntax errors (`10i + 4j`, function header, interactive shell prompts); removed empty cells. |
| `learn.ipynb` | `notebooks/python_and_ml/02_python_core_fundamentals.ipynb` | Renamed with sequence prefix; added markdown guide headers; removed trailing empty cells. |
| `machinelearning.ipynb` | `notebooks/python_and_ml/03_data_analysis_pandas.ipynb` | Renamed to reflect true content (Pandas data manipulation); fixed dict syntax error (`"guru"` missing value) and `df["START*"]` KeyError; updated CSV path. |
| `Data_Visualization.ipynb` | `notebooks/python_and_ml/04_data_visualization.ipynb` | Previously completely empty; completed with concise, production-ready Matplotlib & Pandas visualizations using `data_collection.csv`. |
| `intro_to_ML.ipynb` | `notebooks/python_and_ml/05_intro_to_machine_learning.ipynb` | Previously comment-only notes; completed with detailed ML lifecycle breakdown, paradigm taxonomy, and a minimal working Scikit-Learn Linear Regression model. |
| `Notebook_2.ipynb` | `notebooks/quantum_computing/01_first_steps_quantum_circuits.ipynb` | Renamed to describe Qiskit Fall Fest Notebook A; completed Exercise 1 (gate stacking) and Exercise 2 (Bell state creation); removed trailing empty cell. |
| `notebook_3.ipynb` | `notebooks/quantum_computing/02_chsh_inequality.ipynb` | Renamed to describe Qiskit Fall Fest Notebook B (CHSH Inequality); provided local `StatevectorEstimator` alternative alongside hardware Estimator. |
| `Workshop_1.ipynb` | `notebooks/quantum_computing/03_quantum_workshop_noise_and_adder.ipynb` | Renamed with sequence prefix; completed imports, implemented circuit barrier exercise, and updated half-adder execution for Qiskit 1.x `StatevectorSampler`. |
| `half_adder_Erros.ipynb` | `notebooks/quantum_computing/04_half_adder_and_noise_models.ipynb` | Fixed filename typo (`Erros` -> `errors`); fixed `IndexError` in measurement cell (`QuantumCircuit(2, 2)`); removed redundant empty cells. |
| `Simulation_Method.ipynb` | `notebooks/quantum_computing/05_quantum_simulation_methods.ipynb` | Renamed with sequence prefix; removed mandatory online IBM token check so `FakeManilaV2` runs offline; completed superposition circuit with `AerSimulator`. |
| `Untitled1.ipynb` | `notebooks/quantum_computing/06_grover_oracle_basics.ipynb` | Renamed from default notebook title; fixed Python literal comparison warning; replaced invalid circuit call with `Statevector` Bloch multivector visualization. |

---

## Learning Tracks & Notebook Guides

### Track 1: Python & Machine Learning

#### `01_python_basics_hackathon.ipynb`
- **Focus**: Introduction to Python syntax, basic variables, and types.
- **Topics**: Integers, floats, complex numbers (`10 + 4j`), booleans, string sequencing, multiline strings, lists, tuples, sets, dictionaries, arithmetic operators, and custom functions with default arguments.

#### `02_python_core_fundamentals.ipynb`
- **Focus**: Core language mechanics and data manipulation.
- **Topics**: Type inspections, boolean truthiness evaluation, string slicing and concatenation, `range()` generators, list deletion and concatenation, membership testing (`in`), identity testing (`is`), and dictionary methods (`items()`, `keys()`, `values()`, `update()`, `clear()`).

#### `03_data_analysis_pandas.ipynb`
- **Focus**: Data loading and exploratory data analysis (EDA).
- **Topics**: Transition from Python collections to tabular data; loading `data_collection.csv` using Pandas; inspecting dataframe shapes, heads, tails, and column distributions; handling data types and parsing custom date strings into datetime objects.

#### `04_data_visualization.ipynb`
- **Focus**: Visualizing tabular datasets using Matplotlib and Pandas.
- **Topics**:
  - Horizontal/vertical bar charts showing top sighting locations.
  - Time-series observation trends across dates.
  - Calculating location and vehicle cardinality metrics.

#### `05_intro_to_machine_learning.ipynb`
- **Focus**: Machine Learning concepts and introductory predictive modeling.
- **Topics**:
  - The 7-step Machine Learning Lifecycle (gathering, preparing, choosing model, training, evaluation, tuning, prediction).
  - Supervised (Regression vs. Classification) vs. Unsupervised (Clustering, Dimensionality Reduction) learning.
  - Minimal Scikit-Learn Linear Regression implementation predicting scores based on study hours.

---

### Track 2: Quantum Computing (Qiskit)

#### `01_first_steps_quantum_circuits.ipynb` (Qiskit Fall Fest: Notebook A)
- **Focus**: Getting started with Qiskit 1.x primitives and quantum circuits.
- **Topics**:
  - Quantum circuits with qubits and classical bits.
  - Single-qubit gates: Pauli-X (NOT) gate and Hadamard (H) gate for superposition.
  - Two-qubit gates: CNOT (`cx`) gate for quantum entanglement.
  - Creating and measuring the Bell state $(|00\rangle + |11\rangle)/\sqrt{2}$.
  - Simulating measurement counts using `AerSimulator` and `Sampler`.
  - Transpilation and ISA circuits for IBM Quantum hardware.

#### `02_chsh_inequality.ipynb` (Qiskit Fall Fest: Notebook B)
- **Focus**: Testing Bell's theorem and demonstrating quantum non-locality.
- **Topics**:
  - Theory and mathematical formulation of the Clauser-Horne-Shimony-Holt (CHSH) inequality.
  - Parameterized quantum circuits using `Parameter("theta")`.
  - Defining Pauli observables ($ZZ$, $ZX$, $XZ$, $XX$) with `SparsePauliOp`.
  - Transpilation and mapping observables to ISA layout.
  - Expectation value evaluation using the Qiskit Runtime `EstimatorV2` primitive.
  - Plotting the CHSH witness across phase angles showing violation of the classical bound ($\le 2$) up to Tsirelson's bound ($2\sqrt{2}$).

#### `03_quantum_workshop_noise_and_adder.ipynb` (Workshop 1)
- **Focus**: Practical quantum circuit development, barriers, and noise introduction.
- **Topics**:
  - Environment verification and package imports.
  - Quantum circuit barriers (`qc.barrier()`) to prevent premature gate aggregation during transpilation.
  - Simulating artificial noise using Qiskit Aer `NoiseModel`, `depolarizing_error`, and `thermal_relaxation_error`.
  - Constructing a quantum half-adder circuit with 3 qubits (inputs $a, b$ and auxiliary/sum qubit) using CNOT gates.
  - Executing circuits locally using `StatevectorSampler`.

#### `04_half_adder_and_noise_models.ipynb`
- **Focus**: Advanced noise modeling and error mitigation.
- **Topics**:
  - Custom unitary matrices converted into quantum gates (`UnitaryGate`).
  - Quantum channels, Kraus operators (`Kraus`), and Superoperators (`SuperOp`).
  - Bit-flip and phase-flip Pauli errors (`pauli_error`).
  - Measurement misassignment modeling (`ReadoutError`).
  - Qiskit Runtime Estimator error mitigation settings: resilience levels, gate twirling (`options.twirling.enable_gates`), and readout mitigation (`options.resilience.measure_mitigation`).

#### `05_quantum_simulation_methods.ipynb`
- **Focus**: Offline and local simulation methods.
- **Topics**:
  - Offline simulation using IBM's mock backend `FakeManilaV2` with `SamplerV2`.
  - Single-qubit superposition simulation with `AerSimulator` and probability distribution visualization.

#### `06_grover_oracle_basics.ipynb`
- **Focus**: Grover's search algorithm fundamentals and phase inversion.
- **Topics**:
  - Classical vs. quantum search oracles.
  - Implementing a 2-qubit phase oracle using a Controlled-Z (`cz`) gate marking the $|11\rangle$ target state.
  - Initial state preparation via Hadamard gates.
  - Quantum state inspection and multi-qubit Bloch sphere visualization (`plot_bloch_multivector`).

---

## Summary of Code Fixes & Completions

1. **Syntax & Type Errors Fixed**:
   - `practicehackathon.ipynb`: Corrected `10i + 4j` to `10 + 4j` (valid Python complex syntax).
   - `practicehackathon.ipynb`: Fixed invalid function definition `def myFunction(country : "India")` to `def myFunction(country="India"):`.
   - `practicehackathon.ipynb`: Removed `>>> 'hello'` interactive shell prompt artifact.
   - `machinelearning.ipynb`: Fixed malformed dictionary `{"raghu":"trainer","mahi":"player","guru"}` where `"guru"` had no value.
   - `machinelearning.ipynb`: Fixed `KeyError: 'START*'` by querying valid columns (`Location`, `Number Plate`).
   - `Untitled1.ipynb`: Corrected `if my_input is winner` to `my_input == winner` to prevent `SyntaxWarning`.
   - `half_adder_Erros.ipynb`: Fixed `QuantumCircuit(2)` to `QuantumCircuit(2, 2)` before calling `qc.measure([0,1],[0,1])` to prevent `IndexError`.
   - `Untitled1.ipynb`: Replaced invalid call `grover_circ(0)` with `Statevector.from_instruction(grover_circ)`.

2. **Incomplete Code Completed (with Minimum Clean Lines)**:
   - `Notebook_2.ipynb`: Completed Exercise 1 with 4 required gates (`x` and `h` across qubits) and Exercise 2 with Hadamard and CNOT gates to construct a Bell state.
   - `Workshop_1.ipynb`: Completed empty import cell, added circuit barrier demonstration, and repaired `StatevectorSampler` measurement processing to extract count dictionaries.
   - `Simulation_Method.ipynb`: Completed single-qubit Hadamard superposition circuit with measurement, `AerSimulator` execution, and histogram plotting; decoupled `FakeManilaV2` from online IBM token check.
   - `Data_Visualization.ipynb`: Built a clean visualization notebook displaying city sighting frequency and daily trends.
   - `intro_to_ML.ipynb`: Added ML concepts and a 10-line working Scikit-Learn Linear Regression model.

3. **Code Cleanup**:
   - Deleted all dangling, empty code and markdown cells across all notebooks.
   - Cleared obsolete `.ipynb_checkpoints` cache files and updated `.gitignore`.

---

## Data Assets

### `data/data_collection.csv`
Contains 75 traffic surveillance records with the following schema:
- `Date`: Observation date formatted as `DD-MM-YYYY` (spanning January 2024).
- `Time`: Timestamp of observation (`hh:mm AM/PM`).
- `Location`: US city / municipality name (e.g., `New York`, `Los Angeles`, `Omaha`, `Atlanta`).
- `Number Plate`: Vehicle license plate string (e.g., `ABC1234`, `XYZ5678`).

---

## Setup & Installation

### 1. Prerequisites
- Python **>= 3.10** (recommended Python 3.11 - 3.13)
- `uv` (recommended) or standard `pip`

### 2. Environment Setup

Using `uv` (recommended):
```bash
# Sync dependencies
uv sync

# Or install dependencies with quantum support
uv pip install -e ".[quantum]"
```

Using standard `pip`:
```bash
# Core dependencies (Python & ML track)
pip install pandas numpy matplotlib scikit-learn jupyterlab

# Quantum Computing dependencies (Qiskit track)
pip install "qiskit>=1.0.0" "qiskit-aer>=0.14.0" "qiskit-ibm-runtime>=0.22.0"
```

---

## How to Run

Launch JupyterLab or classic Notebook interface from the workspace root:

```bash
jupyter lab
# or
jupyter notebook
```

Navigate to:
- `notebooks/python_and_ml/` to run Python fundamentals, data analysis, and machine learning.
- `notebooks/quantum_computing/` to explore quantum computing circuits and Qiskit Fall Fest tutorials.



