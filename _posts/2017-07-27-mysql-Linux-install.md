---
title: mac下mysql安装简易教程
date: 2017-01-03 22:18:44
tags: [mac,mysql]
---
----------------------------------
## 1.首先用homebrew 安装mysql##

安装homebrew

<pre><code>/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)</code></pre>  



然后安装mysql

<pre><code>brew install mysql</code></pre>

## 2.一般homebrew安装的软件在/usr/local/bin目录下






启动mysql

<pre><code>mysql.server start</code></pre> 

## 3.简单点的话通过使用脚本 mysql_secure_installation



导航到homebrw目录下面

<pre><code> /usr/local/bin/mysql_secure_installation In order to log into MySQL to secure it, we'll need the currentpassword for the root user.  If you've just installed MySQL, andyou haven't set the root password yet, the password will be blank,so you should just press enter here.
Enter current password for root (enter for none): //输入现行root密码，因为初次使用，所以直接回车OK 
successfully used password, moving on...
Setting the root password ensures that nobody can log into the MySQLroot user without the proper authorisation.
Set root password? [Y/n] Y //是否设置root密码
New password:
Re-enter new password:
Password updated successfully!Reloading privilege tables.. ... Success!
By default, a MySQL installation has an anonymous user, allowing anyone to log into MySQL without having to have a user account created for This is intended only for testing, and to make the installation go a bit smoother. You should remove them before moving into a production environment.    
Remove anonymous users? [Y/n] Y //是否删除匿名用户 ... 
Success!Normally, root should only be allowed to connect from 'localhost'.Thisensures that someone cannot guess at the root password from the network.
Disallow root login remotely? [Y/n] Y //是否禁止远程登录
 ... Success!
By default, MySQL comes with a database named 'test' that anyone can
access.This is also intended only for testing, and should be removed
before moving into a production environment.
Remove test database and access to it? [Y/n] Y //删除测试数据库，并登录
 Dropping test database...
 ... Success!
 Removing privileges on test database...
 ... Success!
Reloading the privilege tables will ensure that all changes made so far
will take effect immediately.
Reload privilege tables now? [Y/n] Y//重新载入权限表
 ... Success!</code></pre>

