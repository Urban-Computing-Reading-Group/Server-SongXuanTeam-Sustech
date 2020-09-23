# Server-SongXuanTeam-Sustech
## Commonly used command

<font color=#FF8C00>made by: </font> Kaiyue Zhang, Du Yin, Yicheng Zhao



* [<strong>常用Linux命令汇总</strong>](#%E5%B8%B8%E7%94%A8linux%E5%91%BD%E4%BB%A4%E6%B1%87%E6%80%BB)
  * [<strong>零：操作注意事项</strong>](#%E9%9B%B6%E6%93%8D%E4%BD%9C%E6%B3%A8%E6%84%8F%E4%BA%8B%E9%A1%B9)
  * [<strong>一：VPN</strong>](#%E4%B8%80vpn)
  * [<strong>二：服务器信息</strong>](#%E4%BA%8C%E6%9C%8D%E5%8A%A1%E5%99%A8%E4%BF%A1%E6%81%AF)
  * [<strong>三：常用命令</strong>](#%E4%B8%89%E5%B8%B8%E7%94%A8%E5%91%BD%E4%BB%A4)
    * [<strong>0 conda环境有关</strong>](#0-conda%E7%8E%AF%E5%A2%83%E6%9C%89%E5%85%B3)
      * [0\.1 <strong>创建环境，并且投射到jupyter的kernel去</strong>](#01-%E5%88%9B%E5%BB%BA%E7%8E%AF%E5%A2%83%E5%B9%B6%E4%B8%94%E6%8A%95%E5%B0%84%E5%88%B0jupyter%E7%9A%84kernel%E5%8E%BB)
      * [0\.2 <strong>tf安装</strong>](#02-tf%E5%AE%89%E8%A3%85)
      * [0\.3 <strong>torch安装</strong>](#03-torch%E5%AE%89%E8%A3%85)
    * [<strong>1 文件和目录相关操作</strong>](#1-%E6%96%87%E4%BB%B6%E5%92%8C%E7%9B%AE%E5%BD%95%E7%9B%B8%E5%85%B3%E6%93%8D%E4%BD%9C)
      * [1\.0 <strong>查看当前目录</strong>](#10-%E6%9F%A5%E7%9C%8B%E5%BD%93%E5%89%8D%E7%9B%AE%E5%BD%95)
      * [1\.1 <strong>给当前目录下所有文件授予最高权限，读写删除等</strong>](#11-%E7%BB%99%E5%BD%93%E5%89%8D%E7%9B%AE%E5%BD%95%E4%B8%8B%E6%89%80%E6%9C%89%E6%96%87%E4%BB%B6%E6%8E%88%E4%BA%88%E6%9C%80%E9%AB%98%E6%9D%83%E9%99%90%E8%AF%BB%E5%86%99%E5%88%A0%E9%99%A4%E7%AD%89)
      * [1\.2 <strong>解压文件，unzip，多个文件筛选</strong>](#12-%E8%A7%A3%E5%8E%8B%E6%96%87%E4%BB%B6unzip%E5%A4%9A%E4%B8%AA%E6%96%87%E4%BB%B6%E7%AD%9B%E9%80%89)
    * [<strong>2 jupyter notebook 操作</strong>](#2-jupyter-notebook-%E6%93%8D%E4%BD%9C)
      * [2\.0 <strong>第一次使用必读</strong>](#20-%E7%AC%AC%E4%B8%80%E6%AC%A1%E4%BD%BF%E7%94%A8%E5%BF%85%E8%AF%BB)
      * [2\.1 <strong>查看目前运行中的jupyter notebook server</strong>](#21-%E6%9F%A5%E7%9C%8B%E7%9B%AE%E5%89%8D%E8%BF%90%E8%A1%8C%E4%B8%AD%E7%9A%84jupyter-notebook-server)
      * [2\.2 <strong>关闭jupyter</strong>](#22-%E5%85%B3%E9%97%ADjupyter)
    * [<strong>3 进程查询，管理命令</strong>](#3-%E8%BF%9B%E7%A8%8B%E6%9F%A5%E8%AF%A2%E7%AE%A1%E7%90%86%E5%91%BD%E4%BB%A4)
      * [3\.1 <strong>查看当前运行的进程，</strong>](#31-%E6%9F%A5%E7%9C%8B%E5%BD%93%E5%89%8D%E8%BF%90%E8%A1%8C%E7%9A%84%E8%BF%9B%E7%A8%8B)
      * [3\.2 <strong>关闭jupyter 的方式一（推荐）</strong><strong>，10123为对应的jupyter notebook 的port</strong>](#32-%E5%85%B3%E9%97%ADjupyter-%E7%9A%84%E6%96%B9%E5%BC%8F%E4%B8%80%E6%8E%A8%E8%8D%9010123%E4%B8%BA%E5%AF%B9%E5%BA%94%E7%9A%84jupyter-notebook-%E7%9A%84port)
      * [3\.3 <strong>关闭jupyter的方式二 :kill pid</strong>（建议不要使用，高危，可能会杀掉其他重要进程）](#33-%E5%85%B3%E9%97%ADjupyter%E7%9A%84%E6%96%B9%E5%BC%8F%E4%BA%8C-kill-pid%E5%BB%BA%E8%AE%AE%E4%B8%8D%E8%A6%81%E4%BD%BF%E7%94%A8%E9%AB%98%E5%8D%B1%E5%8F%AF%E8%83%BD%E4%BC%9A%E6%9D%80%E6%8E%89%E5%85%B6%E4%BB%96%E9%87%8D%E8%A6%81%E8%BF%9B%E7%A8%8B)
    * [<strong>4\. 查看CPU，物理内存(RAM)，硬盘内存(ROM)，显卡使用情况</strong>](#4-%E6%9F%A5%E7%9C%8Bcpu%E7%89%A9%E7%90%86%E5%86%85%E5%AD%98ram%E7%A1%AC%E7%9B%98%E5%86%85%E5%AD%98rom%E6%98%BE%E5%8D%A1%E4%BD%BF%E7%94%A8%E6%83%85%E5%86%B5)
      * [4\.0 <strong>动态查看</strong>](#40-%E5%8A%A8%E6%80%81%E6%9F%A5%E7%9C%8B)
      * [4\.1 <strong>查看CPU运行情况</strong>](#41-%E6%9F%A5%E7%9C%8Bcpu%E8%BF%90%E8%A1%8C%E6%83%85%E5%86%B5)
      * [4\.2 <strong>查看内存大小（按G）</strong>](#42-%E6%9F%A5%E7%9C%8B%E5%86%85%E5%AD%98%E5%A4%A7%E5%B0%8F%E6%8C%89g)
      * [4\.3 <strong>查看当前目录下所有子目录文件夹每个文件夹的硬盘空间占用大小：</strong>](#43-%E6%9F%A5%E7%9C%8B%E5%BD%93%E5%89%8D%E7%9B%AE%E5%BD%95%E4%B8%8B%E6%89%80%E6%9C%89%E5%AD%90%E7%9B%AE%E5%BD%95%E6%96%87%E4%BB%B6%E5%A4%B9%E6%AF%8F%E4%B8%AA%E6%96%87%E4%BB%B6%E5%A4%B9%E7%9A%84%E7%A1%AC%E7%9B%98%E7%A9%BA%E9%97%B4%E5%8D%A0%E7%94%A8%E5%A4%A7%E5%B0%8F)
      * [4\.4 <strong>查看当前目录文件夹所占用的硬盘空间大小：</strong>](#44-%E6%9F%A5%E7%9C%8B%E5%BD%93%E5%89%8D%E7%9B%AE%E5%BD%95%E6%96%87%E4%BB%B6%E5%A4%B9%E6%89%80%E5%8D%A0%E7%94%A8%E7%9A%84%E7%A1%AC%E7%9B%98%E7%A9%BA%E9%97%B4%E5%A4%A7%E5%B0%8F)
      * [4\.5 <strong>查看所有存储设备的使用情况：</strong>](#45-%E6%9F%A5%E7%9C%8B%E6%89%80%E6%9C%89%E5%AD%98%E5%82%A8%E8%AE%BE%E5%A4%87%E7%9A%84%E4%BD%BF%E7%94%A8%E6%83%85%E5%86%B5)
      * [4\.6 <strong>查看显卡：</strong>](#46-%E6%9F%A5%E7%9C%8B%E6%98%BE%E5%8D%A1)
      * [4\.7 <strong>动态查看NVIDIA显卡使用情况，0\.1为刷新频率（s）</strong>](#47-%E5%8A%A8%E6%80%81%E6%9F%A5%E7%9C%8Bnvidia%E6%98%BE%E5%8D%A1%E4%BD%BF%E7%94%A8%E6%83%85%E5%86%B501%E4%B8%BA%E5%88%B7%E6%96%B0%E9%A2%91%E7%8E%87s)
    * [<strong>5 conda有关命令</strong>](#5-conda%E6%9C%89%E5%85%B3%E5%91%BD%E4%BB%A4)
      * [5\.1 <strong>查询conda环境</strong>](#51-%E6%9F%A5%E8%AF%A2conda%E7%8E%AF%E5%A2%83)
      * [5\.2 <strong>conda环境进入和退出</strong>](#52-conda%E7%8E%AF%E5%A2%83%E8%BF%9B%E5%85%A5%E5%92%8C%E9%80%80%E5%87%BA)
      * [5\.3 <strong>conda删除虚拟环境：</strong>](#53-conda%E5%88%A0%E9%99%A4%E8%99%9A%E6%8B%9F%E7%8E%AF%E5%A2%83)
      * [5\.4 <strong>conda环境克隆移植：</strong>](#54-conda%E7%8E%AF%E5%A2%83%E5%85%8B%E9%9A%86%E7%A7%BB%E6%A4%8D)
    * [<strong>6 传文件</strong>](#6-%E4%BC%A0%E6%96%87%E4%BB%B6)
      * [6\.1 <strong>SCP传文件：</strong>](#61-scp%E4%BC%A0%E6%96%87%E4%BB%B6)
      * [6\.2 <strong>http传文件</strong>](#62-http%E4%BC%A0%E6%96%87%E4%BB%B6)

### <font color=#FF0000>**常用Linux命令汇总**</font>

#### <font color=#FF0000>**零：操作注意事项**</font>

<font color=#FF0000>禁止随意使用shotdown，reboot，rm -rf 等命令，请提高安全意识。如果有不确定的命令，请先联系其他人！不要自己操作！</font>

操作建议：

1. 在`/home/cseadmin/`路径下建立自己`姓名`为名字的文件夹，在自己文件夹空间内进行操作。
2. 不要非conda环境下(base)改动各种库，共用的`tf`和`torch`的几个环境（`tf1.14`、`torch1.3`等）不要改动，如果需要改动，请告知，以防紊乱。
3. 如果有自己的需求，可以自己建立自己的conda虚拟环境后在里面使用。公共的tf和torch可以大家公用。
4. 下文中标有\*your_name\*或是\*your_port\*的命令，请大家注意替换成自己的文件夹名或是端口号。但可能仍有部分命令没有注意替换，请大家多多注意。

#### <font color=#FF0000>**一：VPN**</font>

南科大VPN
帐号：11930375
密码：咨询尹渡

#### **二：<font color=#FF0000>服务器</font>信息**

<font color=#FF0000>**由于ip信息保密，相关ip信息，如需使用咨询赵奕丞。**</font>

```powershell
虚拟服务器 1 号
ip: 
ssh端口: 10022
账号：cseadmin
密码：
```

```powershell
虚拟服务器 2 号
ip 
ssh端口 10022
账号：cseadmin
密码：
```

```powershell
jupyter:
ip:port
密码都为: 505505505
```

#### <font color=#FF0000>**三：常用命令**</font>

##### <font color=#FF0000>**0 conda环境有关**</font>

###### <font color=#FF0000>0.1 **创建环境，并且投射到jupyter的kernel去**</font>

运行两句话：（然后后面可以自己conda install所需要的库了）
**创建conda环境**，同时顺带着安装ipykernel，ipykernel用于直接下一步把该环境挂到jupyter notebook里的kernel中去:

```powershell
conda create -n tf1.14 python=3.7.7 ipykernel
```

将tf1.14的**conda环境映射**到jupyter notebook的kernel里去：

```powershell
python -m ipykernel install --user --name tf1.14 --display-name "tf1.14"
```

###### <font color=#FF0000>0.2 **tf安装**</font>

tf（以1.14为例），conda安装，会自动下载好对应的依赖包，除非conda环境不可行，才使用pip install

```powershell
conda install tensorflow-gpu==1.14
```

###### <font color=#FF0000>0.3 **torch安装**</font>

（1.3，1.4，1.5均可以conda install 安装，torch1.6安装使用pip install的方式。）
1.5版本以及以下，建议使用conda install 安装

```powershell
conda install pytorch=1.3 torchvision cudatoolkit=10.1 -c pytorch 
```

1.6版本的torch，建议使用pip设定对应的网址链接进行安装

```powershell
pip install torch==1.6.0+cu101 torchvision==0.7.0+cu101 -f https://download.pytorch.org/whl/torch_stable.html
```

##### <font color=#FF0000>**1 文件和目录相关操作**</font>

###### <font color=#FF0000>1.0 **查看当前目录**</font>

pwd

###### <font color=#FF0000>1.1 **给当前目录下所有文件授予最高权限，读写删除等**</font>

```powershell
sudo chmod -R 777 /home/cseadmin/
```

<font color=#FF8C00>注意事项：</font>
<font color=#FF8C00>1、避免跟人共用端口，自己多开并在QQ群的共享excel备注填写自己的port</font>
<font color=#FF8C00>2、日志文件不要跟其他人的路径重复了，注意把“yindu”修改成自己的名字，同时mkdir log ,
nohup 命令运行jupyter notebook 的log文件路径设置为/home/cseadmin/\*your_name\*/log/jupyter.log</font>

###### <font color=#FF0000>1.2 **解压文件，unzip，多个文件筛选**</font>

(开新端口后需要设置开通该端口的防火墙权限)

```powershell
unzip taxiGps20200618.zip -d /home/cseadmin/data/xmtask2/
```

<font color=#FF0000>批量解压：</font>

```powershell
find . -name 'wycGps*.zip' -exec unzip -d /home/cseadmin/data/xmtask2/  {} \;
```

##### <font color=#FF0000>**2 jupyter notebook 操作**</font> 

###### <font color=#FF0000>2.0 **第一次使用必读**</font>

<font color=#FF0000>注意事项：</font>
<font color=#FF8C00>1、避免跟人共用端口，自己多开并在QQ群的共享excel备注填写自己的port，例如，10123</font>
<font color=#FF8C00>2、日志文件不要跟其他人的路径重复了，注意把“yindu”修改成自己的名字，同时mkdir log ,
nohup 命令运行jupyter notebook 的log文件路径设置为/home/cseadmin/\*your_name\*/log/jupyter.log</font>

<font color=#FF0000>查询端口是否使用：</font> 

```powershell
netstat -anp |grep 10123
```

<font color=#FF0000>第一次运行jupyter需要用到的命令：</font>

由于需要对新开端口进行开放防火墙权限，所以需要运行以下命令：

```powershell
sudo firewall-cmd --zone=public --add-port=10123/tcp --permanent
sudo firewall-cmd --reload
```

<font color=#FF0000>后面运行只用运行nohup jupyter notebook ...这个就好了：</font>

```python
nohup jupyter notebook --no-browser --port=10123 > /home/cseadmin/yindu/log/jupyter.log 2>&1 &
```

###### <font color=#FF0000>2.1 **查看目前运行中的jupyter notebook server**</font>

```python
jupyter notebook list


步骤1：ps -aux | grep jupyter 查看PID
步骤2：kill -9 pid
eg：首先运行ps -aux | grep jupyte 命令，会有如下图（请双击放大）：
第一个框框是命令，第二个左下的框框数字121068就是pid号，第三个框框右下的代表着运行的jupyter port为23333的用户，查群共享文件的excel文件可以看到这是雷天健小朋友在用，
那么关闭这个jupyter的命令就为：
kill -9 121068
```

###### <font color=#FF0000>2.2 **关闭jupyter** </font>

10123为自己设定的自己的jupyter port号

```powershell
fuser -k 10123/tcp
```

##### <font color=#FF0000>**3 进程查询，管理命令**</font>



###### <font color=#FF0000>3.1 **查看当前运行的进程，**</font>

```
ps -l
ps -ef
ps -aux
```

<font color=#FF8C00>--查看jupyter的有关进程</font>

```
ps -aux | grep jupyter
```

###### <font color=#FF0000>3.2 **关闭jupyter 的方式一（推荐）**</font>**，10123为对应的jupyter notebook 的port**

```python
fuser -k 8785/tcp
```

###### <font color=#FF0000>3.3 **关闭jupyter的方式二 :kill pid**</font>（建议不要使用，高危，可能会杀掉其他重要进程）

<font color=#FF0000>步骤1：</font>查看PID

```powershell
ps -aux | grep jupyter 
```

<font color=#FF0000>步骤2：</font>根据查询到的pid杀死对应的进程

```powershell
kill -9 pid
```

<font color=#FF0000>eg：</font>首先运行ps -aux | grep jupyte 命令，会有如下图（请双击放大）：

​      第一个框框是命令，第二个左下的框框数字121068就是pid号，第三个框框右下的代表着运行的jupyter port为23333的用户，查群共享文件的excel文件可以看到这是雷天健小朋友在用，      ![img](https://docimg3.docs.qq.com/image/BNbT9yU_PXwDgnjr8UNmcQ?w=2048&h=980)            

那么关闭这个jupyter的命令就为：

```powershell
kill -9 121068
```

##### <font color=#FF0000>**4. 查看CPU，物理内存(RAM)，硬盘内存(ROM)，显卡使用情况**</font>

###### <font color=#FF0000>4.0 **动态查看**</font>

```python
watch -n 0.5 nvidia-smi
```

**一般来说自己运行显卡运算的程序，需要先查询显卡占用情况，**

###### <font color=#FF0000>4.1 **查看CPU运行情况**</font>

```
top
```

退出 top 的命令为 q （在 top 运行中敲 q 键一次），或者Ctrl+C

###### <font color=#FF0000>4.2 **查看内存大小（按G）**</font>

```powershell
free -g              g代表按照G来查看内存，m则代表m来查看内存
或者
free -h
```

###### <font color=#FF0000>4.3 **查看当前目录下所有子目录文件夹每个文件夹的硬盘空间占用大小：**</font>

```powershell
du -sh *
```

###### <font color=#FF0000>4.4 **查看当前目录文件夹所占用的硬盘空间大小：**</font>

```powershell
du -h --max-depth=0
```

###### <font color=#FF0000>4.5 **查看所有存储设备的使用情况：**</font>

```powershell
df -h
```

###### <font color=#FF0000>4.6 **查看显卡：**</font>

```powershell
nvidia-smi
```

###### <font color=#FF0000>4.7 **动态查看NVIDIA显卡使用情况，0.1为刷新频率（s）**</font>

```powershell
watch -n 0.1 nvidia-smi
```

同样的，以此类比，动态查看内存占用情况为：

```powershell
watch -n 0.5 free -g
```

##### <font color=#FF0000>**5 conda有关命令**</font>

###### <font color=#FF0000>5.1 **查询conda环境**</font>

```powershell
conda env list 
或者：
conda info -e
```

###### <font color=#FF0000>5.2 **conda环境进入和退出**</font>

<font color=#FF0000>第一次激活</font>为：（env为环境名字）

```powershell
conda activatet tf1.13
或者：
source activate tf1.13
```

<font color=#FF0000>第二次及以后</font>进入为：

```powershell
source activate tf1.13
```

<font color=#FF0000>退出</font>为：

```powershell
source deactivate
或者：
conda deactivate
```

###### <font color=#FF0000>5.3 **conda删除虚拟环境：**</font>

```powershell
conda remove -n tf1.13 --all
```

###### <font color=#FF0000>5.4 **conda环境克隆移植：**</font>

自己琢磨或者问尹渡。

##### <font color=#FF0000>**6 传文件**</font>

###### <font color=#FF0000>6.1 **SCP传文件：**</font>

（比如当前服务器为136服务器，要传输一个文件目录到171，命令如下）

```powershell
scp -P 10022 -r /home/cseadmin/anaconda3/envs/haru cseadmin@10.20.48.171:/home/cseadmin/anaconda3/envs/haru
```

###### <font color=#FF0000>6.2 **http传文件**</font>

服务器上设置http服务器传文件：（<font color=#FF0000>需要进入到需要传输的文件夹目录下，在该文件夹目录下执行以下命令</font>）

```powershell
python3 -m http.server
```



