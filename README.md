# Handwritten-Digits
基于Tensorflow的卷积神经网络实现Mnist手写数字识别

- 数据来源：[http://yann.lecun.com/exdb/mnist/](数据来源：http://yann.lecun.com/exdb/mnist/)

### 结构

#### 卷积层1
  - 卷积：32个filter，窗口5\*5，步长1，padding=“SAME”，输入[None, 28, 28, 1]，输出[None, 28, 28, 32]
  - 激活：[None, 28, 28, 32]
  - 池化：窗口2\*2，步长2，padding=“SAME”，输出[None, 14, 14, 32]
  
#### 卷积层2
  - 卷积：64个filter，窗口5\*5，步长1，padding=“SAME”，输入[None, 28, 28, 32]，输出[None, 28, 28, 64]
  - 激活：[None, 14, 14, 64]
  - 池化：窗口2\*2，步长2，padding=“SAME”，输出[None, 7, 7, 64]
  
#### 全连接层
  - [None, 7, 7, 64] * [7*7*64, 10] = [None, 10]
