Atuoencoder and LSTM
LSTM-Autoencoder-2-1.ipynb
autoencoder: autoencoder2.ipynb

selected 14 sensor and all setting values  => encoder
encoder => 8 values 
8 values => stacked to 50
(15631, 50, 8) => to LSTM


input to encoder: 
========================================================================================================================================
========================================================================================================================================
ENCODER:

_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
input_4 (InputLayer)         [(None, 18)]              0         
_________________________________________________________________
dense_18 (Dense)             (None, 32)                608       
_________________________________________________________________
dense_19 (Dense)             (None, 16)                528       
_________________________________________________________________
dense_20 (Dense)             (None, 8)                 136       
=================================================================
Total params: 1,272
Trainable params: 1,272
Non-trainable params: 0_____________________________________


Dense(32, activation='relu')
Dense(16, activation='relu')
Dense(8, activation='relu')

========================================================================================================================================
========================================================================================================================================
LSTM:

input (15631, 50, 9)


_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
lstm_2 (LSTM)                (None, 50, 100)           44000     
_________________________________________________________________
dropout_2 (Dropout)          (None, 50, 100)           0         
_________________________________________________________________
lstm_3 (LSTM)                (None, 50)                30200     
_________________________________________________________________
dropout_3 (Dropout)          (None, 50)                0         
_________________________________________________________________
dense_1 (Dense)              (None, 1)                 51        
_________________________________________________________________
activation_1 (Activation)    (None, 1)                 0         
=================================================================
Total params: 74,251
Trainable params: 74,251
Non-trainable params: 0
_________________________________________________________________


epochs 150
batch 200
validation split 0,05
===============================
MAE: 14.045432090759277

R^2: 0.7646724581718445

RMSE: 19.60206413269043

