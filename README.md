# STM32F103C8T6 Overclocking Results

## 🔧 Test Environment

- **MCU**: STM32F103C8T6  
- **Clock Source**: 8 MHz HSE (High-Speed External)  
- **PLL Multiplier**: x2 to x16  
- **System Clock (SYSCLK)**: 16 MHz to 128 MHz  
- **GPIO Toggle Test**: Single GPIO toggled in tight loop  
- **Power Supply**: 3.3V  
- **Measurement Tools**:
  - GPIO toggle speed measured via oscilloscope
  - Current measured with multimeter
  - Power = Voltage × Current
...
- **GPIO Toggle Code**:
```c
HAL_GPIO_WritePin(GPIOB, GPIO_PIN_5, 1);
HAL_GPIO_WritePin(GPIOB, GPIO_PIN_5, 0);
```
---

## 📊 Overclocking Performance Table

| PLL Multiplier | SYSCLK (MHz) | GPIO Toggle Speed (Hz) | Current (mA) | Power (mW) | Stability |
|----------------|---------------|--------------------------|---------------|-------------|------------|
| x2             | 16            | 175.81 KHz               | 16            | 52          | ✅ Stable  |
| x3             | 24            | 263.75 KHz               | 19            | 61          | ✅ Stable  |
| x4             | 32            | 351.67 KHz               | 22            | 71          | ✅ Stable  |
| x5             | 40            | 439.54 KHz               | 25            | 79          | ✅ Stable  |
| x6             | 48            | 527.48 KHz               | 27            | 89          | ✅ Stable  |
| x7             | 56            | 615.46 KHz               | 30            | 97          | ✅ Stable  |
| x8             | 64            | 703.31 KHz               | 33            | 103         | ✅ Stable  |
| x9             | 72            | 791.31 KHz               | 36            | 112         | ✅ Stable  |
| x10            | 80            | 879.18 KHz               | 39            | 122         | ✅ Stable  |
| x11            | 88            | 966.95 KHz               | 42            | 128         | ✅ Stable  |
| x12            | 96            | 1.0551 MHz               | 44            | 138         | ✅ Stable  |
| x13            | 104           | 1.1430 MHz               | 47            | 146         | ✅ Stable  |
| x14            | 112           | 1.2309 MHz               | 49            | 148         | ✅ Stable  |
| x15            | 120           | 1.3187 MHz               | 51            | 151         | ✅ Stable  |
| x16            | 128           | 1.4060 MHz               | 54            | 161         | ✅ Stable  |


![image](https://github.com/user-attachments/assets/c6167676-f366-4714-bdff-1b2fed33110d)
