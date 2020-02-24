# ssr
Linux上的SSR一键安装脚本

脚本原地址：https://github.com/the0demiurge/CharlesScripts/blob/master/charles/bin/ssr

ubuntu服务器版本命令行如何安装SSR:
一行行输入，回车（#号后是说明，不用输入，只输入前面的命令，输入完后回车，下同）：

wget https://raw.githubusercontent.com/byalan/ssr/master/ssr          # 这个是下载
sudo mv ssr /usr/local/bin                                            # 下载完后移动到这个文件夹
sudo chmod 766 /usr/local/bin/ssr                                     # 这个是赋予权限
ssr install                                                           # 安装
ssr config                                                            # 打开SSR配置
ssr start                                                             # 运行SSR客户端
ssr restart                                                           # 重启SSR客户端
ssr help                                                              # 查看帮助

如在安装时显示如下提示则表示没安装git:
         sudo: git : command mot found       
    则要先安装git:
         sudo apt install git
         
安装完git后再重复刚才的SSR安装

装完后配置，输入：
         ssr config
(输入冒号:wq可以退出配置)： 也可用nano来配置
也可以直接到配置文件的地方，右键 使用默认编辑软件来编辑config配置文件，如果保存不了，是权限问题，想办法解决：
      /usr/local/share/shadowsocksr/config.json
所以建议还是sudo后用none修改
