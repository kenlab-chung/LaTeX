# TexLive

## linux下安装TexLive(以ubuntu16.04为例)

### 1. 访问以下网址下载texlive的ISO文件
```
http://ftp.math.purdue.edu/mirrors/ctan.org/systems/texlive/Images/
https://mirrors.tuna.tsinghua.edu.cn/CTAN/systems/texlive/Images/
```

### 2. 安装per组件
```
sudo apt-get install perl-tk
```

### 3. 加载该ISO文件
```
sudo mount -o loop texlive2018.iso /mnt
```
### 4. 
```
cd /mnt
sudo ./install-tl -gui
```
点击安装即可。

配置环境变量
具体方法：
```
sudo gedit ~/.bashrc
```

在最后添加以下内容：
```
export MANPATH=${MANPATH}:/usr/local/texlive/2019/texmf-dist/doc/man
export INFOPATH=${INFOPATH}:/usr/local/texlive/2019/texmf-dist/doc/info
export PATH=${PATH}:/usr/local/texlive/2019/bin/x86_64-linux
```
然后`ctrl + s`保存退出，输入`source ~/.bashrc`使更改生效。

### 5. 中文支持，需要使用\usepackage{xeCJK}包，需安装
```
sudo apt-get install texlive-lang-chinese
```

### 6. 使用更多软件包和字体进行更完整的安装
```
sudo apt-get install texlive-latex-base texlive-latex-extra 
texlive-latex-recommended texlive-fonts-recommended
```
### 7. 安装XeLatex
```
sudo apt-get install texlive-xetex
```
### 8. 安装texstudio编辑器
```
sudo apt-get install texstudio
```
