# Image-Classification


Description
Identify different types of cell nuclei in a colon cancer sample
Overall Goal
Colon cancer is the 3rd most common cancer in the world.

The normal colon has projections known as villi which absorb food and appear as circles of cells on a microscope image of the tissue (since the villi are cut through):
Histopathology image of early colon cancer.

The cell nuclei of these images can be segmented and coloured according to the different cell types:
Image segmented according to cell type.
(Orange cells are normal, red cells are cancer, green cells are immune cells invading to help, and blue cells are connective tissue.)

The following image shows a worse grade of colon cancer where you can see that the circles of normal cells have disintegrated and the nuclei have become larger and less well formed (due to DNA damage):
More advanced colon cancer with cell types indicated.

Digital pathology aims to apply machine learning to digital pathology images like these to determine if the tissue is normal or cancerous. One approach is to segment out the nuclei of cells from these images and classify them into different cell types including malignant cell nuclei (i.e. cancerous cells).

Your overall goal for this data science task is to train a deep neural network which can take a 64x64 image with a cell nuclei at the centre and classify it into one of the following types which are shown in the figures above:

Normal epithelial cells (shown orange).
Cancer epithelial cells (shown in red).
Immune Leukocyte cells (shown in green).
Connective fibroblast cells (shown in blue).
The “Deep Learning for MSc Coursework 2021” Kaggle site has a training set of nuclei images (train.zip) and also a csv training file containing their identities (train.csv). It also contains test archive (test.zip) which has similar 64x64 images of unlabelled cell nuclei. (Note that the identity of each image is given by its number 'N.png'. This then corresponds to its identity in the csv files.)

You may notice that the classes in the training file are unbalanced with 'Normal' cells being in the minority. However, the testing file is balanced with roughly equal numbers of each cell type. So accuracy is an appropriate metric and this will be used. But you will have to think about how you handle the unbalanced training set.

There is a cell nuclei in the middle of each image. Your overall goal is to develop a deep learning method that can predict the cell type of the images in the test.zip file. You can make multiple submissions each day to the Kaggle site and they will be scored using a portion of the test data.

So you need to submit a 'test.csv' file where the first column is the identifier of the test image and the second column is your predicted cell type given as one of the class identifiers used in the train.csv file (and also given in bold above).

Submission
Please submit the results of your method (test.csv) to the Kaggle site. This will be tested and the accuracy on the unseen test set will be given. You can use a pseudonym on the Kaggle site if you do not wish to reveal your real name to be revealed in this competition. You can make multiple submissions per day to assess what might be the best approach. The leaderboard table will show the score of your best submission and this will constitute 15 marks of the total coursework score of 20 marks (this will be based on getting a score better than particular thresholds rather than a direct conversion of accuracy score !)

ALSO submit your final Jupyter workbook for this result to Moodle (this can be exported from Colab if you are using this). This submission file should be named the same as your Kaggle identifier (with spaces replaced with underscores). So if you are using a Kaggle identifier "Dogs versus Cats" - then you should submit your Jupyter notebook file to Moodle as "Dogs_versus_Cats.ipynb" file. (There is no need to identify yourself in this file since Moodle will associate the file uploaded with your user account.)

These Jupyter notebooks will be marked depending on what you have written to provide instruments and visualizations for you to understand and optimize the training process (i.e. confusion matrices, learning curves, etc.) and the level of annotation of the laboratory notebook to explain what you have done. This will constitute 5 marks of the total coursework score of 20 marks.

Evaluation
Submissions will be assessed using class accuracy. ## Submission Format
Submitted files should should contain a header and have the following format:

Id,  Type
500, Normal
501, Normal
502, Cancer
503, Connective
504, Immune
etc.
Citation
Kevin Bryson. (2021). Deep Learning for MSc Coursework 2021. Kaggle. https://kaggle.com/competitions/deep-learning-for-msc-coursework-2021
