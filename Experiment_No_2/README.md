Title: Water Body Segmentation Using the Water Segmentation Dataset

Dataset: Water Segmentation Dataset
Link: https://www.kaggle.com/datasets/gvclsu/water-segmentation-dataset
Topic: Semantic and Temporal Segmentation of Water Regions

Dataset Description
The Water Segmentation Dataset follows a DAVIS style structure and consists of:
● JPEGImages/480p/ – RGB input images grouped by scene
● Annotations/480p/ – Binary ground truth masks (water vs non water)
● ImageSets/Segmentation/ – Train, validation, and test splits
Some scenes (e.g., Houston) represent true temporal sequences, while others behave as
independent images.

Problem Statement
Develop a water segmentation system that can accurately classify each pixel in an image
as water or non water using the provided dataset. Optionally, analyze how temporal
information can improve segmentation quality in video like sequences.

Key Objectives
Your submission must cover the following stages:
1.Data Preparation
● Load images and corresponding ground truth masks from the dataset
● Resize images and masks to a fixed size
● Normalize pixel values to the range [0, 1]
● Encode mask labels as binary or one hot vectors (if required)
● Split the dataset into training, validation, and test sets
2. Model Selection and Architecture
You may choose any one of the following models:
A: Convolutional Neural Network (CNN)
● Convolutional layers for feature extraction
● Pooling layers for dimensionality reduction
● Fully connected (Dense) layers for prediction
B: Vision Transformer (ViT)
● Image patch embedding
● Transformer encoder blocks with self-attention
● Classification or segmentation head for final output
C: Generative Adversarial Network (GAN)
● Generator network to predict water masks
● Discriminator network to distinguish real vs predicted masks
● Adversarial training to improve segmentation quality
3. Training and Optimization
● Compile the selected model using:
○ Appropriate optimizer (Adam / SGD)
○ Suitable loss function (Binary Cross-Entropy / Dice Loss)
● Train the model using the training dataset
● Monitor performance on the validation dataset
4. Evaluation and Visualization
● Evaluate the trained model on the test dataset
● Measure performance using accuracy , IoU and Dice score
● Plot Training Accuracy vs Validation Accuracy over epochs
● Display sample input images with ground-truth and predicted masks
