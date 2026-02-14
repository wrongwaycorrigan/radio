# Radio Frequency Allocation Database

An XML-based frequency allocation database covering the radio spectrum from 8.3 kHz to 37 GHz, with detailed frequency ranges, modes, and color-coded classifications for radio scanning and monitoring applications.

## Overview

This file provides a comprehensive mapping of radio frequency allocations in XML format, designed for use with Software Defined Radio (SDR) applications, frequency scanning software, and radio monitoring tools. Each frequency range is tagged with its primary use, operating mode, step size, and a color code for visual identification.

## File Format

The database uses an XML structure with `RangeEntry` elements, where each entry defines:

- **minFrequency/maxFrequency**: Frequency range in Hz
- **color**: ARGB hex color code for visual display (format: AARRGGBB)
- **mode**: Radio transmission mode (AM, FM, USB, LSB, CW, NFM, WFM, etc.)
- **step**: Recommended tuning step in Hz

### Example Entry

```xml
<RangeEntry minFrequency="3622500" maxFrequency="3622500" color="5000FFFF" mode="USB" step="10">
  Radiofax - JMH Tokyo (Weather)
</RangeEntry>
```

## Coverage

### Frequency Bands Included

- **HF (3-30 MHz)**: Amateur radio, shortwave broadcast, maritime communications, aviation
- **VHF (30-300 MHz)**: FM broadcast, TV, amateur radio, aviation navigation
- **UHF (300 MHz-3 GHz)**: TV broadcast, mobile communications, personal radio
- **Microwave (3-37 GHz)**: Satellite communications, mobile networks

### Special Features: Japanese Radiofax/WEFAX Frequencies

The database includes comprehensive coverage of radiofax (weather fax) and WEFAX stations operating in and around Japan:

#### JMH Tokyo (Japan Meteorological Agency)
Weather maps and forecasts from the Japan Meteorological Agency:
- 3622.5 kHz
- 7795 kHz  
- 13988.5 kHz

#### JFX Kagoshima (Fisheries)
Fishing industry weather and sea condition faxes:
- 4274 kHz
- 8658 kHz
- 13074 kHz

#### JJC Kyodo News
News agency radiofax service with navigational warnings:
- 4316 kHz
- 8467.5 kHz
- 12745.5 kHz
- **16971 kHz** (primary active frequency)
- 17069.6 kHz
- 22542 kHz

#### 9VF Singapore
Kyodo News repeater station:
- 16035 kHz
- 17430 kHz

#### Shared Fisheries Frequencies
Used by multiple Japanese fisheries stations (JFX/JFC/JFW):
- 6414.5 kHz
- 16907.5 kHz
- 22559.6 kHz

All radiofax entries are color-coded in **cyan** (5000FFFF) and use **USB mode** for reception.

## Service Categories

The database organizes frequencies into major service categories:

- **Amateur Radio**: Licensed ham radio bands (630m through 6m)
- **Broadcasting**: AM radio, FM radio, shortwave, TV
- **Maritime**: Ship stations, coastal telegraph, distress frequencies
- **Aviation**: Navigation aids, mobile communications
- **Radiofax/WEFAX**: Weather and news facsimile transmissions
- **Military/Government**: Navigation, time signals
- **Commercial**: Mobile networks, satellite communications

## Usage

### Compatible Software

This XML format is compatible with many SDR and scanning applications, including:

- SDR# (SDRSharp)
- HDSDR
- SDR-Console
- Unitrunker
- Various spectrum analyzer tools

### Importing

Most SDR applications support importing frequency databases in XML format. Check your software's documentation for the specific import procedure, typically found under:
- File → Import Frequency Database
- Settings → Frequency Manager → Import
- Tools → Band Plan → Load

### Customization

You can edit this file to:
- Add local repeaters or frequencies of interest
- Modify color schemes for your preference
- Adjust step sizes for your region
- Add notes or additional metadata

## Color Coding

Common color schemes used in this database:

- **Red (40FF0000)**: Amateur radio bands
- **Blue (505D88FF)**: Aviation services
- **Gray (55008080)**: Maritime/coastal services
- **Green (4000FF9A)**: FM broadcast
- **Cyan (5000FFFF)**: Radiofax/WEFAX stations
- **Yellow (50FFE55C)**: TV broadcast
- **Purple (44FF00FF)**: Time signals

## Transmission Modes

- **AM**: Amplitude Modulation (broadcast, aviation)
- **FM/WFM**: Frequency Modulation (broadcast, wide-band)
- **NFM**: Narrowband FM (communications)
- **USB/LSB**: Upper/Lower Sideband (HF communications)
- **CW**: Continuous Wave (Morse code)

## Regional Notes

This database reflects frequency allocations with particular focus on:
- Japan and Asia-Pacific region
- ITU Region 3 allocations
- International maritime and aviation bands

Some frequencies may vary by country or region. Always check local regulations before transmitting.

## Contributing

Contributions are welcome! If you notice:
- Outdated frequency allocations
- Missing services in your region
- Inactive radiofax stations
- New stations or services

Please submit updates with sources for verification.

## License

This frequency allocation database is provided for informational and educational purposes. Frequency allocations are based on ITU regulations and publicly available sources.

## Disclaimer

This database is for monitoring and receiving purposes only. Always comply with local regulations regarding radio transmission and reception. Some frequencies may require licenses to transmit or may be restricted for reception in certain jurisdictions.

## Resources

- [ITU Radio Regulations](https://www.itu.int/pub/R-REG-RR)
- [Japan Ministry of Internal Affairs and Communications](https://www.soumu.go.jp/english/)
- [Radiofax Schedules](http://www.hffax.de/)
- [Tokyo Volmet (Aviation Weather)](https://www.tokyo-ac.jp/)

---

**Last Updated**: February 2026
