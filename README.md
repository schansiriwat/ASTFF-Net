# ASTFF-Net
The ASTFF-Net is a robust adaptive spatial-temporal feature fusion network, to enhance the performance of the food image recognition system. 
The architecture of ASTFF-Net is divided into three parts; 
1. Spatial feature extraction network, as the first part to extracted the spatial features using the ResNet50 and then minimized the size
of the parameters using the reduction operation. Further, the convolutional 1D (Conv1D) block was applied to fit the features into the recurrent neural networks.
2. Temporal feature extraction network, as the second part. The spatial features from the first part were given to the long short-term memory (LSTM) that allows
learning various patterns from sequence features.
3. Adaptive feature fusion network, as the final part. The spatial features from the first part and temporal features from the second part were concatenated and assigned to the
Conv1D, followed by the softmax layer. The advantage of ASTFF-Net is that the proposed network can prevent overfitting problems due to the attachment of the global average pooling
and dropout layers. These layers decreased the number of network parameters and dropped the number of connections between layers, respectively.

File Detail:
1. ResNet50Network.ipynb: for train the dataset with transfer learning before extracted spatial feature by using the ResNet50.
2. extractedSpatialFeatures.ipynb: for extracted spatial features by using trained ResNet50.
3. lstmNetwork.ipynb: for train the spatial feature.
4. extractedTemporalFeatures.ipynb: for extracted temporal features by using trained LSTM.
5. ASTFF-Net.ipynb: for combine spatial and temporal and train them to classify the food images dataset.

Reference:
Phiphitphatphaisit, S., & Surinta, O. (2024). Multi-layer adaptive spatial-temporal feature fusion network for efficient food image recognition. Expert Systems with Applications, 255, 124834.
https://doi.org/10.1016/j.eswa.2024.124834
