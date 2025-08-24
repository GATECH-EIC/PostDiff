# Fewer Denoising Steps or Cheaper Per-Step Inference: Towards Compute-Optimal Diffusion Model Deployment [ICCV 2025]
The code for the paper [**Fewer Denoising Steps or Cheaper Per-Step Inference: Towards Compute-Optimal Diffusion Model Deployment**](https://arxiv.org/abs/2508.06160) (ICCV 2025)
- Authors: Zhenbang Du*, Yonggan Fu*, Lifu Wang*, Jiayi Qian, Xiao Luo, and Yingyan (Celine) Lin. *Equal Contribution

## Abstract

Diffusion models have shown remarkable success across generative tasks, yet their high computational demands challenge deployment on resource-limited platforms. This paper investigates a critical question for compute-optimal diffusion model deployment: Under a post-training setting without fine-tuning, is it more effective to reduce the number of denoising steps or to use a cheaper per-step inference? Intuitively, reducing the number of denoising steps increases the variability of the distributions across steps, making the model more sensitive to compression. In contrast, keeping more denoising steps makes the differences smaller, preserving redundancy, and making post-training compression more feasible. To systematically examine this, we propose PostDiff, a training-free framework for accelerating pre-trained diffusion models by reducing redundancy at both the input level and module level in a post-training manner. At the input level, we propose a mixed-resolution denoising scheme based on the insight that reducing generation resolution in early denoising steps can enhance low-frequency components and improve final generation fidelity. At the module level, we employ a hybrid module caching strategy to reuse computations across denoising steps. Extensive experiments and ablation studies demonstrate that (1) PostDiff can significantly improve the fidelity-efficiency trade-off of state-of-the-art diffusion models, and (2) to boost efficiency while maintaining decent generation fidelity, reducing per-step inference cost is often more effective than reducing the number of denoising steps.

<p align="center">
<img width="928" alt="image" src="figures/visualization.pdf"> 
</p>

Code will come soon



## Citation

If you find this work useful for your research, please cite:

````
@inproceedings{zdu2025postdiff,
  title={Early-Bird Diffusion: Investigating and Leveraging Timestep-Aware Early-Bird Tickets in Diffusion Models for Efficient Training},
  author={Du, Zhenbang and Fu, Yonggan and Wang, Lifu and Qian, Jiayi and Luo, Xiao and Lin, Yingyan (Celine)},
  booktitle={International Conference on Computer Vision},
  year={2025}
}
````
