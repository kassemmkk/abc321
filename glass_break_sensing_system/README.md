# Glass Break Sensing System Design

## Project Overview
This project analyzes and compares glass break sensing system implementations using:
1. Off-the-shelf MCU solutions
2. Custom Caravel SoC implementation

## Requirements Analysis

### Functional Requirements
- **Audio Signal Acquisition**: Capture audio signals from microphone
- **Digital Signal Processing**: Real-time frequency analysis and pattern recognition
- **Glass Break Detection**: Identify characteristic frequency patterns (6-8 kHz primary, 13-15 kHz secondary)
- **False Alarm Reduction**: Distinguish glass break from other sounds
- **Communication**: Alert transmission via wireless protocols
- **Power Management**: Low power operation for battery-powered deployment
- **Configuration**: User-configurable sensitivity and parameters
- **Status Indication**: LED/audio feedback for system status

### Performance Requirements
- **Sampling Rate**: Minimum 32 kHz (preferably 48 kHz) for audio capture
- **Processing Latency**: < 100ms for real-time detection
- **Detection Range**: 6-8 meters typical
- **Power Consumption**: < 50mW average, < 500mW peak
- **False Alarm Rate**: < 1 per month under normal conditions
- **Detection Accuracy**: > 95% for actual glass break events

### System Architecture Components
1. **Audio Frontend**: Microphone, amplifier, ADC
2. **Digital Signal Processor**: FFT, filtering, pattern matching
3. **Control Unit**: System management, configuration
4. **Communication Interface**: WiFi/Bluetooth/LoRa
5. **Power Management**: Battery management, sleep modes
6. **User Interface**: Configuration, status indication
7. **Storage**: Configuration, logs, firmware

## Implementation Plan
1. Analyze available IP cores for Caravel implementation
2. Design custom IP cores for missing functionality
3. Compare with off-the-shelf MCU solutions
4. Identify trade-offs and recommendations

## Directory Structure
```
glass_break_sensing_system/
├── docs/                    # Documentation and analysis
├── mcu_reference/          # Off-the-shelf MCU analysis
├── caravel_design/         # Custom Caravel SoC design
├── ip_analysis/            # Available IP core analysis
├── missing_ip/             # Custom IP designs needed
└── comparison/             # Detailed comparison results
```