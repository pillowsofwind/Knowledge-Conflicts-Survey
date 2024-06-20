# 💥Knowledge Conflicts for LLMs: A Survey

---

This is the repository for the survey paper: [Knowledge Conflicts for LLMs: A Survey](https://arxiv.org/abs/2403.08319).

<p align="center">
Rongwu Xu<sup>1</sup>*, Zehan Qi<sup>1</sup>*, Zhijiang Guo<sup>2</sup>, Cunxiang Wang<sup>3</sup>, Hongru Wang<sup>4</sup>, Yue Zhang<sup>3</sup> and Wei Xu<sup>1</sup>.
</p> 

<p align="center">
1. Tsinghua University; 2. University of Cambridge; 3. Westlake University; 4. Chinese University of Hong Kong.<br>
 (*: Equal Contribution)
</p> 

## Recap

<img src="./figures/Types-of-conflicts.png" alt="Types-of-conflicts" style="zoom:50%;" />

We investigate **three** types of knowledge conflicts: context-memory conflict, inter-context conflict, and intra-memory conflict.

- **Context-memory conflict:** Contextual knowledge (context) can conflict with the parametric knowledge (memory) encapsulated within the LLM's parameters.
- **Inter-context conflict:** Conflict among various pieces of contextual knowledge (e.g., noise, outdated information, misinformation, etc.).
- **Intra-memory conflict:** LLM's parametric knowledge may yield divergent responses to differently phrased queries, which can be attributed to the conflicting knowledge embedded within the LLM's parameters.

<img src="./figures/Method.png" alt="Taxonomy" style="zoom:80%;" />

This survey reviews the literature on the causes, behaviors, and possible solutions to knowledge conflicts.

<img src="./figures/Taxonomy.png" alt="Taxonomy" style="zoom:100%;" />

##  Star History  

[![Star History Chart](https://api.star-history.com/svg?repos=pillowsofwind/Knowledge-Conflicts-Survey&type=Date)](https://star-history.com/#pillowsofwind/Knowledge-Conflicts-Survey&Date)