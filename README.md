# Callee-Dataset

This repo provides a dataset for x86_64 indirect call recognition.


## Contents

```
.
|-- README.md
|-- funcs                   # Assembly functions of collected indirect calls
|   |-- callee              # Functions of collected callees
|   `-- callsite            # Functions of collected callsites
`-- icall.release.csv       # Indirect calls with columns (callsite_offset, callee_offset, callsite_binary, callee_binary)
```

## Acknowledgement

The dataset is built upon the following benchmarks:

 * [SPEC CPU 2006](https://www.spec.org/cpu2006/)
 * [UniBench](https://github.com/unifuzz/unibench)

And with the following tool:

 * [ibresolver](https://github.com/Learner0x5a/ibresolver)

## Bibtex
If this work or BinaryCorp dataset are helpful for your research, please consider citing the following BibTeX entry.

```
@article{zhu2023ktrans,
  title={kTrans: Knowledge-Aware Transformer for Binary Code Embedding},
  author={Zhu, Wenyu and Wang, Hao and Zhou, Yuchen and Wang, Jiaming and Sha, Zihan and Gao, Zeyu and Zhang, Chao},
  journal={arXiv preprint arXiv:2308.12659},
  year={2023}
}

@INPROCEEDINGS {10179482,
author = {W. Zhu and Z. Feng and Z. Zhang and J. Chen and Z. Ou and M. Yang and C. Zhang},
booktitle = {2023 IEEE Symposium on Security and Privacy (SP)},
title = {Callee: Recovering Call Graphs for Binaries with Transfer and Contrastive Learning},
year = {2023},
volume = {},
issn = {},
pages = {2357-2374},
abstract = {Recovering binary programs’ call graphs is crucial for inter-procedural analysis tasks and applications based on them. One of the core challenges is recognizing targets of indirect calls (i.e., indirect callees). Existing solutions all have high false positives and negatives, making call graphs inaccurate. In this paper, we propose a new solution Callee combining transfer learning and contrastive learning. The key insight is that, deep neural networks (DNNs) can automatically identify patterns concerning indirect calls. Inspired by the advances in question-answering applications, we utilize contrastive learning to answer the callsite-callee question. However, one of the toughest challenges is that DNNs need large datasets to achieve high performance, while collecting large-scale indirect-call ground truths can be computational-expensive. Therefore, we leverage transfer learning to pre-train DNNs with easy-to-collect direct calls and further fine-tune DNNs for indirect-calls. We evaluate Callee on several groups of targets, and results show that our solution could match callsites to callees with an F1-Measure of 94.6%, much better than state-of-the-art solutions. Further, we apply Callee to two applications – binary code similarity detection and hybrid fuzzing, and found it could greatly improve their performance.},
keywords = {knowledge engineering;privacy;target recognition;transfer learning;binary codes;artificial neural networks;fuzzing},
doi = {10.1109/SP46215.2023.10179482},
url = {https://doi.ieeecomputersociety.org/10.1109/SP46215.2023.10179482},
publisher = {IEEE Computer Society},
address = {Los Alamitos, CA, USA},
month = {may}
}

```