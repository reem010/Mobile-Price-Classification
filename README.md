# Mobile-Price-Classification

## Abstract
This study employs Particle Swarm Optimization (PSO) with a Decision Tree classifier to classify mobile phone prices based on specifications. Through data preprocessing and iterative PSO-based feature selection, the model accurately identifies key features influencing prices. Leveraging PSO's optimization capabilities, the approach achieves high classification accuracy, offering actionable insights for stakeholders in the mobile phone industry.

## Introduction
Mobile price classification is a common task in the field of machine learning where the goal is to build a predictive model that can classify mobile phones into different price ranges based on their features and specifications. The classification model aims to automate the process of determining the price category of a mobile phone, which can be useful for both consumers and sellers in making informed decisions. It provides valuable insights for consumers, helping them compare and make decisions based on estimated price ranges. For sellers, these models assist in determining competitive pricing strategies and understanding market dynamics.

## Dataset
The mobile price classification dataset serves as a valuable resource for training machine learning models to predict the price range of mobile phones based on their specifications, enabling stakeholders in the mobile phone industry to make informed decisions regarding pricing, marketing, and product development.

### Features
The dataset includes attributes or features of mobile phones, such as battery capacity, RAM, internal storage, screen size, camera specifications (e.g., megapixels), operating system, brand, processor speed, and connectivity options (e.g., 3G, 4G, Wi-Fi).

The data features are as follows:
1. `battery_power`: Total energy a battery can store in one time measured in mAh.
2. `blue`: Has bluetooth or not.
3. `clock_speed`: Speed at which microprocessor executes instructions.
4. `dual_sim`: Has dual sim support or not.
5. `fc`: Front Camera mega pixels.
6. `four_g`: Has 4G or not.
7. `int_memory`: Internal Memory in Gigabytes.
8. `m_dep`: Mobile Depth in cm.
9. `mobile_wt`: Weight of mobile phone.
10. `n_cores`: Number of cores of processor.
11. `pc`: Primary Camera mega pixels.
12. `px_height`: Pixel Resolution Height.
13. `px_width`: Pixel Resolution Width.
14. `ram`: Random Access Memory in Mega Bytes.
15. `sc_h`: Screen Height of mobile in cm.
16. `sc_w`: Screen Width of mobile in cm.
17. `talk_time`: Longest time that a single battery charge will last.
18. `three_g`: Has 3G or not.
19. `touch_screen`: Has touch screen or not.
20. `wifi`: Has wifi or not.
21. `price_range`: This is the target variable with value of 0 (low cost), 1 (medium cost), 2 (high cost), and 3 (very high cost).

The dataset consists of 2 files: training and test datasets:
- Train Data Length: 2000
- Test Data Length: 1000

The train data has 4 classes: [0, 1, 2, 3]

[Kaggle Dataset Link](https://www.kaggle.com/datasets/iabhishekofficial/mobile-price-classification/data?select=train.csv)

## Methodology
The methodology involves optimizing feature selection through PSO, training a Decision Tree classifier on the selected features.

### Data Preprocessing
The code reads and preprocesses the training and test datasets, handling encoding and dropping irrelevant columns.

### PSO-Based Feature Selection
The PSO algorithm is utilized to select the optimal subset of features from the training data. The PSO algorithm initializes particles representing different feature subsets and iteratively updates their positions based on fitness evaluation. Fitness evaluation is performed using a Decision Tree classifier, where the fitness of each particle is determined by its classification accuracy.

### Model Training and Testing
Once the optimal feature subset is selected using PSO, the Decision Tree classifier is trained on the selected features. The trained model is then used to make predictions on the training data. The accuracy of the trained model is calculated using a custom accuracy function.

### Results Evaluation
The code outputs the training accuracy of the Decision Tree classifier, providing an indication of the model's performance in classifying mobile phone prices.
