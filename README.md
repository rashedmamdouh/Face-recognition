# Face Recognition Project

## Problem Statement

The goal of this project is to perform face recognition, which involves identifying the subject ID for a given image. The dataset consists of grayscale images, each of size 92x112, for 40 different subjects. The project involves the following steps:

1. **Download and Understand the Dataset: (ALREADY ATTACHMENT)**
   - Download the dataset from the provided URL: [ATT Database of Faces](https://www.kaggle.com/kasikrit/att-database-of-faces)
   - The dataset contains 10 images per subject, resulting in 400 images in total.

2. **Generate Data Matrix and Label Vector:**
   - Convert each image into a vector of 10304 values (92x112) corresponding to the image size.
   - Stack the 400 vectors to create a single Data Matrix (D) and generate the label vector (y). Labels range from 1 to 40, corresponding to the subject ID.

3. **Split the Dataset into Training and Test Sets:**
   - Split the Data Matrix D into training and test sets such that:
     - Odd rows are kept for training.
     - Even rows are kept for testing.
   - This results in 5 instances per person for both training and testing.
   - Split the label vector accordingly.

4. **Classification using PCA (Principal Component Analysis):**
   - Compute the projection matrix U using PCA with different values of alpha (e.g., 0.8, 0.85, 0.9, 0.95).
   - Project the training and test sets separately using the same projection matrix.
   - Utilize a simple classifier, such as the first Nearest Neighbor, to determine class labels.
   - Report the accuracy for each alpha value separately.

5. **Classifier Tuning using K-Nearest Neighbors (KNN):**
   - Adjust the number of neighbors in the K-NN classifier to 1, 3, 5, and 7.
   - Plot or tabulate the performance measure (accuracy) against the K value. This analysis applies to both PCA and non-PCA scenarios.

6. **Experimentation and Comparison:**
   - Explore different training and test split scenarios, such as using 7 instances per subject for training and 3 instances per subject for testing.
   - Compare the results obtained in these scenarios with those from the 50% split.
   - Experiment with different classifiers to fine-tune the algorithm.

The objective of this project is to achieve accurate face recognition and explore various techniques, including PCA and KNN, to optimize the recognition process.

**Note:** Make sure to download and preprocess the dataset as mentioned in step 1 and 2 before proceeding with the rest of the project.
