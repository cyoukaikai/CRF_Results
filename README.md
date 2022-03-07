# CRF_Results

### Release log
- FCOS3D R-101-FPN [done, 2022-3-7]


### Notation

|    Term     | meaning  |
| :-----------------: | :-----:|
|R-50  | ResNet-50 |
|R-101  | ResNet-101 |
|X-101  | ResNeXt-101 |
|FPN | feature pyramid network |
|dconv |deformable convoluation |
|dconv(c4-c5) |deformable convoluation at stages c4, c5 of FPN|

### FCOS



|    Backbone     | Conv |  data   | batch size | img size | Lr schd |  mAP | NDS | note|
| :-----------------: | :-----:| :---: | :---: | :-----: | :------: | :----: | :----: | :----------: | 
|    R-50-FPN     | -           | 0.2     |   8     | 800x448  | 1x    |      13.6% |	21.4% |  |
|    R-50-FPN     | -           | 0.2     |   8     | 800x448  | 2x    |     14.2%	| 24.3%	 |  |
|    R-50-FPN     | -           | 0.2     |   8     | 800x448  | 3x    |     14.4%	| 25.0% ||
|    R-50-FPN     | -           | 1       |   8     | 800x448  | 1x    |      -	| - ||
| R-101-FPN	|-	|1	|8	|800x448	|1x|	23.8%	|33.3%||
| R-101-FPN	      | dconv(c4-c5)| 	0.2	| 2	| 1600x900	| 1x	| 17.2%	| 27.0%| |
| R-101-FPN	      | dconv(c4-c5)	| 1	| 32	| 1600x900| 1x	| 29.8%| 	37.7%| released weights|
