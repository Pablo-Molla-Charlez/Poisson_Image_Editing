# Poisson Image Editing

This is a Python implementation of the [poisson image editing](https://www.cs.virginia.edu/~connelly/class/2014/comp_photo/proj2/poisson.pdf) paper to seamlessly blend two images, performed by user PPPW. My personal contributions refer to the application of such method into the IAD (Industrial Anomaly Detection) field, in particular, using the technique to data augment the number of current samples in the AeBAD (Aero-engine Blade Anomaly Detection Dataset) Dataset. 

![](figs/example1/Poisson_Editing_Example_Hazelnut.png)

For example, in order to create more realistic and elaborated anomaly images given the original mask (label), the original anomalous image and a non-anomalous image in which we want to integrate the anomaly. Then the Poisson image editing process will start and the images named as `new_anomaly_mask_000.png` (ground_truth image) and `new_anomaly_000.png` (new anomalous image), are saved in the corresponding directory as specified in the variable `base_dir`. 


## Folders and Files within the Repository
Here's a brief description of each file's functionality:

* `main.py`: take command line argument and call `paint_mask.py`, `move_mask.py` and `poisson_image_editing.py`. 

* `paint_mask.py`: pop up a window for drawing the mask on the source image.

* `move_mask.py`: pop up a window for adjusting the mask location on the target image.

* `poisson_image.editing.py`: take source, target, mask image and mask offset, run the Poisson image editing algorithm for seamless image blending. 

* `poisson_image.editing.ipynb`: a notebook demonstrating the process. 
