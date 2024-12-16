# Loss Functions in Deep Learning - Classification Table

| Category | Loss Function | Description | Common Use Cases |
|----------|---------------|-------------|------------------|
| **Regression** | MSE (Mean Squared Error) | Measures average squared difference between predicted and actual values | • Continuous value prediction<br>• General regression tasks |
| | MAE (Mean Absolute Error) | Measures average absolute difference between predicted and actual values | • Regression with outliers<br>• Financial predictions |
| | Huber Loss | Combines MSE for small errors and MAE for large errors | • Robust regression<br>• Outlier-sensitive tasks |
| **Classification** | Binary Cross-Entropy | Measures dissimilarity between predicted probability and true label | • Binary classification<br>• Yes/no predictions |
| | Categorical Cross-Entropy | Measures dissimilarity between predicted probability distribution and true one-hot encoded label | • Multi-class classification<br>• Multiple category prediction |
| | Hinge Loss | Encourages correct classifications with large margins | • Support Vector Machines<br>• Margin-based classification |
| **Object Detection** | Focal Loss | Modified cross-entropy that focuses on hard examples | • Object detection<br>• Imbalanced datasets |
| **Autoencoders** | Reconstruction Loss | Measures difference between input and reconstructed output | • Image reconstruction<br>• Data compression |
| | KL Divergence | Measures difference between latent distribution and prior distribution | • Variational autoencoders<br>• Distribution matching |
| **GANs** | Discriminative Loss | Measures discriminator's ability to distinguish real/fake samples | • GAN training<br>• Adversarial networks |
| | Generative Loss | Measures generator's ability to produce realistic samples | • GAN training<br>• Image generation |
| **Embedding** | Triplet Loss | Measures distance between positive and negative pairs | • Face recognition<br>• Similarity learning |

