PHP项目中开启debug模式

#添加方式
====1.NGINX.conf===
location /pinche
    {
        rewrite ^/(.*)$ /index.php/\$1 break;
        fastcgi_index index.php;
        fastcgi_pass 127.0.0.1:9000;
        fastcgi_param DEBUG 1; #加入debug参数
        include fastcgi.conf;
    }
====2. /etc/php-fpm.conf
  env[DEBUG]=1
=====php code ====
  if(isset($_SERVER['DEBUG'])){
      $cache=off;
      $config = Config\Db\Pinche::$CONFIG_MYSQL_DEVELOP;
  }else{
      $cache=on;
      $config = Config\Db\Pinche::$CONFIG_MYSQL;
  }

 
