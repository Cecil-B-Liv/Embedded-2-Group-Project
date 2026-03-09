# Embedded 2 Group Project

## Project Overview
This project is part of the **EEET-2481: Embedded System Design and Implementation** course at the School of Science, Engineering and Technology. The project demonstrates practical implementation of embedded systems principles through two main exercises: UART Communication and a Stopwatch System using the NUC140 microcontroller platform.

## Course Information
- **Course**: EEET-2481 Embedded System Design and Implementation
- **School**: School of Science, Engineering and Technology
- **Lecturer**: Thanh Pham
- **Group**: 12
- **Submission Date**: 15/01/2025

## Team Members
| Name | Student ID |
|------|-----------|
| Huynh Ngoc Tai | s3978680 |
| Tran Quang Minh | s3988776 |

## Project Structure

```
Embedded-2-Group-Project/
├── README.md
├── Question1/
│   ├── Source code (UART Communication Exercise)
│   ├── Hardware configuration
│   └── Test results
├── Question2/
│   ├── Source code (Stopwatch System Exercise)
│   ├── Timer0 interrupt configuration
│   └── Test results
└── Assignment Report/
    └── Detailed documentation and analysis
```

---

## Exercise 1: UART Communication

### Overview
This exercise implements bidirectional UART communication between the NUC140 microcontroller and a host computer using a terminal application.

### Technical Specifications
- **Clock Frequency**: 22.1184 MHz
- **Baud Rate**: 115200 bps
- **Data Format**: Standard UART configuration
- **Communication Type**: Bidirectional (receive and transmit)

### Implementation Details
- UART module initialization and configuration
- Message transmission and reception setup
- Terminal application integration for testing
- Message echoing verification

### Key Features
✓ Reliable data transmission at high baud rate  
✓ Real-time message echoing capability  
✓ Proper UART protocol implementation  
✓ Verified communication with terminal software

### Testing & Verification
- Terminal application successfully receives and displays transmitted data
- Message echoing confirms bidirectional communication
- UART communication operates reliably at 115200 bps
- All data transmission/reception tests passed

---

## Exercise 2: Stopwatch System

### Overview
This exercise implements a comprehensive stopwatch system with multiple operational modes and lap time recording capabilities using Timer0 interrupts.

### Technical Specifications
- **Timer Module**: Timer0 with interrupt-driven operation
- **Microcontroller**: NUC140 (ARM Cortex-M0)
- **Interrupt Handling**: Timer0 interrupt service routine (ISR)

### Operational Modes

| Mode | Description | Trigger |
|------|-------------|---------|
| **Idle** | System at rest, ready to start | Initial state |
| **Count** | Timer actively counting elapsed time | K1 button press |
| **Pause** | Timer paused, time maintained | K9 button press |
| **Check** | Display lap time while maintaining count | K5 button press |

### Button Controls
- **K1**: Start/Resume counting
- **K9**: Pause/Resume operation
- **K5**: Record and display lap time

### Key Features
✓ Precise time measurement using Timer0 interrupts  
✓ Multiple operational modes for flexible operation  
✓ Lap time recording and display capability  
✓ Button-controlled operation with debouncing  
✓ Accurate time tracking and state management

### Testing & Verification
- Timer0 interrupts functioning correctly
- All operational modes (Idle, Count, Pause, Check) verified
- Button controls responding as expected
- Lap time recording and display working properly
- Multi-mode operation transitions confirmed
- Time accuracy validated

---

## Technical Specifications

### Microcontroller: NUC140
- **Architecture**: ARM Cortex-M0
- **Operating Frequency**: Up to 48 MHz
- **Flash Memory**: Up to 64 KB
- **SRAM**: 8 KB
- **GPIO Pins**: Multiple GPIO pins for peripheral connection
- **Peripherals**: UART, Timer, GPIO interrupt support

### Development Environment
- **IDE**: Keil μVision MDK (Microcontroller Development Kit)
- **Compiler**: ARM C/C++ Compiler
- **Debugger**: Integrated Keil debugger with hardware support
- **Target Platform**: NUC140 evaluation board

### Hardware Components & Connections
- NUC140 microcontroller board
- UART communication interface (RS-232/USB)
- Push-button switches (K1, K9, K5)
- Timer0 module with interrupt capability
- LED indicators (if applicable)

---

## Development Environment Setup

