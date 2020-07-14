---
layout: post
title: "Getting Started PyTorch in Google Colab"
categories: ml
author:
- Yi Zhang
---
 
## [Google Colab](https://research.google.com/colaboratory/faq.html)

Notebooks run by connecting to virtual machines (VM) that have **maximum lifetimes** that can be as much as **12 hours**. Maximum VM lifetime and idle timeout behavior may vary over time, or based on your usage. In Colab

* Connect

  `Coonect to hosted runtime ` vs `Connect to local runtime`

* `None` vs `GPU` or `TPU`

  `Edit`,  `Notebook settings` , `Hardware accelerator`

* `!` command, e.g.,

  ```
  !nvidia-smi
  ```

* `%` command, e.g.,

  ```
  %matplotlib inline
  ```



## Install PyTorch and Torchvision

In Colab

```
!pip install http://download.pytorch.org/whl/cu92/torch-0.4.1-cp36-cp36m-linux_x86_64.whl
!pip install torchvision
```



## Use Data From Google Drive

Copy the required data file into Google Drive account. In Colab

```python
from google.colab import drive
drive.mount('/content/drive/')
```
