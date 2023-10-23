## C#在unity 1

> #### 创建变量

**public (公开)**

**private（私有）**

| public/private | int        | health   | =5                        |
| -------------- | ---------- | -------- | ------------------------- |
| 公开/私有      | 变量类型   | 变量名称 | 初始值                    |
|                | float      |          | 5.5f（新版本不加f也行）   |
|                | bool       |          | true/false（默认是false） |
| unity默认      | GameObject |          |                           |
|                | Transform  |          | 保存代码（win)CTRL + S    |

所有在**Hierarchy**出现（创建）的东西 都代表**gameobject**

在创建的C#文件中 **public gameobject**来创建一个变量，把在**Hierarchy**中创建的**gameobject**拖拽到**inspector**中，这样就可以获得了，可以使用这个**gameobject**里面所有的**conponent**

哪一个**conponent**需要编辑,就定义一个类型的变量

#### Start 和 Update

点击play的bottom（按钮），所有在**Start**写的代码都会被执行

**Update**是每一帧执行一次

另外一个预制 **Awake**   无论**script**是否启动，都在开始的时候运行

