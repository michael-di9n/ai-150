# Problem 1: Train/Test Split
1. Classify images into object catergeories
   1. Each image consist of a single object with one category
   2. 20 categories
   3. 5k images per category
   4. In reallife all catogies are likly to appear

Randomly split the data into train/validation/test

Rule of thumb is 80/20 for training and test then 80/20 fir traububg abd vakudatuib

1. Take 10%==500 images for evalauating the model set aside for test
2. Take 10%==500 for validation
3. Take 80% for training the model 
![alt text](image.png)
https://stackoverflow.com/questions/13610074/is-there-a-rule-of-thumb-for-how-to-divide-a-dataset-into-training-and-validatio

Kilian points out that five categories have higher error rate gives 10k images for each of these
- These may be 'similar' images
We have an influx of 10k images for these five categories
What could go wrong if we just add it then retrain it?
  - Overpresentation of 5 caterogies and underpresentation of 15 categories leads to a imbalanced data set
  -  ratio 15000:5000 == 3:1
  -  Minority % : 5000/150000 * 100 = 3% 
  - 15k images for 5 categories it will be come better at identifiying these 5 but worse at identifying the other 15 i.e., overtunning for these five categories

Imbalanced datasets
https://developers.google.com/machine-learning/crash-course/overfitting/imbalanced-datasets#

Solution:
- Downscaling i.e., cutting majority class
- Upweighting i.e., add extra weight to downsampled class