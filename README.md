# 数据库管理平台

DBEOPS是数据库管理运营web化的有益尝试，旨在提升DBA的工作效率，支持丰富的运维功能，后台组件使用python语言开发，前端页面使用 iView 开发。

## 系统体验
http://47.105.207.43:8011/

用户：admin/admin


## Features

- python语言开发，部署维护简单
- 灵活的插件机制，支持传参，自动同步到客户端
- web 管理界面简洁高效


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
	   - 基于goInception[https://github.com/hanchuanchuan/goInception.git]完成
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
- 定时任务
	- 任务列表
		- 新增
		- 删除
		- 暂停
		- 执行
		- 恢复
	- 调度日志
- 用户管理
    - 用户组
    - 注册
- 产品线管理
    - 新增、删除
    - 添加主机 
    - 添加用户
- 主机管理
	- 新增、删除
	- 分配
- 模版管理
- 插件管理
	

## Snapshot 效果展示

- Login

![login](/img/dbmp/logo.png)

- Product

![login](/img/dbmp/product.png)

- Dashboard

![](/img/dbmp/dashboard.png)

- 部署管理
	- MySQL部署
	![](/img/dbmp/mysql-deploy.jpg)
	- 部署列表
	![](/img/dbmp/mysql-deploy-list.png)
- MySQL管理
	- 集群列表
		- 集群列表
		- 集群详情
		![](/img/dbmp/mysql-cluster-detail.png)
			- 包含实例
				- 会话
				![](/img/dbmp/mysql-cluster-processlist.png)
				- 锁
				![](/img/dbmp/mysql-cluster-lock.png)
				- 参数
				![](/img/dbmp/mysql-cluster-parameter.png)
				- 账号
					- 账号列表
					![](/img/dbmp/mysql-cluster-privileges.png)
					- 新建用户
					![](/img/dbmp/mysql-cluster-privileges-new.png)
					- 用户授权
					![](/img/dbmp/mysql-cluster-privileges-grant.png)
					- 修改密码
					![](/img/dbmp/mysql-cluster-privileges-chpwd.png)
					- 克隆用户
					![](/img/dbmp/mysql-cluster-privileges-clone.png)
				- 数据字典
				![](/img/dbmp/mysql-cluster-dictionary.png)
				![](/img/dbmp/mysql-cluster-dictionary-detail.png)
				- 创建从库
				![](/img/dbmp/mysql-cluster-slave-create.png)
			- 任务列表
			![](/img/dbmp/mysql-cluster-job-list.png)
			- 复制管理
			![](/img/dbmp/mysql-cluster-repl.png)
			- 备份列表
			![](/img/dbmp/mysql-cluster-backup-list.png)
	- SQL上线
		- SQL上线
			![](/img/dbmp/mysql-sqlonline.png)
		- SQL上线列表
			![](/img/dbmp/mysql-sqlonline-list.png)
		- 多种执行方式
			![](/img/dbmp/mysql-sqlonline-exectype.png)
		- 执行过程记录
			![](/img/dbmp/mysql-sqlonline-exec-detail.png)
		- 回滚SQL【可下载】
			![](/img/dbmp/mysql-sqlonline-rollbacksql.png)
		- SQL语法高亮及自动补全
			![](/img/dbmp/mysql-sqlonline-syntax.png)
	- SQL优化
		- 执行计划
		![](/img/dbmp/mysql-sqloptimize-explan.png)
		- 优化建议
			- SOAR
			![](/img/dbmp/mysql-sqloptimize-soar.png)
			- SQLAdvisor
			![](/img/dbmp/mysql-sqloptimize-sqladvisor.png)

- 实例管理
	- 实例列表
	![](/img/dbmp/engine-list.png)
	- 组列表
	![](/img/dbmp/engine-list.png)
	- 组详情【包含实例】
	![](/img/dbmp/engine-group-engine-list.png)
	- 组详情【插件列表】
	![](/img/dbmp/engine-group-plugin-list.png)

- 系统巡检
	- 巡检项目配置
	![](/img/dbmp/check-threshold.png)
	- 巡检结果展示
		- 汇总
		![](/img/dbmp/check-result.png)
		- 库大小
		![](/img/dbmp/check-dbsize.png)
		- 自增ID使用率
		![](/img/dbmp/check-autoinc.png)
		- 冗余索引
		![](/img/dbmp/check-redundant-keys.png)
		- 碎片率
		![](/img/dbmp/check-fragmentation-ratio.png)
		- 慢查询
			- 汇总
			![](/img/dbmp/check-slow-summary.png)
			- 明细
			![](/img/dbmp/check-slow-detail.png)

- 备份管理
	- 备份列表
		![](/img/dbmp/backup-list.png)
		![](/img/dbmp/backup-log.png)
	- 策略列表
		- 创建策略
			![](/img/dbmp/backup-strategy-create.png)
		- 策略列表
			![](/img/dbmp/backup-strategy-list.png)
		- 状态不为“正常”时查看历史备份情况
			![](/img/dbmp/backup-strategy-stat.png)
			
- 定时任务
	- 任务列表
		![](/img/dbmp/schedule-job-list.png)
	- 调度日志
		![](/img/dbmp/schedule-job-log.png)

- 产品线管理
	- 产品线列表
		![](/img/dbmp/product-list.png)
	- 产品线详情【包含主机】
		![](/img/dbmp/product-detail.png)
	- 产品线详情【包含用户】
		![](/img/dbmp/product-admin-user-list.png)
		
- 主机管理
	- 主机列表
		![](/img/dbmp/host.png)
	- 新建主机
		![](/img/dbmp/product-admin-add-host.png)
	- 删除主机
		![](/img/dbmp/product-admin-delete-host.png)
	- 分配主机
		![](/img/dbmp/product-admin-allocation-host.png)
	
- 模版管理
	- 模版列表
		![](/img/dbmp/parameter-model-list.png)
	- 创建模版
		![](/img/dbmp/parameter-model-new.png)
	- 编辑模版
		![](/img/dbmp/parameter-model-edit.png)
	
- 插件管理
	- 插件列表
		![](/img/dbmp/admin-plugin-list.png)
	- 创建插件
		![](/img/dbmp/admin-plugin-new.png)
- 用户管理
	![](/img/dbmp/user.png)
		
