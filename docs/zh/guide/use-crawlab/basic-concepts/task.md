# 任务

任务是 [爬虫](./spider) 触发的进程，能够抓取网站数据、进行特殊操作、提供其他一些功能。它是运行爬虫进程的基本单位。

在 Crawlab 中，您不仅可以一键运行任务，还可以可视化的查看统计数据、实时日志、已抓取数据等任务信息。此外，您还可以设置 `Priority` 来决定任务的执行顺序。

## 运行任务

您可以 [通过爬虫运行任务](/guide/use-crawlab/basic-concepts/spider.html#run-spider)，或执行下面的步骤。
1. 导航至 `Tasks` 页面
2. 点击左上方的 `New Tasks` 按钮
3. 选择 `Spider` 及其他信息
4. 点击 `Confirm`

## 重新运行任务

1. 导航至 `Tasks` 页面
2. 点击右侧的 `Restart` 按钮

## 监控任务

Crawlab 提供任务监控功能，让您能够紧密观察抓取结果数据以及爬虫抓取效率。

### 查看日志

您可以在 Crawlab 中查看实时日志。
1. 导航至任务详情页
2. 点击 `Logs` 标签

### 查看数据
您可以实时查看已抓取数据
1. 导航至任务详情页
2. 点击 `Data` 标签

## 取消任务

如果任务是 `Pending` 或 `Running` 状态，您可以取消它，通过
1. 在 `Tasks` 页面中点击右侧的 `Cancel`，或
2. 在任务详情页点击导航条上的 `Cancel` 按钮
