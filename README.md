# 数据库管理平台

DBE是数据库管理运营web化的有益尝试，旨在提升DBA的工作效率，支持丰富的运维功能，后台组件使用python语言flask开发，前端页面使用iView开发。

目前已覆盖MySQL数据库管理工作的80%以上。

## 系统体验
http://121.37.236.104:8011/

用户：admin/admin

## Features

- 基于RESTful API 前后端分离
- python语言开发，部署维护简单
- 灵活的插件机制，支持传参，自动同步到客户端
- web 管理界面简洁高效

## 联系作者
QQ群:978120898

## 前端源码
https://github.com/weiyong-dba/dbe-frontend

前端源码基于[owl-frontend](https://github.com/TalkingData/owl-frontend)二次开发，感谢原作者的辛苦劳动。

## 功能

- 自动化部署
	- 支持多版本部署
	- 支持主从部署
	- 多主机部署
	- 支持参数模版
	- 自定义参数部署

- MySQL管理
	- 集群列表
		- 集群列表
		- 新增集群
		- 删除集群
		- 集群详情
			- 包含实例
				- 会话【支持结束会话，支持会话直接调用SQL优化】
				- 锁【监控锁情况】
				- 参数
				- 账号【支持新建用户，删除用户，用户授权，修改密码，克隆用户】
				- 数据字典【展示表结构、建表SQL、索引等信息】
				- 创建从库 【基于备份自动完成slave部署及配置】
			- 任务列表【展示相关任务执行情况】
			- 复制管理【支持取消同步，跳过错误，修改同步】
			- 备份列表【展示实例备份情况】
	- SQL上线
	   - 基于[goInception](https://github.com/hanchuanchuan/goInception.git)完成
	   - SQL美化
	   - SQL语句检测【自动SQL审核】
	   - SQL执行【支持原生SQL方式、gh-ost、pt-osc、支持备份】
	   - SQL预约执行【支持预约时间执行】
	   - 历史审核记录
	   - 历史执行记录【支持查看回滚SQL】
	- SQL优化
	 	 - SOAR
	 	 - SQLAdvisor
- 实例管理
    - 实例列表
    - 组列表
    	- 包含实例
	- 包含插件【该组包含的实例会执行这些插件，系统巡检修改数据通过插件收集】

- 系统巡检
	- 巡检项目阈值配置
	- 巡检结果展示
		- 库大小【展示数据库文件大小、表数量等】
		- 自增ID使用率
		- 冗余索引【支持删除冗余索引】
		- 表碎片
		- 慢查询【支持慢查询自动轮换、支持慢查询调用SQL优化】
- 备份管理【已集成到插件】
	- 备份策略
	- 备份列表
- 定时任务【类crontab】
	- 任务列表
		- 新增任务
		- 删除任务
		- 暂停任务
		- 执行执行
		- 恢复任务
	- 调度日志【任务执行记录】
- 用户管理
    - 用户组
    - 新建用户
- 产品线管理
    - 新增、删除
    - 添加主机 
    - 添加用户
- 主机管理
	- 新增、删除
	- 分配
- 模版管理
	- 新建模版
	- 配置模版默认值
- 插件管理
	- 创建插件【插件路径、参数、执行周期等】
	- 插件更新【agent自动判断插件checksum，自动同步最新版本】

## License
- Apache 2.0

任何二次开发及二次开源项目请严格遵守相应开源许可

2020 © weiyong-dba
