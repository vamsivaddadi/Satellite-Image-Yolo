# Building detecting in SatelliteImage using YoloV8

This repository contains of the script for the performaing building predictions on the satellite image using the weights and image provided.

As the image is too large the model may not perform well as it might over look the edges in the image so the image has been divided into patches for better predictions of the size (512,512,3) with a consider overlap to avoid any loss of edges in the images which might mis-classify.

For this project **Ultralytics** library is used.

We perform predictions on each patch and save the predcitions as an array. Once the predictions are completed then all the patches are used to reconstruct as the original image.

After few experiments with the conf value is set to 0.15.

The reconstructed image is as below:
![rec_pred (3)](https://github.com/vamsivaddadi/Satellite-Image-Yolo/assets/79320932/73c0fc2a-9b91-4faf-a7d8-6d2a55d8ba51)
