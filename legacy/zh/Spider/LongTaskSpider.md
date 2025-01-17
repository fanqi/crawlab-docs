## 长任务爬虫

长任务爬虫（Long-Task Spiders）是一种特殊的 [自定义爬虫](CustomizedSpider.md)，这种爬虫跑任务不会停止，一般会一直获取消息队列中的 URL 并抓取，只有当用户主动停止或遇到错误时才会停止运行。长任务爬虫通常是分布式运行的，为的是有效的利用网络带宽资源和其他计算资源，将分布式节点的效率利用到极致。典型的例子就是基于 Scrapy 的分布式爬虫 [scrapy-redis](https://github.com/rmax/scrapy-redis)。

要启用长任务爬虫，只需要在 **创建爬虫** 或 **爬虫详情** 中打开 “是否为长任务开关” 就可以了。

您可以在 **爬虫列表** 中选择 “长任务” 来过滤所有长任务爬虫。
