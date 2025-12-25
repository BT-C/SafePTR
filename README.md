<div align="center">
</div>

# SafePTR: Token-Level Jailbreak Defense in Multimodal LLMs via Prune-then-Restore Mechanism

<a href='https://github.com/BT-C/HIO'><img src='https://img.shields.io/badge/Project-Page-Green'></a>
<a href='https://github.com/BT-C/HIO'><img src='https://img.shields.io/badge/Demo-Page-purple'></a>
<a href='https://arxiv.org/pdf/2405.15356'><img src='https://img.shields.io/badge/Paper-PDF-orange'></a>
![License](https://img.shields.io/badge/License-BSD-blue.svg)


This is the official repository of the following paper and a project that study positional perception in LVLMs.
> **[SafePTR: Token-Level Jailbreak Defense in Multimodal LLMs via Prune-then-Restore Mechanism]([https://arxiv.org/pdf/2405.15356](https://arxiv.org/abs/2507.01513))**<br>
> NeurIPS 2025<br>
>  Beitao Chen, Xinyu Lyu, Lianli Gao, Jingkuan Song, Heng Tao Shen<br>


# Introduction
By incorporating visual inputs, Multimodal Large Language Models (MLLMs) extend LLMs to support visual reasoning. However, this integration also introduces new vulnerabilities, making MLLMs susceptible to multimodal jailbreak attacks and hindering their safe deployment. Existing defense methods, including Imageto-Text Translation, Safe Prompting, and Multimodal Safety Tuning, attempt to address this by aligning multimodal inputs with LLMs’ built-in safeguards. Yet, they fall short in uncovering root causes of multimodal vulnerabilities, particularly how harmful multimodal tokens trigger jailbreak in MLLMs? Consequently, they remain vulnerable to text-driven multimodal jailbreaks, often exhibiting overdefensive behaviors and imposing heavy training overhead. To bridge this gap, we present an comprehensive analysis of where, how and which harmful multimodal tokens bypass safeguards in MLLMs. Surprisingly, we find that less than 1% tokens in early-middle layers are responsible for inducing unsafe behaviors, highlighting the potential of precisely removing a small subset of harmful tokens, without requiring safety tuning, can still effectively improve safety against jailbreaks. Motivated by this, we propose Safe Prune-then-Restore (SafePTR), an training-free defense framework that selectively prunes harmful tokens at vulnerable layers while restoring benign features at subsequent layers. Without incurring additional computational overhead, SafePTR significantly enhances the safety of MLLMs while preserving efficiency. Extensive evaluations across three MLLMs and five benchmarks demonstrate SafePTR’s state-of-the-art performance in mitigating jailbreak risks without compromising utility

Visit our 🏠 [project page](https://github.com/BT-C/SafePTR) and 📃 [paper](https://arxiv.org/abs/2507.01513) to explore more!

<img src="./assets/framework.png">

## 🎈News

#### 📌 Pinned

* [2025.09.29] 📃 Our SafePTR is accepted by [NeurIPS 2025]([https://neurips.cc/virtual/2024/poster/95118](https://neurips.cc/virtual/2025/loc/san-diego/poster/118476))!
* [2025.5.30] 📃 Our paper is accesible at [arxiv]([https://arxiv.org/pdf/2405.15356](https://arxiv.org/abs/2507.01513)) now. 



[![Code License](https://img.shields.io/badge/Code%20License-Apache_2.0-green.svg)](https://github.com/tatsu-lab/stanford_alpaca/blob/main/LICENSE)
[![Data License](https://img.shields.io/badge/Data%20License-CC%20By%20NC%204.0-red.svg)](https://github.com/tatsu-lab/stanford_alpaca/blob/main/DATA_LICENSE)

**Usage and License Notices**: The data, code, and checkpoint are intended and licensed for research use only. They are also restricted to uses that follow the license agreement of LLaMA, Vicuna, and Chat GPT. The dataset is CC BY NC 4.0 (allowing only non-commercial use) and models trained using the dataset should not be used outside of research purposes.


## Acknowledgement
   - [LLaVA-1.5](https://github.com/haotian-liu/LLaVA). The LLaVA-v1.5 part of HIO is based on the official LLaVA-1.5 implementation, which is a great open-source work on LVLM.
   - [MiniGPT-4](https://github.com/Vision-CAIR/MiniGPT-4). The MiniGPT-4 part of HIO is based on the official MiniGPT-4 implementation. 


