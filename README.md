# Poisson Image Editing

This repository contains a Python implementation of the [Poisson Image Editing](https://github.com/Pablo-Molla-Charlez/Poisson_Image_Editing/blob/master/Poisson_Image_Editing_Paper.pdf) paper, which allows for seamless blending of two images. This implementation is provided by user PPPW.

My personal contributions involve applying this method to the field of Industrial Anomaly Detection (IAD). Specifically, I use this technique for data augmentation on the MVTec Anomaly Dataset to enhance the model's learning capabilities in [AnomalyGPT](https://github.com/Pablo-Molla-Charlez/AnomalyGPT). The MVTec AD dataset is designed for benchmarking anomaly detection methods, focusing on industrial inspection. It contains over 5000 high-resolution images across 15 different object and texture categories. Each category includes defect-free training images and a test set with various defects and non-defective images.

\begin{center}
\includegraphics[width=\textwidth]{figs/example1/MVTec-AD.png}
\end{center}

\begin{center}
\includegraphics[width=\textwidth]{figs/example1/Poisson_Editing_Example_Hazelnut.png}
\end{center}

To create more realistic and detailed anomaly images, the following elements are needed:
- The original mask (label) describing the anomaly location.
- The original anomalous image.
- A non-anomalous image where the anomaly will be integrated.

The Poisson image editing process will then generate `new_anomaly_mask_000.png` (ground_truth image) and `new_anomaly_000.png` (new anomalous image), which will be saved in the directory specified by the `base_dir` variable.

## Repository Structure

A brief description of each file's functionality:

* `poisson_image_editing.py`: Takes the source, target, and mask images along with the mask offset, and runs the Poisson image editing algorithm for seamless image blending.

* `poisson_image_editing.ipynb`: A notebook demonstrating the process.
