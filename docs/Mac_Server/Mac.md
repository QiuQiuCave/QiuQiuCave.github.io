# 将Mac mini作为家庭服务器使用
Mac mini m4 有高性能低功耗接口齐全的优点，我把它放在机柜上充当家庭服务器使用，记录一下配置过程。
## 前期配置
- 在设置中关闭屏幕保护，在用户与群组中开启“自动以此身份登录”，开启断电后自动启动。
## 远程控制配置
- 在通用-共享中开启远程管理，配置用户权限
- 在另一台mac中打开“屏幕共享.app”，输入服务器的局域网ip地址，以“vnc://192.168.31.170”为例，输入在服务器中配置好的用户名与密码，即可远程访问，可在服务器配置中选择“高性能”，可以获得接近于直连屏幕的体验。
## 文件共享配置
我选择外接了一块1t的固态硬盘作为家里的共享文件夹

- 将外接硬盘格式化为ExFAT格式
- 在MAC服务器中打开通用-共享-文件共享
- 配置好共享的硬盘或文件夹
- 配置好用户访问权限

