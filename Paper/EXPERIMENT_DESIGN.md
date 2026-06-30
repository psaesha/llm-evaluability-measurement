# Experiment Design

## Construct and Operationalisation
Evaluability is operationalized via **selective evaluation**. For each judge configuration, every verdict carries an uncertainty score; sweeping a threshold τ traces a **risk–coverage curve** (risk = error against gold, coverage = fraction retained below τ). Evaluability at a target reliability is **coverage at matched risk**, summarized by **AUARC**.

Inferential chain (stated explicitly to keep the design non-circular):

1. The per-language **gold subset** certifies that uncertainty tracks correctness in language *L* (AUROC, ECE, risk–coverage).
2. τ is calibrated from the gold risk–coverage curve in *L*.
3. On the **reference-free bulk**, coverage at the gold-calibrated τ measures the envelope at scale — trustworthy to the degree step 1 validated the proxy in *L*.
