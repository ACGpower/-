## Unity组件

> ### **Transform**：

Position —— 位置信息

Rotation —— 旋转信息

   Scale  —— 缩放信息

Translate( ) —— 位移信息

  Rotate（） —— 旋转方法

全局  ——》

局部 ——》（local）

> ### 渲染

渲染三维模型

**未绑定骨骼**：

Mesh Filter

Mesh Renderer；

**绑定骨骼**：

Skinned Mesh Renderer（蒙皮网格）；

***Materials**——模型的材质

二维

**Sprite Renderer**：图片素材，颜色，材质等等都可以更换

> ### **相机**Camera：

（特别注意）**projection**：

1. 选择**Perspective**，则使用符合透视规律的三维透视投影

2. 选择**Orthographic**，正交投影，多用于二维游戏

*通过将相机改为正交，来使用三维素材模拟二维效果

> ### 光照light：

*光照计算非常消耗性能，对于一些固定光源产生的光照效果和阴影，可以提前将数据烘焙出来，节省计算资源

> ### 粒子系统Particlesystem：

炫酷的粒子效果

> ### 物理系统：

最基本运用——碰撞检测：

条件：双方都具备Collider（碰撞体组件），受碰撞影响的一方必须具备Rigidbody（刚体组件)

勾选碰撞体上的**Is Trigger**,碰撞体将只作为一个触发器，只监测物体与触发器的交叠状态，不对物体的运动产生影响。

两种针对触发和碰撞进行监测的生命周期方法：

OnCollision

OnTrigger

*除了碰撞检测还有其他效果的组件

> ### 动画

#### Animation ：

用于普通的动画播放控制；

#### Animator：

用于具备复杂转换关系的动画（比如RPG中的角色不同状态的动画之间的转换）——》**statemachine**（状态机）；

快速打开动画制作窗口：（win）Ctrl + 6

unity——>Window——>Animation——>Animator：打开状态机窗口对动画状态进行配置

> ### 多媒体（视频和音频）

**Video Player **可以用于播放视频（可以带声音），可以指定将视频渲染到相机前，UI上甚至材质上

**Audio Source** 播放音频，可配置混音器对游戏的整体音效进行控制

> ### 导航寻路

在**Navigation**窗口中对地形进行烘焙，为需要自动寻路的物体挂载**Nav Mesh Agent**组件，然后就可以在代码中为物体设置目的地。

```c#
using UnityEngine.AL;
public NavMeshAgent agent;
agent.SetDestination(aPosition);
```

> ### UI

打开Unity的UI就可以看见丰富的预制UI，创建好的UI物体会自动挂载好相应的组件，且属于**Canvas**画布物体的子物体，没有**Transform**，取而代之的是**Rect Transform**，根据UI的特性进行很多的扩展，结合画布的配置，可以方便地对不同分辨率的屏幕进行自适应

![](C:\Users\邹子康\AppData\Roaming\Typora\typora-user-images\image-20231023144708493.png)

### 总结

组件既可以在引擎界面进行预先配置，也可以代码在运行阶段动态更改，可以定义一个公开变量，在unity中拖动获取一个组件