## 使用场景
swagger UI，删除swagger-ui.html，保留/v2/api-docs。

## 使用说明
放到网站根目录中。

假设网站是example.com，测试站点为https://swagger-ui.domain/ 

访问https://example.com/swagger-ui.html#https://swagger-ui.domain/ 即可

1. 文件最好放到https站点下
2. 可以配置本地host，`1.2.3.4 swagger`防止referer泄漏
3. burp配置"Match and Replace"。
    1. Type: Response Header
    2. Match: [空]
    3. Replace: Access-Control-Allow-Origin: https://swagger
    4. Comment: 自定义
