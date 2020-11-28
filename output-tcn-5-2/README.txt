tcn-5-2.ipynb


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
					125

MAXLIFE = 125
Using TCN library:

input (8631, 120, 25)

TCN:
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
input_1 (InputLayer)         [(None, 120, 25)]         0         
_________________________________________________________________
tcn (TCN)                    (None, 120, 12)           4692      
_________________________________________________________________
tcn_1 (TCN)                  (None, 6)                 1224      
_________________________________________________________________
dense (Dense)                (None, 1)                 7         
=================================================================
Total params: 5,923
Trainable params: 5,923
Non-trainable params: 0
_________________________________________________________________
tcn_2 filters 12
tcn_3 filters 6
dropout on TCN 0,2
dropout on TCN 0,2
dilations=[1, 2,4,8,16,32]
dilations=[1, 2,4,8,16,32]

epochs 100 no early stop
batch 200
validation split 0,05
loss = root_mean_squared_error
===============================
MAE: 6.88822603225708

R^2: 0.9241577386856079

RMSE: 10.296293258666992