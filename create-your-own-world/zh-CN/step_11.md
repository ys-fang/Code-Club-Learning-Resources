## 门和钥匙

如果你的世界中有一些房门被锁上，玩家必须找到钥匙才能继续游戏，这时该怎么办？

+ 切换至 `钥匙` 子图。右键单击并选择 **显示**，使其出现在工作区上。

+ 编辑 `钥匙` 子图的造型使其呈蓝色。

+  切换你的工作区背景至房间 3，并将 `钥匙` 子图放在难以到达的位置！

 ![screenshot](images/world-key.png)

+ 向 `钥匙` 子图添加代码以确保其仅在房间 3 中可见。

+ 创建一个被称作 `库存`{:class="blockdata"}的新列表变量。此处将是你储存你的 `玩家` 子图收集到的所有物品的地方。

[[[generic-scratch-make-list]]]

+ 收集钥匙的代码与收集硬币的代码十分相似。不同之处在于你将钥匙添加为库存。

```blocks
	点击绿旗时
  等待直到 <碰到 [player v] ?>
  新增项目 [blue key] \( [inventory v] \)
  停止 [角色的其他程序 v]
  隐藏
```

+ 测试你的 `钥匙` 子图，看看你是否能收集钥匙并将其添加到你的库存中。请记得向你的工作区添加代码以在游戏开始时清空你的库存。

```blocks
	删除第 (全部 v) 项 \( [inventory v] \)
```

+ 现在让我们来添加锁上的房门。右键单击 `蓝色房门` 子图并选择 **显示**，然后将该子图放置在横跨两面墙壁间空隙的位置。

![screenshot](images/world-door.png)

+ 向 `蓝色房门` 子图添加代码，使其仅在房间 3 内可见。

+ 一旦你的库存中有了蓝色钥匙，`蓝色房门` 子图就会隐藏，以使你的 `玩家` 子图通过。

```blocks
	点击绿旗时
  等待直到 <链表 [inventory v] 包含 [blue key] ?>
  停止 [角色的其他程序 v]
  隐藏
```

+ 测试你的项目，看看你是否能收集蓝色钥匙来打开房门！