# Dogs_vs_Cats
My first deep learning project with PyTorch: Classify Dogs and Cats with PyTorch models

This project follows the Kaggle Dogs vs Cats competition (https://www.kaggle.com/c/dogs-vs-cats-redux-kernels-edition). The details of the data and competition rules can be found in the link. 

All model version specifications are in the version.info file in the respective folders.

<hr>
<h2>Data</h2>
The training data contains 12500 images of cats and dogs respectively with the label being part of the image file name. The images are coloured and of various sizes.

The test data contains 12500 unlabelled images. This is the dataset used for evaluation for the competition. The evaluation metric used in the competition is LogLoss.

For training purposes, 1000 images of cats and dogs respectively are selected randomly from the training data as the validation data. The training loss and validation loss are both computed; the best model is obtained when there is a lower validation loss. 

<hr>
<h2>Transfer Learning with ResNet</h2>

The pretrained ResNet101 model is used for the transfer learning, with the last classification layer modified to fit the binary classification.
The model has been trained with 120 epochs and the best model is the one trained with 109 epochs. Due to the moel size issue, the model is not uploaded to Github repo.

The training loss and validation loss of the best model are 0.3370 and 0.3262. The best model gives a lgoloss score of 0.87131, better than that at 1099 position on the leaderboard.

<hr>
<h2>Self constructed CNN</h2>

After learning more about Neural Networks with PyTorch, I built a simple CNN for this problem. I tried with different network architectures, a different loss function and learning rates. The information is in the version.info in the respective directory, with the performance on the training dataset (including the validation set) and the test data performance. 

So far, there are three versions of self constructed CNN. 

All three versions use the 3x3 kernel size for the convolutional layers with 2x2 kernel for the maxpooling layer. Two linear layers are used with the ReLU activation function. A dropout layer with the probability 0.2. 

The loss function used is BCEWithLogitsLoss due to its better stability than BCELoss with Sigmoid function. Different optimizers are used with varying learning rates. No schedulers are used.

The best version out of the three is Version 2. The problem with version 1 is that the learning rates is too small that the training takes very long to see siginificant improvements. As for version 3, although the validation loss is the lowest, from the loss graph, it is observed that the model is likely to be overtrained. Version 2 model definitely has rooms for improvements with more training.


    
