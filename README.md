# Federated_Learning
夏季学期第八组实现的简易联邦学习。复现方法如下：


## 一、运行环境
各台设备必须运行在同一个局域网之下。
## 二、服务端
1.安装python3.6、pip3，并运行以下依赖包：
```python
pip3 install -U MNN
pip3 install cherrypy
pip3 install ws4py
```
2.运行server.py
## 三、客户端
1.数据和初始化模型通过命令行工具adb下载到Android设备本地
```
cd End2end-Federated-Learning/data
adb push mnist.snapshot.mnn /data/local/tmp/mnn/mnist.snapshot.mnn
adb push mnist_data /data/local/tmp/mnist_data
```
2.修改app/src/main/java/com/demo/MainActivity.java中的SERVER_URL为服务端的ip地址

3.连接android设备，并运行项目（必须和服务端在同一个局域网下才能正常运行）
