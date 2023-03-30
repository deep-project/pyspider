
### 说明

###### 修改版的pyspider 使其适配更高版本的python 在centos7 + python3.9环境下测试通过。

###### 主要修改了async关键词冲突、固定了一些依赖的版本防止报错。

###### 给分组加了一个tabs切换，切换cf的cdn到字节跳动的cdn

--------------

### 使用方法

1.设置环境变量

    export PYCURL_SSL_LIBRARY=nss;
2.安装

    pip install git+https://github.com/deep-project/pyspider.git

3.启动

    pyspider

--------------

#### 　<font color=FF0000>目前推荐在3.9下运行，3.10以上需要手动修改 tornado源码</font>
```
tornado/httputil.py 106行
collections 改 collections.abc
```
也许还会有其他问题，暂时未测试。