	1.http请求地址和资源文件映射如下:

		/{application}/{profile}[/{label}]
		/{application}-{profile}.yml
		/{label}/{application}-{profile}.yml
		/{application}-{profile}.properties
		/{label}/{application}-{profile}.properties

	2.
	配置中心内容
		spring.application.name=enreka-config-client
		spring.cloud.config.label=master
		spring.cloud.config.profile=test
		#spring.cloud.config.uri= http://localhost:8888/

		eureka.client.serviceUrl.defaultZone=http://localhost:8889/eureka/
		spring.cloud.config.discovery.enabled=true
		spring.cloud.config.discovery.serviceId=config-server
		server.port=8881
	
	
	
	各自含义
		spring.application.name 配置客户端的名称
		spring.cloud.config.label 指明远程仓库的分支
		spring.cloud.config.profile

			dev开发环境配置文件
			test测试环境
			pro正式环境
		spring.cloud.config.uri= http://localhost:8888/ 指明配置服务中心的网址。
		
		spring.cloud.config.discovery.enabled 是从配置中心读取文件。
		spring.cloud.config.discovery.serviceId 配置中心的servieId，即服务名。