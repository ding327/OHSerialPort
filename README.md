# OHSerialPort
 鸿蒙串口通信

注：底层发送与接收字节数暂限制1024个

使用方法：
将lib文件夹放入工程之中即可（entry文件夹下）；

打开串口：
this.fd = serialPort.open_port(this.uartPort, this.bandRate);

关闭串口:
let result: number = serialPort.close_port(this.fd);

发送数据：支持string和数组[]
let value: number = serialPort.send_data(this.fd, message)

接收数据：支持string和数组
let strData: string = serialPort.receive_data_str(this.fd);
let rawData: number[] = serialPort.receive_data(this.fd)


