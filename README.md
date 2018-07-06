项目描述：
    * 本项目意在对图像中的logo的位置和大小进行定位，然后根据inpaiting算法，对logo进行去除和图像修复。
算法描述：1、定位算法是调用主图识别服务接口，获取logo的坐标信息。
          2、对第一步定位到的logo区域用大小相同的全白图片进行填充，即遮挡了logo，但是此时的图像需要修复。
          3、图像修复，在tensorflow框架下利用GAN进行图像修复。

inpainting——project_location:：
           *231：/data1/storage_proxy/bucket_private_global/dl_project/data/inpainting

0. install:
    * Install python3.
    * Install [tensorflow](https://www.tensorflow.org/install/) (tested on Release 1.3.0, 1.4.0, 1.5.0, 1.6.0, 1.7.0).
    * Install tensorflow toolkit [neuralgym](https://github.com/JiahuiYu/neuralgym) (run `pip install git+https://github.com/JiahuiYu/neuralgym`).

1.data:
   * KZ nologo data and  same coco datas (http://cocodataset.org/#download)   

2.train：
   * Prepare training images 
   * Run `python3 train.py`.

3.test:
   * Run `python3 test0626.py`.
