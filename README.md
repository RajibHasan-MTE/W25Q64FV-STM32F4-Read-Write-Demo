# W25Q64FV-STM32F4-Read-Write-Demo

![Pinout](DOCS\img.jpg)

This repository demonstrates how to interface the Winbond W25Q64FV 64Mbit (8MB) SPI Flash memory with STM32F4 microcontrollers using SPI protocol.
**Goal**: Enable learning and development by providing working code for initializing, reading, writing, and erasing memory blocks on the W25Q64FV.
Manufacturer: Winbond
Memory Size: 64 Megabits (8 Megabytes)

# 🧠 Memory Organization:
- Pages: 256 Bytes each
- Sectors: 64KB each (with 16 pages per sector)
- Blocks: Includes 32KB and 64KB erase blocks

## 📌 W25Q64FV Flash Memory IC Pinout

# 🔐 Security Features:

-Block Protection: Protect certain memory regions
-Software & Hardware Write Protection
-Power-down mode for ultra-low power

# 🧩 Packages Available:
-8-pin SOIC, WSON, and others (compact for PCB integration)

🛠️ Applications:

- Embedded systems
- Code storage for microcontrollers
- Data logging
- Consumer electronics
- IoT devices
---

## Project Features

- SPI initialization for W25Q64FV
- Flash memory ID read (Manufacturer ID, Device ID)
- Page program (write 256 bytes)
- Page and buffer read
- Sector erase (4KB)
- Chip erase
- Memory verification
- Low-level SPI communication using HAL

---

## Memory Overview

| Feature               | Value             |
|-----------------------|------------------|
| Flash Size            | 64 Mbit / 8 MB    |
| Page Size             | 256 Bytes         |
| Sector Size           | 4 KB              |
| Block Sizes           | 32 KB, 64 KB      |
| Interface             | SPI (1/2/4-bit)   |
| Voltage               | 2.7V – 3.6V       |

---

## Requirements

- STM32F4 microcontroller (e.g., STM32F401RE, STM32F411, STM32F407)
- STM32CubeIDE
- Winbond W25Q64FV module (breakout or soldered)
- Logic level compatible SPI connection

---

## 📁 Folder Structure

 	W25Q64FV-STM32F4-Read-Write-Demo/
 	├── Core/
 	│ ├── Inc/
 	│ │ 	└── w25q64fv.h # Driver header
 	│ └── Src/
 	└── w25q64fv.c # Driver source
 	├── main.c # Example usage
 	├── README.md
 	└── W25Q64FV-Demo.ioc # STM32CubeMX project file


## 🔌 SPI Pin Mapping Example (for STM32F4)

| Signal  | STM32F4 Pin |
|---------|-------------|
| CS      | GPIOA_PIN_4 |
| SCK     | GPIOA_PIN_5 |
| MISO    | GPIOA_PIN_6 |
| MOSI    | GPIOA_PIN_7 |

Adjust according to your STM32F4 board configuration and set via CubeMX or directly in code.

---

## 🚀 Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/RajibHasan-MTE/W25Q64FV-STM32F4-Read-Write-Demo.git
2. Open the .ioc file with STM32CubeIDE.

3. Generate the project and build.

4. Flash to your STM32F4 board.

5. Observe flash operations via UART or debugger.

📖 Learning Resources
W25Q64FV Datasheet (Winbond)

STM32 HAL SPI Documentation

More about SPI Flash Memory

📬 Contributing
This repository is open for educational purposes. Contributions and improvements are welcome! Please submit a pull request or open an issue for feedback or help.

📄 License
This project is licensed under the MIT License — feel free to use and share!

👨‍💻 Author
Rajib Hasan – GitHub Profile
Student, Embedded Systems Developer, Robotics Enthusiast.

Let me know if you want help with:
- `w25q64fv.c/.h` driver code
- `main.c` read/write test logic
- STM32CubeIDE `.ioc` configuration setup

I'll prepare those files for your repository as well.








