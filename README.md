# Julia parallel computing on hyperspectral image unmixing.  

This project was developed for a school project at IMT Atlantique.

## What does this project ?  

In this project, I deal with the so-called problem of **Hyperspectral Image Unmixing**.
The aim of this project was mainly to implement numerical methods of optimization in **Julia** using parallel computing.
Finally, I made comparisons of performances (time execution) between sequential and parallel executions.

## The Hyperspectral Image Unmixing

In this section I will describe briefly the optimization problem that I needed to resolve.

Given the endmembers matrix (estimated before) and spectral data of an image, I must compute the relative abundance matrix.

This problem can be translated to a constrained minimization of a function with two constraints : 

* non negativity
* each matrix's column sum equal to 1

I first resolve this problem with gradient descent algorithm with respect to only the first constraint. And then I resolve the problem with respect of the two constraints using Julia libraries for optimization.

## Source code 

You can follow along the project by opening up the [notebook](https://github.com/thibaultspriet/hyperspectral_image_unmixing/blob/master/projectNotebook.ipynb).
In this notebook, you will be able to see the source code and also the explanations (in French 🇫🇷).

## Results

In this section, I will illustrate some of the results of this work.

Firstly, this is the image I worked on :  

![base image](https://github.com/thibaultspriet/hyperspectral_image_unmixing/blob/master/src-img.png). 

In this image, we can identify four different materials that are : gravel, grass, soil and trees). This four materials are the so-called endmembers, and you can see in the following image their reflectance value given the spectral band :

![endmembers](https://github.com/thibaultspriet/hyperspectral_image_unmixing/blob/master/endmembers.png)  

Finally you can see (on the left picture) the 4 abundance matrixs in which we can spot the 4 endmembers and (on the right) a comparison of time executions.  

Abundance Matrix             |  Time executions comparisons
:-------------------------:|:-------------------------:
![abundance](https://github.com/thibaultspriet/hyperspectral_image_unmixing/blob/master/abundance.png)  |  ![time execution](https://github.com/thibaultspriet/hyperspectral_image_unmixing/blob/master/time-execution.png)

## Working with the project

For those of you that are really interested, you can fork and/or download the project. To be able to run the project, you will need to have a **Julia** support and download some of its libraries.
I will not go in details about installation but you can find all information on the [official website](https://julialang.org).  

## Keep in touch

If you have any questions, I will be very happy to answer (in English or French 😄) : 
 * 📧 : thibaultspriet@outlook.fr
 * 🤝 : [/thibault-spriet](https://www.linkedin.com/in/thibault-spriet/)  
 
Feel free to open up an issue and/or send a pull request.
