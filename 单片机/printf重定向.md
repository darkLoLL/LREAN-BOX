```c
// 需要引用 stdio.h
#ifdef __GNUC__  
#define PUTCHAR_PROTOTYPE int __io_putchar(int ch)  
#else  
#define PUTCHAR_PROTOTYPE int fputc(int ch, FILE *f)  
#endif  
PUTCHAR_PROTOTYPE  
{  
    //具体哪个串口可以更改huart1为其它串口  
    HAL_UART_Transmit(&huart1, (uint8_t *)&ch, 1 , 0xffff);  
    return ch;  
}
