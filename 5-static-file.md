## 静态资源服务器

web服务器一大用途就是托管静态资源。当然这件事用Java PHP都行，但是事情交给专业人士来做嘛。



然后学习过程中，不要迷失在细节之中，我们学习的是抽象的web服务器的用法，nginx只是一个载体。

想一想我们该做什么？

- 监听某个端口
- 将请求的URL中的path和计算机上某个目录对应起来
- 手动

其实就是这个简单啊，那我们来看对应到nginx配置文件



```
server {
    listen 80;
    server_name music.static.bitfish.xyz;
    root /var/www/music.static.bitfish.xyz;
    index index.html;
}
```



把对应的请求映射到 /var/www/music.static.bitfish.xyz 文件夹。

