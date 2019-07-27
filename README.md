

![Neural3DMM architecture](images/architecture_figure1.png "Neural3DMM architecture")

# Project Abstract 
*Generative models for 3D geometric data arise in many important applications in 3D computer vision and graphics. In this paper, we focus on 3D deformable shapes that share a common topological structure, such as human faces and bodies. Morphable Models were among the first attempts to create compact representations for such shapes; despite their effectiveness and simplicity, such models have limited representation power due to their linear formulation. Recently, non-linear learnable methods have been proposed, although most of them resort to intermediate representations, such as 3D grids of voxels or 2D views. In this paper, we introduce a convolutional mesh autoencoder and a GAN architecture based on the spiral convolutional operator, acting directly on the mesh and leveraging its underlying geometric structure. We provide an analysis of our convolution operator and demonstrate state-of-the-art results on 3D shape datasets compared to the linear Morphable Model and the recently proposed COMA model.* 

[Paper Arxiv Link](https://arxiv.org/abs/1905.02876)


# Repository Requirements

This code was written using Pytorch 0.4.1, however should run with Pytorch 1.0 as well. We use tensorboardX for the training metrics. We recommend setting up a virtual environment using [Miniconda](https://docs.conda.io/en/latest/miniconda.html) and specifically with Python2 (we need Python 2 not for training but for the downsampling and upsampling, see below). To install Pytorch in a conda environment simply run 

```
$ conda install pytorch torchvision -c pytorch
```

Then the rest of the requirements can be installed with 

```
$ pip install -r requirments.txt
```


### Downsampling & Upsampling
For the downsampling code we use a function from the [COMA repository](https://github.com/anuragranj/coma) which in turn uses the [MPI-Mesh](https://github.com/MPI-IS/mesh) package (a mesh library similar to Trimesh or Open3D). This package requires Python 2, which is why we recommend doing everything with Python 2. However once you have cached the generated downsampling and upsampling matrices, it is possible to run the training code with Python 3 as well if necessary. In order to install MPI-Mesh do the following (or read their installation instructions if something is unclear):

```
$ git clone https://github.com/MPI-IS/mesh.git
$ apt-get install libboost-all-dev
$ make
$ make install
```




# Data Organization

The following is the organization of the dataset directories expected by the code:

* data_root
  * dataset_name (eg DFAUST)
    * 


# Running the Code



1. pytorch
``conda install pytorch torchvision -c pytorch
``

2. tensorboardX
``
pip install tensorboardX
``

3. Mpi-mesh
``
git clone https://github.com/MPI-IS/mesh.git
``

``
apt-get install libboost-all-dev
``

``
make
``

``
make install
``

OR

4. trimesh
``
pip install trimesh
``

6. pip install -r requirements.txt