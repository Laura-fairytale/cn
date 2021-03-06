# 设置自动备份

云数据库 MongoDB 支持自动备份，实例创建完成后每天执行一次全量备份，备份数据保存在京东云对象存储，最长保留7天，目前不收取任何费用。备份任务默认开始时间为每天的0:00-1:00，您可以根据业务情况调整自动备份时间。


## 注意事项
- 自动备份文件不支持删除。
- 如当天已执行自动备份，修改自动备份时间在当前时间之后，仍会创建备份。

## 操作步骤
1. 登录 [MongoDB 控制台](https://mongodb-console.jdcloud.com/mongodb)。
1. 在实例列表页面，选择目标实例，点击实例名称，进入实例详情页面。
1. 在实例详情页面，依次点击备份与恢复 > 备份策略，进入备份策略页面。
   
   ![](https://github.com/jdcloudcom/cn/blob/master/image/mongodb/mongo-017.png)

1. 在备份策略页面，点击"修改策略"，打开修改策略弹窗。

   ![](https://github.com/jdcloudcom/cn/blob/master/image/mongodb/mongo-018.png)

1. 在修改策略弹窗，重新选择期望的自动备份时间。
	
1. 点击“确定”，保存修改。

## 相关参考

- [手动创建备份](https://github.com/jdcloudcom/cn/blob/master/documentation/Cloud-Database-and-Cache/MongoDB/Operation-Guide/Backup/CreateBackup.md)
- [下载备份](https://github.com/jdcloudcom/cn/blob/master/documentation/Cloud-Database-and-Cache/MongoDB/Operation-Guide/Backup/DownloadBckup.md)
- [数据恢复](https://github.com/jdcloudcom/cn/blob/master/documentation/Cloud-Database-and-Cache/MongoDB/Operation-Guide/Backup/RestoreInstance.md)
- [根据备份创建实例](https://github.com/jdcloudcom/cn/blob/master/documentation/Cloud-Database-and-Cache/MongoDB/Operation-Guide/Backup/CreateInstance2.md)
- [根据时间点创建实例](https://github.com/jdcloudcom/cn/blob/master/documentation/Cloud-Database-and-Cache/MongoDB/Operation-Guide/Backup/CreateInstance3.md)


