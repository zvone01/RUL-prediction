Same as tcn-2-0 but this one uses dropout from tcn not added dropoput as a layer.
tcn-2-0.ipynb

Using TCN library:

input (15631, 50, 25)

TCN:

_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
input_2 (InputLayer)         [(None, 50, 25)]          0         
_________________________________________________________________
tcn_2 (TCN)                  (None, 50, 32)            31072     
_________________________________________________________________
tcn_3 (TCN)                  (None, 16)                8224      
_________________________________________________________________
dense_1 (Dense)              (None, 1)                 17        
=================================================================
Total params: 39,313
Trainable params: 39,313
Non-trainable params: 0
_________________________________________________________________
tcn_6 filters 32
tcn_7 filters 16
dropout 0,2
dropout 0,2

epochs 100
batch 200
validation split 0,02
===============================
93/93 - 1s - loss: 343.9002 - mean_absolute_error: 13.4724 - r2_keras: 0.7934
