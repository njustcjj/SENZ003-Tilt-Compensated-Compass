# SENZ003-Tilt-Compensated-Compass

###### 翻译

> `英文`请参考 [`这里`](https://github.com/njustcjj/SENZ003-Tilt-Compensated-Compass/blob/master/README.md).

> `中文`请参考 [`这里`](https://github.com/njustcjj/SENZ003-Tilt-Compensated-Compass/blob/master/README_CN.md).

![](https://github.com/njustcjj/SENZ003-Tilt-Compensated-Compass/blob/master/pic/SENZ003.jpg "SENZ003") 

### 产品介绍

> 本模块采用了意法公司最新推出的电子罗盘芯片MPU-6050，集成了3轴磁场，3轴加速度传感器，可以提供倾斜补偿后的输出。 
> MPU-6050芯片的加速计、磁力计、A/D转化器集成在一起，通过I2C总线和处理器通信。这样只用一颗芯片就实现了6轴的数据检测和输出。

#### 用途：

- 运用感测游戏
- 行人导航器
- “零触控”手势用户接口
- 认证
- 带补偿的电子罗盘
- 地图循环
- 方位探测
- 动作触动设备
- 自由落体侦测
- 手持设备的智能省电设备
- 方向显示
- 动态交互输入设备
- 碰撞识别与记录设备
- 振动监测和补偿


### 产品参数

* 供电电压：3.3V
- 接口电平：3.3V
- 量程：
	- - 2/+4/8g 动态可选量程
	- +-1.3 to +- 8.1 全量程高斯磁场
- 16-bit 数据输出
- 通讯接口：I2C
- 接口类型：Gadgeteer Type I 接口、0.1"插针孔连接传统arduino
- 开关功能：上拉电阻选择开关
- 嵌入式自我测试
- 模块尺寸：32x27mm

### 使用教程

#### 引脚定义

> 1脚-信号输出
>
> 2脚-电源地
>
> 3脚-电源正

##### 用法及注意事项
1. 元件开始通电工作时，没有接触丁烷气体，其电导率也急剧增加，约一分钟后达到稳定，这时方可正常使用，这段变化在设计电路时可采用延时处理解决。
2. 加热电压的改变会直接影响元件的性能，所以在规定的电压范围内使用为佳。
3. 元件在接触标定气体1000ppm丁烷后10秒钟以内负载电阻两端的电压可达到 ( Vdg-Va )差值的70% ( 即响应时间 )；脱离标定气体1000ppm丁烷30秒钟以内负载电阻两端的电压下降到 ( Vdg -Va )差值的70% ( 即恢复时间 )。
4. 符号说明
 * 检测气体中电阻-Rdg
 * 检测气体中电压-Vdg

    Rdg与 Vdg的关系：Rdg=RL(VC/Vdg-1)
5. 负载电阻可根据需要适当改动，以满足设计的要求。
6. 使用条件：温度-15~40℃；相对湿度20～85%RH；大气压力80～106KPa。
7. 环境温湿度的变化会给元件电阻带来小的影响，可进行湿度补偿，最简便的方法是采用热敏电阻补偿之。
8. 避免腐蚀性气体及油污染，长期使用需防止灰尘堵塞防爆不锈钢网。

#### 连线图

![](https://github.com/njustcjj/SENZ003-Tilt-Compensated-Compass/blob/master/pic/SENZ003_connect.png "连线图") 

### 示例代码

    void setup() 
    { 
      Serial.begin(9600); // 9600 bps
    }
    void loop() 
    {
      int val;
      val=analogRead(0);
      Serial.println(val ,DEC);// val信息加载在Serial中传输
      delay(100);
    }


### 购买[*SENZ003 电子罗盘传感器*](https://www.ebay.com/).