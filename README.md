# `unrpa` - Extract files from the RPA archive format.

[![PyPI](https://img.shields.io/pypi/v/unrpa)](https://pypi.org/project/unrpa/) 
[![PyPI - Python Version](https://img.shields.io/pypi/pyversions/unrpa)](https://www.python.org/)
[![GitHub](https://img.shields.io/github/license/Lattyware/unrpa)](https://github.com/Lattyware/unrpa/blob/master/COPYING)
[![MyPy Check](https://github.com/Lattyware/unrpa/workflows/MyPy%20Check/badge.svg)](https://github.com/Lattyware/unrpa/actions?query=workflow%3A%22MyPy+Check%22)



简体中文|[English]()

## About

`unrpa`是从RPA格式文件中提取文件的工具 (关于细节可以查看[the Ren'Py Visual Novel Engine](http://www.renpy.org/)).

其可以被作为一个`library`使用

## 安装教程

### 通过Package manager(软件包管理器)

众所周知，安装一个`package`的最佳方法是通过软件包管理器，`unrpa`当然也是如此

我们为`Arch Linux`用户维护了一个[`unrpa`AUR软件包](https://aur.archlinux.org/packages/unrpa/)。

### 通过pip

您还可以通过`Python`软件包管理器pip安装`unrpa`。 您可以在`Windows`上执行以下操作：

    py -3 -m pip install "unrpa"


或者在`Unix`系统上使用`python3`而不是`py -3`

你可以查看[官方文档](https://packaging.python.org/tutorials/installing-packages/)以获得更多帮助。

### 从源代码安装source

你也可以下载[最新的发行版](https://github.com/Lattyware/unrpa/releases/latest)进行安装

## 依赖(Dependencies)

您需要`Python 3.7`或更高版本才能运行它**(**通过软件包管理器安装`Python`，也可以直接从[python.org](https://www.python.org/downloads/)安装**)**

如果您尝试更多的`RPA`存档，则可能需要安装其他依赖包
如果需要，`unrpa`会告诉我们如何安装它们

关于`unrpa`软件包维护者可以查看[`setup.py`](https://github.com/Lattyware/unrpa/blob/master/setup.py)以获取完整信息

### 一些例子

通过软件包管理器或`pip`安装后，你就可以通过打开终端或命令提示符并执行以下操作来使用`unrpa`：

    unrpa -mp "path/to/output/dir" "path/to/archive.rpa"

如果从源代码运行，则需要直接执行`python`:

 - 在大多数`unix`系统上，在包含`unrpa`的目录中打开一个终端，然后执行：

     `python3 -m unrpa -mp "path/to/output/dir" "path/to/archive.rpa"`
    
 - 在大多数`Windows`系统上，在包含`unrpa`的目录中打开命令提示符，然后执行：

       `py -3 -m unrpa -mp "path\to\output\dir" "path\to\archive.rpa"`

## 命令行的用法

```
usage: unrpa [-h] [-v] [-s] [-l | -t] [-p PATH] [-m] [--version]
             [--continue-on-error] [-f VERSION] [-o OFFSET] [-k KEY]
             FILENAME [FILENAME ...]
```

### Options

| 位置参数 | 作用描述                    |
| -------- | --------------------------- |
| FILENAME | 将要提取的`rpa`文件路径名字 |

| 可选参数             | 作用描述                                                     |
| -------------------- | ------------------------------------------------------------ |
| -h, --help           | 显示一些帮助信息并退出                                       |
| -v, --verbose        | explain what is being done, duplicate for more verbosity (default: 1). |
| -s, --silent         | 不输出没必要的信息                                           |
| -l, --list           | list the contents of the archive(s) in a flat list.          |
| -t, --tree           | list the contents of the archive(s) in a tree view           |
| -p PATH, --path PATH | extract files to the given path (default: the current working directory). |
| -m, --mkdir          | will make any missing directories in the given extraction path. |
| --version            | 查看版本号并退出                                             |

| 高级参数                    | 作用描述                                                     |
| --------------------------- | ------------------------------------------------------------ |
| --continue-on-error         | try to continue extraction when something goes wrong.        |
| -f VERSION, --force VERSION | ignore the archive header and assume this exact version. Possible versions: RPA-1.0, RPA-2.0, RPA-3.0, ALT-1.0, ZiX-12A, ZiX-12B, RPA-3.2, RPA-4.0. |
| -o OFFSET, --offset OFFSET  | ignore the archive header and use this exact offset.         |
| -k KEY, --key KEY           | ignore the archive header and use this exact key.            |


## Errors

### Common errors

  - Check you are using the latest version of Python 3.
  - Check you are using quotes around file paths.
  - Video guides may be out of date, please check this file for up-to-date advice on using the tool.

### New errors

If something goes wrong while extracting an archive, please [make an issue](https://github.com/Lattyware/unrpa/issues/new). 

New variants of the RPA format get created regularly, so new games might not work - generally support can be added quickly though.