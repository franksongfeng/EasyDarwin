# EasyDarwin开源流媒体服务器


## 主要功能特点

- 基于Golang开发维护；
- 支持Windows、Linux、macOS平台；
- 支持RTSP推流分发（推模式转发）；
- 支持RTSP拉流分发（拉模式转发）；
- 服务端录像 参考:https://blog.csdn.net/jyt0551/article/details/84189498
- 服务端录像检索与回放 参考:https://blog.csdn.net/jyt0551/article/details/84189498
- 关键帧缓存；
- 秒开画面；
- Web后台管理；
- 分布式负载均衡；


## 安装部署

- [直接下载运行Release包](https://www.easydarwin.org/p/easydarwin.html)

- 直接运行(Windows)

    EasyDarwin.exe
    
    以 `Ctrl + C` 停止服务

- 以服务启动(Windows)

    ServiceInstall-EasyDarwin.exe
    
    以 ServiceUninstall-EasyDarwin.exe 卸载 EasyDarwin 服务

- 直接运行(Linux/macOS)

		cd EasyDarwin
		./easydarwin
		# Ctrl + C

- 以服务启动(Linux/macOS)

		cd EasyDarwin
		./start.sh
		# ./stop.sh

## 二次开发

### 准备工具

        # go tools
        go get -u -v github.com/kardianos/govendor
        go get -u -v github.com/penggy/gobuild

        # npm tools
        npm i -g apidoc
        npm i -g rimraf


### 编译命令

- 获取代码

        cd $GOPATH/src/github.com
        mkdir EasyDarwin && cd EasyDarwin
        git clone https://github.com/EasyDarwin/EasyDarwin.git --depth=1 EasyDarwin
        cd EasyDarwin

- 以开发模式运行

        npm run dev

- 以开发模式运行前端 Run as dev mode

        npm run dev:www       

- 编译前端  Build www

        cd web_src && npm i
        cd ..
        npm run build:www

- 编译 Windows 版本 Build windows version

        npm run build:win

- 编译 Linux/macOS 版本 (在 bash 环境下执行) Build linux/macOS version

        npm run build:lin       

- 清理编译文件 Clean

        npm run clean 


## 获取更多信息

**EasyDarwin**开源项目：[www.EasyDarwin.org](http://www.easydarwin.org)

Copyright &copy; EasyDarwin.org Team 2012-2025
