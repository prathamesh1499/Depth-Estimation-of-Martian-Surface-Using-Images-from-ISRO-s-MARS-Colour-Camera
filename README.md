# Depth Estimation of Martian Surface using ISRO’s MARS Color Camera Images

# Published 
**Published in: 2021 2nd Global Conference for Advancement in Technology (GCAT)** - https://ieeexplore.ieee.org/document/9587677<br>
**Date of Conference:** 1-3 Oct. 2021<br>
**Date Added to IEEE Xplore:** 13 November 2021<br>
**ISBN Information:**<br>
Electronic ISBN:978-1-6654-1836-2 <br>
Print on Demand(PoD) ISBN:978-1-6654-3070-8<br>
**INSPEC Accession Number:** 21297225<br>
**DOI:** 10.1109/GCAT52182.2021.9587677<br>
**Publisher:** IEEE<br>
**Conference Location:** Bangalore, India<br>


## Authors
- [@Akash Khamkar](https://www.github.com/AkashKhamkar) <br>
- [@Arjun Pukale](https://www.github.com/ArjunPukale) <br>
- [@Prathamesh Joshi](https://www.github.com/prathamesh1499)


Proposing Pix2Pix model for image to image translation from Domain A (ISRO satellite image of Martian Surface) to Domain B (Corresponding Depth Image)<br>

<br>
<b>Abstract</b>
</br>
<br>Depth estimation from satellite images is a fundamental task when studying the terrain of a celestial body. Existing solutions for depth estimation often use datasets that include either images of an indoor scene or images related to (self-driving). This paper presents a Pix2pix type of neural network for computing the depth of the Martian surface using the images captured by ISRO’s Mars Orbiter. In this paper, we have implemented Pix2Pix (Generator Discriminator) architecture using two different loss functions- LSGAN and Vanilla loss functions and then compared their results to select a better loss function for computing accurate depth maps. We also created our own dataset using images provided by ISRO that contains 343 Training Images and 37 testing images.</br>

<br>Currently, the Indian Space Research Organization (ISRO) is carrying out various research projects regarding the planet Mars. Earlier, it deployed Mars orbiter in the year 2013 for collecting information which can be further used for conducting even more in-depth research about the planet’s topography, temperature, atmosphere, etc. </br>

One such research area that ISRO is currently focusing on is estimating the depths of various valleys, canyon systems of the Martian planet. As per the current scenario, one such method for estimating depths is using Lidar technology. 

We proposed a method where we use Generative Adversarial Networks to estimate such Depth Maps using just a single input image, without using hardwares like sterio, lidar, etc. This Depth Map can be further used for creating 3D models or simulations of the surface for researching and further planning of future missions.   
</br>

<br>
<b>Data Collection</b>
</br>
For this project currently there exists no specific dataset, which consists of both the satellite images and the depth maps, hence we created our own dataset for this project. 
<br>
The dataset we created consists of two type of images -<br>
&emsp;1. Satellite images which were taken from ISRO’s Mars Orbiter in different lighting conditions.<br>
&emsp;2. Depth image obtained from NASA’s MOLA map.<br>

<br>
<b>Data Preprocessing</b>
</br>
1. We gathered 1:1 identical pair of images from Isro satellite images and Nasa's Mola Depth Map respectively, along Valles Marineris canyon system at the map scale of 53km .<br>
2. A total of 38 images were collected which were captured by MOM at different intervals of time in its orbits. <br>
3. Each image was augmented to a set of 10 images thus reaching a total count of 380 images.<br>
4. Different augmentation techniques were used such as :<br>
&emsp;Resize<br>
&emsp;Rotate<br>
&emsp;Shift Scale<br>
&emsp;Center Crop<br>
&emsp;Horizontal flip<br>
&emsp;Vertical flip<br>
&emsp;Blur<br>
&emsp;Brightness<br>
&emsp;Contrasts<br>
&emsp;Hue Saturation<br> 
5. These images were randomly partitioned into training (343) & testing (37) .<br>
6. Each Training Image is of size 256x256.<br>



### Sample Pair Image<br>
![OUTPUT](./Images/sample_pair_image.jpg)

### Model Used:
We have used [<b>Pix2Pix</b>](https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix) model to solve this Task.<br>
![OUTPUT](./Images/pix2pix.png)
<br>
We have tested this model with two loss functions:
&emsp;1.Vanilla Gan Loss
&emsp;2.Lsgan Loss
<br>
## Results<br>
### Output:
![OUTPUT](https://github.com/prathamesh1499/Depth-Estimation-of-Martian-Surface-Using-Images-from-ISRO-s-MARS-Colour-Camera/blob/main/Images/comparison.jpg)<br>

### Loss Function vs Performance Metrics:
![OUTPUT](https://github.com/prathamesh1499/Depth-Estimation-of-Martian-Surface-Using-Images-from-ISRO-s-MARS-Colour-Camera/blob/main/Images/loss_func_vs_metrics.jpg)<br>

### Performance Metric Distribution:
![OUTPUT](./Images/Metric_dist.png)<br>

### References
```
@inproceedings{isola2017image,
  title={Image-to-Image Translation with Conditional Adversarial Networks},
  author={Isola, Phillip and Zhu, Jun-Yan and Zhou, Tinghui and Efros, Alexei A},
  booktitle={Computer Vision and Pattern Recognition (CVPR), 2017 IEEE Conference on},
  year={2017}
}
```
