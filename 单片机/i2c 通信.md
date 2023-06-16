# iic通信

*IIC*一共有只有两条总线，一条双向的串行数据总线*SDA(send data)*，一条串行时钟线*SCL(Serial clock line)*

## *IIC*时序

### 空闲状态

*SCL*和*SDA*保持高电平

### 开始信号

*SCL*保持高电平，*SDA*由高电平变为低电平延时$>4.7us$，*SCL*变为低电平

```c
SDA=1;
delay_us(5);
SCL=1; // 确保SDA SCL高电平
delay_us(5);
SDA=0;
delay_us(5);
SCL=0;
```

### 停止信号

```c
SCL=0;
SDA=0;
delay_us(4);
SCL=1;
SDA=1;
delay_us(5);
```

