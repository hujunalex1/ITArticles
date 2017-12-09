---
style: plain
---
# Python 单元测试框架之Nose  

## 安装(以下2种方法)
### 1. pip install nose 

### 2. 下载安装包[下载地址](http://pypi.python.org/pypi/nose/) 
	* 解压 tar -zxvf nosexxxx 
	* python setup.py insatll
### 3. 测试是否安装成功 
	控制台中输入nosetests，有提示之类就证明哦了


## 实例 

### 1. 新增test.py文件，保存在E:\Temp\test 目录下

```
# coding=utf-8  


def setup():
	print "function setup"

def testfunction1():
	print "testfunction1"
	assert True 

def testfunction2():
	print "testfunction2"
	assert True 

def tearDown():
	print "function tearDown"

```
### 2. 当前目录在命令行下执行nosetests 即可。

### 3. 执行过程
	* nose实际的执行过程是这样的：　　
	* setUp()->Testfunc1()->Testfunc2()->tearDown()

## 参数 

* nosetests  –v :debug模式，看到具体执行情况 

* nosetests -s 即可看到调用顺序 

* nosetests --collect-only -v :不运行程序，只是搜集并输出各个case的名称

* nosetests -x  :一旦case失败立即停止，不执行后续case

* nosetests -w ，指定一个目录运行测试。目录可以是相对路径或绝对路径

* nosetests test.py 执行 test.py中的所有用例  

* nosetests test.py:testfunction1 执行test.py中的testfunction1用例

