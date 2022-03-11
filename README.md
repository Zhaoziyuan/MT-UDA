

<div align="center">

# MT-UDA: Towards Unsupervised Cross-modality Medical Image Segmentation with Limited Source Labels


[![MICCAI2021](https://img.shields.io/badge/Conference-MICCAI2021-green)](https://link.springer.com/chapter/10.1007/978-3-030-87193-2_28)



</div>

Pytorch implementation of our method for MICCAI2021 paper: "MT-UDA: Towards Unsupervised Cross-modality Medical Image Segmentation with Limited Source Labels". 


## Abstract
Annotating medical images is laborious, expensive, and requires human expertise, which induces the label scarcity problem. Especially when encountering the domain shift, the problem becomes more serious. The conventional UDA methods suffer from severe performance degradation when source domain annotations are scarce. In this paper, we explore a challenging UDA setting - limited source domain annotations. We aim to investigate how to efficiently leverage unlabeled data from the source and target domains with limited source annotations for cross-modality image segmentation. To achieve this, we propose a new label-efficient UDA framework, termed MT-UDA, in which the student model trained with limited source labels learns from unlabeled data of both domains by two teacher models respectively in a semi-supervised manner. We evaluate our method on MM-WHS 2017 dataset and demonstrate that our approach outperforms the state-of-the-art methods by a large margin under the source-label scarcity scenario.

<p align="center">
<img src="https://github.com/jacobzhaoziyuan/MT-UDA/blob/main/assets/archi.png" width="550">
</p>


## Dataset
* Download the MM-WHS: Multi-Modality Whole Heart Segmentation Challenge (MM-WHS) dataset from [MMWHS Challenge](https://paperswithcode.com/dataset/mm-whs-2017)

    * The original data contains cardiac 20 CT and 20 MR images.
    * The pre-processed data has been released from [PnP-AdaNet](https://github.com/carrenD/Medical-Cross-Modality-Domain-Adaptation). 
    * The training data can be downloaded [here](https://drive.google.com/file/d/1m9NSHirHx30S8jvN0kB-vkd7LL0oWCq3/view). The testing CT data can be downloaded [here](https://drive.google.com/file/d/1SJM3RluT0wbR9ud_kZtZvCY0dR9tGq5V/view).
The testing MR data can be downloaded [here](https://drive.google.com/file/d/1Bm2uU4hQmn5L3GwXz6I0vuCN3YVMEc8S/view?usp=sharing).
    * Note: for MR-to-CT adaptation, the model is trained on MR and tested on fake MR generated by [CycleGAN](https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix).





## Installation
    Install PyTorch 1.10.2 + CUDA 11.2 
    Clone this repo.
    
```
git clone https://github.com/jacobzhaoziyuan/MT-UDA
cd MT-UDA
```


## Train


## Evaluate

    
    
    






## Citation
If you find the codebase useful for your research, please cite the paper:
```
@inproceedings{zhao2021mt,
  title={MT-UDA: Towards Unsupervised Cross-modality Medical Image Segmentation with Limited Source Labels},
  author={Zhao, Ziyuan and Xu, Kaixin and Li, Shumeng and Zeng, Zeng and Guan, Cuntai},
  booktitle={International Conference on Medical Image Computing and Computer-Assisted Intervention},
  pages={293--303},
  year={2021},
  organization={Springer}
}
```

## Acknowledgement

Part of the code is adapted from open-source codebase and original implementations of algorithms, 
we thank these authors for their fantastic and efficient codebase:
* CycleGAN: https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix
* PnP-AdaNet: https://github.com/carrenD/Medical-Cross-Modality-Domain-Adaptation
* SIFA: https://github.com/cchen-cc/SIFA
* SSL4MIS: https://github.com/HiLab-git/SSL4MIS
