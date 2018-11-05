<link rel="icon" href="img/anglerlogos/rainbow.png" type="image/x-icon" />
<img src="img/anglerlogos/rainbow.png" title="Angler" alt="Angler">

# angler

`angler` (named for '**a**djoint **n**onlinear **g**radients') is a package for simulating and optimizing optical structures.

It provides a finite-difference frequency-domain (FDFD) solver for simulating for linear and nonlinear devices in the frequency domain.

It also provides an easy to use package for adjoint-based inverse design and optimization of linear and nonlinear devices.

`angler` is released as part of a paper `Adjoint method and inverse design for nonlinear optical devices`, which can be viewed [here](broken_link).

If you use `angler`, please cite us.

## Prerequisites

For angler to work, you must have MKL installed on your device.

The best way to do this is through conda

	conda install MKL
	
The python wrapper for MKL that we are using does not work well when MKL is pip installed.

## Installation

	git clone https://github.com/fancompute/angler.git
	cd angler
	python setup.py install
	
For angler to work, you must have MKL installed on your device.  The best way to do this is through conda as pip installing MKL will not work with the python wrapper we are using.

	conda install MKL	
	
## Examples / Quickstart

There are several jupyter notebook examples in the `Notebooks/` directory.

For a good introduction, try:

	Notebooks/Splitter.ipynb

For more specific applications:

#### Electromagnetic simulations

For modeling linear devices with our FDFD solver (no optimization), see

	Notebooks/Linear_system.ipynb

For modeling nonlinear devices wuth FDFD (no optimization), see 

	Notebooks/Nonlinear_system.ipynb

#### Inverse design & optimization

For examples optimizing a linear device, see 

	Notebooks/Splitter.ipynb
	Notebooks/Accelerator.ipynb

For examples of optimizing nonlinear devices, see

	Notebooks/2_port.ipynb
	Notebooks/3_port.ipynb
	Notebooks/T_port.ipynb

## Package Structure

`angler` provides two main classes, `Simulation` and `Optimization`, which perform most of the functionality.

Generally, `Simulation` objects are used to perform FDFD simulations, and `Optimization` classes run inverse design and optimization algorithms over `Simulation`s.  To learn more about how `angler` works and how to use it, please take a look at [angler/README.md](angler/README.md) for a more detailed explanation.

## Tests

To run all tests:

	python -m unittest discover tests

Or to run individually:
	
	python tests/individual_test.py

## Contributing

`angler` is under development and we welcome suggestions, pull-requests, feature-requests, etc.

If you contribute a new feature, please also write a few tests and document your changes in [angler/README.md](angler/README.md) or the wiki.

## Authors

`angler` was written by Tyler Hughes, Momchil Minkov, and Ian Williamson.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details. Copyright 2018 Tyler Hughes.

## Acknowledgments

* our logo was made by [Nadine Gilmer](http://nadinegilmer.com/)
* RIP Ian's contributions before the code merge
