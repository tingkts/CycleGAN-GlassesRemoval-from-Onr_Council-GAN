Forked from [Onr/Council-GAN](https://github.com/Onr/Council-GAN). Demo it in Windows 10.

</br>

__**Environment**__ :


&ensp; Windows 10

&ensp; NVIDIA GeForce GTX 1050 Ti

&ensp; CUDA 11.0：

```
λ nvcc --version
nvcc: NVIDIA (R) Cuda compiler driver
Copyright (c) 2005-2020 NVIDIA Corporation
Built on Wed_Jul_22_19:09:35_Pacific_Daylight_Time_2020
Cuda compilation tools, release 11.0, V11.0.221
Build cuda_11.0_bu.relgpu_drvr445TC445_37.28845127_0
```

&ensp; cuDNN 8.0.5：

```
C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.0\include
λ cat cudnn_version.h

#define CUDNN_MAJOR 8
#define CUDNN_MINOR 0
#define CUDNN_PATCHLEVEL 5

#define CUDNN_VERSION (CUDNN_MAJOR * 1000 + CUDNN_MINOR * 100 + CUDNN_PATCHLEVEL)
```

&ensp; Python env. ：

```
(Onr-Council-GAN) λ python -V
Python 3.6.13 :: Anaconda, Inc.

(Onr-Council-GAN) λ pip -V
pip 21.3.1 from A:\IDE\Anaconda3\envs\Onr-Council-GAN\lib\site-packages\pip (python 3.6)
```

&ensp; [conda environment.yml](./environment.yml)

&ensp; [pip requirements.txt](./requirements.txt)

&ensp;&ensp; * &nbsp;require to install [cmake](./cmake-3.22.1-windows-x86_64.msi) for [dlib](./dlib-19.8.1-cp36-cp36m-win_amd64.whl) installation.

</br>

__**Usage**__ ：

glasses removal :
```python
python test_gui.py --config pretrain/glasses_removal/128/galsses_council_folder.yaml --checkpoint pretrain/glasses_removal/128/a2b_gen_3_01000000.pt --a2b 1
```


</br>

__**Issue**__ ：

- [UnicodeDecodeError: 'cp950' codec can't decode byte 0xf0 in position 920: illegal multibyte sequence](https://www.google.com/search?q=UnicodeDecodeError%3A+%27cp950%27+codec+can%27t+decode+byte+0xf0+in+position+920%3A+illegal+multibyte+sequence&rlz=1C1GCEU_zh-TWTW892TW892&oq=UnicodeDecodeError%3A+%27cp950%27+codec+can%27t+decode+byte+0xf0+in+position+920%3A+illegal+multibyte+sequence&aqs=chrome..69i57j69i58.1056j0j7&sourceid=chrome&ie=UTF-8)


</br>
</br>

----
Ref ：

- [[筆記][CVPR2020] Council-GAN: Breaking the cycle — Colleagues are all you need | by Mackerel Chang | Medium](https://iomanker.medium.com/%E7%AD%86%E8%A8%98-cvpr-2020-council-gan-breaking-the-cycle-colleagues-are-all-you-need-d0003ae75864)

</br>

Misc. ：

- [pip 文件损坏导致 pip无法使用 报错 ImportError: cannot import name 'main' from 'pip._int](https://blog.csdn.net/weixin_40040107/article/details/102581918)

```
    1、 首先执行命令：

            python -m ensurepip --default-pip

    2、 下载 get-pip.py 文件 地址为

            https://bootstrap.pypa.io/get-pip.py

    3、 最后从命令行进入到 get-pip.py 所在的目录，执行命令 ：

            python get-pip.py

        注意 此步骤执行的时候可能会报出权限错误， 此时应执行

            python get-pip.py  --user

    执行 pip --version 查看pip是否安装完成
```

- [Windows 系统查看 CUDA 和 cuDNN 版本_wangpan007的博客-CSDN博客_windows查看cudnn版本](https://blog.csdn.net/wangpan007/article/details/106788268)