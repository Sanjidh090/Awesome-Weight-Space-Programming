# Awesome Weight-Space Programming

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated collection of research and open-source projects for **Weight-Space Programming**: reading, reasoning about, constructing, repairing, and editing neural networks directly through their parameters.

## Contents

- [Start Here](#start-here)
- [Direct Weight-Space Programming](#direct-weight-space-programming)
- [Weight Reading and Understanding](#weight-reading-and-understanding)
- [Weight Generation and Construction](#weight-generation-and-construction)
- [Model Editing and Merging](#model-editing-and-merging)
- [Community Projects and Tools](#community-projects-and-tools)
- [Related Resources](#related-resources)
- [Contributing](#contributing)

## Start Here

- [**Sparks of Weight-Space Programming**](https://rikiyat.github.io/blog/weight-space-programming/) — Rikiya Takehi, Jayden Teoh, Alex Zhang, and Omar Khattab's introduction to the field, covering weight understanding, network repair and construction, and language-model editing.
- [RikiyaT/lm_understand-logs](https://github.com/RikiyaT/lm_understand-logs) — Released experiment artifacts and logs associated with the article.
- [OpenWSP](https://github.com/openwsp/openwsp) — Open tooling for reading, editing, and versioning model weights.

## Direct Weight-Space Programming

Work that directly asks models or agents to inspect or modify neural-network weights.

- [Sparks of Weight-Space Programming](https://rikiyat.github.io/blog/weight-space-programming/) — Demonstrates identification of network behavior from weights, repairing a control policy, constructing game-playing networks, and editing a language model.
- [Weight-Space Programming from Scratch on Simple Tasks](https://csinva.io/weight-space-programming-autoresearch/analyze/toy_examples/report.html) — An agent designs and repeatedly edits small transformer weights for bounded algorithmic tasks. [Code](https://github.com/csinva/weight-space-programming-autoresearch)
- [WSPBench](https://github.com/alexcarterhq/wspbench) — A research preview for comparing weight-analysis and weight-editing conditions.
- [Weight-Space Claude](https://github.com/nihilistau/weight-space-claude) — A Claude-based harness and experiments for selected weight-reading and construction tasks.

## Weight Reading and Understanding

- [Consistency Is Not Understanding: Orbit Audits for Neural Field Weight Readers](https://arxiv.org/abs/2611.05798) — Audits weight readers under function-preserving neuron permutations and positive ReLU rescalings.
- [Permutation Equivariant Neural Functionals](https://arxiv.org/abs/2302.14040) — Neural architectures that process network weights while respecting permutation symmetries. [Code](https://github.com/AllanYangZhou/nfn)
- [Neural Functional Transformers](https://arxiv.org/abs/2305.13546) — Attention-based models for learning over neural-network parameters. [Code](https://github.com/AllanYangZhou/nfn)
- [Equivariant Deep Weight Space Alignment](https://arxiv.org/abs/2310.13397) — Learns to align weights from networks with equivalent functions. [Code](https://github.com/AvivNavon/deep-align)

## Weight Generation and Construction

- [HyperNetworks](https://arxiv.org/abs/1609.09106) — A foundational method in which one network generates the parameters of another.
- [Parameter Prediction for Unseen Deep Architectures](https://arxiv.org/abs/2110.13100) — Predicts parameters for unseen architectures from architecture graphs. [Code](https://github.com/facebookresearch/ppuda)
- [Thinking Like Transformers](https://arxiv.org/abs/2106.06981) — Introduces RASP, a language for expressing attention-style algorithms.
- [Tracr: Compiled Transformers as a Laboratory for Interpretability](https://arxiv.org/abs/2301.05062) — Compiles readable programs into transformer weights with known structure. [Code](https://github.com/google-deepmind/tracr)
- [Learning Transformer Programs](https://arxiv.org/abs/2306.01128) — Learns constrained transformers that can be converted into human-readable programs. [Code](https://github.com/princeton-nlp/TransformerPrograms)

## Model Editing and Merging

- [Locating and Editing Factual Associations in GPT](https://arxiv.org/abs/2202.05262) — Localizes and updates factual associations in feed-forward weights. [Code](https://github.com/kmeng01/rome)
- [Editing Models with Task Arithmetic](https://arxiv.org/abs/2212.04089) — Combines fine-tuned weight differences as task vectors. [Code](https://github.com/mlfoundations/task_vectors)

## Community Projects and Tools

- [Weight-Space Programming for the Social Safety Net](https://github.com/ctrimm/weight-space-programming) — Experiments constructing networks that implement piecewise-linear formulas.
- [Weight-Space Programming from Scratch](https://github.com/csinva/weight-space-programming-autoresearch) — Saved circuits and autonomous experiments on arithmetic, sorting, parity, counting, and Boolean tasks.
- [Weight-Space Programming Experiments](https://github.com/lextoumbourou/weight-space-programming-experiments) — Cross-model game identification and constrained weight-reading experiments.
- [Beyond Math](https://github.com/Unjuno/beyond-math-weight-space-programming) — Audits released editing traces and probes whether edits affect non-math behavior.
- [wsr](https://github.com/suayptalha/wsr) — A toolkit for weight-space reading and programming.
- [WSP Kit](https://github.com/AuremHQ/weight-space-programming) — Engineering tools for editing and evaluating open-weight models.

## Related Resources

- [A Mathematical Framework for Transformer Circuits](https://transformer-circuits.pub/2021/framework/index.html) — Residual-stream, QK, and OV vocabulary for understanding transformer computation.
- [Awesome Mechanistic Interpretability](https://github.com/sindresorhus/awesome) — For general mechanistic-interpretability resources, see the [Awesome list](https://github.com/sindresorhus/awesome).

## Contributing

Contributions are welcome. Please include the primary source, a short description, and a clear explanation of how a paper, project, benchmark, or tool relates to weight-space programming.

When reporting experiments, distinguish weight reading, direct construction, compilation, learned weight generation, and targeted model editing. Include the target architecture, available information about the weights, feedback or evaluation used, search budget, and evidence or reproducibility artifacts when available.
