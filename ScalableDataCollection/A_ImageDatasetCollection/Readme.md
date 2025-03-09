# Fruit Image Dataset
## Overview
The **Fruit Image Dataset** contains high-quality images of 20 different fruits, each categorized into its respective folder. The dataset includes metadata with details such as the category, image name, URL source, and resolution. This dataset is ideal for machine learning tasks such as image classification, object detection, and computer vision applications.

## Dataset Name
**FruitVision Dataset**

## Description
The FruitVision Dataset consists of images of fruits sourced from Bing Image Search. Each category contains 50 images labeled with a structured naming convention (`<category>_img<number>.jpg`). Metadata is provided in a CSV file (`metadata.csv`) containing:
- Fruit category
- Image filename
- Source URL
- Resolution (width x height)

### Categories
The dataset includes the following 20 fruit categories:
1. Apple  
2. Banana  
3. Mango  
4. Orange  
5. Grapes  
6. Pineapple  
7. Watermelon  
8. Papaya  
9. Pear  
10. Pomegranate  
11. Peach  
12. Plum  
13. Kiwi  
14. Lemon  
15. Strawberry  
16. Cherry  
17. Dragon Fruit  
18. Custard Apple  
19. Jackfruit  
20. Tamarind  

## Use Case
### Fruit Classification Model
This dataset can be used to train a machine learning model to classify fruits based on their images. For example:
1. **Objective:** Build an image classification model using Convolutional Neural Networks (CNNs).
2. **Steps:**
   - Preprocess the images (resize, normalize).
   - Split the dataset into training, validation, and testing sets.
   - Train a CNN model using frameworks like TensorFlow or PyTorch.
   - Evaluate the model's accuracy on unseen data.

### Example Applications
- Automated fruit identification for grocery stores.
- Quality control systems in agriculture.
- Educational tools for teaching computer vision concepts.




## Problems Faced / Limitations

1. Irrelevant Search Results for Common Fruits

When searching for fruit images using only the fruit name (e.g., "Apple" instead of "Apple fruit"), search engines often return unrelated images. Some common issues include:

- Apple: Results include Apple Inc. products (iPhones, MacBooks, logos) instead of the fruit.

- Orange: Results may include orange-colored objects, wallpapers, or the telecom company "Orange."

- Pear: Some results include pear-shaped objects or patterns rather than the fruit itself.





2. Incorrect Image Context

Even when images contain fruits, they are sometimes part of complex scenes rather than standalone fruit images. Issues include:

- Fruits in fruit baskets, making segmentation difficult.

- Cut fruits, causing variations in texture and shape.

- Dishes containing fruits, leading to inconsistent labeling.




3. Variation in Image Quality and Resolution

Some images are pixelated or blurry, which can impact model performance.

Resolution inconsistencies require preprocessing steps like resizing and normalization.





4. Different Perspectives and Backgrounds

Some images are taken in natural environments (trees, markets), while others have artificial backgrounds.

Variations in lighting conditions and angles may introduce bias into the model.





## Possible Solutions

- Using refined search queries, such as "Apple fruit" instead of just "Apple."

- Manually filtering out unrelated images before adding them to the dataset.

- Applying data augmentation techniques to address lighting and angle variations.

- Despite these limitations, the FruitVision Dataset remains a valuable resource for fruit classification and computer vision applications with proper preprocessing and curation.