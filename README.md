# FashionMNIST_Image_Classification
This approach (see [notebook](https://github.com/GSukr/FashionMNIST_Image_Classification/blob/master/FM_SG.ipynb)) investigates whether multiple CNN models can achieve higher classification accuracy than any individual model.

### Two simple strategies for combining models are examined:
1. Classification based on the average class probabilities of models
2. Using the mode class for prediction

### Conclusions:
1. A simple CNN can achieve classification accuracy of over 93%
2. Combining 3 models improves accuracy around 94.4%
3. It takes around 16 seconds per epoch using Colaboratory GPU accelerator and Test accuracy does not improve significantly after the first 20 epochs
4. Combining a few more models trained over 20 epochs may further improve classification accuracy in a resonable amount of time.
5. Classification accuracy is significantly lower for 4 classes: 'T-shirt/top', 'Pullover', 'Coat', and 'Shirt'.

### Opportunities for improvement:
1. Devise alternate methods for combining models
2. Increase the diversity of constituent models
3. Introduce regularization methods that prevent over-fitting beyond 20 epochs
4. Develop a two-phased approach: Predict using a combination of models in the first phase and use a separate model to re-classify examples
predicted as 'T-shirt/top', 'Pullover', 'Coat', or 'Shirt
