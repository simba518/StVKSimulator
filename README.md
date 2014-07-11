StVKSimulator
=============

A simple simulation framework with UI and only supports full svtk elastic model. Only depends on Boost and Eigen3.

INTRODUCE----------------------------------------------------------------------------

The codes for this project is extracted from the Utility and SolidSimulator Project. It is designed more simple and with much fewer dependency, and much easy to be compiled on different systems.

FOLDS-------------------------------------------------------------------------------

1. Data: 
   + *.ini: init file, see TestCase/HelloDino/main.cpp
   + model/con_nodes.bou: constraint nodes with format of: number_of_constrained_nodes, the index of the constrained nodes.
   + mesh.abq: volumetric mesh, generated using netgen. see http://sourceforge.net/projects/netgen-mesher/
   + mesh.elastic: define the elastic material for the volumetric model.

2. Lib: 
   + Common: a set of auxiliary tools, such as the definition of the tetrahedron mesh, vtk writer, extention of assert definiation and so on.
   + ElasticModel: define the elastic model (StVK materail here) and a set of simulators based on implicit integration.
   + Math: extend the eigen library.

3. TestCase/HelloDino: A demo show the ussage of this library: load data and initilize the simulator, i.e set constrained nodes, external forces, then simulate, and finally write the results to a set of vtk in ./tempt/hello_dion*.vtk.

DEPENDENCY--------------------------------------------------------------------------

it denpends on two libraries:

1. eigen3: http://eigen.tuxfamily.org/index.php?title=Main_Page

2. boost: http://www.boost.org/

See ./CMakeLists.txt and TestCase/HelloDino/CMakeLists.txt.


CONTACT INFO--------------------------------------------------------------------------------

Author: Siwang Li @ ZJU

Email:  lisiwangcg@gmail.com