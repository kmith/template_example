

================
Laplace Equation
================

This example solves the weak form of the standard Laplace equation,

|laplace_equation1|

using the Galerkin Finite Element method. |conductivity_tensor| and |phi| are the rank two conductivity tensor and a scalar field (e.g. temperature) respectively. A homogeneous and isotropic material with |equation1| (identity tensor) is considered in this example. As a result, |conductivity_tensor| in the above equation becomes redundant and the equation reduces to

|laplace_equation2|.

Only Dirichlet boundary conditions are prescribed.

.. |laplace_equation1| image:: ./docs/images/laplace_equation1.svg
   :align: middle

.. |conductivity_tensor| image:: ./docs/images/conductivity_tensor.svg 
   :align: middle

.. |phi| image:: ./docs/images/field_scalar.svg
   :align: middle
   
.. |equation1| image:: ./docs/images/equation1.svg
   :align: middle

.. |laplace_equation2| image:: ./docs/images/laplace_equation2.svg
   :align: middle
   
Building the example
====================

The fortran version of the example can be configured and built with CMake::

  mkdir examples
  cd examples
  git clone https://github.com/OpenCMISS-Examples/laplace_equation
  cd laplace_equation
  cmake -DOpenCMISSLibs_DIR=/path/to/opencmisslib/install
  make

Running the example
===================

Fortran version::

  cd src/fortran
  ./laplace_equation

Python version::

  PYTHONPATH="/path/to/opencmisslibs/install/.../.../Release/opencmiss.iron" python laplace_equation.py   
  
The results can be visualised by running `visualise.com <./src/fortran/visualise.com>`_ with the `Cmgui visualiser <http://physiomeproject.org/software/opencmiss/cmgui/download>`_.

The following figure shows the finite element mesh (computational domain) and solution (scalar field variable, |phi|).  
 
.. |figure1a| image:: ./docs/images/mesh.svg
   :align: middle
   :width: 300
   :scale: 100
   
.. |figure1b| image:: ./docs/images/field_solution.svg
   :align: middle  
   :width: 300
   :scale: 100
    
|figure1a|  |figure1b|  

Figure 1. (a) Finite element mesh (b) Solution
    
Prerequisites
=============

There are no additional input files required for this example as it is self-contained.

License
=======

License applicable to this example is described in `LICENSE <./LICENSE>`_.
