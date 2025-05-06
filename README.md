# Final_Project: Implementing SAM 2.1 Hiera Small and Base Plus
**Environment**<br>
To run both implementations, access to Google Colab and Google Drive is neccessary. <br>
The Python version must be greater than Python 3.10 <br>
**Google Drive Folder**<br>
To import the dataset or finetuned models please navigate to this google drive link: <br>
https://drive.google.com/drive/folders/10CfsXCHP5cfL6iWXgBgFjCMRPeT48Cfg?usp=sharing

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
