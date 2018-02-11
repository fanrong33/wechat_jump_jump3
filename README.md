# wechat_jump 的思考
首先我们需要了解人类是如何学习的？严格来说是人类的大脑是如何学习的？
我们人类彻底理解一个物体，我们可以抽象出形状，不管是圆形的，正方形的，长方形的，圆柱体，凹形的。

人眼撇一眼，就可以高速识别出一个物体，不需要太清晰的图像，减低处理压力。
人眼其实只是输入，识别能力其实是大脑，大脑的视觉神经具有边缘检测的能力，边缘敏感，就是为了构造这个物体的轮廓，为了快速理解这个物体，以便不被吃掉，为了生存。

所以，所有看到的东西（图像）2D的，在你头脑中其实都是3D的抽象的物体（忽略了物体的细节图案啊花纹啊什么的，加快大脑的处理速度，降低了能量消耗）。


然后用强化学习来完成接下来的目标。(感觉还是需要一些物理知识，或者是常识)

* 跳一跳的目标是为了跳到物体顶面的中心，可以拿到最高分
* 而现实世界如果目标是拿起这个物体，则是为了找到合适的拿起位置。

所以微信跳一跳是非常好的一个游戏，开启了人工智能的大门。



## Roadmap
### Plan 1
利用opencv模板匹配+边缘检测识别棋子的坐标和下一个物体顶面的中心点坐标，根据两个点的距离，预估按压的时间来进行跳跃。
 * 缺点：仅对所有纯色平面和部分非纯色平面有效，对高尔夫草坪面、木纹桌面、药瓶和非菱形的碟机无法正确识别中心点，毕竟它不理解什么是物体，什么是物体的正上面😔💭

### Plan 2
神经网络
https://github.com/zhanyongsheng/LetsJump

### Plan 3
强化学习
