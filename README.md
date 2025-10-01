# Minimal_ADPL76030

## Overview

This repository contains a minimal KiCad design project for the Analog Devices ADPL76030, a synchronous 4-switch buck-boost DC/DC controller. The project includes schematic designs and PCB layout files for implementing this versatile power supply controller.

## Disclaimer

> [!NOTE]
> This project is provided "as is" and without any warranty, express or implied. For more details, please see the [LICENSE](LICENSE) file.

## About the ADPL76030

The ADPL76030 from Analog Devices is a high-efficiency synchronous 4-switch buck-boost DC-to-DC controller. It can regulate output voltage and current from an input voltage that can be above, below, or equal to the output voltage.

Key features include:

- **Wide Input Voltage Range:** 4V to 55V.
- **High Efficiency:** Up to 95% at 1.4 MHz.
- **Spread Spectrum Frequency Modulation:** For low EMI.
- **Fault Protection:** Includes various protection features.
- **Current Monitoring:** Provides current monitoring capabilities.
- **Package:** Available in a 28-lead LFCSP package.

## Project Structure

```
minimal_adpl76030/
├── minimal_adpl76030.kicad_pro       # Project configuration file
├── minimal_adpl76030.kicad_sch       # Main schematic file
├── minimal_adpl76030.kicad_pcb       # PCB layout file
├── fp-lib-table                    # Footprint library table
├── sym-lib-table                   # Symbol library table
├── docs/                           # Documentation files
│   ├── bom/                        # Bill of Materials
│   │   └── minimal_adpl76030_ibom.html # Interactive BOM file
│   ├── pictures/                   # Images and photos
│   │   ├── 1_minimal_adpl76030_side.png
│   │   ├── 2_minimal_adpl76030_top.png
│   │   ├── 3_minimal_adpl76030_bottom.png
│   │   ├── 4_minimal_adpl76030_left.png
│   │   └── 5_minimal_adpl76030_right.png
│   └── schematics/                 # Schematic PDF exports
│       └── minimal_adpl76030_schematics.pdf
└── KiCAD_Symbols_Generator/        # Submodule for symbol generation from CSV data
```

## Project Features

This design provides a minimal implementation of the ADPL76030 with:

- Proper power supply connections
- Buck-boost functionality
- Standard footprint for the 28-pin LFCSP package

## Getting Started

### Prerequisites

- [KiCad EDA](https://www.kicad.org/) version 9.0 or later installed on your system
- Git (for cloning the repository and submodule management)

### Opening the Project

1. **Clone the repository** (including submodules):
   ```bash
   git clone --recursive https://github.com/ionutms/Minimal_ADPL76030.git
   ```
   
   If you've already cloned the repository without submodules, initialize them with:
   ```bash
   git submodule init
   git submodule update
   ```

2. **Open the project in KiCad**:
   - Launch KiCad
   - Click "Open Existing Project"
   - Navigate to the cloned repository folder
   - Select the `minimal_adpl76030.kicad_pro` file

3. **Explore the design**:
   - Open the schematic editor to view the circuit design
   - Open the PCB editor to view the board layout
   - Review the symbol and footprint libraries used in the design

### Project Files

- **Main schematic**: `minimal_adpl76030.kicad_sch` - Contains the primary circuit design with the ADPL76030 and support components
- **PCB layout**: `minimal_adpl76030.kicad_pcb` - Physical board design file with proper component placement
- **Project configuration**: `minimal_adpl76030.kicad_pro` - KiCad project settings

## Dependencies

This project has the following dependencies:

### 1. KiCAD Symbols Generator

This repository uses [KiCAD_Symbols_Generator](https://github.com/ionutms/KiCAD_Symbols_Generator) as a submodule for custom symbol generation.

To initialize the submodule after cloning this repository:

```bash
git submodule update --init --recursive
```

### 2. 3D Models

This project requires the [3D_Models_Vault](https://github.com/ionutms/3D_Models_Vault) repository for 3D models.

#### Setup for KiCAD 9:

1. Clone the 3D models repository:
   ```bash
   git clone https://github.com/ionutms/3D_Models_Vault.git
   ```

2. In KiCAD 9, add an environment variable:
   - Variable name: `KICAD9_3D_MODELS_VAULT`
   - Variable value: Full path to where you cloned the 3D_Models_Vault repository

## Usage

After setting up the dependencies, open the project in KiCad 9 to access all features including the 3D models.

## Symbol Generator Submodule

This project includes the KiCAD_Symbols_Generator as a submodule, which provides tools for generating KiCad symbols from CSV data files. For more information on using this tool, see the [KiCAD_Symbols_Generator documentation](minimal_adpl76030/KiCAD_Symbols_Generator/README.md).

## Documentation

The `docs` folder contains:
- Schematic PDF exports
- Images and photos of the design

## Visuals

The following images showcase the PCB design from different perspectives:

![Top View](minimal_adpl76030/docs/pictures/2_minimal_adpl76030_top.png)
*Top View of the PCB*

![Side View](minimal_adpl76030/docs/pictures/1_minimal_adpl76030_side.png)
*Side View of the PCB*

![Bottom View](minimal_adpl76030/docs/pictures/3_minimal_adpl76030_bottom.png)
*Bottom View of the PCB*

![Left View](minimal_adpl76030/docs/pictures/4_minimal_adpl76030_left.png)
*Left View of the PCB*

![Right View](minimal_adpl76030/docs/pictures/5_minimal_adpl76030_right.png)
*Right View of the PCB*

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## References

- [ADPL76030 Datasheet](https://www.analog.com/media/en/technical-documentation/data-sheets/adpl76030.pdf)
- [KiCad EDA](https://www.kicad.org/)