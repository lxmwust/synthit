synthit
=======

[![Build Status](https://travis-ci.org/jcreinhold/synthit.svg?branch=master)](https://travis-ci.org/jcreinhold/synthit)
[![Coverage Status](https://coveralls.io/repos/github/jcreinhold/synthit/badge.svg?branch=master)](https://coveralls.io/github/jcreinhold/synthit?branch=master)
[![Documentation Status](https://readthedocs.org/projects/synthit/badge/?version=latest)](http://synthit.readthedocs.io/en/latest/?badge=latest)
[![Python 3.6](https://img.shields.io/badge/python-3.6-blue.svg)](https://www.python.org/downloads/release/python-360/)

This package contains code to *synthesize* magnetic resonance (MR) and computed tomography (CT) brain images. Synthesis is the procedure 
of learning the transformation that takes a specific contrast image to another estimate contrast.

For example, given a set of T1-weighted (T1-w) and T2-weighted (T2-w) images, we can learn the function that maps the intensities of the
T1-w image to match that of the T2-w image via a random forest regressor or deep neural network. In this package, we supply 
the framework and some basic algorithms for this type of synthesis. See the `Relevant Papers` section (at the bottom of 
the README) for a *very* non-exhaustive list of some papers relevant to the work in this package.

** Note that this is an **alpha** release. If you have feedback or problems, please submit an issue (it is very appreciated) **

This package was developed by [Jacob Reinhold](https:jcreinhold.github.io) and the other students and researchers of the 
[Image Analysis and Communication Lab (IACL)](http://iacl.ece.jhu.edu/index.php/Main_Page).

[Link to main Gitlab Repository](https://gitlab.com/jcreinhold/synthit)

Requirements
------------

- antspy
- matplotlib
- numpy
- pyro
- scikit-learn
- scikit-image
- pytorch
- xgboost

Basic Usage
-----------

Install from the source directory

    python setup.py install
    
or (if you actively want to make changes to the package)

    python setup.py develop

Test Package
------------

Unit tests can be run from the main directory as follows:

    nosetests -v --with-coverage --cover-tests --cover-package=synthit tests
    
Relevant Papers
---------------

[1] A. Jog, A. Carass, S. Roy, D. L. Pham, and J. L. Prince, “Random forest regression for magnetic resonance image synthesis,” Med. Image Anal., vol. 35, pp. 475–488, 2017.

[2] C. Zhao, A. Carass, J. Lee, Y. He, and J. L. Prince, “Whole Brain Segmentation and Labeling from CT Using Synthetic MR Images,” in MICCAI MLMI, vol. 10541, pp. 291–298, 2017.

[3] S. Roy, A. Carass, and J. L. Prince, “Magnetic resonance image example-based contrast synthesis,” IEEE Trans. Med. Imaging, vol. 32, no. 12, pp. 2348–2363, 2013.

[4] J. M. Wolterink, A. M. Dinkla, M. H. F. Savenije, P. R. Seevinck, C. A. T. van den Berg, and I. Išgum, “Deep MR to CT synthesis using unpaired data,” in MICCAI, 2017, vol. 10557 LNCS, pp. 14–23.
