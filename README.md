# 💥Knowledge Conflicts for LLMs: A Survey


This is the repository for the survey paper: [Knowledge Conflicts for LLMs: A Survey](https://arxiv.org/abs/2403.08319). 

🌟Star us for future lookups! 关注不迷路！🌟

<p align="center">
<img src="./figures/Types-of-conflicts.png" alt="Types-of-conflicts" width="400" /> <br>
</p> 

<p align="center">
<strong>
Rongwu Xu<sup>1</sup>*, Zehan Qi<sup>1</sup>*, Zhijiang Guo<sup>2</sup>, Cunxiang Wang<sup>3</sup>, Hongru Wang<sup>4</sup>, Yue Zhang<sup>3</sup> and Wei Xu<sup>1</sup>
</strong>
</p> 

<p align="center">
1. Tsinghua University; 2. University of Cambridge; 3. Westlake University; 4. The Chinese University of Hong Kong<br>
 (* Equal Contribution)
</p> 

## 📝 Citation

If you find our survey useful, please consider citing:
``` bib
@article{xu2024knowledge,
  title={Knowledge Conflicts for LLMs: A Survey},
  author={Xu, Rongwu and Qi, Zehan and Wang, Cunxiang and Wang, Hongru and Zhang, Yue and Xu, Wei},
  journal={arXiv preprint arXiv:2403.08319},
  year={2024}
}
```

## ❤️ Recap

We investigate **three** types of knowledge conflicts: context-memory conflict, inter-context conflict, and intra-memory conflict.

- **Context-memory conflict:** Contextual knowledge (context) can conflict with the parametric knowledge (memory) encapsulated within the LLM's parameters.
- **Inter-context conflict:** Conflict among various pieces of contextual knowledge (e.g., noise, outdated information, misinformation, etc.).
- **Intra-memory conflict:** LLM's parametric knowledge may yield divergent responses to differently phrased queries, which can be attributed to the conflicting knowledge embedded within the LLM's parameters.

This survey reviews the literature on the **causes, behaviors, and possible solutions** to knowledge conflicts.

<p align="center">
<img src="./figures/Taxonomy.png" alt="Taxonomy" width="680" /> <br>
 Taxonomy of knowledge conflicts: we consider three distinct types of conflicts and analysis causes, behaviors, and solutions.
</p>

## 🚀 Table of Contents

- [Type I: Context-memory conflict](#section1)
  - [I-i: Causes](#section1-i)
  - [I-ii: (Behavior) Analysis](#section1-ii)
  - [I-iii: (Mitigating) Solutions](#section1-iii)
- [Type II: Inter-context conflict](#section2)
  - [II-i: Causes](#section2-i)
  - [II-ii: (Behavior) Analysis](#section2-ii)
  - [II-iii: (Mitigating) Solutions](#section2-iii)
- [Type III: Intra-memory conflict](#section3)
  - [III-i: Causes](#section3-i)
  - [III-ii: (Behavior) Analysis](#section3-ii)
  - [III-iii: (Mitigating) Solutions](#section3-iii)

## Type I: Context-memory conflict {#section1}

### I-i: Causes {#section1-i}

#### Temporal Misalignment

1. Mind the gap: Assessing temporal generalization in neural language models, _Lazaridou et al._, **Neurips 2021**.[[Paper](https://proceedings.neurips.cc/paper/2021/hash/f5bf0ba0a17ef18f9607774722f5698c-Abstract.html?ref=ruder.io)]
2. Time Waits for No One! Analysis and Challenges of Temporal Misalignment, _Luu et al._, **NAACL 2022**. [[Paper](https://aclanthology.org/2022.naacl-main.435/)]
3. Time-aware language models as temporal knowledge bases, _Dhingra et al._, **TACL 2022**.[[Paper](https://direct.mit.edu/tacl/article/doi/10.1162/tacl_a_00459/110012/Time-Aware-Language-Models-as-Temporal-Knowledge)]
4. Towards continual knowledge learning of language models, _Jang et al._, **ICLR 2022**, [[Paper](https://arxiv.org/abs/2110.03215)]
5. Temporalwiki: A lifelong benchmark for training and evaluating ever-evolving language models, _Jang et al._, **EMNLP 2023**, [[Paper](https://aclanthology.org/2022.emnlp-main.418/)]
6. Streamingqa: A benchmark for adaptation to new knowledge over time in question answering models, _Liska et al._, **ICML 2022**. [[Paper](https://proceedings.mlr.press/v162/liska22a.html)]
7. Can LMs Generalize to Future Data? An Empirical Analysis on Text Summarization, _Cheang et al._, **EMNLP 2023**, [[Paper](https://aclanthology.org/2023.emnlp-main.1007/)]
8. RealTime QA: What's the Answer Right Now?, _Kasai et al._, **Neurips 2024**, [[Paper](https://proceedings.neurips.cc/paper_files/paper/2023/hash/9941624ef7f867a502732b5154d30cb7-Abstract-Datasets_and_Benchmarks.html)]

#### Misinformation Pollution 

1. Attacking open-domain question answering by injecting misinformation, _Pan et al._, **AACL 2023**, [[Paper](https://aclanthology.org/2023.ijcnlp-main.35.pdf)]
2. On the risk of misinformation pollution with large language models, _Pan et al._, **EMNLP 2023**, [[Paper](https://aclanthology.org/2023.findings-emnlp.97.pdf)]
3. Defending against misinformation attacks in open-domain question answering, _Weller et al. _, **EACL 2024**, [[Paper](https://aclanthology.org/2024.eacl-short.35.pdf)]
4. The earth is flat because...: Investigating llms’ belief towards misinformation via persuasive conversation, _Xu et al._, **ACL 2024**, [[Paper](https://arxiv.org/pdf/2312.09085)]
5. Prompt injection attack against llm-integrated applications, _Liu et al._, **arXiv 2024**, [[Paper](https://arxiv.org/pdf/2306.05499)]
6. Benchmarking and defending against indirect prompt injection attacks on large language models, _Yi et al._, **arXiv 2024**, [[Paper](https://arxiv.org/pdf/2312.14197)]
7. Adaptive chameleon or stubborn sloth: Unraveling the behavior of large language models in knowledge conflicts, _Xie et al._, **ICLR 2024**, [[Paper](https://arxiv.org/pdf/2305.13300)]
8. Poisoning web-scale training datasets is practical, _Carlini et al._, **S&P 2024**, [[Paper](https://www.computer.org/csdl/proceedings-article/sp/2024/313000a175/1V5U7f5aGPu)]
9. Can llm-generated misinformation be detected, _Chen and Shu_, **ICLR 2024**, [[Paper](https://arxiv.org/pdf/2309.13788)]

### I-ii: (Behavior) Analysis {#section1-ii}

1. Entity-Based Knowledge Conflicts in Question Answering, _Longpre et al._, **EMNLP 2021**, [[Paper](https://aclanthology.org/2021.emnlp-main.565.pdf)]
2. Rich Knowledge Sources Bring Complex Knowledge Conflicts: Recalibrating Models to Reflect Conflicting Evidence, _Chen et al._, **EMNLP 2022**, [[Paper](https://aclanthology.org/2022.emnlp-main.146.pdf)]

### I-iii: (Mitigating) Solutions {#section1-iii}

## Type II: Inter-context conflict {#section2}

### II-i: Causes {#section2-i}

### II-ii: (Behavior) Analysis {#section2-ii}

### II-III: (Mitigating) Solutions {#section2-iii}

## Type III: Intra-memory conflict {#section3}

### III-i: Causes {#section3-i}

### III-ii: (Behavior) Analysis {#section3-ii}

### III-iii: (Mitigating) Solutions {#section3-iii}

## Star History  

[![Star History Chart](https://api.star-history.com/svg?repos=pillowsofwind/Knowledge-Conflicts-Survey&type=Date)](https://star-history.com/#pillowsofwind/Knowledge-Conflicts-Survey&Date)
