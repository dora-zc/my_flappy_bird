# Flappy_bird
> 小鸟飞翔游戏。

### 设计模式的使用
> 除了util外，所有模块都使用了沙箱模式；
另外这些模块还使用工厂模式；
bird模块使用了单利模式；
gameScene使用了观察者模式。

### 继承的使用
> 除了util外，其他模块要么使用了原型覆写的继承方式，
要么使用了混入式继承。

### 模块之间的依赖
> 几乎所有的模块即依赖util模块，所以它需要先引入；
gameScene模块依赖：bird、land、pipe、sky模块，
主函数模块依赖：gameScene、overScene模块。

### util模块
- extend: 实现混入继承
- loadImage: 图片加载器

### bird模块
- draw: 绘制鸟
- update: 更新下一帧绘制时所需的数据

### land模块
- draw: 绘制大地
- update: 更新下一帧绘制时所需的数据

### sky模块
- draw: 绘制天空
- update: 更新下一帧绘制时所需的数据

### pipe模块
- draw: 绘制管道
- update: 更新下一帧绘制时所需的数据

### gameScene模块
- addListener：添加小鸟死亡事件的听众
- triggerBirdOver: 触发小鸟死亡事件，通知所有听众
- draw：绘制场景

### overScene模块
- draw：绘制场景
