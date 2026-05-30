# TSP-Nearest-Insertion-3-opt
A practical study comparing five heuristic algorithms for the Traveling Salesman Problem (TSP), organized into greedy construction methods and local search improvement methods.
# TSP — A Comparative Study of Greedy and Local Search Algorithms

A practical study comparing five heuristic algorithms for the Traveling Salesman Problem (TSP), organized into greedy construction methods and local search improvement methods.

---

## Algorithms Implemented

**Greedy Construction**
- Nearest Insertion — O(n²)
- Cheapest Insertion — O(n³)
- Farthest Insertion — O(n³)

**Local Search**
- 2-opt — improves a tour by reversing segments between two edges
- 3-opt — more powerful improvement using three-edge reconnections

All local search methods are applied on top of a greedy-constructed initial tour.

---

## Project Structure

```
TSP-Nearest-Insertion-3-opt/
├── data/               # TSPLIB .tsp dataset files
├── tsp_solver.py       # Main pipeline — sourcecode only 
├── tsp_solver.ipynb    # Main pipeline (with output) from Colab
└── README.md
```

---

## Setup

```bash
git clone https://github.com/phuongphuongha139-commits/TSP-Nearest-Insertion-3-opt.git
cd TSP-Nearest-Insertion-3-opt
python main.py
```

No external dependencies beyond the Python standard library.

---

## Datasets

Benchmarked on 10 TSPLIB instances:

| Dataset  | Cities |
|----------|--------|
| berlin52 | 52     |
| bier127  | 127    |
| gil262   | 262    |
| linhp318 | 318    |
| pr439    | 439    |
| rat575   | 575    |
| d657     | 657    |
| rat783   | 783    |
| pr1002   | 1002   |
| rl1323   | 1323   |

---

## Output

For each dataset, the program prints:

- Initial construction cost vs. final cost after local search
- Improvement percentage
- Gap from known optimal (where available)
- Runtime in seconds

Summary table at the end shows best result per dataset across all 7 pipelines (`NI`, `NI+2opt`, `NI+3opt`, `CI`, `CI+3opt`, `FI`, `FI+3opt`).

---

## Key Findings

- Local search (especially 3-opt) significantly reduces tour length over pure greedy solutions
- Farthest Insertion tends to produce the best greedy-only tours
- 3-opt achieves better quality than 2-opt at the cost of longer runtime
- For large instances (n > 500), runtime becomes the main constraint

Algorithms Implemented
Greedy Construction

Nearest Insertion — O(n²)
Cheapest Insertion — O(n³)
Farthest Insertion — O(n³)

Local Search

2-opt — improves a tour by reversing segments between two edges
3-opt — more powerful improvement using three-edge reconnections
