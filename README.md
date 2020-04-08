[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

<h1 align="center"> ~ Multi-Frame Super-Resolution Task ~ </h1>

![RAMS logo](media/proba_v_dataset_logo.png)

Are you a Deep Learning practitioner, but you are tired of dealing with Cats and Dogs datasets? Do you want to work on a real problem with a high impact on the research community, but it is always tricky to get your hand's on the final preprocessed data? If that's the case, you are in the right place!

We created this repository for two primary reasons:

- Give easy access to a unique [dataset](https://kelvins.esa.int/proba-v-super-resolution/data/), introduced by ESA in 2019, to work on the very challenging task of multi-frame super-resolution. If you've never heard about this computer vision task,[this survey](https://ieeexplore.ieee.org/abstract/document/8782382) could help you. Anyway, in a few words, its aim is pretty intuitive and straightforward: reconstruct a high-resolution image from a set of low-resolution frames. So, with a practical and easy to use [jupyter notebook](https://github.com/EscVM/RAMS/blob/master/preprocessing_dataset.ipynb) we give you the possibility to preprocess this [dataset](https://kelvins.esa.int/proba-v-super-resolution/data/) and dive directly into the design of your methodology. It's a very flexible pipeline where all steps can be easily omitted. All data are included with this repository, already split in train validation and testing. At the end of the process you will have three primary tensors: **X** with shape (B, 128, 128, T), **y** with shape (B, 384, 384, 1), and **y_mask** with shape (B, 384, 384, 1) with the quality maps of the ground-truths in y. Your task is straightforward...find a way to turn X into y. In other words, fuse the T images at 128x128, for each scene B, and get a corresponding image 384x384 at the triple of the resolution. It's a very challenging and fascinating task with a significant impact on the work of many peer researchers, but not yet so investigated.

- Give access to our pre-trained solution (currently unavailable) that me and [fsalv](https://github.com/fsalv) in a joint effort we have conceptualized and implemented. We've tested and proved our ideas with a joint account under the name of our robotics lab [PIC4SeR](https://pic4ser.polito.it/) in the post-mortem challenge of the [ESA website](https://kelvins.esa.int/proba-v-super-resolution-post-mortem/leaderboard/). Yes, because what is beautiful about this dataset is that you can still prove your effort submitting your results directly on the [ESA website](https://kelvins.esa.int/proba-v-super-resolution-post-mortem/home/). On the other hand, you can use the validation we provide inside this repository to directly compare your signs of progress with the [original winner](https://github.com/diegovalsesia/deepsum) of the ESA challenge. So, in any case, you will have direct feedback on your efforts and prove your ability with machine learning and deep learning projects!

Good Luck!

<p align="center">
<img src="media/misr_task.png" >
</p>
