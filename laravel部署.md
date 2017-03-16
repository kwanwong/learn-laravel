**Laravel线上部署的最佳实践**

**旧项目**
> 1.停掉服务

    $ php artisan down

> 2.从git拉代码

    $ git pull origin master

> 3.编译前端文件

    $ gulp --production

> 4.清理

    $ php artisan clear-compiled

    $ php artisan optimize

> 5.上线

    $ php artisan up

**新项目**
> 1.拉代码

    $ git clone git@example@com:foo.git

> 2.安装依赖

    $ composer install --optimize-autoloader --no-dev

    $ composer dump-autoload --optimize

> 3.编译前端文件

    $ gulp --production

> 4.清理

    $ php artisan clear-compiled

    $ php artisan optimize