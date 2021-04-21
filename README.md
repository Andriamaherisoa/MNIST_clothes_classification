# MNIST_clothes_classification

On espère obtenir la structure du réseau décrit ci-dessous en rajoutant des couches au réseau de neuronnes basique de fashion_MNIST:   

_________________________________________________________________
Layer (type)                 Output Shape              Param #  
=================================================================
conv2d (Conv2D)              (None, 26, 26, 32)        320      
_________________________________________________________________
max_pooling2d (MaxPooling2D) (None, 13, 13, 32)        0        
_________________________________________________________________
conv2d_1 (Conv2D)            (None, 11, 11, 64)        18496    
_________________________________________________________________
max_pooling2d_1 (MaxPooling2 (None, 5, 5, 64)          0        
_________________________________________________________________
conv2d_2 (Conv2D)            (None, 3, 3, 64)          36928    
_________________________________________________________________
flatten (Flatten)            (None, 576)               0        
_________________________________________________________________
dense (Dense)                (None, 64)                36928    
_________________________________________________________________
dense_1 (Dense)              (None, 10)                650      
=================================================================
Total params: 93,322
Trainable params: 93,322
Non-trainable params: 0
_________________________________________________________________

On pourra utiliser une configuration de calcul du type :

model.compile(optimizer='rmsprop',loss='categorical_crossentropy',metrics=['accuracy'])

Dans ce cas, il faudra faire l'import :

from tensorflow.keras.utils import to_categorical

Estimer le nombre de périodes qui permettent d'obtenir les meilleurs résultats et comparer avec le réseau initial sans convolution.

Vous pourrez réaliser un notebook Google Colab ou un notebook Jupyter comportant toutes vos explications, à déposer ci-dessous sur l'espace dépôt.
