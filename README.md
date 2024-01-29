This notebook creates a custom Convolution Neural Network (CNN), that distinguishing between images from four classes of Alzheimer's patients with an accuracy of the rate of 99% on both the validation and test datasets.

The dataset used in training and validating this model consisted of 6,400 brain scan images organized in four subfolders, where each folder denoted the patient's classification. The data was split into 80% training, 10% validation, and 10% testing. Images are consistently aligned brain slices from a top-down perspective in jpeg format. All jpegs were 8-bit grayscale with black backgrounds.

Before this notebook, pre-trained Convolution Neural Networks (CNNs) such as VGG16, VGG19, ResNet, and EfficientNet were tried. It was believed that these models would take advantage of transfer learning and eliminate the need for architecture experimentation; however, these fine-tuned experiments achieved a maximum accuracy ceiling of less than 90%, which may be the result of the significant differences in the underlying training datasets: ImageNet vs. brain scans. 

Multiple custom models were attempted. The architectural approach to build a Sequential Model in Keras with convolutional layers for extracting features followed by flattening and dense layers for classification. Pooling layers were added after convolutions to focus on the image's most critical parts. Dropout layers were added to be used during training and turned off during evaluation and deployment. Batch normalization was included after convolution and dense layers.

More details can be found regarding the larger project this notebook was developed in support of at Omdena Challenge: Early Detection of Alzheimer's. 
