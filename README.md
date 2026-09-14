# CERA

CERA: Cross-Execution Recovery through Effect Adoption for Stochastic Agents.

This repository contains the benchmark-generation and E0 evaluation pipeline for the SOSP 2027 study.

## Run order

1. `notebooks/generate_cera_bench.ipynb`
2. `notebooks/E0A_controlled_recovery.ipynb`
3. `notebooks/E0B_external_divergence.ipynb`

Set `RUN_MODE = "debug"` for a small end-to-end validation run. Set `RUN_MODE = "full"` for the primary study.

The notebooks write all generated artifacts under `benchmark/`, `data/osworld/`, `results/`, and `figures/`. Model weights are downloaded to the local model cache and are not stored in this repository.

## Repository layout

```text
cera/
├── README.md
├── requirements.txt
├── LICENSE
├── .gitignore
├── configs/
│   ├── benchmark.yaml
│   ├── models.yaml
│   └── experiments.yaml
├── notebooks/
│   ├── generate_cera_bench.ipynb
│   ├── E0A_controlled_recovery.ipynb
│   └── E0B_external_divergence.ipynb
├── benchmark/
│   ├── tasks/
│   ├── traces/
│   ├── oracles/
│   └── manifests/
├── data/
│   └── osworld/
├── results/
│   ├── E0A/
│   └── E0B/
└── figures/
    ├── E0A/
    └── E0B/
```

The empty artifact directories are retained with `.gitkeep` files; generated benchmark data, OSWorld traces, results, and figures should not be committed unless explicitly required for release.

## Reproducibility

Each generated benchmark case records the task, model, seed, fault, trace paths, oracle path, and generation metadata. Experiment outputs contain machine-readable summaries and manifests suitable for reproducing the paper figures.

## Model licensing

Model weights are not redistributed here. Each model remains subject to its upstream license and access terms. The repository stores model identifiers and experiment metadata only.
