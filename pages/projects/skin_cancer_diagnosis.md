---
layout: page
title: Skin cancer diagnosis based on images acquired from smartphones and patient clinical information
---

Here I describe the skin cancer project that I'm leading in my Lab. The main goal of my Ph.D. is to provide algorithms to handle this problem. I'm gonna describe everything we developed and what we are doing right now. But first, you may want to know how all of this started. So, it's described <a href="http://pachecoandre.com.br/melanoma-detection-using-a-smartphone-application/" target="_blank" rel="noopener">here</a>.
<h3>Motivation</h3>
Skin cancer is the most common dysplasia around the world. Currently, around 3 million skin cancers occur globally each year [1]. In Brazil, it is one of the most serious public health issues. According to the Brazilian Cancer Institute [2], the skin cancer accounts for 33% of all cancer diagnoses in the country. This is the highest diagnosis rate among all kind of cancer. Further, over the past decade, the skin cancer incidence increased 55% and for 2018-2019 it is expected 180 thousand new cases in the whole country. Nowadays, every hour a person dies in Brazil due to a skin cancer disease [2].

<span style="font-weight: 400;">In order to diagnosis the skin cancer, dermatologists screen the skin lesion using their experience to diagnosis it. However, there are different types of skin cancer and some of them are very hard to diagnosis even for a trained dermatologist. To increase their diagnosis reliability, they use a dermatoscope, a medical instrument that allows the visualization of the subsurface structures of the skin revealing lesion details in colors and textures. In addition, they also take into accounting some pieces of information about the patient's profile and lesion aspects, such as time of sun exposure, family ancestry, if the lesion bleeds or hurts, if it itches, among others. As Brazil is an economically emerging country, <strong>most of its countryside cities do not have dermatologists nor dermatoscopes available for general practitioners</strong>. Certainly, this issue delays and decreases the clinical diagnosis reliability. Thereby, an approach to automatically detect skin cancer that does not depend on dermatoscopy images is very desired, mainly for general practitioners and medical students. According to Ericsson mobility report [3], there are now more than four billion smartphones around the world. In Brazil, more than 130 millions of people, around 77% of the population, have their own smartphone [4]. Therefore, a computer-aided diagnosis (CAD) system embedded in smartphones seems to be a low-cost approach that may assist doctors and medical students to provide a more reliable skin cancer diagnosis mainly in emerging countries like Brazil</span>
<h3>Objective</h3>
The main goal of this project is to develop new methodologies to automatically diagnosis the skin cancer using images acquired from smartphone cameras and the clinical information related to the patient and the skin lesion. The focus will be on proposing a deep learning technique that is able to combine both images and clinical information. Moreover, we also aim to contribute to a web platform in order to open our acquired database for research purposes as well as getting the contribution of similar data from others researchers around the world. As far as we know, there is no public skin cancer images database taken from standard camera available for research. Thus, we want to fulfill this gap. Lastly, our long-term goal is to embed the algorithm developed in this project into a smartphone application in order to assist doctors and medical students to provide a faster and more reliable skin cancer diagnosis to the people. Therefore, we hope that in the future our application may reduce the impact of the dermatoscope's lack in many regions in Brazil.
<h3>Work description</h3>
There are some good works doing skin cancer detection for dermatoscopy images [5,6]. A public dataset of dermatoscopy images is provided by ISIC.  However, as stated before, most cities in Brazil don't have dermatoscope available. Therefore, we need to handle this issue and the first step is to obtain a dataset, since there's no public dataset of skin cancer images acquired from standard cameras. So, how can we obtain such dataset?

In the late of 2017, we started a partnership with the Dermatological Assistance Program (PAD) of the Federal University of Espírito Santo. This program, which was founded in 1989, provides medical assistance to low incoming people who can't afford with a private skin cancer treatment. Normally, once per month a group of dermatologists, plastic surgeon, and medical students go to the countryside cities to provide the medical care, which takes place over the whole weekend. On average, 300 people are seen by the doctors and students. First, the doctors promote the prevention phase. They talk with the population in order to teach them good practices to reduce the probability to get the skin cancer. Next, the patient's profile is collected by the students. In the following, this patient is led to the dermatologists, which screen the lesion and provide the diagnosis. These dermatologists are extensively trained and are able to provide the diagnostic with high confidence. Finally, if the patient's lesion is at an advanced level, he/she is led to the plastic surgeon to proceed with a surgical process. In this case, this lesion needs to be removed and sent to the biopsy process. On the other hand, if the lesion isn't that bad, the patient is led to a treatment less invasive, for example, using some specific medicine on the skin. <strong>Therefore, since 1989, thousands of lives were saved through this program, which provides a full treatment, from the screening to the surgical process.</strong>

