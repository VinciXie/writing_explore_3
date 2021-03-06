
### 小成功：

刚入职的时候, 算是有一次小成功, 即我在入职的第一周, 要求从完全陌生的三个库里选出一个来, 展现我们的图像, 作为之后的开发, 三个库都很陌生, 那么就需要一个选择原则。

现状：

- a库展现效果很好, 图片是提前加载并缓存, 但是插件少, 不易做功能, 之后可能要自己手写各种插件, 已经为一个插件纠结很久了

![a库效果](./images/a.gif)

- b库比a库展现效果差一点, 图片是按需加载并缓存, 但是插件比较丰富, 不过目前不支持我们使用的图像格式

![b库效果](./images/b.gif)

- c 库是一个很轻量级的地图库, 插件很丰富, 但是展现效果最差, 图像加载很慢

![c库效果](./images/c.gif)


因为我们老大的要求是图像要达到 a 库的效果, 这样其实只能选择 a 库, 但我不甘心, 又研究了b, 然后有所了解, 但是没有研究透, b的文档很难读。

不过这时发现一个类似的网站, 能使用b库展现同样的图像格式。

那个时候我存在着一个信念, 别人 5 个月能转行, 我就能, 别人两个月能学会前端, 我就能, 别人能用 b 库展现同样的资源, 尤其是前端源码还是公开的, 那我就能搞定, 于是我放弃了研究a库, 开始钻研b库, 然后仔细看 api 和相关源码, 最后发现问题是出在资源加载的路径上, 注释了两行代码之后, 图像资源成功加载。

但一开始加载效果有问题, 继续研究之后, 推测是后端参数设置的问题, 然后通过调整参数, 取得了非常好的加载效果, 选型问题被我解决。

接着是自带 api 的使用, 由于文档难读, 我又没掌握正确的使用方法, 遇到坑了一些困难, 但没想到, 由于我虽然不懂, 但是反复的看, 对各种陌生的 api 和名词也熟悉了, 也找到了一个通俗易懂的入门教程, 然后借着对例子的修修改改掌握了基本用法 。我刚刚入职两周多, 就可以完成老板想要的功能了。

项目也算由此取得突破性进展, 算是一个小成功, 老板表扬了我, 并且表示对另外两个前端的表现不满意, 结果那两个人就不开心走了。


### 失败的例子


再回顾前一份工作中的失败例子, 我的印象中好像有很多。因为做生产, 东西复杂, 就是属于容易出问题的。

比如做我之前做的真空灌注工艺, 简单来说先把纤维布铺好, 然后盖上真空袋密封好, 然后抽真空捡漏

![真空导入工艺](./images/真空导入工艺.png)


如果没有漏气, 灌注树脂, 树脂会被大气压压入真空袋, 浸润纤维, 浸润完全后就封住入口和抽气口. 等待树脂固化. 固化完后脱膜, 得到产品.
船体就是这样一次成型的

![船体](./images/船体的一次成型.jpg)

当然, 最理想的情况是一次成功, 但是实际情况会受到各种因素的干扰.

- 查漏气一般需要 20 分钟以上才能确定

- 如果这个时候漏气了, 要检漏

- 不漏就可以配树脂, 树脂的量要把握好, 多了就是浪费, 少了又要临时加

- 抽好了树脂要等树脂固化

- 产品做好了要脱膜水切割, 万一切坏了之前所有的工作可能全部报废

所以试错的成本还是比较高的

那个时候天真的我每次做产品, 都预期最着完美的情况, 即一次成功, 不出问题.

但现实却是, 凡是有可能出错的地方都会出错(墨菲定律)

对于真空成型来说, 最麻烦的就是真空袋膜漏气, 且真空袋可能在任何一个阶段漏气

检漏阶段, 一般来说很难判断哪里漏了, 实在不行就得换真空袋, 重新检漏

抽树脂的过程中漏气了, 要赶紧找到漏气的点, 不然不停有空气进去就完蛋了

抽完了树脂要等固化, 厚的地方容易过热, 要及时浇水降温, 否则局部发白鼓包, 轻则磨掉再补, 重则返工重做

这个可不是编程, 会报错会及时反馈, 每次出问题都要很紧急, 常常是在救火, 更重要的是, 一旦做坏, 就会感觉之前的工作全部都白费了, 所以我的内心经常非常沮丧,

而我总觉得我掌握了大量的理论知识, 理论与实践结合应该比工人做的更好, 所以每次在做之前我都假想, 这次是我亲自动手做, 所以应该不会出问题.

导致的后果是, 我以为不会出问题, 所以没有做充分的准备, 所以问题一出现, 我就要救火, 所以常常救火, 常常懊恼自己怎么没有做好准备

还有就是我总是以为, 我能够尝试更科学的树脂配比, 更好的固化方案, 更少的原材料消耗, 以达到更优的产品质量. (即更少的树脂用量减少原材料消耗, 更长的固化时间使得固化后变形更少)

然而问题是, 我只是有一定的理论基础, 但实际上做的东西, 很少做产品测试, 自己的记录也不充分, 相关反馈也少, 最终我都没确定这样的做法究竟使性能提高了多少.

