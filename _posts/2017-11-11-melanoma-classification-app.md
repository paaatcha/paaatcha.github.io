---
title: "Melanoma detection using a smartphone application"
classes: wide
header:
  teaser: "assets/imgs/skin_cancer/17.jpeg"
categories:
  - Blog  
tags:
  - Projects
  - Machine Learning
  - Deep Learning
  - Health Informatics
  - TCC
  
app:
  - url: assets/imgs/skin_cancer/17.jpeg
    image_path: assets/imgs/skin_cancer/17.jpeg
    
  - url: assets/imgs/skin_cancer/18.jpeg
    image_path: assets/imgs/skin_cancer/18.jpeg

cm:
  - url: assets/imgs/skin_cancer/16.png
    image_path: assets/imgs/skin_cancer/16.png

skin:
  - url: assets/imgs/skin_cancer/12.jpg
    image_path: assets/imgs/skin_cancer/12.jpg
    
  - url: assets/imgs/skin_cancer/13.jpg
    image_path: assets/imgs/skin_cancer/13.jpg
    
  - url: assets/imgs/skin_cancer/14.jpg
    image_path: assets/imgs/skin_cancer/14.jpg
    
  - url: assets/imgs/skin_cancer/15.jpg
    image_path: assets/imgs/skin_cancer/15.jpg
---

In early 2017, we started a project at LABCIN-UFES to develop a smartphone application to classify melanoma. This project was the <a href="https://github.com/gabrielucelli" target="_blank" rel="noopener">Gabriel Ucelli’s</a> undergraduate thesis, which you can access via this <a href="https://www.dropbox.com/s/trux54zl7y5kksd/proposta.pdf?dl=0" target="_blank" rel="noopener">link</a> (in Brazilian Portuguese only). <a href="https://www.inf.ufes.br/~rkrohling/“ target=”_blank" rel="noopener">Prof. Renato A. Krohling</a> was the advisor, and I was the co-advisor of this work.

As we didn't have our own dataset, we used a public one provided by <a href="https://isic-archive.com/" target="_blank" rel="noopener">ISIC</a>. This dataset consists of dermoscopy images, and you can see some samples below:

{% include gallery id="skin" layout="half" %}

The project’s goal was straightforward: to design a deep lerning model to detect melanoma and embed it in a smartphone application. We tried different CNN models in order to solve this problem. 


We found that very deep models, like VGG, inception V3, GoogleNet, were not good options because the network may consume all smartphone memory. In addition, for this type of network, the connection weights become a large file to save and load, which is not suitable for a smartphone. Thus, the best option we found was the <a href=“https://ai.googleblog.com/2017/06/mobilenets-open-source-models-for.html” target=“_blank” rel=“noopener”>mobileNet</a> [1], a CNN developed specifically to work correctly on smartphones. The trained MobileNet model achieved the following performance:

{% include gallery id="cm" %}

Next, we deployed this model in the smartphone application. All trained models and discussion are described in the <a href="https://www.dropbox.com/s/trux54zl7y5kksd/proposta.pdf?dl=0" target="_blank" rel="noopener">thesis</a>.

The application was developed using Java and Kotlin. You can see some screenshots below:

{% include gallery id="app" layout="half" %}

First, we need to crop a region on the skin. Next, the app shows the probability of it being melanoma or something else. In this case, according to the model, this spot on my skin has a 99.5% chance of being something else.


However, we have a problem here. The network was trained using dermoscopy images, and we used the smartphone's camera to take the picture. In this specific case, it works well. However, it's not typical. The solution is to train the network using smartphone images. But where can we find these images? As far as we know, there is no public dataset for that. Thus, we started a new project to fill this gap that will be described soon.

**Update**: to learn more about this new project and how to contribute, please check this [post](/projects/skin_cancer_diagnosis/).
{: .notice--info}

In any case, this app was just a proof of concept. It works well for dermoscopy images and was developed only for Androids. You can download the `.apk` by <a href="https://drive.google.com/file/d/10sNEGhkci7OobqCXcO0FbENQVSWGU8qA/view?usp=sharing" target="_blank" rel="noopener">clicking on this link. </a>The source code is also available on <a href="https://github.com/gabrielucelli/Melanoma-Detector" target="_blank" rel="noopener">https://github.com/gabrielucelli/Melanoma-Detector</a>

However, it is important to note that we do not intend to release such an app for general users. As mentioned, it was just a proof of concept. Our goal now is to help clinicians to improve the skin cancer diagnosis in particular in Brazil’s countryside.


#### References
[1] Howard, Andrew G., et al. "Mobilenets: Efficient convolutional neural networks for mobile vision applications." <i>arXiv preprint arXiv:1704.04861</i>(2017).