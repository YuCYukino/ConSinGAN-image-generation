# ConSinGAN-image-generation  
## 实验环境  
Python 3.9  
### 需要的依赖包  
absl-py                 1.3.0  
albumentations          1.3.0  
cachetools              5.2.0  
certifi                 2022.12.7  
charset-normalizer      2.1.1  
colorama                0.4.6  
contourpy               1.0.6  
cycler                  0.11.0  
fonttools               4.38.0  
google-auth             2.15.0  
google-auth-oauthlib    0.4.6  
grpcio                  1.51.1  
idna                    3.4  
imageio                 2.23.0  
importlib-metadata      5.2.0  
joblib                  1.2.0  
kiwisolver              1.4.4  
Markdown                3.4.1  
MarkupSafe              2.1.1  
matplotlib              3.6.2  
networkx                2.8.8  
numpy                   1.23.5  
oauthlib                3.2.2  
opencv-python-headless  4.6.0.66  
packaging               22.0  
Pillow                  9.3.0  
pip                     21.2.3  
protobuf                3.20.3  
pyasn1                  0.4.8  
pyasn1-modules          0.2.8  
pyparsing               3.0.9  
python-dateutil         2.8.2  
PyWavelets              1.4.1  
PyYAML                  6.0  
qudida                  0.0.4  
requests                2.28.1  
requests-oauthlib       1.3.1  
rsa                     4.9  
scikit-image            0.19.3  
scikit-learn            1.2.0  
scipy                   1.9.3  
setuptools              57.4.0  
six                     1.16.0  
tensorboard             2.11.0  
tensorboard-data-server 0.6.1  
tensorboard-plugin-wit  1.8.1  
threadpoolctl           3.1.0  
tifffile                2022.10.10  
torch                   1.13.0+cu117  
torchaudio              0.13.0+cu117  
torchvision             0.14.0+cu117  
tqdm                    4.64.1  
typing_extensions       4.4.0  
urllib3                 1.26.13  
Werkzeug                2.2.2  
wheel                   0.38.4  
zipp                    3.11.0  
## 数据集下载  
单图片训练，任意图片均可，或从本项目的Image/Generation文件夹中选择  
## 运行方式  
将图片放进Image/Generation文件夹下，执行以下命令即可
```
python main_train.py --gpu 0 --train_mode generation --input_name Images/Generation/angkorwat.jpg
```  
如果想更改参数，例如更改学习率或训练阶段数目，只需执行下面代码  
```
python main_train.py --gpu 0 --train_mode generation --input_name Images/Generation/colusseum.png --lr_scale 0.5
```  
```
python main_train.py --gpu 0 --train_mode generation --input_name Images/Generation/colusseum.png --train_stages 7
```  
## 实验结果  
生成的图片详见报告，下面展示训练时长结果  
  
参数  | 训练时长  
 ---- | -----  
 默认参数  | 24.4min 
 lr_scale=0.5  | 24.4min 
 7个训练阶段  | 29.3min 
