# magnet_design
Design instructions for the ORI Magnet Lidar Mapping device

Magnet is a compact, rugged LiDAR mapping unit developed at the Oxford Robotics Institute (ORI) for research into 3D mapping and mobile robot autonomy. It integrates a Hesai QT64 LiDAR, a Microstrain GX5-15 IMU, and an Intel NUC computer, all housed within a modular enclosure. The device is capable of running real-time 3D mapping algorithms and can be mounted on a robot or used as a handheld device.

This repository provides the 3D CAD files and basic manufacturing guidance required to reproduce the hardware. Note that Magnet requires additional software to perform 3D mapping or enable autonomy in robotic applications.

## Core Components

| Component         | Model                                      |
|------------------|--------------------------------------------|
| Onboard Computer | [Intel NUC Topaz 3 i7](https://simplynuc.co.uk/product/nuc13tzi7/) |
| IMU              | [Microstrain 3DM-GX5-AR](https://www.hbkworld.com/en/products/transducers/inertial-sensors/vertical-reference-units--vru-/3dm-gx5-ar#!ref_microstrain.com)|
| LiDAR            | [HESAI QT64](https://www.datrontechnology.co.uk/qt64/)|

## Mechanical Design & CAD
This repository contains the STEP files for the CAD models and the corresponding STL files for 3D printing.

- **Overall size and weight:** `110 × 110 × 148 mm` (including QT64), `1106 g`
- **Design files directory:** [`CAD`](./CAD/STEP) and [`CAD/STL`](./CAD/STL)
- **URDF link:** [`magnet_description`](https://github.com/ori-drs/magnet_description)

## Assembly Notes
- **Case:** 3D printed in PLA using a Bambu Lab printer.  
- **Heatsink:** Cut from a 3 mm aluminium sheet.  
  *Note: A metal sheet is highly recommended to ensure effective heat dissipation during prolonged LiDAR operation*

- **Tappex inserts (for 3D printed parts):**
  - **Top case:** 16 × M3 × 5.2 mm (unflanged)
  - **Bottom case:** 8 × M4 × 3.0 × 7.9 mm (flanged)  
    *These inserts are used to mount Magnet onto robots or rigs.*
  - **IMU mount:** 2 × M3 × 5.2 mm (unflanged)
- **Power inlet:** 2.5mm DC Socket (e.g. L712AS)
- **Wiring logic:**  
  *(Insert figure here)*  
  *Note: This is not a schematic diagram. For detailed electronic connections, please refer to the datasheets of the respective components.*

## Power supply
- **Input voltage:** 12–19 V  
- **Maximum power:** 90 W    
  *Note: These values are specific to our physical prototype and may vary depending on the components used in your build.*