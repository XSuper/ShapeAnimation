# ShapeAnimation
### 整理之前项目中的一个帧动画实现，用SurfaceView实现并添加多种状态控制，效果上仅添加简单的从中心点扩展演变和透明度变化！

#### 欢迎大家下载体验或提供更好的效果实现

## 演示
![image](./screenshots/star_demo.gif)![image](./screenshots/pause_demo.gif)![image](./screenshots/stop_demo.gif)

## 实现原理
ShapeAnimationView继承自SufaceView，使用DrawThread和Canvas绘制界面！
通过开启、暂停、停止、销毁等状态控制动画显示，这里既有停止又有销毁，是为了防止重复创建View，仅需复用View通过改变参数得到不同形状的动画呈现！
另外就是对于shape.XML文件的解析，所有的Shape都是通过在720*1280屏幕上描点绘制！PullParse解析得到描点数据后获取中心点和极值得到所有的有中心扩展演变的数据模型！

## 使用注意事项
Shape切换需要等上一个动画效果跑完后即state置为stop状态后才能够切换成功得到设置后的效果！

## 改进和期待
这个效果实现很久了，一直没有整理！之前在[codepen.io](http://codepen.io/)上看到过一个用JS实现的更酷炫动画（遗憾未找到链接地址）：不用绘制已有的效果，直接输入英文语句即可得到如同ShapeAnimation类似的酷炫动画来呈现这条语句！这或许就是当前项目改进方向，省去xml文件绘制，直接由用户输入得到效果！


License
=======

    The MIT License (MIT)
    
    Copyright (c) 2016 Leone90
    
    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the "Software"), to deal
    in the Software without restriction, including without limitation the rights
    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
    copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:
    
    The above copyright notice and this permission notice shall be included in all
    copies or substantial portions of the Software.
    
    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
    SOFTWARE.
