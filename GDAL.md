# [GDAL简介](https://gdal.org/index.html)

GDAL is a translator library for raster and vector geospatial data formats that is released under an X/MIT style Open Source [License](https://gdal.org/license.html#license) by the [Open Source Geospatial Foundation](http://www.osgeo.org/). As a library, it presents a single raster abstract data model and single vector abstract data model to the calling application for all supported formats. It also comes with a variety of useful command line utilities for data translation and processing. The [NEWS page](https://github.com/OSGeo/gdal/blob/v3.4.0/gdal/NEWS.md) describes the November 2021 GDAL/OGR 3.4.0 release.

上面文字引自GDAL[官方介绍](https://gdal.org/index.html)，GDAL是遥感数据处理最常用的第三方库之一，支持多种栅格数据（Tiff（如Landsat）,HDF（大多数MODIS采用HDF4格式存储）, jp2（Sentinel-2）等）和矢量数据，能有效解决绝大多数遥感数据处理问题。本文按照个人学习曲线进行更新，旨在督促自己的同时，给同样初学GDAL（Python）的同学提供一点帮助。

## 1、GDAL下载和安装

**方法1：conda install**

推荐使用Anaconda 配置python环境，<!--详见[Anaconda常见命令]()-->。

+ 查询GDAL可用版本：conda/pip search gdal，选择合适的版本（一般不会有最新版本），如果没有合适的版本请使用方法2
+ 命令行安装GDAL：conda/pip install gdal=版本号， 不加版本号可能会默认安装老版本

该方法可能由于数据源服务器在境外，网速较慢，容易出现安装过程中断。出现这种情况推荐采用国内源（[参考博客](https://blog.csdn.net/weixin_44789149/article/details/109504715)）或[更改系统代理](https://xn--mesr8b36x.net/#/register?code=TfyKHTJ7)解决。
其他参考：[pytorch安装](https://blog.csdn.net/weixin_44789149/article/details/109504715)



**方法2：手动下载安装**

+ **下载网址1：**https://www.lfd.uci.edu/~gohlke/pythonlibs/#gdal

+ **下载网址2：**https://gdal.org/download.html<br>
下载对应[python](https://so.csdn.net/so/search?from=pc_blog_highlight&q=python)版本的whl文件，在命令行中`pip install whl文件完整路径`安装（windows方式），如下图：
![图片](https://user-images.githubusercontent.com/75717920/144560580-fbcb0632-5c0c-4198-afb9-d01b6438b451.png)
```from osgeo import gdal```
![图片](https://user-images.githubusercontent.com/75717920/144563294-c2c4c34d-92ad-44e2-9825-cd829963027b.png)


## 2、GDAL常用工具


