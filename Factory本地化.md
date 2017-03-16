**本地化Model Factory**
> factory本地化后，可实现对中文及其他语言的支持

*实现方法：*

    重写Faker/Generator
    
*步骤：*

*1.打开文件*

    app/Providers/AppServiceProvider.php

*2.引入相关类*

    use Faker/Gererator as FakerGenerator
    use Faker/Factory as FakerFactory
    
*3.在boot()中加入以下代码*

    $this->app->singleton(FakerGeneraror::class, function(){
        return FakerFactory::create('zh_CN');
    });
    
*4.完成*