# AI diet management based on recommended daily intake

Food Calorie Automatic Calculation Service

<br/>

## 1. Background & Purpose

- When a user takes a picture and uploads it, calories are calculated based on the recommended daily intake
- Plan to write a thesis by adding a service that recommends new foods based on insufficient nutritional information

<br/>

## 2. Organizer/Supervisor & Team Members

- Organizer/Supervisor: BOAZ, Korea’s first big data association
- Team members: 3 other students

<br/>

## 3. Project Duration

- 2022.03. ~ 2022.05. (3 months)

<br/>

## 4. Project Introduction

<img src='https://user-images.githubusercontent.com/75362328/212490413-bec8a077-b588-4d0e-808b-bec592dad31f.png' width='100%' height='80%'>

As interest in weight management and eating habits has increased due to the prolonged COVID-19, we propose a simple and sustainable food detection and nutritional analysis service using AI. This allows ordinary people who are not experts to know the type of food, nutritional components and calories, and can provide a useful service to people who are on a diet or managing their weight.

Among AI Hub’s ‘Nutrition Analysis for Health Management and Food Image for Dietary Management’ data set, **12 categories of labels that people usually eat were selected**. This data set consists of source data, labeling data, and energy tables, so total energy (kcal) could be obtained through carbohydrates, proteins, and fats. In addition, by using the nutritional components of the ‘integrated food nutritional component DB’, a total of eight nutritional meta-information for one serving per person was calculated and constructed.

In the detector, the bounding box was well caught, but the performance of the multi food classification part was not good, so after learning the classifier first, I tried to learn it by bringing the classifier from the detector to the backbone. Therefore, when food images came in as input, **Inception v3 model pre-trained Backbone model** was developed. In other words, the model learned from Food Image Classifier was used as a pre-trained model to learn the classifier.

Food Detection uses **Fast R-CNN model** to detect food of various sizes well. The food detected through this will calculate the calories and print it out based on the nutritional content labeling standards of the Ministry of Food and Drug Safety. In the process, to prevent overfitting, we proposed a partial augmentation (augmentation only for a specific class) method that augments data only for classes with low performance, and it was confirmed that this method is efficient in terms of time/memory. We plan to write a thesis by adding a service that estimates the amount of food and **provides customized nutritional information of food amount**.

<br/>

## 5. Role in charge of the project

- Data set construction & pre-processing based on the integrated food nutritional component DB
- Development of Pre-trained Model using Inception Block
- UFC (Food Detection) model training and optimization
- Performance comparison and experimentation using new methodologies such as Partial Augmentation

<br/>

## 6. Presentation Materials

[Final Presentation on Diet Management](https://drive.google.com/file/d/1WHLYcqsBX77WnHvQ3lNthGz2nd195Wj3/view)
