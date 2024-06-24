
**Table of Contents**

[TOCM]

[TOC]

# About
*Classification Of Pet And Dog Images Using Famous Cnn Architecture. 
*

**Project submitted to:** AWS Nanodegree Summer Program on Udacity
**Last Edit:** 2024-06-24 20:46:50 Monday 
**By:** FtimaBen

#Default files
- Classified images folder: *pet_images *
- Uploaded images folder: *uploaded_images*
- Results: *results_uploaded_images / results_pet_images*
- Dog names (breed) file:  *dognames.txt*
- Labels file: *imagenet1000_clsid_to_human.txt*

# Models

- AlexNet
- VGG16
- ResNet18

# Run code
-  Classify uploaded images command line

`$ sh run_models_batch_uploaded.sh --dir pet_images --arch vgg|alexnet|resnet --dogfile dognames.txt`

-  Classify default images command line

`$ sh run_models_batch.sh --dir pet_images --arch vgg|alexnet|resnet --dogfile dognames.txt`

- Help with arguments 

`$ sh run_models_batch_uploaded.sh --help`

#Results Of The Classification Of The Uploaded Images
## Image file: Teddy_01.JPG

![Teddy_01.JPG](https://github.com/FtimaBen/Pet_Dogs_Classifier/blob/Submit-classifier-not-reviewed/uploaded_images/Teddy_01.JPG)

###VGG16
1. 	True label: **teddy**	 Predicted label: **teddy, teddy bear**
2. 	This image is **not a dog** image.
3. 	The classifier perdicted it as **not a dog** image.
4. 	vgg prediction is **Correct**.

###ResNet18
1. 	True label: **teddy**	 Predicted label: **teddy, teddy bear**
2. 	This image is **not a dog** image.
3. 	The classifier perdicted it as **not a dog** image.
4. 	resnet prediction is **Correct**.

###AlexNet
1. 	True label: **teddy**	 Predicted label: **teddy, teddy bear**
2. 	This image is **not a dog** image.
3. 	The classifier perdicted it as **not a dog** image.
4. 	alexnet prediction is **Correct**.

## Image file: Dog_01.JPG

![Dog_01.JPG](https://github.com/FtimaBen/Pet_Dogs_Classifier/blob/Submit-classifier-not-reviewed/uploaded_images/Dog_01.JPG)

###VGG16
1. 	True label: **dog**	 Predicted label: **bow tie, bow-tie, bowtie**
2. 	This image **is a dog** image.
3. 	The classifier perdicted it as **not a dog** image.
4. 	vgg prediction is **False**.

###ResNet18
1. True label: **dog**	 Predicted label: **cowboy hat, ten-gallon hat**
2. This image **is a dog** image.
3. The classifier perdicted it as **not a dog** image.
4. resnet prediction is **False**.

###AlexNet
1. True label: **dog**	 Predicted label: **sombrero**
2. 	This image **is a dog** image.
3. 	The classifier perdicted it as **not a dog** image.
4. 	alexnet prediction is **False**.

## Image file: Gray_whale_01.JPG

![Gray_whale_01.JPG](https://github.com/FtimaBen/Pet_Dogs_Classifier/blob/Submit-classifier-not-reviewed/uploaded_images/Gray_whale_01.JPG)

###VGG16
1. - True label: **gray whale**	 Predicted label: **grey whale, gray whale, devilfish, Eschrichtius gibbosus, Eschrichtius robustus**
2. - This image is **not a dog** image.
3. - The classifier perdicted it as **not a dog** image.
4. - vgg prediction is **Correct**.

###ResNet18
1. 	True label: **gray whale**	 Predicted label: **grey whale, gray whale, devilfish, Eschrichtius gibbosus, Eschrichtius robustus**
2. 	This image is **not a dog** image.
3. 	The classifier perdicted it as **not a dog** image.
4. 	resnet prediction is **Correct**.

###AlexNet
1. True label: **gray whale**	 Predicted label: **grey whale, gray whale, devilfish, Eschrichtius gibbosus, Eschrichtius robustus**
2. This image is **not a dog** image.
3. The classifier perdicted it as **not a dog** image.
4. alexnet prediction is **Correct**.

## Image file: Dog_02.JPG

![Dog_02.JPG](https://github.com/FtimaBen/Pet_Dogs_Classifier/blob/Submit-classifier-not-reviewed/uploaded_images/Dog_02.JPG)

###VGG16
1. 	True label: **dog**	 Predicted label: **bow tie, bow-tie, bowtie**
2. 	This image **is a dog** image.
3. 	The classifier perdicted it as **not a dog** image.
4. 	vgg prediction is **False**.

###ResNet18
1. 	True label: **dog**	 Predicted label: **cowboy hat, ten-gallon hat**
2. 	This image **is a dog** image.
3. 	The classifier perdicted it as **not a dog** image.
4. 	resnet prediction is **False**.

###AlexNet
1. 	True label: **dog**	 Predicted label: **sombrero**
2. 	This image **is a dog** image.
3. 	The classifier perdicted it as **not a dog** image.
4. 	alexnet prediction is **FALSE**.

#Summary Uploaded Images
*Full summaries in folder : results_uploaded_images/*

| |Percentage VGG16| Percentage ResNet18 | Percentage AlexNet |
|---------------------|
| Pct match | 50.0% | 50.0% | 50.0% |
| Pct correct dogs | 0.0% | 0.0% | 0.0% |
| Pct correct breed | 0.0% | 0.0% | 0.0% |
| Pct correct notdogs | 100.0% | 100.0% | 100.0% |

#Summary Pet Images
*Full summaries in folder : results_images/*

| |Percentage VGG16| Percentage ResNet18 | Percentage AlexNet |
|---------------------|
| Pct match | 87.5% | 82.5% | 75.0% |
| Pct correct dogs | 100.0% | 100.0% | 100.0% |
| Pct correct breed | 93.33% | 90.0% | 80.0% |
| Pct correct notdogs | 100.0% | 90.0% | 100.0% |

#Conclusion and answered questions
Questions regarding Uploaded Image Classification:

1. Did the three model architectures classify the breed of dog in Dog_01.jpg to be the same breed? If not, report the differences in the classifications.

	**Answer: The three models could not classify the dog correctly because of the hat the dog was wearing.**

2. Did each of the three model architectures classify the breed of dog in Dog_01.jpg to be the same breed of dog as that model architecture classified Dog_02.jpg? If not, report the differences in the classifications.

	**Answer: The models gave the same wrong answer.**

3. Did the three model architectures correctly classify Animal_Name_01.jpg and Object_Name_01.jpg to not be dogs? If not, report the misclassifications.

	**Answer: Yes**

4. Based upon your answers for questions 1. - 3. above, select the model architecture that you feel did the best at classifying the four uploaded images. Describe why you selected that model architecture as the best on uploaded image classification.

	**Answer: The three models could not recognize the dog but recognized the hat**

**Conclusion: ** VGG16 gave the best results with the pet images but with uploaded images the models gave the same results.