但更少的树脂用量, 更长的固化时间, 确实使得我在遇到真空袋漏气的时候情况变得更加紧急, 临时加的树脂总是还会浪费一些, 更久的固化时间也导致了更多的不确定性, 提高了风险.

风险发生的时候, 我的内心还很崩溃, 最后过很多次, 也有多次导致产品差点报废的经历, 多次痛定思痛后, 我也接受了这个事实.

每件产品无论大小都可能出错, 每次都要做最好的准备和最坏的打算, 否则我就容易内心很崩溃.

不过这也确确实实的扭转了一些我的世界观, 我发现原来可以通过把一件事情做坏的方式去把它做好.

总之, 我拥有了丰富的把一件产品差点搞废的经验, 以致于我几乎可以在做之前就想到所有搞砸的可能, 然后通过我自己的准备, 将其一一避免, 就如芒格所说:

> 我只想知道将来我会死在什么地方,这样我就永远不去那儿了。

当然, 也有问题避免不了的, 那我也提前做好心理准备, 把我的心理上的损失, 也尽可能降低.

有一道著名的餐馆的面试题目：

如果你的餐盘掉下来，你又无力挽救，那你该怎么办？

最佳答案就是：用尽全力，把餐盘抛向离你最近的没有妇女和孩子的方向。

每次做坏了东西, 就这样想想, 东西已经做坏, 而我又无力挽救, 最好的处理方式不是浪费时间浪费心情, 而是马上去着手重做, 争取把下一个做好.


另外我还明白, 这个世界根本不会按照我的理论, 我的想象来走, 永远在出各种各样的意外, 就如墨菲定律能成为定律也正是如此.

总结起来就是, 我从一个容易失败的工作中, 得到的不仅是沮丧, 还得到了处理和面对失败的能力

<!-- 这段不要 start -->
还记得之前我每次在颓废一段时间之后, 都会做各种学习规划, 说这周末一定要学点什么, 干点什么

然后一到周末, 什么各种活动来了, 同学也有事要去帮忙, 什么聚会, 什么生活杂事, 仿佛自己颓废的时候就有事, 一下定决心要好好学习, 就各种事情来打扰我, 仿佛别人在和自己作对, 生活总是在和自己开玩笑, 总是来干扰自己的学习.

甚至我已平静的接受了这个事实, 没有事情的时候还好, 一旦有个什么事情, 我就预感各种事情都会一起来, 然后就真的各种事情, 反正我也不知道是不是生活的玩笑
<!-- 这段不要 end -->

那这个能力还用在了什么地方呢..辞职的时候..

辞职是一个重大决定, 我需要要放弃部分安全感, 那这个安全感到底指什么呢

如果安全感比较难理解, 那与安全相对的恐惧则容易理解一些, 这是人的基本情绪

恐惧的内容有: 辞职会不会给这些前同事留下很不好的印象, 领导挽留我要怎么办, 我会很长时间没有收入, 或者入不敷出, 还可能转行失败, 没找到工作. 前面的恐惧都还好, 最终的恐惧是我找不到工作, 没有饭吃了, 可能要回家啃老还是怎么搞.

在内心追问之后, 我发现最终恐惧的是, 我离开了这家公司后, 无法养活我自己.

那么利用我与失败为友的各种经验, 我应该提前想好解决方案, 避免失败的可能.

从辞职开始, 假设领导硬要留我, 我就说我已经报了一个培训班, 半个月后就会开课了, 不留后路.

然后, 假设我学完了前端, 要找两个月才能找到工作, 我需要选一个价格低且靠谱的培训班, 以便留下足够的钱支持我在大城市无收入生活3个月.

假设, 我最终真的转行失败, 之前所有的钱都打了水漂...那我可以再回老本行试一试

假设, 真的没人要我...我可以回家端盘子! 不过我判断, 以我的能力, 这个事件不会发生.

最后, 我既然都假设到这个份上了, 我既然已经可以面对最终的失败了, 那我就没什么恐惧了, 辞职转行就可以从思想层面慢慢转化到行为层面了.然后做出了我人生最重要的决定.

所以现在的我, 一点都不怕失败, 因为失败给了我很多成长, 我好像是一个容易从负反馈中获得成长的人


---
然后华佼今天给了我一点负反馈...其实我是求之不得的, 因为上一份工作的经历加上我本身的心态, 是能够承受大量的负反馈的, 而现在的环境太过安逸了, 太难接受到负反馈了
---


2017年7月13号 8:20反馈：

1）“要求从完全陌生的三个库里选出一个来, 展现我们的图像”--能否给出图像效果实例？
为什么需要一个选择原则？谁告诉你的？还是你自己认为的？原因写出来。
"所以根据我的信念, 如果别人能搞定, 那我就能搞定, "为什么你有这样的信念？
“这时发现一个类似的网站, 能使用b库展现同样的图像格式。”建议给出gif动图展示。
“最后发现问题, ”是什么问题？

