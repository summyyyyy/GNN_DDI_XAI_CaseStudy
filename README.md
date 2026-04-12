# Case Study: GNN-Based Drug-Drug Interaction Prediction with Explainable AI and Continuous Toxicity Endpoints

## Purpose of This Case Study

This notebook is an **empirical companion** to a systematic review on GNN-based DDI prediction, XAI for molecular graphs, and continuous toxicity endpoints.

### What This Case Study Provides

1. **Head-to-head GCN vs GAT comparison** on the standard Tox21 scaffold-split benchmark (Wu et al., 2018) across **all 12 assay tasks** with masked multi-task BCE loss — results sit directly in the published benchmark table.
2. **Honest DDI baseline + cross-drug attention ablation** on DrugBank (86-class), demonstrating quantitatively why SSI-DDI / MHCADDI-style co-attention helps.
3. **Two clearly separated XAI methods** — GNNExplainer (mask-optimisation, Ying et al., 2019) vs GAT attention weights (built-in) — with explicit methodological distinction.
4. **Transfer learning to real continuous toxicity endpoints** using the TDC LD50_Zhu dataset (rat oral LD50, mg/kg) via scaffold split.

### Scope Statement

This case study uses simplified GNN architectures as controlled baselines. It does **not** claim to fully reproduce SSI-DDI, MHCADDI, or DrugDAGT, which require additional engineering. Results are compared against those papers only where the experimental conditions are equivalent.

## Scope and Relevance to the Review (2016–2026)

- **GNN for DDI (2018–present):** GCN (Kipf & Welling, 2017), GAT (Veličković et al., 2018), cross-drug co-attention (Deac et al., 2019; Nyamabo et al., 2021).
- **XAI for molecular graphs (2019–present):** GNNExplainer mask-optimisation (Ying et al., 2019) vs built-in attention weights — two distinct methods.
- **Continuous toxicity modelling (2016–present):** Shift from binary Tox21 classification to continuous LD50 endpoints.
