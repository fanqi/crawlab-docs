# 定时任务

很多时候，我们会需要周期性的运行 [爬虫](./spider) 的 [任务](./task)，而您需要的是定时任务。

在 Crawlab 中，*定时任务* 这个概念跟 Linux 中的 [crontab](https://www.tutorialspoint.com/unix_commands/crontab.htm) 类似。它是一个长期存在的作业，能够周期性的运行爬虫任务。

::: tip
如果您希望配置一个每天/周/月自动运行抓取任务的网络爬虫，您应该设置一个 *定时任务*。定时任务是自动化的首选，尤其是对于增量抓取的爬虫。
:::

## 创建定时任务

1. 导航至 `Schedules` 页面
2. 点击左上方的 `New Schedule` 按钮
3. 输入基础信息，包括 `Name`、[Cron 表达式](https://www.tutorialspoint.com/unix_commands/crontab.htm)、`Spider`
4. 点击 `Confirm`

创建好的定时任务默认是启用的，它应该能够在 cron 表达式对应的时刻触发 [任务](./task)。

::: tip
您可以通过设置 `Cron Expression` 为 `* * * * *`（每分钟运行一次）来调试定时任务模块是否正常工作，即查看每分钟开始时是否有任务触发。
:::

## 启用/禁用

您可以启用或禁用节点来控制它是否能运行爬虫任务。您可以在 `Schedules` 页面或详情页中点击 `Enabled` 属性中的切换按钮来控制。

## Cron 表达式

*Cron 表达式* 描述周期性的简单标准格式。它跟 Linux 的 `crontab` 是同一格式。

```
*    *    *   *    *  Command_to_execute
|    |    |    |   |       
|    |    |    |    Day of the Week ( 0 - 6 ) ( Sunday = 0 )
|    |    |    |
|    |    |    Month ( 1 - 12 )
|    |    |
|    |    Day of Month ( 1 - 31 )
|    |
|    Hour ( 0 - 23 )
|
Min ( 0 - 59 )
```

- 星号 (*) 表示该字段所有可能的值，例如每天、每小时
- 逗号 (,) 表示一部分值，例如: "1,3,4,7,8"
- 破折号 (-) 表示范围，例如: "1-6"，等同于 "1,2,3,4,5,6"
- 斜线 (/) 可以用作指定某数值，例如 "\*/3" 在小时字段等同于 "0,3,6,9,12,15,18,21"， "\*" 表示 '每小时' 但 "/3" 表示只有第 1、4、7 等值被使用了

::: warning
Crawlab 中的 *Cron 表达式* 使用的是跟 Linux 中 `crontab` 相同的格式。也就是说，最小单位是 **`分钟`**。它跟某些使用秒作为最小单位的 crontab 风格定时任务框架不同。
:::

::: tip
如果您不确定如何编写 Cron 表达式，您可以导航至 [https://crontab.guru](https://crontab.guru/) 来进行校验。
:::