Recently, a Brazilian TV news broadcast produced an amazing documentary about PAD. Obviously, it is in Portuguese, but you can activate the translate in youtube if you can't understand the language.

<iframe src="https://www.youtube.com/embed/5nwDBwNCrR0" width="315" height="315" frameborder="0" allowfullscreen="allowfullscreen"></iframe>

&nbsp;

By means of our partnership, we developed a system to collect and store all patient's profile, as well as the skin lesion images acquired from smartphones. Our system is composed of two main parts. The first one is the server. It was built in Java (back-end and front-end) and plays the role of storing and presenting all patient's data. Below you can see some screenshots of the system (you also <a href="http://labcin1.ufes.br" target="_blank" rel="noopener">can access this system</a>, however, as it contains sensible data, only allowed people can use that).

<a href="http://pachecoandre.com.br/wp-content/uploads/2018/07/1.png"><img class="alignnone size-medium wp-image-396" src="http://pachecoandre.com.br/wp-content/uploads/2018/07/1-300x155.png" alt="" width="300" height="200" /></a> <a href="http://pachecoandre.com.br/wp-content/uploads/2018/07/3.png"><img class="alignnone size-medium wp-image-398" src="http://pachecoandre.com.br/wp-content/uploads/2018/07/3-300x144.png" alt="" width="300" height="144" /></a> <a href="http://pachecoandre.com.br/wp-content/uploads/2018/07/2.png"><img class="alignnone size-medium wp-image-397" src="http://pachecoandre.com.br/wp-content/uploads/2018/07/2-300x120.png" alt="" width="300" height="120" /></a>

In order to send information to the web system, we developed a smartphone application, for both Android and iPhone. Through this app, the doctors and students take the photos of the skin lesion, fulfill some questions about the patient and send everything to the web server. Below, you can see some pics of our app. Actually, you can <a href="https://play.google.com/store/apps/details?id=ufes.pad.app&amp;hl=es_DO" target="_blank" rel="noopener">download</a> it if you want, but it works only on a local network.

<a href="http://pachecoandre.com.br/wp-content/uploads/2018/07/4.png"><img class="alignnone size-medium wp-image-400" src="http://pachecoandre.com.br/wp-content/uploads/2018/07/4-169x300.png" alt="" width="169" height="300" /></a> <a href="http://pachecoandre.com.br/wp-content/uploads/2018/07/5.png"><img class="alignnone size-medium wp-image-401" src="http://pachecoandre.com.br/wp-content/uploads/2018/07/5-169x300.png" alt="" width="169" height="300" /></a> <a href="http://pachecoandre.com.br/wp-content/uploads/2018/07/6.png"><img class="alignnone size-medium wp-image-402" src="http://pachecoandre.com.br/wp-content/uploads/2018/07/6-169x300.png" alt="" width="169" height="300" /></a>

Below, you can also check some sample of images from our dataset. As you can note, they are quite different from the <a href="https://challenge2018.isic-archive.com/" target="_blank" rel="noopener">dermatoscopy ones.</a>

