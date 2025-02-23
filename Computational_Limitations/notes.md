- impact of image size:
    the more pixels, the more convolutional operations
    the more pixels, the more parameters -------> the more network operations
  

https://arxiv.org/pdf/2007.05558

- in modern DL, overparameterizing has benefits as overfitting is prevented
- training scales with: numberParameters * numberDatapoints; in reality much higher
- to significantly improve performance, more parameters are needed
- classic tradeoff between more parameters and worse performance

- with advancements in computing power, economical costs remained the same while performance increased a lot (especially with GPUs)
- 2009: DL models remained too slow for large-scale applications -> use smaller scale models or use fewer training data
- turning point when porting DL to GPUs
- however, many GPUs and training time necessary for the "good" models

- many papers do not report details of computation amount needed -> accuracy in focus (45, 46, 47)
- Metrics to measure computational burden (during pre-training, training and fine-tuning)
    1. Network operations: epochs * flopsPerNetworkPass * NetworkPassesPerEpoch -> I guess better for our analysis
    2. Hardware Burden: Processors * ComputationRate * Time
- polynomial growth in computing per performance
- algorithmic efficiency improved, but not enough for inflation in computational burden


https://medium.com/walmartglobaltech/computational-complexity-of-deep-learning-a-birds-eye-view-2250b7c098a1

- idea: Test GPU vs CPU?






----






95831 images

Ganz normales Laden, Code Beispiel, 16 Byte pro Pixel, 272 Byte für Datenstruktur
-> np.float64 hat schonmal 8 Byte


Loading image normally, as expected, the numpy array containing the values for the pixels has about 1MB. However, normalizing necessary -> np.float64 (8 Bytes)