# PyLEMS 

###A [LEMS](http://neuroml.org/lems/)/[NeuroML2](http://neuroml.org/neuroml2.php) simulator written in Python


*Note: PyLEMS is currently in the process of major refactoring.*

## Installation
Check the code out of github.

    % git clone git@github.com:LEMS/pylems.git

This will create a directory named pylems. Add this directory to your PATH and PYTHONPATH variables.

## Usage
pylems [\<options\>] \<LEMS file\>

### Options
- -I/-include \<path\> - Adds a directory to the model file include search path
- -XI/-xsl-include \<path\> - Adds a directory to the XSL preprocessor include path

## Tasks
- Implement flattening
- Decouple events from runnables
- Perform dimension-checking on expressions.
- Simple LEMS API for creating, reading and writing LEMS model files (DONE)
- Implement LEMS API over lems.model.* (NeuroML API?)
  - Interface with libNeuroML and Pyramidal to export Neuron MOD files
  - Export C files (Interface? Steve Marsh’s project?)
- Assertions.
- XPath implementation.
- Implement Runnables from Component types instead of expanded typeless Components (Required for efficient C/C++ code generation, but conflicts with flattening)


## Examples

### *NeuroML* examples (from https://github.com/NeuroML/NeuroML2/tree/master/NeuroML2CoreTypes)

- Example 0 --  Working
- Example 1 --  Working with incorrect initialisation of m, h, n
- Example 2 --  Working
- Example 3 --  Working, but with startup issue as example 2
- Example 4 --  Not working
- Example 5 --  Not running (Need to be able to parse conditions in parameter for select expressions)
- Example 6 --  Working
- Example 7 --  Not running
- Example 8 --  Working, with stability problems.
- Example 9 --  Not working
- Example 10 -- Working, but with startup issue as example 2
- Example 11 -- Working
- Example 12 -- Not running
- Example 13 -- Not running
- Example 14 -- Not running
- Example 15 -- Not running
- Example 16 -- Not running
- Example 17 -- Not working
      
## LEMS elements that do not work
- XPath based parameters - DerivedParameter, PathParameter
- Assertions

## Travis integration

pylems is integrated with the the [Travis Continuous Integration service](http://travis-ci.org/).

[![Build Status](https://travis-ci.org/LEMS/pylems.png?branch=master)](https://travis-ci.org/LEMS/pylems)


