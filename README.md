# Dogs_vs_Cats
My first deep learning project with PyTorch: Classify Dogs and Cats with PyTorch models

This project follows the Kaggle Dogs vs Cats competition (https://www.kaggle.com/c/dogs-vs-cats-redux-kernels-edition). The details of the data and competition rules can be found in the link. 

<hr>
<h2>Transfer Learning with ResNet</h2>

I used transfer learning with the pretrained ResNet101 model and modified the last classification layer to suit the dog-cat binary classification. 1000 images of each class are randomly chosen as the validation data. During the training process, a best model is obtained if the model obtains a lower validation loss. 

The model has been trained with 120 epochs and the best model is the one trained with 109 epochs. Due to the size issue, the model is not uploaded to Github repo.

The model trained with 109 epochs gives a score of 0.87131, better than that at 1099 position on the leaderboard.

<hr>
<h2>Self constructed CNN</h2>

After learning more about Neural Networks with PyTorch, I built a simple CNN for this problem. I tried with different network architectures, a different loss function and learning rates. The information is in the version.info in the respective directory, with the performance on the training dataset (including the validation set) and the test data performance. 
