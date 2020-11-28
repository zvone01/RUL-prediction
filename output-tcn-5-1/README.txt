tcn-5-1.ipynb


Piecewise linear function with zero gradient and unit gradient

		^
		|
MAXLIFE |-----------
		|            \
		|             \
		|              \
		|               \
		|                \
		|----------------------->
					137

MAXLIFE = 137
Using TCN library:

input (17431, 32, 25)

TCN:
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
input_2 (InputLayer)         [(None, 32, 25)]          0         
_________________________________________________________________
tcn_2 (TCN)                  (None, 32, 12)            4692      
_________________________________________________________________
tcn_3 (TCN)                  (None, 6)                 1224      
_________________________________________________________________
dense_1 (Dense)              (None, 1)                 7         
=================================================================
Total params: 5,923
Trainable params: 5,923
Non-trainable params: 0
_________________________________________________________________
tcn_2 filters 12
tcn_3 filters 6
dropout on TCN 0,2
dropout on TCN 0,2
dilations=[1, 1, 1, 1, 1, 1]
dilations=[1, 1, 1, 1, 1, 1]

epochs 100 no early stop
batch 200
validation split 0,05
loss = root_mean_squared_error
===============================
MAE: 13.854104995727539

R^2: 0.8082378506660461

RMSE: 17.11075210571289