---
layout: page
title: Melanoma detection using a smartphone application
---

In the early of 2017, we started a project to develop a smartphone application to automatically detect melanoma. This project was the <a href="https://github.com/gabrielucelli" target="_blank" rel="noopener">Gabriel Ucelli's</a> undergraduate thesis, which you can check in this <a href="https://www.dropbox.com/s/trux54zl7y5kksd/proposta.pdf?dl=0" target="_blank" rel="noopener">link</a> (unfortunately, it's in Portuguese only). The <a href="https://www.inf.ufes.br/~rkrohling/" target="_blank" rel="noopener">Prof. Renato A. Krohling</a> was the advisor and I was the co-advisor of this work.

As we didn't have an own dataset, we used a public one provided by <a href="https://isic-archive.com/" target="_blank" rel="noopener">ISIC</a>. This dataset is composed of dermatoscopy images. You may see some samples below:

<a href="http://pachecoandre.com.br/wp-content/uploads/2018/07/ISIC_0024494.jpg"><img class="alignnone size-medium wp-image-429" src="http://pachecoandre.com.br/wp-content/uploads/2018/07/ISIC_0024494-300x225.jpg" alt="" width="300" height="225" /></a> <a href="http://pachecoandre.com.br/wp-content/uploads/2018/07/ISIC_0024467.jpg"><img class="alignnone size-medium wp-image-428" src="http://pachecoandre.com.br/wp-content/uploads/2018/07/ISIC_0024467-300x225.jpg" alt="" width="300" height="225" /></a> <a href="http://pachecoandre.com.br/wp-content/uploads/2018/07/ISIC_0024457.jpg"><img class="alignnone size-medium wp-image-427" src="http://pachecoandre.com.br/wp-content/uploads/2018/07/ISIC_0024457-300x225.jpg" alt="" width="300" height="225" /></a> <a href="http://pachecoandre.com.br/wp-content/uploads/2018/07/ISIC_0024386.jpg"><img class="alignnone size-medium wp-image-426" src="http://pachecoandre.com.br/wp-content/uploads/2018/07/ISIC_0024386-300x225.jpg" alt="" width="300" height="225" /></a>

The project's goal was quite simple: providing a deep model to detect melanoma and put it in a smartphone application. We tried different CNN models in order to solve the problem. We figured out that very deep models, like VGG, inception V3, GoogleNet, were not good options because the network may consume all smartphone memory. In addition, for this kind of network, the connection weights become a large file to save/load, which is not good for a smartphone as well. Thus, the best option we found was the <a href="https://ai.googleblog.com/2017/06/mobilenets-open-source-models-for.html" target="_blank" rel="noopener">mobileNet</a> [1], a CNN developed specially to work properly on smartphones. The mobileNet's trained model achieved the following performance:

<a href="http://pachecoandre.com.br/wp-content/uploads/2018/07/Screenshot_2018-07-17_15-34-36.png"><img class="alignnone wp-image-436" src="http://pachecoandre.com.br/wp-content/uploads/2018/07/Screenshot_2018-07-17_15-34-36-300x255.png" alt="" width="441" height="375" /></a>

Next, we deployed this model in the smartphone application. All trained models and discussion are described in the <a href="https://www.dropbox.com/s/trux54zl7y5kksd/proposta.pdf?dl=0" target="_blank" rel="noopener">thesis</a>.

The application was developed using Java and Kotlin. You can see some screenshots below:

<a href="http://pachecoandre.com.br/wp-content/uploads/2018/07/d01604fd-039d-4440-abed-5035dc524157.jpeg"><img class="alignnone size-medium wp-image-439" src="http://pachecoandre.com.br/wp-content/uploads/2018/07/d01604fd-039d-4440-abed-5035dc524157-169x300.jpeg" alt="" width="169" height="300" /></a><a href="http://pachecoandre.com.br/wp-content/uploads/2018/07/4163a0a5-60b3-4edc-83f8-6eb2b92f570a.jpeg"><img class="alignnone size-medium wp-image-438" src="http://pachecoandre.com.br/wp-content/uploads/2018/07/4163a0a5-60b3-4edc-83f8-6eb2b92f570a-169x300.jpeg" alt="" width="169" height="300" /></a>

First, we need to crop a region on the skin. Next, the app shows the probability to be a melanoma or others. In this case, this spot on my skin has 99,5% of chance, according to the model, to be others.

Nonetheless, we have a problem here. The network was trained using dermatoscopy images and I used the smartphone's camera to take the pic. In this case specifically, it works well. However, it's not the usual. The solution is to train the network using smartphone images. But, where can we find these images? Well, as far as we know, there's no public dataset for that. Thus, we started a <a href="http://pachecoandre.com.br/skin-cancer-detection/" target="_blank" rel="noopener">new project</a> to fulfill this gap.

In any case, this app was a proof of concept. It works well for dermatoscopy images. It was developed only for androids and you can download the .apk by <a href="https://drive.google.com/file/d/10sNEGhkci7OobqCXcO0FbENQVSWGU8qA/view?usp=sharing" target="_blank" rel="noopener">clicking in this link. </a>The source code is also available on <a href="https://github.com/gabrielucelli/Melanoma-Detector" target="_blank" rel="noopener">https://github.com/gabrielucelli/Melanoma-Detector</a>

[1] Howard, Andrew G., et al. "Mobilenets: Efficient convolutional neural networks for mobile vision applications." <i>arXiv preprint arXiv:1704.04861</i>(2017).