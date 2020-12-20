# Optimizer-lr-tuning
## Analyze the performance of 7 optimizers by varying their learning rates 

When we train our model on datasets, we need the error to converge to a minimum for efficient analysis. Choosing a good optimizer out of the plethora of options is one of the most important decisions that will after this process. A good optimizer will make sure that we get the required accuracy after few epochs of training. The best optimizer for training varies from problem to problem and dataset to dataset. Another important aspect of faster convergence is the learning rate of the optimizer. Since, an optimizer can proceed with many different learning rates, it is important to identify a learning rate that works best for the problem we have. Too high a learning rate might lead to lack of convergence and too low a learning rate will slow down the training process. So, it is essential to test different learning rates to find the best one which converges faster. 
It has been observed that having a high learning rate initially is better for faster searching of the loss landscape. Subsequently, it has also been observed that reducing the learning rate as the number of epochs increases helps the optimizer to not make sudden jumps out of a minimum it is approaching, thus helping it to reach a minimum. So, we use different learning rate schedulers to see which one will work best with the optimizer to reach a minimum faster, if at all it does aid the optimizers.

### Experiment Design Strategy
The Dataset we have is that of Cardiac MRI Segmentation. The dataset contains around 4k images for training. We are dividing the dataset into 80% as training and 20% as validation sets. 
We are creating a U-Net model to train the dataset as given in the paper. (Chuckyee, 2017)
#### Unet Architecture (Yee, 2017)
![image](https://user-images.githubusercontent.com/15833382/102724910-f30ee000-4338-11eb-8705-5c9af9256153.png)

We are not use data augmentation methods given in the paper for training.
We used Weighted categorical Cross entropy as our loss function which we call as pixel loss.
Mean Intersection-Over-Union was used along with Accuracy as a metric for evaluation as our task is semantic image segmentation
Dice loss was also computed as an evaluation metric.
#### Batch size = 32
We use the following 7 different optimizers for our experiment. 
- SGD 
- RMSprop 
- Adagrad 
- Adadelta
- Adam
- Adamax
- Nadam










