# CRF_Results

### Release log
- FCOS3D R-101-FPN [done, 2022-3-7]
- 3D Faster R-CNN R-101-FPN	[done, 2022-3-9]
- 3D Faster R-CNN R-50-FPN 	[done, 2022-3-11]
- 3D Faster R-CNN CRF_R-50-FPN_rconv_c	[done, 2022-3-12]


### Ongoing work
- Integrating CenterFusion to MMdetection3D

### Notation

|    Term     | meaning  |
| :-----------------: | :-----:|
|R-50  | ResNet-50 |
|R-101  | ResNet-101 |
|X-101  | ResNeXt-101 |
|FPN | feature pyramid network |
|dconv |deformable convoluation |
|dconv(c4-c5) |deformable convoluation at stages c4, c5 of FPN|
|CRF | camera-radar fusion|
|rconv_c|radar features obtained by convoluation, fused with image features at location c |


<p align="center">
  <img src="fusion_location.png" width="450" height="350">
<img src="car4.png" width="450" height="350">
</p>


### FCOS


|    Backbone     | Conv |  data   | batch size | img size | Lr schd |  mAP | NDS | note|
| :------------: | :------------:| :---: | :---: | :-----: | :------: | :----: | :----: | :----------: | 
|    R-50-FPN     | -           | 0.2     |   8     | 800x448  | 1x    |      13.6% |	21.4% |  |
|    R-50-FPN     | -           | 0.2     |   8     | 800x448  | 2x    |     14.2%	| 24.3%	 |  |
|    R-50-FPN     | -           | 0.2     |   8     | 800x448  | 3x    |     14.4%	| 25.0% ||
|    R-50-FPN     | -           | 1       |   8     | 800x448  | 1x    |      23.6%	| 32.3% ||
| R-101-FPN	      |-	          |1	      |8	|800x448	|1x|	23.8%	|33.3%||
| R-101-FPN	      | dconv(c4-c5)| 	0.2	| 2	| 1600x900	| 1x	| 17.2%	| 27.0%| |
| R-101-FPN	      | dconv(c4-c5)| 1	| 32	| 1600x900| 1x	| 29.8%| 	37.7%| released weights|



### 3D Faster R-CNN

|    Backbone     | Conv |  data   | batch size | img size | Lr schd |  mAP | NDS | note|
| :------------: | :------------:| :---: | :---: | :-----: | :------: | :----: | :----: | :----------: | 
|    R-50-FPN     | -           | 0.2     |   8     | 800x448  | 1x    |      11.6%	|19.8%|  |
|    R-50-FPN     | -           | 0.2     |   8     | 800x448  | 2x    |     12.8%	|20.6%	 |  |
|    R-50-FPN     | -           | 0.2     |   8     | 800x448  | 3x    |    13.1%	|21.0% ||
|    R-50-FPN     | -           | 1       |   8     | 800x448  | 1x    |     24.3%	|29.8%||
|CRF_R-50-FPN_rconv_c	|-	|1	|8	|800x448|	1x	|24.8%|	30.8%||
| R-101-FPN	      | -	          | 1	      |   8	    | 800x448	 |  1x  |	26.9%	|32.1%||

