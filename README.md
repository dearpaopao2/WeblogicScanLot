	软件作者：Tide_RabbitMask
	感谢来自网络的开源POC，
	我只是进行了魔改和接口统一。
    免责声明：Pia!(ｏ ‵-′)ノ”(ノ﹏<。)
    本工具仅用于安全测试，请勿用于非法使用，要乖哦~
        
    V2.0简介：
	提供weblogic批量检测功能。
	【没有遇到过weblogic批量检测工具的小朋友举起你的爪爪！】
	
	V2.0开发背景：
	最近拿到一项授权任务，需要从百万级的域名/IP中进行weblogic 漏洞分析。
	鉴于时间比较紧张，我只能尽可能模糊的进行url的存活检测、weblogic服务器识别，
	然后对再筛选后的结果进行weblogic poc批量检测，此步骤也就用到了此工具。
	配套的域名/IP weblogic批量筛选工具会在稍后看心情同步放出。
	不许吐槽我只检测了7001端口！百万级数据你想让我死是不！
	综上:V2.0不是V1.0的升级版，只是多进程版本，所以舍弃了部分功能。
	对于当个目标站点的检测，依然推荐您使用V1.0。
	
	V1.1特色：
		1.舍弃V 1.0交互与EXP
		2.多进程任务高效并发
		3.简洁直观的监控界面
		4.健全的日志记录功能
		5.健全的异常处理机制
	
    V1.1涉及POC详情如下：
        #控制台路径泄露
        managerURL200  
        
        #SSRF：
        CVE-2014-4210      
        
        #JAVA反序列化： 
        CVE-2016-0638  
        CVE-2016-3510   
        CVE-2017-3248   
        CVE-2018-2628 
        CVE-2018-2893   
        
		
    【软件使用Demo】
	【此处只提供了本机单机扫描demo，多线程实战场面太过血腥，请在家长陪同下自行体验】
	
	#控制台：
    =========================================================================
	__        __   _     _             _
	\ \      / /__| |__ | | ___   __ _(_) ___     _     _
	 \ \ /\ / / _ \ '_ \| |/ _ \ / _` | |/ __|  _| |_ _| |_
	  \ V  V /  __/ |_) | | (_) | (_| | | (__  |_   _ _   _|
	   \_/\_/ \___|_.__/|_|\___/ \__, |_|\___|   |_|   |_|
								 |___/

								 By Tide_RabbitMask | V 2.0

	Welcome To Weblogic++ !!

	[*]任务加载成功，目标:127.0.0.1:7001

	[*]任务检测完成，目标:127.0.0.1:7001

	>>>>>End of task
    =========================================================================
	
	#日志文件：
    =========================================================================
	
	[+]目标weblogic控制台地址暴露!路径为:http://127.0.0.1:7001/console/login/LoginForm.jsp
	[+]目标weblogic存在UDDI组件!路径为:http://127.0.0.1:7001/uddiexplorer/
	[+]127.0.0.1:7001存在JAVA反序列化漏洞：CVE-2016-0638
	[-]127.0.0.1:7001未检测到CVE-2016-3510
	[-]127.0.0.1:7001未检测到CVE-2017-3248
	[-]127.0.0.1:7001未检测到CVE-2018-2628
	[+]127.0.0.1:7001存在JAVA反序列化漏洞：CVE-2018-2893

	=========================================================================
