# kubernetes-zookeeper

kubernetes 部署 zookeeper 支持 host 方式部署。

请修改 `deploy/hostMachine` 部署配置以 `hostNetwork` 模式部署。

Taint 配置如下：

```
$ kubectl label nodes <nodes> zhangyue-ops.com/schedule-hbase-01=true
$ kubectl taint nodes <nodes> application=bigdata:NoSchedule
$ kubectl taint nodes <nodes> organization=user:NoSchedule
$ kubectl taint nodes <nodes> special=true:NoSchedule
```
