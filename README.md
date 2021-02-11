# README

## DESCRIPTION

> 使用ssh实现同一局域网下不同cp的文件传输



## 安装服务端和客户端

```bash
$ sudo apt-get install openssh-client ##这是安装客户端
$ sudo apt-get install openssh-server ##这是安装服务端
```

  安装完成后默认自动开启

```bash
$ sudo service ssh stop ##关闭ssh
$ sudo service ssh start ##开启ssh
```



## 远程控制服务器

**连接**

```bash
$ ssh usr@ip
```


  如果是首次连接，server联机的 Key 尚未被建立，输入 yes 

**从服务器下拉文件或目录**

```bash
$ scp servername@192.168.0.101:/var/www/test/a.txt  /var/www/
$ scp -r servername@192.168.0.101:/var/www/test  /var/www/
```

**上传本地文件或目录到服务器**

```bash
$ scp /var/www/test.php servername@192.168.0.101:/var/www/
$ scp -r /var/www/ servername@192.168.0.101:/var/www/
```


