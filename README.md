(Work in Progress)

# LLM Evaluability Measurement
This project investigates whether task decomposition extends the operating range of LLM judges in multilingual, reference-free evaluation.

## Abstract
LLM-as-judge evaluation is increasingly used in settings where reference outputs are unavailable, but a single-pass ("monolithic") judge often fails on inputs that fall outside its competence — most visibly in lower-resource languages and harder contexts. This work investigates whether task decomposition — splitting evaluation into separately-prompted, individually-simpler steps (in ParakhAI: claim/opinion extraction → verdict classification → reason generation) — extends the operating range of a fixed, imperfect judge, allowing it to reliably evaluate conditions it could not handle in one pass.

The target construct is deliberately not accuracy but evaluability: the set of (language, context, metric) conditions under which the judge produces a trustworthy verdict. Because the setting is reference-free, we use model uncertainty as an intrinsic, reference-free proxy for when a judge is struggling, certified on a small per-language gold subset that validates the proxy and calibrates decision thresholds. We further argue and test a boundary: decomposition reduces reasoning/compositional uncertainty but is inert against genuine knowledge or language-competence gaps (epistemic floors). The success pattern of decomposition therefore partitions conditions into reasoning-limited (recoverable) versus knowledge-limited (not), turning rival explanations into measured quantities.

The central empirical claim is that decomposition expands evaluability most where the monolithic judge is weakest distinguishing a genuine coverage-expanding method from a generic prompting trick.
