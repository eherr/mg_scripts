# Morphablegraphs Scripts

Scripts to create statistical motion models and run motion synthesis based on the [morphablegraphs](https://github.com/eherr/morphablegraphs) library.   
Note, the [mg_server](https://github.com/eherr/mg_server) repository provides a stateful  motion synthesis server for integration with a game engine. The motion modelling and the motion synthesis can also be run inside the [motion_preprocessing_tool](https://github.com/eherr/motion_preprocessing_tool).

## Usage

### Motion Primitive Construction
Set the path to data folder for modelling in config\service.config, "data_folder"
Call the motion primitive modelling pipeline mg_construction_pipeline.py from command line with parameters elementary_action motion_primitive
E.g.: python mg_construction_pipeline walk rightStance


### Motion Synthesis

There are two interfaces to run the algorithm:
mg_command_line_interface.py - A simple command line interface without arguments.
It automatically loads the latest input file in the input directory specified in config\service.config.

mg_rest_interface.py - Starts a web server that provides the REST interface localhost:port/run_morphablegraphs.
It can be called using a HTTP POST message with a string containing the input file as message body.

An example input file is provided in example_input.json.


## Developers

Han Du<sup>1</sup>, Erik Herrmann<sup>1</sup>, Markus Mauer<sup>2</sup>, Martin Manns<sup>2</sup>, Fabian Rupp<sup>2</sup>  <br/>
<sup>1</sup>DFKI GmbH  
<sup>2</sup>Daimler AG  


## License
Copyright (c) 2019 DFKI GmbH.  
MIT License, see the LICENSE file.