### Prerequisites
1. **Keil μVision IDE** - Download and install from Arm Keil official website
2. **NUC140 Device Pack** - Add to Keil for device support
3. **Hardware**: NUC140 evaluation board with debugger connection
4. **USB Connection**: For UART communication and debugging

### Project Configuration
1. Open the project in Keil μVision
2. Select NUC140 device target
3. Configure clock frequency to 22.1184 MHz
4. Set UART parameters: 115200 bps, 8-bit data, 1 stop bit, no parity
5. Enable Timer0 module with interrupt configuration
6. Connect UART interface for terminal communication

### Building the Project
```
1. Open project file in Keil MDK
2. Build solution (F7 key)
3. Verify no compilation errors
4. Flash to NUC140 device
5. Run and test functionality
```

---

## Testing & Verification Procedures

### UART Communication Testing
1. Connect NUC140 board via USB
2. Open terminal application (e.g., Putty, TeraTerm)
3. Configure terminal: 115200 bps, 8-bit, 1 stop bit
4. Transmit test messages
5. Verify message echoing and reception
6. Document successful communication

### Stopwatch System Testing
1. Flash the stopwatch program to NUC140
2. Press K1 to start counting
3. Press K9 to pause/resume
4. Press K5 to check/record lap time
5. Verify mode transitions and timer accuracy
6. Test multiple counting and pause cycles
7. Confirm lap time display functionality

---

## Key Achievements

### Exercise 1 - UART Communication
- Successfully implemented UART at 115200 bps
- Achieved reliable bidirectional communication
- Verified message transmission and reception
- Integrated with terminal application
- All specifications met and tested

### Exercise 2 - Stopwatch System
- Implemented accurate Timer0 interrupt handling
- Developed stable multi-mode operation system
- Implemented button control with proper debouncing
- Added lap time recording functionality
- All modes verified and working correctly

---

## Source Code Organization

### Question1 (UART Communication)
- `uart_init.c/h` - UART initialization and configuration
- `uart_comm.c/h` - Communication functions (send/receive)
- `main.c` - Main program with UART testing
- `startup_code` - System initialization code

### Question2 (Stopwatch System)
- `timer0.c/h` - Timer0 configuration and interrupt handler
- `stopwatch.c/h` - Stopwatch logic and mode management
- `button_control.c/h` - Button input handling and debouncing
- `display.c/h` - Display output for time and lap information
- `main.c` - Main program with stopwatch application

---

## Documentation & Reports

The assignment report contains:
- Detailed implementation methodology
- Circuit diagrams and hardware schematics
- Code explanation and functional analysis
- Testing procedures and results
- Challenges encountered and solutions
- Performance analysis and conclusions
- Appendices with source code listings

---

## How to Use This Repository

1. **Clone the repository** to your local machine
2. **Navigate to Question1 or Question2** folders for specific exercises
3. **Open in Keil μVision** for development and testing
4. **Refer to assignment report** for detailed documentation
5. **Follow testing procedures** to verify functionality
6. **Review source code** for implementation details

---

## Troubleshooting

### UART Communication Issues
- Verify clock frequency is set to 22.1184 MHz
- Check UART baud rate configuration (should be 115200 bps)
- Ensure correct COM port selection in terminal application
- Verify USB cable connection to NUC140 board

### Stopwatch System Issues
- Confirm Timer0 interrupt is properly enabled
- Check button connections and GPIO configuration
- Verify debouncing timing in button control module
- Test with oscilloscope if timing accuracy issues occur

---

## References & Resources

- NUC140 Datasheet - Device specifications and peripheral details
- Keil MDK Documentation - IDE and compiler reference
- ARM Cortex-M0 Reference Manual - CPU architecture details
- UART Protocol Standards - Communication specifications
- Timer Module Documentation - Interrupt and counting modes

---

## Contact & Support

For questions or issues regarding this project, please contact:

- **Huynh Ngoc Tai** (s3978680)
- **Tran Quang Minh** (s3988776)

Or reach out to the course lecturer:
- **Lecturer**: Thanh Pham

---

## License

This project is part of the EEET-2481 course at the School of Science, Engineering and Technology. All code and documentation are for educational purposes.

---

**Last Updated**: 15/01/2025  
**Course**: EEET-2481 Embedded System Design and Implementation  
**Group**: 12