2） “那天有重要客人来我们公司参观”——有多重要？
“但上午为了实现某个需求”——这个需求与给客户的演示相关吗？需要说明
我们老板之后的说法是“从来没有想今天这么丢人过”。——事后有没有跟老板沟通过这次损失有多大？自己有没有做什么弥补？如果没有做过, 现在可以补上, 然后补充在这个故事里面。

3）“再回顾前一份工作中的失败例子, 我的印象中好像有很多。”——后面一个事例也没有看到。一个事例包含时间、地点、人物、事件起因、经过、结果。而不是仅仅是想法。


---

7月16日早上, 华佼建议的反思

唉,  你说的我刚刚反思了很久,  可以说是我人生上的一个巨大的问题.

就是我不能很好的分辨一件事情的重要程度,  并且每次到了重要的时候,  都会拖延很久,  所以我目前做的最正确的一件事情是,  转行,  但是这个决策是做了两个月之久.

不过对于生活中的快决策,  我还是很难把控,  在帮助别人这件事情上,  我总是想着,  能帮助别人是一件很好的事情,  并且我也会从中得到成就感.  所以往往就把别人的事情放在更高优先级了.

然后你说的我在工作中失误的那件事,  我现在确实能感觉到老板对我打的分数是降低了的,  但是我之前是真的没有意识到,  我只是觉得我犯了一个对我自己来说不该犯的严重错误,  因为这个错误之前犯过很多次,  也有了很深刻的教训,  但没想到这次竟然还是在掉到了同样的坑里.  所以非常恼火,  当时心里也是一惊.  你说的对我们老板造成的影响,  我大概知道就是给用户留下了很不好的印象.  就是平时做的东西都还不错,  怎么一到关键时候就不行了呢.  所以最近老板的态度也没有之前那么好了.  总之上次是特意警告过我们几个了,  说不允许再有下次了,  我相信以我长期失败的经验,  打概率是应该不会再掉链子了,  但说不清楚会不会有小概率又脑袋犯糊.  在重要的事情上行动力下降.

这件事情对我来说这么难,  可能就是我以前受到我父母的影响,  他们都没有什么决策能力,  总是在重要的事情上面无作为,  我深受其害,  这也是镜像神经元的效果,  然后我努力了很多年,  到现在我自认为已经在一定程度上摆脱了他们的影响.

这个问题之前我有意识到,  但我没有意识到这件事情这么严重,  如果我不改掉的话,  我可能还是会活成了我父母的样子,  但是从来没有人来点醒我.

从心理学的角度来看,  我越是回忆这些事情,  影响其实越深刻,  所以我也不去刻意回忆了,  只要自己能变得更好.

当然最好的方法,  不是就这样想想,  而是去找那些在关键时候能够做好决策的人,  然后去看看他们怎么行动,  还是得让自己的镜像神经元起作用,  (但是去哪里找这样的人呢,  突然想到有很多成功人士很喜欢读一些伟大人物的传记,  这会不会是一个好方法呢)


总之今天听君一言,  我对我自己的认识有清晰了一层,  人生中能够给直言不讳给我反馈的人实在是太少了

其实这个失败我之前也提到过,  就是我多次以为自己能把事情做好,  但最后搞砸.  然后我好不容易在多次的失败中有了效果远远超出理论的,  这样深切的体会,  即 我不能认为我对世界的理解就是世界的样子,  客观世界真实样子必须要通过反馈来修正我的理解.

然后将这些经验用在了我转行上,  然后正确做出了我人生中目前最要的一次决策,  但随着时间的流逝,  这种体验也在渐渐消失,  我怕我又回到之前那种样子了.

然后,  对于之前你帮我修改的那篇文章,  我也是非常抱歉你花了那么多时间,  但我却没太重视,  这点我也不做解释了,  因为其实对于已经没做好的事情,  我是以对待沉没成本的心态来处理,  如果损失已经造成且无法挽回,  那就尽最大努力把它减到最小.

其实我潜意识可能也意识到了,  最近很奇怪的想起了两篇以前学过的文言文
《邹忌讽齐王纳谏》和《触龙说赵太后》

我会将如何判断一件事的重要性,  并去做好它,  作为我接下来最重要的反思.

我知道即使短时间表现再好,  也架不住我长期在重要时候掉链子.

最后,  华佼,  人生这个长跑,  还是很幸运能遇到你的,  


2017-7-17 11:54 反馈：

总体两个故事按反馈改得不错。建议接下来要做的修改是：

1） b.gif, c.gif 看不太明白是要做什么，另外建议在录制gif的起点图片上，多停留1s的样子，让人能够清楚的看到起点和终点，看清楚加载的过程是为了达到什么目的；

2）失败的例子中，关于现在公司的那件事情，删掉；用注释标记不要的部分，删掉；不要留在文档里；

3）现在分出两个新文档；一个是选择库并应用成功的故事，一个是从用上一份工作中失败的经验教训，指导做辞职决定的故事。

4）“即我在入职的第一周, 要求从完全陌生的三个库里选出一个来,” 交代下背景，因为你的读者可能不是你的同行，会看不懂。
