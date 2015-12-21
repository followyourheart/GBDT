# GBDT

参考了[bluekingsong](https://github.com/bluekingsong/simple-gbdt)和[qiyiping](https://github.com/qiyiping/gbdt)的实现  

实现了regression、binary classification、multi-calss classification

相关公式可以参考我整理的[GBDT.ipynb文件](http://nbviewer.ipython.org/github/liudragonfly/GBDT/blob/master/GBDT.ipynb)

在data目录下提供了一个测试数据集


# 注：
因为Python 2.7 和 3.*对于metaclass的处理不一样，直接在Python2.7上使用此代码会出现Bug。可将
```
class RegressionLossFunction(metaclass=abc.ABCMeta):
```

改成

```
class RegressionLossFunction:
    __metaclass__ = abc.ABCMeta
```

```
class ClassificationLossFunction(metaclass=abc.ABCMeta):
```

改成

```
class ClassificationLossFunction:
    __metaclass__ = abc.ABCMeta
```
