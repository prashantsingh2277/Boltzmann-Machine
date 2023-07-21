# Boltzmann-Machine
Boltzmann machine: Energy-based model with stochastic binary units used for unsupervised learning. Fully connected network, learns to minimize energy during training. Tasks: data clustering, dimensionality reduction, feature learning. Limitation: slow, computationally expensive for large-scale use.
Data Preprocessing:

The code reads three datasets: movies, users, and ratings, from MovieLens data.
It also reads training and test sets (u1.base and u1.test) for collaborative filtering.
Data Conversion:

The data is processed and converted into a user-item interaction matrix, where rows represent users, columns represent items (movies), and the values represent user ratings for movies.
Data Transformation:

The user ratings are converted into binary values (1 for liked, 0 for not liked) for training the RBM.
RBM Class:

The code defines an RBM class, with functions to initialize the RBM model, sample hidden and visible units, and train the model using contrastive divergence.
Model Training:

The RBM model is trained on the training set, where the visible units are input user ratings, and hidden units are learned to represent latent features or preferences.
Model Testing:

The trained RBM model is then used to predict user-item ratings on the test set.
The test loss is calculated as the mean absolute difference between predicted and actual ratings for test data.
The code follows the steps of training the RBM on the training set using contrastive divergence and then evaluating its performance on the test set. The final output includes the training loss for each epoch and the test loss, representing the model's accuracy in predicting user-item interactions.

Note: The code contains a small typo; the sample_h method is defined twice. The second sample_h method should be corrected to sample_v, which samples visible units given hidden units.

Overall, this code showcases a basic implementation of an RBM for collaborative filtering, with potential improvements and optimizations to enhance its performance and accuracy in real-world recommendation systems.
