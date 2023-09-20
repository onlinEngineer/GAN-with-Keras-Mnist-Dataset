# GAN-with-Keras-Mnist-Dataset
GAN with Keras Mnist Dataset

### PART-1:

Modify the discriminator based on the following:

1. Use at least 3 convolutional layers in the discriminator.
2. Do not use dense layers, except for the output layer.
2. The input should be 2D image of size 28x28 (You can use Reshape layer of Keras to get correct shaped input from the discriminator). 

Re-train your GAN and make sure that you get similar quality output images as the original GAN.


# MAIN MODEL
In this assignment, we used keras minest dataset with a shape of 60000,784 which is 60000x28x28x1 to create GAN.
### Model
Our model is having 2 model which are discriminator and generator. In discriminator part, Discriminator will take the input from real data which is of the size 784 and also the images generated from Generator, and we will input the noise image of size 100 to the Generator. The output generated from the Generator will be fed to the Discriminator. After that, we create the GAN where we combine the Generator and Discriminator. When we train the generator, we will freeze the Discriminator. While discriminator model input dim is 784, generator model input dim is 64.
### Discriminator Model of Main Model

![image](https://github.com/onlinEngineer/GAN-with-Keras-Mnist-Dataset/assets/70773825/0cba37c9-99ff-43ff-83a3-4dcfba9cd0e7)

### Generator Model of Main Model

![image](https://github.com/onlinEngineer/GAN-with-Keras-Mnist-Dataset/assets/70773825/99e4973c-51be-4c37-a428-22a359585d36)

### GAN
We will input the noise image of size 100 to the Generator. The output generated from the Generator will be fed to the Discriminator.

![image](https://github.com/onlinEngineer/GAN-with-Keras-Mnist-Dataset/assets/70773825/3de03136-57c8-4c65-b10d-1d3a496cc2de)

### Epochs

After 50 epochs with a 128-batch size, our images shown in the following figure.
Epoch completed time is approximately 5.49 minutes which is pretty fast but as shown in the images, quality of generated images is not good.

![image](https://github.com/onlinEngineer/GAN-with-Keras-Mnist-Dataset/assets/70773825/cccc52d9-a0e5-45bd-8893-b068f002daad)



### PART-2:

Now, modify the generator as well, so that the whole GAN becomes a convolutional neural network:

1. Use at least 3 convolutional layers in the generator. You may also like to use batch normalization layers after each convolutional layer. Try using ReLU or Leaky ReLU for activation. 
2. Do not use any dense layers.
2. The input should be 2D noise image of size 8x8 (You can use Transposed convolution layer of Keras (Conv2DTranspose) to go from 8x8 sized input to 28x28 sized output).

# PART 2 MODEL 1
In this part, we used keras minest dataset with a shape of 60000,784 which is 60000x28x28x1 to create GAN and at least 3 Convolutional layer that input shape is 28x28x1 in the discriminator.
### Model
In discriminator part, Discriminator will take the input from real data which is of the size 28x28x1 and also the images generated from Generator, and we will input the noise image of size 100 to the Generator. The output generated from the Generator will be fed to the Discriminator. After that, we create the GAN where we combine the Generator and Discriminator. When we train the generator, we will freeze the Discriminator. While discriminator model input shape is 28x28x1, generator model input dim is 64.

### Discriminator Model of Model 1

![image](https://github.com/onlinEngineer/GAN-with-Keras-Mnist-Dataset/assets/70773825/d994e6b0-bbe5-4321-aad8-6dcb9e5824ec)

### Generator Model of Model 1

![image](https://github.com/onlinEngineer/GAN-with-Keras-Mnist-Dataset/assets/70773825/fc5c3826-2162-4c15-aa51-798cbb3edb42)

### GAN
We will input the noise image of size 100 to the Generator. The output generated from the Generator will be fed to the Discriminator

![image](https://github.com/onlinEngineer/GAN-with-Keras-Mnist-Dataset/assets/70773825/44fb2dfe-29d0-4356-8a84-3bb580c9ae5f)

### Epochs
After 50 epochs with a 128-batch size, our images shown in the following figure. Epoch completed time is 12.42 minutes. This model is slower than the first model but when we compare the quality of images, second model is clearly much better quality than the first model.

![image](https://github.com/onlinEngineer/GAN-with-Keras-Mnist-Dataset/assets/70773825/5255cd0c-1ea3-47fd-b558-485eaf6dc2cb)

# PART 2 MODEL 2
In this part, we update the generator part and convert dense layers to convolutional layers that input shape is 8x8x1. To create GAN and at least 3 Convolutional layer in the generator.
### Model
In discriminator part, Discriminator will take the input from real data which is of the size 28x28x1 and also the images generated from Generator, and we will input the noise image of size 100 to the Generator. The output generated from the Generator will be fed to the Discriminator. After that, we create the GAN where we combine the Generator and Discriminator. When we train the generator, we will freeze the Discriminator. While discriminator model input shape is 28x28x1, generator model input shape is 8x8x1.

### Discriminator Model of Model 2

![image](https://github.com/onlinEngineer/GAN-with-Keras-Mnist-Dataset/assets/70773825/821e6e9a-fcc2-4294-8e26-9ae44d7ebdc2)


### Generator Model of Model 2

![image](https://github.com/onlinEngineer/GAN-with-Keras-Mnist-Dataset/assets/70773825/c5f8fa87-dfba-43e1-91af-ebb03ed07283)


### GAN
We will input the noise image of size 100 to the Generator. The output generated from the Generator will be fed to the Discriminator

![image](https://github.com/onlinEngineer/GAN-with-Keras-Mnist-Dataset/assets/70773825/14be15a5-762b-4d8c-864b-d626238e77e6)

### Epochs
After 50 epochs with a 128-batch size, our images shown in the following figure. Epoch completed time is 19.32 minutes. This model is slower than the first and second model, hovewer,
There is no unmeaningful pixels in the images even if quality of number is bad. Also, we should consider that this model is less complex than the other models. So, with a better models or parameters, images can be improved.

![image](https://github.com/onlinEngineer/GAN-with-Keras-Mnist-Dataset/assets/70773825/15284f9f-95a5-409d-be98-e6faf5d3d9a8)




