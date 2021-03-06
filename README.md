# VQ-VAE

This is a lightweight (200 loc) implementation of the VQ-VAE [Neural Discrete representation learning](https://arxiv.org/pdf/1711.00937.pdf).  
[TensorComprehensions](https://github.com/facebookresearch/TensorComprehensions) is used 
to reduce memory required to calculate distance to embeddings.  

A sensitivity term is introduced, to make all embeddings used. A sensitivity is substracted from a distance to embedding that is not used for some time. Before finding minimum distance.

## requirements
 - Python 3.6 
 - PyTorch 0.3
 - TensorComprehensions

# Training
By default it trains on cifar10

```
python vq-vae-img.py
```
Edit hyperparams, paths in source code to train on ImageNet  

I used https://lera.ai to track model learning progress. It is off by default, use ``--lera`` to enable it.

### ImageNet reconstruction after 40k iterations (K=512, D=128)
![ImageNet](./imagenet.jpg)

# License
MIT
