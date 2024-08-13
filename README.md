# MHISTwithNNs

Computer Vision Project Requirements

Gastrointestinal Images Classification
Cancer Detection
Objectives:

    Train different neural network architectures from scratch.
    Learn about different performance measures for unbalanced data.
    Experience approaches to balance a dataset for training.
    Apply transfer learning from a deep neural network model.

Dataset description:

    Paper: A Petri Dish for Histopathology Image Analysis (https://arxiv.org/abs/2101.12355).

    GitHub link: https://bmirds.github.io/MHIST/

    Description: MHIST is minimalist in that it comprises a straightforward binary classification task of fixed-size colorectal polyp images, a common and clinically significant task in gastrointestinal pathology. MHIST contains 3152 fixed-size images, each with a gold-standard label determined from the majority vote of seven board-certified gastrointestinal pathologists, that can be used to train a baseline model without additional data processing. MHIST is not an equally balanced dataset that contains different numbers of images per class: (a) 2162 images per class HP: hyperplastic polyp (benign), (b) 990 images per class SSA: sessile serrated adenoma (precancerous).

    Availability: Publicly available (for academic purposes).

    Resources needed: CPU

    Data size: 2175 train data + 977 test data.

 
Requirements:

    Preprocessing of the data and data augmentation before training.
    Train three different neural network architectures from scratch.
        Fully Connected Network.
        CNN network.
        Vision Transformer.


    Choosing the number of layers, neurons, and other hyperparameters is left for you to experiment with their effect on the performance. Keep in mind that the dataset is unbalanced, so you would need metrics to evaluate the training other than training accuracy. Include the sensitivity, specificity, recall, precision, and F1 score metrics for the training and testing results.  During the train-test-split at the beginning, make sure the training and testing data follow the same unbalanced distribution. You would need to provide a graph showing all the training and testing measures across all epochs. Don’t try to balance the training set at this state. Finally, compare between all the three models and comment on their performance for this unbalanced task.

    Repeat part (3) using the same network architectures after balancing the training set. Remember that we only balance the training set and leave the testing set as is. If you balance the training set, you can rely on the accuracy this time along with other measures. Please try at least two balancing techniques and comment on their effectiveness in the process. These techniques could be Random Under Sampling, Random Over Sampling, SMOTE oversampling, Borderline Oversampling with SVM, and Adaptive Synthetic Sampling (ADASYN).


    For this part, we would like to explore the effect of transfer learning on this dataset. Therefore, please finetune a pre-trained neural network, for example, ResNet18 and ResNet50, on the given dataset. Use the balanced dataset from the best balancing technique you found. Then, load the pre-trained network (preferably pre-trained on ImageNet). Train that network for a few epochs on the balanced dataset and test it using the test set. Finally, compare the results of this network with the best network from part (4) and comment on the effectiveness of transfer learning on real-life applications.
