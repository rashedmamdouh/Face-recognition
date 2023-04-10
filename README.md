Face recognition
Problem Statement
We intend to perform face recognition. face recognition means that for a given image you
can tell the subject id. Our database of subjects is very simple. It has 40 subjects. Below we
will show the needed steps to achieve the goal of the assignment.

1. Download the dataset and understand the format (10 Points)
   a. URL dataset is available at the following link.
   https://www.kaggle.com/kasikrit/att-database-of-faces
   b. The dataset has 10 images per 40 subjects. Every image is a grayscale image of
   size 92x112.
2. Generate the Data Matrix and the Label vector (20 Points)
   a. Convert every image into a vector of 10304 (92x112) values
   corresponding to the Image Size.
   b. Stack the 400 vectors into a single Data Matrix D and generate the label
   vector y. The labels are integers from 1:40 corresponding to the subject
   id.
3. Split the Dataset into Training and Test sets  
   (not split randomly, as I might end with a whole class/subject in the test set that the
   model never saw in the training set)
   a. From the Data Matrix D (400x10304) keep the odd rows for training
   and the even rows for testing. This gave me 5 instances per person
   for training and 5 instances per person for testing.
   b. Split the label vector accordingly.

4. Classification using PCA.
   a. Use the pseudo-code below for computing the projection matrix U. Define the
   alpha ={0.8,0.85,0.9,0.95}
   b. Project the training set and test sets separately using the same projection matrix.
   c. Use a simple classifier (first Nearest Neighbor to determine the class labels).
   d. Report Accuracy for every value of alpha separately.

5. Classifier Tuning using KNN
   a. Set the number of neighbors in the K-NN classifier to 1,3,5,7.
   b. Plot (or tabulate) the performance measure (accuracy) against the K value. This is to be
   done for PCA as well.

6. a. Use different Training and Test splits. Change the
   number of instances per subject to 7 and keep 3 instances
   per subject for testing. compare the results I had with the
   ones I got earlier with a 50% split.
   b. Using a different classifier for tuning my algorithm.
