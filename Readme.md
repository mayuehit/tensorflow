[toc]
#### 一、vsCode搭建python环境
下载python https://www.python.org/downloads/
#### 二、安装python插件
搜素python
#### 三、创建venv
py -m venv env_3_8_x, 虚拟环境对应的文件夹已经创建
#### 四、 激活虚拟环境
.\env_3_8_x\Scripts\activate
#### 五、退出
deactivate
#### 六、虚拟环境使用
python -V
#### 七、安装tensorflow pip包
pip install --upgrade tensorflow
太慢解决方法,指定源
pip install -i https://pypi.tuna.tsinghua.edu.cn/simple/ --upgrade tensorflow
#### 八、tensorflow使用
python -c "import tensorflow as tf; tf.enable_eager_execution(); print(tf.reduce_sum(tf.random_normal([1000, 1000])))"
#### 九、vsCode指定python Interpreter
为虚拟环境的python
#### 十、报错和解决
Could not load dynamic library 'cudart64_110.dll'; dlerror: cudart64_110.dll not found
pip list 查看tensorflow版本,降低版本，或者将cudart64_110.dll拷贝到C:/windows/system32
module 'tensorflow' has no attribute 'enable_eager_execution'
把tf.enable_eager_execution()删去就好。新版本不需要调用
#### 十一、交互式
pip install jupyter
python -m ipykernel install --user --name=env_3_8_x
jupyter notebook
#### 十二、更快速搭建环境的方法
docker pull  直接拉取tensorflow的环境镜像运行
#### 十三、开源中文字体识别项目
https://github.com/jjcheer/ocrcn_tf2
#### 十四、中文字体数据集
http://www.nlpr.ia.ac.cn/databases/handwriting/Home.html gnt格式
#### 十五、gnt格式可以转成png格式
https://blog.csdn.net/Vincent_Tong_/article/details/115241570
#### 十六、训练统一使用tfrecord格式
tfrecord格式介绍 https://blog.csdn.net/weixin_41558411/article/details/123456957
#### 十七、初始代码报错
pip install  -i https://pypi.tuna.tsinghua.edu.cn/simple  alfred-py
pip install  -i https://pypi.tuna.tsinghua.edu.cn/simple  opencv-python
pip install  -i https://pypi.tuna.tsinghua.edu.cn/simple tensorflow_datasets
修复代码bug  e.with_traceback()-> e.with_traceback(None)