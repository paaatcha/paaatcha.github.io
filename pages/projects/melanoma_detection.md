---
layout: page
title: Melanoma detection using a smartphone application
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

In early 2017, we started a project to develop a smartphone application to automatically detect melanoma. This project was the <a href="https://github.com/gabrielucelli" target="_blank" rel="noopener">Gabriel Ucelli’s</a> undergraduate thesis, which you can check in this <a href="https://www.dropbox.com/s/trux54zl7y5kksd/proposta.pdf?dl=0" target="_blank" rel="noopener">link</a> (unfortunately, it’s in Portuguese only). The <a href="https://www.inf.ufes.br/~rkrohling/“ target=”_blank" rel="noopener">Prof. Renato A. Krohling</a> was the advisor and I was the co-advisor of this work.

As we didn't have our own dataset, we used a public one provided by <a href="https://isic-archive.com/" target="_blank" rel="noopener">ISIC</a>. This dataset is composed of dermoscopy images. You may see some samples below:

{% include gallery id="skin" layout="half" %}

The project’s goal was quite simple: designing a deep lerning model to detect melanoma and embed it in a smartphone application. We tried different CNN models in order to solve this problem. We figured out that very deep models, like VGG, inception V3, GoogleNet, were not good options because the network may consume all smartphone memory. In addition, for this kind of network, the connection weights become a large file to save/load, which is not good for a smartphone as well. Thus, the best option we found was the <a href=“https://ai.googleblog.com/2017/06/mobilenets-open-source-models-for.html” target=“_blank” rel=“noopener”>mobileNet</a> [1], a CNN developed specially to work properly on smartphones. The mobileNet’s trained model achieved the following performance:

{% include gallery id="cm" %}

Next, we deployed this model in the smartphone application. All trained models and discussion are described in the <a href="https://www.dropbox.com/s/trux54zl7y5kksd/proposta.pdf?dl=0" target="_blank" rel="noopener">thesis</a>.

The application was developed using Java and Kotlin. You can see some screenshots below:

{% include gallery id="app" layout="half" %}

First, we need to crop a region on the skin. Next, the app shows the probability to be a melanoma or others. In this case, this spot on my skin has 99,5% of chance, according to the model, to be others.

Nonetheless, we have a problem here. The network was trained using dermoscopy images and we used the smartphone's camera to take the pic. In this case specifically, it works well. However, it's not the usual. The solution is to train the network using smartphone images. But, where can we find these images? Well, as far as we know, there's no public dataset for that. Thus, we started a <a href="http://pachecoandre.com.br/skin-cancer-detection/" target="_blank" rel="noopener">new project</a> to fulfill this gap.

In any case, this app was a proof of concept. It works well for dermoscopy images. It was developed only for androids and you can download the .apk by <a href="https://drive.google.com/file/d/10sNEGhkci7OobqCXcO0FbENQVSWGU8qA/view?usp=sharing" target="_blank" rel="noopener">clicking in this link. </a>The source code is also available on <a href="https://github.com/gabrielucelli/Melanoma-Detector" target="_blank" rel="noopener">https://github.com/gabrielucelli/Melanoma-Detector</a>

However, it is important to note that we do not intend to release such an app for general users. As mentioned, it was just a proof of concept. Our goal now is to help clinicians to improve the skin cancer diagnosis in particular in Brazil’s countryside.

[1] Howard, Andrew G., et al. "Mobilenets: Efficient convolutional neural networks for mobile vision applications." <i>arXiv preprint arXiv:1704.04861</i>(2017).