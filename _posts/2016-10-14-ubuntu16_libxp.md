---

layout: post title: (ubuntu 16.04) xop 2.3 所需依赖 libXp 的安装 categories: linux

excerpt: xop 是一个广泛应用的X射线追迹模拟软件包，libXp 是其2.3版本（目前开放下载的版本）运行所需的依赖。在之前的ubuntu 14.04，libxp包括在官方源中，而16.04中尚未收录维护，需要自行编译。
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

引用自[来源](https://afni.nimh.nih.gov/afni/community/board/read.php?1,151673,151693)

1.	安装可能需要的依赖：apt-get install dh-autoreconf quilt x11proto-print-dev libpng16\*
2.	下载[源码包](http://packages.ubuntu.com/source/trusty/libxp)，获得三个文件：libxp_1.0.2-1.dsc，libxp_1.0.2.orig.tar.gz，libxp_1.0.2-1ubuntu1.diff.gz，版本号适当更改。将这三个文件放进新建文件夹：libXp。
3.	cd至libXp，键入：dpkg-source -x libxp_1.0.2-1.dsc
4.	进入生成的子文件夹：libXp-1.0.2，键入：dpkg-buildpackage -uc -us -rfakeroot -b
5.	安装编译好的文件：dpkg -i libxp-dev_1.0.2-1ubuntu1_amd64.deb libxp6_1.0.2-1ubuntu1_amd64.deb
