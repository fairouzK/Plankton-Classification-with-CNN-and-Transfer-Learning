# Plankton-Classification

#### Dataset
The dataset contains images of phytoplankton species of different sizes and shapes.
When placed in their respective species folder, the dataset has 19 classes.
Originally the dataset had around 304 images.
Images from WHOI Plankton dataset were added to increase size of the data set.
The images per class range from as low as 3 to as high as 182 causing class imbalance
The data was divided into training, validation and test sets in the ratio 80-10-10.  
It can be downloaded from <a href = "https://www.kaggle.com/datasets/feruzz/plankton-dataset"> Kaggle. </a>


#### Models
A total of 3 models were implemented: 
1. Basic model with 6 layers
2. Pretrained model as feature extractor: The pretrained model used is VGG16 with the classifier (convolutional layers) frozen. Then a new classifier composed of FC dense layers was added on top of the feature extractor.
3. Pretrained model in Fine-tune mode: VGG16 with top layer frozen. A new classifier composed of FC dense layers was added on top. Then the model is trained. Next, some layers are unfrozen. Then the model is retrained.


#### Results
Pretrained model in Fine-tune mode outperformed the rest.
Metrics | Basic Model | Feature Extractor | Fine-tune Mode |
--- | --- | --- | --- 
F1 score in traning data | 64% | 77% | 87.4% 
Test Accuracy | 64.4% | 79.7% | 88% 

### Authors
Feruz Elmay <br>
Biyanu Zerom <br>
Miguel Ramirez <br>
