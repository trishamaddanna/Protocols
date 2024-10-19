# Protocols
1. UART is a Universal Asynchronous Receiver Transmitter protocol that is used for serial communication. Two wires are established here in which only one wire is used for transmission whereas the second wire is used for reception. Data format and transmission speeds can be configured here.
DEVICE A that is having transmitter PIN and a receiver pin; DEVICE B is having a receiver and transmission pin. The Transmitter of DEVICE A is one that should be connected with the receiver pin of DEVICE B and the transmitter pin of DEVICE B should be connected with the receiver pin of DEVICE A we just need to connect two wires for communication. 
If DEVICE A wants to send data, then it will be sending data on the transmitter’s pin and here receiver of this DEVICE B will receive it over and if DEVICE A wants to receive the data, then that is possible on the RX line that will be forwarded by TX of DEVICE B. 
On comparing this serial communication of UART with parallel then it can be observed that in parallel multiple buses are required. Based on the number of lines bus complexity of UART is better but parallel communication is good in terms of speed. 
So, when speed is required at that time we should select parallel communication and for a low-speed application, UART must be used and the bus complexity will be less.

2. SPI stands for Serial Peripheral Interface. It is a protocol that is synchronous serial communication. It is used to communicate between the peripheral devices i.e. input and output devices and microcontrollers. It is allowed to transfer high-speed data.
It is popular with digital communication applications and embedded systems. SPI can transfer the data and receive data from one device to another device at a time.
It is mainly used for connecting the microcontrollers to peripheral devices like sensors, displays, and memory chips. It facilitates the full-duplex, synchronous serial communication between one or more slave devices and a microcontroller.

3. I2C stands for Inter-Integrated Circuit. It is a bus interface connection protocol incorporated into devices for serial communication.
It uses only 2 bi-directional open-drain lines for data communication called SDA and SCL. Both these lines are pulled high.
Serial Data (SDA) : Transfer of data takes place through this pin.
Serial Clock (SCL) : It carries the clock signal.
I2C operates in 2 modes: Master mode, Slave mode
Each data bit transferred on SDA line is synchronized by a high to the low pulse of each clock on the SCL line.
Here are the steps of I2C (Inter-Integrated Circuit) data transmission
Start Condition: The master device sends a start condition by pulling the SDA line low while the SCL line is high. This signals that a transmission is about to begin.
Addressing the Slave: The master sends the 7-bit address of the slave device it wants to communicate with, followed by a read/write bit. The read/write bit indicates whether it wants to read from or write to the slave.
Acknowledge Bit (ACK): The addressed slave device responds by pulling the SDA line low during the next clock pulse (SCL). This confirms that the slave is ready to communicate.
Data Transmission: The master or slave (depending on the read/write operation) sends data in 8-bit chunks. After each byte, an ACK is sent to confirm that the data has been received successfully.
Stop Condition: When the transmission is complete, the master sends a stop condition by releasing the SDA line to high while the SCL line is high. This signals that the communication session has ended.
