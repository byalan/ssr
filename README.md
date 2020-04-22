# Linux上的SSR一键安装脚本

脚本原地址：
https://github.com/the0demiurge/CharlesScripts/blob/master/charles/bin/ssr

# ubuntu服务器版本命令行如何安装SSR:
一行行输入，回车（//号后是说明，不用输入，只输入前面的命令，输入完后回车，下同）：

    wget https://raw.githubusercontent.com/byalan/ssr/master/ssr       //下载
    sudo mv ssr /usr/local/bin                   //下载完后移动到这个文件夹                                    
    sudo chmod 766 /usr/local/bin/ssr            //这个是赋予权限                         
    ssr install                                  //安装                           
    ssr config                                   // 打开SSR配置                        
    ssr start                                    // 运行SSR客户端                       
    ssr restart                                  //重启SSR客户端                                                
    ssr help                                     // 查看帮助                            

# 如在安装时显示如下提示则表示没安装git:
         sudo: git : command mot found    
    则要先安装git:    
         sudo apt install git
         
安装完git后再重复刚才的SSR安装

# 新问题

安装的时候竟然是装在/home/登陆的用户名/.local/share/下，使用sudo安装也一样，运行的时候，就得加上sudo ssr start这样的命令

# 装完后配置，输入：
         ssr config
(输入冒号:wq可以退出配置)： 也可用nano来配置
也可以直接到配置文件的地方，右键 使用默认编辑软件来编辑config配置文件，如果保存不了，是权限问题，想办法解决：
    /usr/local/share/shadowsocksr/config.json  
大致前面几项需要配置一下
 
    "server": "******", // 代理服务地址
    "server_ipv6": "::",
    "server_port": 11873, // 端口号
    "local_address": "127.0.0.1", //本地socks5监听地址 
    "local_port": 1080,//本地socks5代理端口
 
    "password": "xxxxxx", //密码
    "method": "rc4-md5",//加密方式
    "protocol": "xxxxx",//协议
    "protocol_param": "xxxxxx",//协议参数
    "obfs": "xxxxxx",//混淆方式
    "obfs_param": "xxxxxxxx",//混淆参数
    
# 所以建议还是sudo后用none修改 
