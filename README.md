# STM32 Hardware Journey

本仓库记录了个人从软件底层（C语言/数据结构）转向嵌入式硬件实战的学习历程。包含从基础外设驱动到 RTOS 系统的实战代码，所有工程均基于现代开源工具链构建。

## 🛠️ 开发环境与技术栈
- **主控芯片**：STM32F103C8T6
- **代码生成与配置**：STM32CubeMX
- **编辑器与插件**：VS Code + STM32CubeIDE for VS Code
- **编译工具链**：ARM GNU Toolchain (arm-none-eabi-gcc 13.3.1)
- **构建系统**：CMake + Ninja
- **烧录与调试**：ST-Link V2

## 📂 项目列表

### [01_blink_led](./01_blink_led) - 基础 GPIO 控制
- **功能描述**：配置 PC13 引脚为推挽输出，利用 `HAL_GPIO_TogglePin` 实现板载 LED 的 500ms 周期闪烁。
- **核心掌握**：STM32CubeMX 工程配置、系统时钟树基础配置（RCC/HSE）、SWD 调试接口配置、交叉编译流程。
- **技术难点（已解决）**：脱离 Keil，在 Windows 下纯手工配置 CMake 工具链，解决 `arm-none-eabi-gcc` 找不到、Ninja 构建死锁以及 VS Code IntelliSense 路径不匹配等环境问题。

## 🚀 后续规划
- [ ] **02_uart_ring_buffer**：配置串口中断，结合自研的环形缓冲区（Ring Buffer）实现高可靠的数据收发。
- [ ] **03_i2c_oled**：驱动 OLED 屏幕，掌握 I2C 通信协议与时序。
- [ ] **04_freertos_base**：移植 FreeRTOS，学习任务调度与队列机制。

---
*持续更新中...*