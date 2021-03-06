# 控制台扩容操作

云硬盘是云上可扩展的存储设备，云硬盘创建完成后，随着业务需求的增长，当现有云硬盘容量无法满足当前系统的存储需求时，您可以随时扩展其大小，以扩大其存储容量，同时保持云硬盘上原有的数据不变。为了保证云硬盘扩容的空间可用，您不仅需要扩展云硬盘容量的大小，还需要扩展其上的文件系统以保证新增的云硬盘空间可用。请在控制台操作完成后，参考[扩容文件系统（有分区）](https://docs.jdcloud.com/cn/cloud-disk-service/expand-file-system-multi-partition)或[扩容文件系统（Linux无分区）](https://docs.jdcloud.com/cn/cloud-disk-service/expand-raw-disk-file-system)，对文件系统进行扩容。

<br>

##  扩容注意事项

### 扩容前



- 仅可用状态的云硬盘支持扩容(云硬盘在非挂载且无正在进行的操作时为“可用”状态）。



- 建议在扩容云硬盘之前创建云硬盘快照，以备份数据。



- 云硬盘如果正在执行创建快照的操作，则此时不允许进行扩容操作。



- 目前仅包年包月计费类型的云硬盘支持扩容操作，按配置计费类型的云硬盘暂时不支持扩容操作。



- 挂载在实例上的云硬盘，需要先将云硬盘从实例上卸载，卸载云硬盘之后，才可以进行扩容操作。

### 扩容后

- 只做云硬盘容量的扩容，未做文件系统的扩容。

- 扩容生效之后的云硬盘，仍然需要用户手动格式化新扩展的存储空间，新增的云硬盘空间才可见；具体操作方法详见[云硬盘扩容概述](https://docs.jdcloud.com/cn/cloud-disk-service/cloud-disk-expansion-overview)。

<br>

##  操作指南


1、打开[京东云控制台](https://console.jdcloud.com/)，选择【弹性计算】-【云主机】-【云硬盘】；

2、在云硬盘列表页面找到需要进行容量升级的云硬盘，点击云硬盘列表中对应的云硬盘名称跳转到其详情页面；

3、点击右上角【操作】-【升级容量】，进入【升级容量】弹窗；

<br>

![](https://github.com/jdcloudcom/cn/blob/edit/image/Elastic-Compute/CloudDisk/cloud-disk/cloud-disk-014.jpg)

<br>


4、选择或直接输入升级后的容量数值，点击【确定】完成支付后即可进入控制台查看扩容后的云硬盘容量；

<br>

![](https://github.com/jdcloudcom/cn/blob/edit/image/Elastic-Compute/CloudDisk/cloud-disk/cloud-disk-015.jpg)

<br>

5、扩容成功，则相关信息更新；若扩容失败，则出现提示框；如果多次扩容失败，请联系客服。
