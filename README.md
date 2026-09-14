# CERA

CERA: Cross-Execution Recovery through Effect Adoption for Stochastic Agents.

Run order

1. `notebooks/generate_cera_bench.ipynb`
2. `notebooks/E0A_controlled_recovery.ipynb`
3. `notebooks/E0B_external_divergence.ipynb`

Set `RUN_MODE = "debug"` for a small end-to-end validation run. Set `RUN_MODE = "full"` for the primary study.

Repository layout

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
└── figures/
```
