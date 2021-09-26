# Exercise 6: Instance Segmentation

## Setup

Create a `conda` environment for this exercise and activate it:

```
conda create -n 06_instance_segmentation python
conda activate 06_instance_segmentation
```

After entering this virtual environment, install pytorch, ipykernel and ipywidgets by using the following command

```
conda install pytorch torchvision torchaudio cudatoolkit=10.2 -c pytorch

conda install ipykernel

conda install -c conda-forge ipywidgets

jupyter nbextension enable --py widgetsnbextension --sys-prefix

conda install -c conda-forge matplotlib

conda install -c anaconda scipy

pip install tqdm h5py zarr pillow numpy imgaug==0.4.0 mahotas scikit-image tensorboard torchsummary
```

Start Jupyter within this environment:

```
jupyter notebook
```

...and continue with the instructions in the notebook.


## HOW-TO: Introduction to the exercise
---

- 1.foreground_segmentation.ipynb

    data: example_toy_data

    In this notebook, you will do semnatic segmentation on synthetical data and you will get in touch with the concept of early stopping and see how the learning rate, batch size and other hyperparameters influence your training process.

- 2.instance_segmentation.ipynb

    data: data_kaggle_test

    In this notebook, you will move from semnatic segmentation to instance segmetation. You will try to use different kinds of labels/annotations to train an UNet to do instance segmentation.

- 3.tile_and_stitch.ipynb

    data: data_kaggle_test

    pretrained_net: net_60000

    This notebook is the extension of the instance_segmentation.ipynb notebook. You will just work on metric learning scenario. You will use an UNet with valid padding which has the periodic shift-equivariance property. This property helps to reduce the false splits when you deal with the large images in Tile & Stitch manner if you apply some specific rules.

- 4.epithelia_segmentation_challenge.ipynb 

    data: data_epithelia

    solution: example_epithelia_segmentation.ipynb

    In this notebook, you will do similar jobs as you work on instance_segmentation.ipynb notebook. But the dataset changes from kaggle dataset to epithelia dataset.

Please look into the respective .ipynb file to see the details. For some exercise, it would be better to run on GPU. 


