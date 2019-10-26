# Single-Pathway DeepMedic
> This repo is an reimplement of Single-Pathway DeepMedic.

## Requirements
* The code has been written in Python 3.6.3 and Pytorch 1.0.1
* Make sure to install all the libraries given in requirement.txt, and you can do so by the 
following command

```pip install -r requirement.txt```


## Dataset
We run experiments on [BRATS 2015 Subset](http://cseweb.ucsd.edu/~yaq007/dataset.zip). It includes training set and testing set with lables.
This subset has 20 brain turmor subjects for training and 54 subjects for testing, each of which includes four moldalities: FLAIR, T1, T1c, T2, and mask and ground truth. The ground truth of patient images have four different labels:

* label 1: necrosis
* label 2: edema
* label 3: non-enhancing tumor
* label 4: enhancing tumor
* label 0: everything else

The evaluation is done for 3 different tumor sub-compartements:
* Whole tumor: label 1, 2, 3, 4
* Enhance tumor: label 4
* Tumor core: 1, 3, 4


## How to preprocess the dataset?
You can use generate_mask.ipynb to generate mask for each image.


## How to run Single-Pathway DeepMedic?
Training and testing for Single-Pathway DeepMedic are written in Single_Pathway_DeepMedic.ipynb. If you have any question about the code, you can create a new issue.