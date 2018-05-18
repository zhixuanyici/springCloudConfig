	1.http请求地址和资源文件映射如下:

		/{application}/{profile}[/{label}]
		/{application}-{profile}.yml
		/{label}/{application}-{profile}.yml
		/{application}-{profile}.properties
		/{label}/{application}-{profile}.properties

	2.各自含义
	spring.application.name 配置客户端的名称
	spring.cloud.config.label 指明远程仓库的分支
	spring.cloud.config.profile

		dev开发环境配置文件
		test测试环境
		pro正式环境
	spring.cloud.config.uri= http://localhost:8888/ 指明配置服务中心的网址。