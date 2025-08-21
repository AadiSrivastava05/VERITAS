# VERITAS: Verification and Explanation of Realness in Images for Transparency in AI Systems
The official repository for the paper "VERITAS: Verification and Explanation of Realness in Images for Transparency in AI Systems" by Srivastava et al.   
ArXiv link: https://arxiv.org/abs/2507.05146    

## Abstract
The widespread and rapid adoption of AI-generated content, created by models such as Generative Adversarial Networks (GANs) and Diffusion Models, has revolutionized the digital media landscape by allowing efficient and creative content generation. However, these models also blur the difference between real images and AI-generated synthetic, or “fake”, images, raising concerns regarding content authenticity and integrity. While many existing solutions to detect fake images focus solely on classification and higher-resolution images, they often lack transparency in their decision-making, making it difficult for users to understand why an image is classified as fake. In this paper, we present VERITAS, a comprehensive framework that not only accurately detects whether a small
(32x32) image is AI-generated but also explains why it was classified that way through artifact localization and semantic reasoning. VERITAS produces human-readable explanations that describe key artifacts in synthetic images. We show that this architecture offers clear explanations of the
basis of zero-shot synthetic image detection tasks. 

## Features
- **Artifact Detection and Explainability**: Utilizes advanced interpretability techniques to highlight and analyze distinguishing features.
- **Super-Resolution for Detailed Analysis**: Applies super-resolution techniques to improve artifact detection in case of low-resolution images.
- **Small Image Analysis**: Studies realness and explanation of artifacts in artifact-constrained images of size 32x32 as seen in CIFAR-10 and CIFAKE. 

## Methodology
-  Super-resolve input image using DRCT
-  Localize relevant regions with GradCAM heatmaps
-  Divide image into patches weighted by attention
-  Use CLIP-based similarity for artifact classification
-  Generate textual explanations via MOLMO

## Repository Structure
- Code relevant to the architecture proposed in the paper can be found at [VERITAS](VERITAS_pipeline_notebooks)
- Classification_experiments and classification+VERITAS contains code for a variety of classification architectures reviewed in the paper. The materials in this repository are provided "as is" without any guarantees of accuracy or correctness.
- Pipeline Structure contains images to describe the pipelines discussed in the paper


## License
VERITAS: Verification and Explanation of Realness in Images for Transparency in AI Systems © 2025 by Aadi Srivastava, Vignesh Natarajkumar, Utkarsh Bheemanaboyna, Devisree Akashapu, Nagraj Gaonkar, and Archit Joshi is licensed under CC BY-SA 4.0. 

To view a copy of this license, visit [https://creativecommons.org/licenses/by-sa/4.0/](https://creativecommons.org/licenses/by-sa/4.0/).

## Citation
If you found this useful, please cite the paper as follows

```bibtex
@misc{srivastava2025veritasverificationexplanationrealness,
      title={VERITAS: Verification and Explanation of Realness in Images for Transparency in AI Systems}, 
      author={Aadi Srivastava and Vignesh Natarajkumar and Utkarsh Bheemanaboyna and Devisree Akashapu and Nagraj Gaonkar and Archit Joshi},
      year={2025},
      eprint={2507.05146},
      archivePrefix={arXiv},
      primaryClass={cs.CV},
      url={https://arxiv.org/abs/2507.05146}, 
}
```

## Contact
Incase of any questions, please contact Aadi Srivastava (aadisrivastava.iitm@gmail.com) or Vignesh Natarajkumar (vigneshn@smail.iitm.ac.in)





