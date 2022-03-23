en.krddy.com-2020
=============

凯瑞达英文官网2020年版


域名绑定、301转向及nginx配置
-----

新建配置文件: ``sudo nano /etc/nginx/sites-available/en.krddy.com``

编辑配置文件及保存: 

    server {
      server_name en.krddy.com;
      index index.html;
      root /srv/en.krddy.com-2020/_site;
      error_page 404 /Error.html;
      add_header Strict-Transport-Security "max-age=15768000" always;
    }

建立链接: ``sudo ln -s /etc/nginx/sites-available/en.krddy.com /etc/nginx/sites-enabled/``

重启nginx: ``sudo service nginx restart``


下载及生成网站
-----

1. 下载网站源码: ``git clone git://github.com/zackwong/en.krddy.com-2020.git``

2. 进入源码根目录: ``cd en.krddy.com-2020``

3. 生成网站: ``jekyll build``


开发者
---------

* Zack Wong &lt;hzzzoo@126.com&gt;

