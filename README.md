## About

This script allows designing a cantilever geometry ready to be 3d printed over tensors using as an input a network of tensors and getting as an output the g-code. 


![alt_text](https://github.com/fmruy/3dpa_research/blob/main/images/image1.png "image_tooltip")


This research is developed in the Postgraduate in 3D Printing Architecture - 2022-2023. More information about the design process can be found at [blog.iaac.net](https://blog.iaac.net/) or in the Credits section.

![alt_text](https://github.com/fmruy/3dpa_research/blob/main/images/image6.jpg "image_tooltip")
![alt_text](https://github.com/fmruy/3dpa_research/blob/main/images/image7.jpg "image_tooltip")


## Prerequisites & Requirements



* Rhinoceros 3D version 7 (Win only). 
* Grasshopper plugins: 
    * Kangaroo Physics
    * Parakeet (Network Regions)
    * Anemone (Loop start and Loop end)
    * Lunch Box (Reverse Surface Direct, Sort Duplicated Curves)
    * Heteroptera

_Not working on Mac due to several plugins needed._


## Installation and Source Files


* Open .gh file
    * EXP_21_01_3dPrinter.gh
    * EXP_22_01_Kuka.gh


## Units

The system works in millimeters. It can be used in generic units.


## Workflow

The basic Grasshopper workflow could be divided into the following basic steps:

1. Import network of tensors as curves (or generate them parametrically)
2. Wall design
    1. Design wall 
    2. Generate wall grid subdivision
3. Vaults design
    1. Design vaults
    2. Generate vault grid subdivision based on wall subdivision
4. Redesign wall to improve vault support (optional)
    1. Adapt wall top period based on vaults
5. Get sliced printing path for walls and vaults
6. Save G-Code

In order to get the sliced printing path for vaults you will need to activate GH “data dam” and “buttons” under Kangaroo, Catenary Calculator, and following Data Dam.

![alt_text](https://github.com/fmruy/3dpa_research/blob/main/images/image2.png "image_tooltip")

Some guides are included in the script to easily move between workflow steps.

![alt_text](https://github.com/fmruy/3dpa_research/blob/main/images/workflow-example.gif "image_tooltip")


## Printers and Robots

The final set of contoured curves can be used on the different printers of robots. For the purpose of this research, a table 3D Printer and a Kuka robot were used.


### 3D Printer


![alt_text](https://github.com/fmruy/3dpa_research/blob/main/images/image3.png "image_tooltip")




* 3D printer
* Cartridge, clay holder, and nozzle
* Air pressure pump
* Max size: 220 x 220 x 180 mm
* Scales: 1.10 to 1.5


### ABB or KUKA robots

![alt_text](https://github.com/fmruy/3dpa_research/blob/main/images/image4.png "image_tooltip")




* Robot
* Cartridge, clay holder, and nozzle
* Air pressure pump or manual pump
* Max size: variable
* Scales: 1.1 to 1.5


### Wasp crane


![alt_text](https://github.com/fmruy/3dpa_research/blob/main/images/image5.png "image_tooltip")


_Image credit: WASP_



* Crane 
* Clay holder and nozzle
* Air pressure pump or manual pump
* Max size: Cylinder 3800 x 2000 mm
* Scales: 1.1 to 1.5


---


## Credits

2022 3DPA / [iaac](https://github.com/IaaC)

This research is a project of IAAC, Institute for Advanced Architecture of Catalonia developed in the Postgraduate in 3D Printing Architecture - 2022-2023 by the student(s) Nestor Beguin, Paco Pioline, and Francisco Magnone Rienzi during the course 3DPA 22/23: Research with Oriol Carrasco and Ashkan Foroughi.


### Research Team

Nestor Beguin, Paco Pioline, [Francisco Magnone Rienzi](https://github.com/fmruy)


### Source Plugins

This project contains plugins and codes based on free open-source and proprietary projects:



* [Kangaroo Physics](https://www.food4rhino.com/en/app/kangaroo-physics) by Daniel Piker - License Type: Proprietary
* [Parakeet](https://www.food4rhino.com/en/app/parakeet) by Parakeet3d - License Type: Proprietary
* [Anemone](https://www.food4rhino.com/en/app/anemone) by Mateusz Zwierzycki - License Type: Other
* [Lunch Box](https://www.food4rhino.com/en/app/lunchbox) by Nathan Miller - License Type: Other
* [Heteroptera](https://www.food4rhino.com/en/app/heteroptera) by Amin Bahrami - License Type: Other


## License

[MIT License](https://opensource.org/licenses/MIT)
