# MCNN-based_HSI_Classification
## Papers
* MCNN-CP: Hyperspectral Image Classification Using Mixed Convolutions and Covariance Pooling (TGARS 2020) [paper](https://ieeexplore.ieee.org/document/9103280/)  
* MCNN-PS & Oct-MCNN-PS: Hyperspectral Image Classification Using Hybrid Octave and Sub-Pixel Convolutional Neural Network (TGARS Submitted)

## 1. Environment setup
This code has been tested on on a personal laptop with Intel i7-9750H 2.6-GHz processor, 32-GB RAM, and an NVIDIA GTX1650 graphic card, Python 3.6, tensorflow_gpu-1.14.0, Keras-2.2.4, CUDA 10.0, cuDNN 7.6. Please install related libraries before running this code:

    pip install -r requirements.txt

## 2. Download the datesets:
* IP:
[Indian Pines corrected](http://www.ehu.eus/ccwintco/uploads/6/67/Indian_pines_corrected.mat) and
    [Indian Pines gt](http://www.ehu.eus/ccwintco/uploads/c/c4/Indian_pines_gt.mat)
* KSC:
[Kennedy Space Center corrected](http://www.ehu.eus/ccwintco/uploads/2/26/KSC.mat) and
    [Kennedy Space Center gt](http://www.ehu.eus/ccwintco/uploads/a/a6/KSC_gt.mat)
* UP:
[University of Pavia corrected](http://www.ehu.eus/ccwintco/uploads/e/ee/PaviaU.mat) and
    [University of Pavia gt](http://www.ehu.eus/ccwintco/uploads/5/50/PaviaU_gt.mat)
* SA:
[Salinas Scene corrected](http://www.ehu.eus/ccwintco/uploads/a/a3/Salinas_corrected.mat) and
    [Salinas Scene gt](http://www.ehu.eus/ccwintco/uploads/f/fa/Salinas_gt.mat)

and put them into data directory.

## 3. Download the models (loading models):

* [models](https://pan.baidu.com/s/1fnthMICtci2lfuWEihkDJA) code: caor

and put them into models directory.

## 4. Download the pretrained_models (loading model parameters):
* IP:
[Indian Pines](https://pan.baidu.com/s/1shzME97Y7Ci_5EvM9qdTWQ) code: d59l
* KSC:
[Kennedy Space Center](https://pan.baidu.com/s/1J5aj643pY8jTpP0bw5maKA) code: 6r2f
* UP:
[University of Pavia](https://pan.baidu.com/s/1wM8vBRewnBHmCHvPbnBnOg) code: 8h4m
* SA:
[Salinas Scene](https://pan.baidu.com/s/1DZAd5Ufm5DkCLUCVCz33dQ) code: io53

and put them into pretrained_models directory.

## 5. Test

    python validate.py                \
	--dataset IP                      \ # dataset_name
	--model Oct-MCNN-PS               \ # model_name
	--ratio 0.7                         # test_ratio
           
The testing result will be saved in the classification_report.txt.

## 6. Cite
If you use MCNN-CP in your work please cite our paper:

    @ARTICLE{9103280,
      author={J. {Zheng} and Y. {Feng} and C. {Bai} and J. {Zhang}},
      journal={IEEE Transactions on Geoscience and Remote Sensing}, 
      title={Hyperspectral Image Classification Using Mixed Convolutions and Covariance Pooling}, 
      year={2020},
      volume={},
      number={},
      pages={1-13},
    }
