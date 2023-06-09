# st-link连接STM32

## stlink-v2的接口定义

```
 RST -| |- SWCLK
SWIM -| |- SWDIO
 GUD || |- GUD
3.3V -| |- 3.3V
5.0V -| |- 5.0V
```

## SWD接口定义

```
  VCC -| |- VCC
  N/U -| |- GND
  N/U -| |- GND
SWDIO -| |- GND
SWCLK -| |- GND
  N/U || |- GND
  SWO -| |- GND
RESET -| |- GND
  N/C -| |- GND
  N/C -| |- GND
```

连接st-link和SWD对应接口

#### 补充

JTAG接口定义

```
     VCC -| |- VCC
    TRST -| |- GND
     TDI -| |- GND
TWIO/TMS -| |- GND
TCK/TCLK -| |- GND
    RTCK || |- GND
     TDO -| |- GND
   RESET -| |- GND
     N/C -| |- GND
     N/C -| |- GND
```

## openocd + stlink下载

关于cfg文件

```cfg
# link.cfg file
source [find interface/stlink.cfg]

transport select hla_swd

source [find target/stm32f1x.cfg]
```
