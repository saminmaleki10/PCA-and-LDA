# PCA-and-LDA
Face recognition using Yale B Face Database


The script is divided into two parts:

# Part A

Take each 50 × 50 pixels training image and vectorize it into a 2500-dimensional vector. 

Then perform principal component analysis (PCA) on the entire set of image vectors to 
obtain the first d principal components. The d eigenvectors (when converted back to 
images) are the Eigenfaces.

For each of the training images, project to the d-dimensional Eigenspace. Once this 
is done, classification should be performed by nearest neighbor with the Euclidean distance
metric in the Eigenspace.

Evaluate the algorithm on the frontal pose of the ten people in the Yale B Face Database. 
From the set of all ten individuals, 5 subsets are considered, indexed as below: 

i. Set 1. person*_01.png to person*_07.png 

ii. Set 2. person*_08.png to person*_19.png 

iii. Set 3. person*_20.png to person*_31.png 

iv. Set 4. person*_32.png to person*_45.png 

v. Set 5. person*_46.png to person*_64.png

Train the Eigenface algorithm with d = 9 and d = 30 on all images in subset 1 (70 images). 
Then, evaluate the algorithm on subsets 1-5.

# Part B

For this part we will extend the Eigenface algorithm to perform the LDA algorithm. 

Extend the Eigenface implementation by, first, projecting the training images via 
Eigenfaces to a “𝑛 – 𝑐” dimensional space, and second, applying Fisher’s LDA to obtain 
“c – 1” dimensional feature vector for each image. (Note: 𝑛 is the total number of samples
and 𝑐 is the number of classes)

Evaluate the LDA algorithm similar to before. Train LDA algorithm with c = 10 on 
all images in subset 1, and classify subsets 1-5 as we did in Part A.

