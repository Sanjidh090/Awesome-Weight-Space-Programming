# Awesome Weight-Space Programming

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A paper-first collection of research on **Weight-Space Programming** (WSP): using language models or other learned systems to read, understand, construct, repair, and edit neural-network weights.

This repository distinguishes peer-reviewed papers and arXiv preprints from blog posts, because the evidence standards and publication statuses differ.

## Contents

- [Starter](#starter)
- [Papers on Direct Weight-Space Programming](#papers-on-direct-weight-space-programming)
- [Papers Citing the Starter Blog](#papers-citing-the-starter-blog)
- [Weight-Space Representation and Weight Reading](#weight-space-representation-and-weight-reading)
- [Weight Generation and Constructed Networks](#weight-generation-and-constructed-networks)
- [Related Model Editing](#related-model-editing)
- [Citation Status](#citation-status)
- [Contributing](#contributing)

## Starter

The starting point for this collection is:

- **[Sparks of Weight-Space Programming: LLMs can natively read & write neural network weights](https://rikiyat.github.io/blog/weight-space-programming/)** — Rikiya Takehi, Jayden Teoh, Alex Zhang, and Omar Khattab, 2026. MIT CSAIL blog post and released experiment logs.
  - [Experiment logs and networks](https://github.com/RikiyaT/lm_understand-logs)
  - Covers weight reading, control-policy repair, network construction, and language-model weight editing.
  - This is a blog post, not a peer-reviewed paper. Report its experimental evidence separately from later preprints and published work.

## Papers on Direct Weight-Space Programming

### 2026

- **[Interpretable weight-space programming builds transparent transformers and brain encoding models](https://arxiv.org/abs/2611.18114)** — arXiv:2611.18114, 2026.
  - Introduces interpretable weight-space programming (iWSP), where an LLM agent iteratively builds transparent transformers and brain encoding models by explicitly hand-crafting weights and features in code.
  - Uses no backpropagation for parameter construction; prior knowledge, agent feedback, and trial iterations replace gradient training.

- **[WeightCode: Installing New Capabilities into Neural Networks via Weight Programming](https://arxiv.org/abs/2611.25476)** — arXiv:2611.25476, 2026.
  - Frozen language models synthesize executable weight programs that install new capabilities, preserve existing behavior, and can be replayed on compatible networks.
  - Includes separate evidence for held-out acceptance, replay across trained networks, and sequential editing.

- **[Consistency Is Not Understanding: Orbit Audits for Neural Field Weight Readers](https://arxiv.org/abs/2611.05798)** — arXiv:2611.05798, 2026.
  - Audits whether weight readers recognize represented functions when function-preserving neuron permutations and positive ReLU rescalings change raw tensor coordinates.
  - A useful replication and evaluation reference for claims about LLM weight understanding.

## Papers Citing the Starter Blog

The following papers or preprints are candidates for this section because public manuscript text, repositories, or project documentation cite or discuss the starter blog.

| Paper | arXiv / venue | How it relates |
| --- | --- | --- |
| [Interpretable weight-space programming builds transparent transformers and brain encoding models](https://arxiv.org/abs/2611.18114) | arXiv:2611.18114 | Related concurrent approach; public project documentation distinguishes iWSP from the MIT CSAIL Sparks blog. |
| [WeightCode: Installing New Capabilities into Neural Networks via Weight Programming](https://arxiv.org/abs/2611.25476) | arXiv:2611.25476 | Cites the Sparks of Weight-Space Programming blog as related direct weight-editing work. |

> Before adding a citation row, verify it in the paper PDF or arXiv source rather than relying only on a blog, README, GitHub summary, or model card.

## Weight-Space Representation and Weight Reading

- **[Permutation Equivariant Neural Functionals](https://arxiv.org/abs/2302.14040)** — Allan Zhou et al., NeurIPS 2023.
  - Neural layers for processing weights while respecting permutation symmetries.
  - [Code](https://github.com/AllanYangZhou/nfn)

- **[Neural Functional Transformers](https://arxiv.org/abs/2305.13546)** — Allan Zhou et al., NeurIPS 2023.
  - Attention-based permutation-equivariant models over weight spaces.
  - [Code](https://github.com/AllanYangZhou/nfn)

- **[Equivariant Deep Weight Space Alignment](https://arxiv.org/abs/2310.13397)** — Aviv Navon et al., ICML 2024.
  - Learns network alignments under permutation symmetries, relevant to comparing parameter representations.
  - [Code](https://github.com/AvivNavon/deep-align)

- **[Deep Neural Networks as Point Clouds](https://arxiv.org/abs/2101.08031)** — Balazs? add verified authors and venue. <!-- Replace or remove if citation metadata has not been verified. -->

## Weight Generation and Constructed Networks

- **[HyperNetworks](https://arxiv.org/abs/1609.09106)** — David Ha, Andrew Dai, and Quoc V. Le, 2016.
  - Generates the weights of another network with a learned weight generator.

- **[Parameter Prediction for Unseen Deep Architectures](https://arxiv.org/abs/2110.13100)** — Boris Knyazev et al., NeurIPS 2021.
  - Predicts parameters for unseen architectures from architecture graphs.
  - [Code and dataset](https://github.com/facebookresearch/ppuda)

- **[Thinking Like Transformers](https://arxiv.org/abs/2106.06981)** — Gail Weiss, Yoav Goldberg, and Eran Yahav, ICML 2021.
  - Introduces RASP for expressing computations that can be compiled into attention-style mechanisms.

- **[Tracr: Compiled Transformers as a Laboratory for Interpretability](https://arxiv.org/abs/2301.05062)** — David Lindner et al., NeurIPS 2023.
  - Compiles readable programs into transformer weights with known structure.
  - [Code](https://github.com/google-deepmind/tracr)

- **[Learning Transformer Programs](https://arxiv.org/abs/2306.01128)** — Dan Friedman, Alexander Wettig, and Danqi Chen, NeurIPS 2023.
  - Learns constrained transformers that can be converted into human-readable programs.
  - [Code](https://github.com/princeton-nlp/TransformerPrograms)

## Related Model Editing

These papers are useful baselines or mechanisms, but their algorithms are generally not direct LLM weight-programming claims.

- **[Locating and Editing Factual Associations in GPT](https://arxiv.org/abs/2202.05262)** — Kevin Meng et al., NeurIPS 2022.
  - Localizes factual associations and updates them through targeted feed-forward weight edits.
  - [Code](https://github.com/kmeng01/rome)

- **[Editing Models with Task Arithmetic](https://arxiv.org/abs/2212.04089)** — Gabriel Ilharco et al., ICLR 2023.
  - Forms and combines task vectors from fine-tuned weight differences.
  - [Code](https://github.com/mlfoundations/task_vectors)

## Citation Status

The starter blog is a 2026 release, and the field is advancing rapidly. The collection therefore separates:

1. **Directly cited by the blog or released experiment notes** — links and data from the original release.
2. **Papers that cite the blog** — papers with a verified reference in the PDF, arXiv source, or bibliography.
3. **Related papers** — foundational or comparable work that does not necessarily cite the blog.

Record verification evidence in every pull request. For a paper, cite:

- Official arXiv or venue page
- PDF or arXiv source reference section
- Exact title and year
- Whether it cites the blog, uses weight-space programming terminology, or is only foundational/related

## Contributing

We especially welcome paper additions and corrections.

Please open a pull request that:

- Adds one paper per entry or organizes several under the appropriate heading
- Links the paper's official arXiv, conference, or journal page
- Links code or released artifacts only when relevant
- States whether it cites the starter blog, performs direct weight-space programming, or is related work
- Distinguishes a preprint from a peer-reviewed publication
- Records limitations and whether results have been independently reproduced

**Good proposal format**

```markdown
- **[Paper title](official-url)** — Authors, venue/year.
  - One-sentence summary of the contribution.
  - Citation status: cites the starter blog / does not cite the blog / foundational relation.
  - [Code or artifact](url), if available.
  - Key limitation or evidence caveat.
```
