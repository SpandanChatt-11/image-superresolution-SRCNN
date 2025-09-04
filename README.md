# Image Super Resolution using SRCNN
In today’s digital world, the demand for high-quality images is everywhere — from medical imaging to satellite monitoring and even restoring old photographs. However, 
many times we only have access to low-resolution images, which makes it difficult to extract fine details. This project focuses on Single Image Super-Resolution (SISR) 
using a Super-Resolution Convolutional Neural Network (SRCNN), one of the earliest deep learning models for image enhancement. 
The central idea is simple: given a blurry, low-resolution image, can we reconstruct a sharper and more detailed version of it? To achieve this, we first degrade high
resolution benchmark images by downscaling and then apply bilinear interpolation to bring them back to the original size. These serve as the input to the SRCNN model, 
which is trained to minimize the difference between its output and the true high resolution image. Importantly, the model operates on the Y channel (luminance) of 
the YCrCb color space, since this channel holds most of the structural details that the human eye is sensitive to. 
The network consists of three layers — patch extraction, non-linear mapping, and reconstruction — which progressively learn to capture edges, textures, and fine 
structures. The quality of results is measured using metrics like PSNR (Peak Signal to-Noise Ratio) and MSE (Mean Squared Error), showing that SRCNN significantly 
improves the clarity of degraded images. Experiments on regular, medical, and satellite images highlight its effectiveness in recovering details that traditional 
interpolation methods often fail to preserve. In conclusion, this project demonstrates how deep learning can be used to breathe new life into low-quality images. While SRCNN is a foundational model, it opens the 
door to more advanced super-resolution techniques, which hold immense potential for real-world applications such as medical diagnosis, surveillance, and scientific research.
