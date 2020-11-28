jupyter nootebook dokumenti s testiranjem predviđanja RUL na cMPASSdatastetu
svi imaju isti preprocesing i iste postavke za treniranje.

testiran je LSTM sa autoencoderom:
Predictive maintenance-using-LSTM- Autoencoder
	(greška s autoenkoderom krivo sam ga napravija umisto da kad ga rreniram otkinem pola ja sam to direktno stavija na lstm)
	lstm autoenkoder koji smanjuje na 14
	lstm 50 units
	dropout 0,2
	lstm 100 units
	dropout 0,2
	dense layer

LSTM-Autoencoder-v2
	(ovaj radi ali nema ništa bolje rezultate od  LSTM bez autoencodera)
	lstm autoenkoder koji smanjuje na 14
	lstm 50 units
	dropout 0,2
	lstm 100 units
	dropout 0,2
	dense layer
	(MAE: 12.879725199873729;  R^2: 0.7635883637653884)
	
LSTM- Autoencoder-simpler lstm.ipynb
	(pokušaj smanjivanja broja lstm layera, brže treniranje ali slabiji rezultat)
	lstm autoenkoder koji smanjuje na 14 (svi imaju isti)
	
	verzija 1:
	lstm 50 units
	dense layer
	(MAE: 15.400349206821893; R^2: 0.6912001980248318)
	
	verzija 2:
	lstm 100 units
	dropout 0,2
	dense layer	
	(MAE: 14.357305403678648; R^2: 0.7328173838635926)
	
	verzija 3:
	lstm 50 units	
	dropout 0,2
	dense layer
	(MAE: 14.558566390827139; R^2: 0.7269390110046633)