<a href="http://pachecoandre.com.br/wp-content/uploads/2018/07/706-9021-6665-1238_1523738473945.jpg"><img class="alignnone wp-image-454" src="http://pachecoandre.com.br/wp-content/uploads/2018/07/706-9021-6665-1238_1523738473945.jpg" alt="" width="175" height="175" /></a> <a href="http://pachecoandre.com.br/wp-content/uploads/2018/07/706-2065-6021-8564_1523738321142.jpg"><img class="alignnone wp-image-453" src="http://pachecoandre.com.br/wp-content/uploads/2018/07/706-2065-6021-8564_1523738321142-300x300.jpg" alt="" width="174" height="174" /></a> <a href="http://pachecoandre.com.br/wp-content/uploads/2018/07/702-9025-1371-3772_1533412016927.jpg"><img class="alignnone wp-image-452" src="http://pachecoandre.com.br/wp-content/uploads/2018/07/702-9025-1371-3772_1533412016927-300x300.jpg" alt="" width="175" height="175" /></a> <a href="http://pachecoandre.com.br/wp-content/uploads/2018/07/700-9009-8447-2599_1523738293975.jpg"><img class="alignnone wp-image-451" src="http://pachecoandre.com.br/wp-content/uploads/2018/07/700-9009-8447-2599_1523738293975-300x300.jpg" alt="" width="175" height="175" /></a> <a href="http://pachecoandre.com.br/wp-content/uploads/2018/07/708-7041-2493-7893_1534513357093.jpg"><img class="alignnone wp-image-450" src="http://pachecoandre.com.br/wp-content/uploads/2018/07/708-7041-2493-7893_1534513357093-297x300.jpg" alt="" width="175" height="177" /></a>

From the images above, we can note that developing an approach to automatically detect the skin cancer using them is a very challenging task. We have to handle a plenty of problems, among them:
<ul>
 	<li><span style="font-weight: 400;">The smartphone images present high variability caused by lighting, zoom, camera model, ink markings, etc.</span></li>
 	<li>The number of images available for this task is limited. The data collection is going on.</li>
 	<li>The number of samples for each type of skin cancer is very imbalanced</li>
</ul>
Thereby, in order to tackle those challenges, we complement the image data with 26 different patient clinical features, such as age, the lesion region, and size, the patient daily habits, family ancestry etc. Therefore, each skin lesion in our dataset has an image and its related clinical data. That is what the dermatologists do, they do not trust only on the screening, they also use the patient clinical information in order to provide a more trustable diagnostic. In this sense, we believe we cannot waste this clinical information, but include it into the recent developments in order to improve even more the diagnosis.

Currently, the convolutional neural network (CNN) has proved to be the most appropriate technique to address the skin cancer detection [7]. So, we are working in aggregation methodologies to include the patient clinical data and the image into the network. In addition, we are also investigating additional techniques, such as the Restricted Boltzmann Machine (RBM), Autoencoders and Generative Adversarial Networks in order to tackle those problematic aspects of our project.

A remarkable advantage of this project is that we're very close to the dermatologists. Different works handle the skin cancer detection, however, using only the Computer Science's point of view. In our case, we know exactly what the doctors need. Moreover, we're continuously learning about the small details of this task. For example, we've learned the skin cancer has preferred body regions, that is, two moles/spot may have the same characteristics, however, the diagnostic depends on the body's region. Therefore, this kind of information is very hard to obtain if we aren't in touch with the doctors.

&nbsp;

<hr />

<h3>References</h3>
[1]  WHO. How common is the skin cancer? 2018. World Health Organization (WHO). Available on http://www.who.int/uv/faq/skincancer/en/index1.html.

<span style="font-weight: 400;">[2]  National Institute of Cancer José Alencar Gomes (INCA). “The cancer incidence in Brazil”. (2018, May 4). Retrieved from </span><a href="http://www.inca.gov.br/estimativa/2018"><span style="font-weight: 400;">http://www.inca.gov.br/estimativa/2018</span></a><span style="font-weight: 400;">.</span>

[3]  Ericsson. Ericsson mobility report. Stockholm, Sweden, 2017. Available on https://www.ericsson.com/assets/local/mobility-report/documents/2017/ericsson- mobility-report-june-2017.pdf.

[4] IBGE. Internet and television access and smartphone possession for personal use. 2016. Brazilian Institute of Geography and Statistics Foundation. Available on https://biblioteca.ibge.gov.br/visualizacao/livros/liv101543.pdf.

<span style="font-weight: 400;">[5] Yu, Lequan, et al. "Automated melanoma recognition in dermoscopy images via very deep residual networks." IEEE transactions on medical imaging 36 (4), p. 994-1004, 2017.</span>

<span style="font-weight: 400;">[6]  Valle, Eduardo, et al. "Data, Depth, and Design: Learning Reliable Models for Melanoma Screening." arXiv preprint arXiv:1711.00441, 2017.</span>