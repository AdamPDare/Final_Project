# Final_Project: Finetuning SAM 2.1 Hiera Small and Base Plus
**Environment**<br>
To run both implementations, access to Google Colab and Google Drive is neccessary. <br>
The Python version must be greater than Python 3.10 <br>
**Google Drive Folder**<br>
To import the dataset or finetuned models please navigate to this google drive link: <br>
https://drive.google.com/drive/folders/10CfsXCHP5cfL6iWXgBgFjCMRPeT48Cfg?usp=sharing

<br>**Code Files**<br>
* FP_SAM_HBase.ipynb <br>
  * Contains all the code utilised to finetune SAM 2.1 Hiera Base Plus <br>
* FP_SAM_HS.ipynb <br>
  * Contains all the code utilised to finetune SAM 2.1 Hiera Small<br>

**Finetuning**<br>
For optimal finetuning, please use Google Colab's A100 GPUs. The finetuning process will run on other GPUs but will require a lot more training time <br>

<br> **Folders** <br>
* BraTS2020_TrainingData<br>
  * Contains the original dataset before Discrete Wavelet Transform Image fusion is applied<br>
* BraTS2020_ValidationData<br>
  * Contains data with no ground truths that could be used for model inference<br>
* sliced_TrainingDataset_T<br>
  * Stores All of the sliced MRI scans that have had Discrete Wavelet Transform Image fusion applied. This is the dataset used for finetuning and evaluating the models<br>
* sliced_GroundTruths_T<br>
  * Stores all of the sliced ground truths for the MRI scans. This is used to evaluate the models generated masks.<br>
* sliced_TrainingDataset_T.zip<br>
  * This is the zipped version of sliced_TrainingDataset_T. This is copied across to Google Colab's runtime memory<br>
* sliced_GroundTruths_T<br>
  * This is the zipped version of sliced_GroundTruths_T. This is copied across to Google Colab's runtime memory<br>
* Model_Checkpoints<br>
  * Stores all the model weights during fine tuning. (This is done once every five epochs)<br>
* Final_Saved_Model<br>
  * Stores all the final model weights that are used to test the model.<br>


**Final Finetuned Models**<br>
The SAM 2.1 Hiera Base model weights are stored in the folder Final_Saved_Model:
* finetunedSAM2_Base.torch

The SAM 2.1 Hiera Small Model weights are stored in the folder Final_Saved_Model:
* finetunedSAM2_S_V2_t2.torch

**Citations**<br>
[1] B. H. Menze, A. Jakab, S. Bauer, J. Kalpathy-Cramer, K. Farahani, J. Kirby, et al. "The Multimodal Brain Tumor Image Segmentation Benchmark (BRATS)", IEEE Transactions on Medical Imaging 34(10), 1993-2024 (2015) DOI: 10.1109/TMI.2014.2377694 <br>

[2] S. Bakas, H. Akbari, A. Sotiras, M. Bilello, M. Rozycki, J.S. Kirby, et al., "Advancing The Cancer Genome Atlas glioma MRI collections with expert segmentation labels and radiomic features", Nature Scientific Data, 4:170117 (2017) DOI: 10.1038/sdata.2017.117 <br>

[3] S. Bakas, M. Reyes, A. Jakab, S. Bauer, M. Rempfler, A. Crimi, et al., "Identifying the Best Machine Learning Algorithms for Brain Tumor Segmentation, Progression Assessment, and Overall Survival Prediction in the BRATS Challenge", arXiv preprint arXiv:1811.02629 (2018) <br>

@article{ravi2024sam2,
  title={SAM 2: Segment Anything in Images and Videos},
  author={Ravi, Nikhila and Gabeur, Valentin and Hu, Yuan-Ting and Hu, Ronghang and Ryali, Chaitanya and Ma, Tengyu and Khedr, Haitham and R{\"a}dle, Roman and Rolland, Chloe and Gustafson, Laura and Mintun, Eric and Pan, Junting and Alwala, Kalyan Vasudev and Carion, Nicolas and Wu, Chao-Yuan and Girshick, Ross and Doll{\'a}r, Piotr and Feichtenhofer, Christoph},
  journal={arXiv preprint arXiv:2408.00714},
  url={https://arxiv.org/abs/2408.00714},
  year={2024}
}

