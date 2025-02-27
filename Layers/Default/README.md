# Board: STMicroelectronics [STM32H7B3I-DK](https://www.st.com/en/evaluation-tools/stm32h7b3i-dk.html)

## Default Board Layer

Device: **STM32H7B3LIHxQ**

System Core Clock: **72 MHz**

This setup is configured using **STM32CubeMX**, an interactive tool provided by STMicroelectronics for device configuration.
Refer to ["Configure STM32 Devices with CubeMX"](https://open-cmsis-pack.github.io/cmsis-toolbox/CubeMX/) for additional information.

### System Configuration

| System resource       | Setting
|:----------------------|:--------------------------------------
| Heap                  | 64 kB (configured in the STM32CubeMX)
| Stack (MSP)           |  1 kB (configured in the STM32CubeMX)

### STDIO mapping

**STDIO** is routed to Virtual COM port on the ST-LINK (using **USART1** peripheral)

### CMSIS-Driver mapping

| CMSIS-Driver          | Peripheral            | Board connector/component                     | Connection
|:----------------------|:----------------------|:----------------------------------------------|:------------------------------
| Driver_GPIO0          | GPIO                  | Arduino digital I/O pins D2..D10, D14..D19    | ARDUINO_UNO_D2..D10, D14..D19
| Driver_I2C4           | I2C4                  | Arduino I2C pins D20..D21                     | ARDUINO_UNO_I2C
| Driver_MCI1           | SDMMC1                | MicroSD card slot (CN4)                       | CMSIS_MCI
| Driver_SPI2           | SPI2                  | Arduino SPI pins D10..D13                     | ARDUINO_UNO_SPI
| Driver_USART1         | USART1                | ST-LINK connector (CN14)                      | STDIN, STDOUT, STDERR
| Driver_USART2         | USART2                | STMod+ pins PMOD2-TX, PMOD3-RX (P1)           | CMSIS_USART
| Driver_USART4         | UART4                 | Arduino UART pins D0..D1                      | ARDUINO_UNO_UART
| Driver_USBD1          | USB_OTG_HS            | USB_OTG_HS connector (CN15)                   | CMSIS_USB_Device
| CMSIS-Driver VIO      | GPIO                  | LEDs (LD3, LD2) and USER button (B2)          | CMSIS_VIO

Reference to [Arduino UNO connector description](https://open-cmsis-pack.github.io/cmsis-toolbox/ReferenceApplications/#arduino-shield).

### CMSIS-Driver Virtual I/O mapping

| CMSIS-Driver VIO      | Board component
|:----------------------|:--------------------------------------
| vioBUTTON0            | USER button (B2)
| vioLED0               | LED red     (LD3)
| vioLED1               | LED blue    (LD2)
