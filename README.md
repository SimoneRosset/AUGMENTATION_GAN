# AUGMENTATION_GAN
CNN classification performance improvements on COVID-19 X-rays dataset, thanks to synthetic data augmentation.

**Abstract**
Large-scale annotated datasets have proven to be extremely important part that powers the convolutional neural networks (CNNs) and other deep learning methods. However, it has been observed that obtaining such an enormous dataset is quite challenging in certain domains.

Medical domain is one such area where obtaining an enormous number of images in order to train a classifier is highly challenging and practically inefficient. In this project we try to address the stated critical issue with the help of Generative Adversarial Networks (GANs). We demonstrate that GAN can be used to generate synthetic medical images when trained with even small number of available real images. Not only this the quality of synathetic images are quite high and thus can be used to augment the original training dataset for further Machine Learning applications. In order to validate the quality of generated images we train a classifier firstly using classical augmentation techniques (rotation, translation, flip and scale) on smaller dataset of real images. After that another classifier is trained but using real and synthetic images generated by GAN as training dataset. In the latter case we did not use any classical augmentation function. 

In this project we took inspiration from the work done by Maayan Frid-Adar et. al. in this paper: [*GAN-based Synthetic Medical Image Augmentation for increased CNN Performance in Liver Lesion Classification*](https://arxiv.org/pdf/1803.01229.pdf), and by Mohamed Loey et. al. and in this paper: [*Within the Lack of Chest COVID-19 X-ray Dataset: A Novel Detection Model Based on GAN and Deep Transfer Learning*](https://www.mdpi.com/2073-8994/12/4/651/pdf)

**Dataset**: [covid-chestxray-dataset](https://github.com/ieee8023/covid-chestxray-dataset)

4 classes


<p align="center" width="100%">
<img src="https://github.com/SimoneRosset/AUGMENTATION_GAN/blob/master/images/classes.png" alt="" width= '800px'/>
</p>

**Results**: [here](/results/)

We definitely achieved the high quality synthesis of chest X-ray scans using generative adversarial networks (GANs).

We designed a CNN-based solution for pneumonia infection classification task, with comparable results to state-of-the-art methods.

We demonstrated how synthetic augmentation of the CNN training set, using the generated synthetic data by GANs, highly improved classification results: the classification performance using only classic data augmentation yielded 82.7% sensitivity and 90.4% specificity. By adding the synthetic data augmentation the results increased to 90.6% sensitivity and 97.2% specificity.

We obtain an high total accuracy gain, from 0.827 to 0.907:

<p align="center" width="100%">
<img  src="https://github.com/SimoneRosset/AUGMENTATION_GAN/blob/master/images/tot_acc.png" alt="" width= '600px'/>
</p>


CNN classification performances with classic data augmentation:

<p align="center" width="100%">
<img src="https://github.com/SimoneRosset/AUGMENTATION_GAN/blob/master/images/best_classic.png" alt="" width= '800px'/>
</p>

CNN classification performances with synthetic (DCGAN generated) data augmentation:

<p align="center" width="100%">
<img src="https://github.com/SimoneRosset/AUGMENTATION_GAN/blob/master/images/best_synthetic.png" alt="" width= '800px'/>
</p>

Here the correspondent confusion matrix:

<p align="center" width="100%">
<img src="https://github.com/SimoneRosset/AUGMENTATION_GAN/blob/master/images/best_confusion_synthetic.png" alt="" width= '400px'/>
</p>

Training history (best - 0.907 total accuracy in 720 epochs on trainset made by 270 original images, 2000 classic and 1000 synthetic augmented):

<p align="center" width="100%">
<img src="https://github.com/SimoneRosset/AUGMENTATION_GAN/blob/master/images/best_history.png" alt="" width= '100%'/>
</p>

**Documentation**: [here](/report.pdf)

**Keywords**: Image synthesis, Convolutional Neural Network, Generative Adversarial Network, Data Augmentation. 
