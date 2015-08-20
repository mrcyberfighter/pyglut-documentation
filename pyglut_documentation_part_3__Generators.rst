
=================
pyglut generators
=================

:mod:`pyglut` -- python opengl utilities
========================================

.. module:: pyglut

:platform: `Linux, Windows`
  
:synopsis: `pyopengl programming helper classes and functions set.`

.. moduleauthor:: Eddie Brüggemann <mrcyberfighter@gmail.com>

-----------------
pyglut generators
-----------------

+++++++++++++++++++
Polygons generators
+++++++++++++++++++

.. function:: generate_polygon_on_xy_radius(edges,radius,center,offset=0)

  Return an polygon on plan XY: 
  
    * From edges sides. 
    
    * From radius radius. 
    
    * With offset offset.

  :argument edges: The number of edges from the polygon to generate.
  
  :argument radius: The radius from the polygon to generate.
  
  :argument offset: The offset in degrees to orientate the polygon.
  
  Generate an polygon with the given edges number, radius with even an offset.
  
  In the plan XY. 
  
  :return: An list of objects from type :obj:`Vertex` composing the polygon.
  
.. function:: generate_polygon_on_xz_radius(edges,radius,center,offset=0)

  Return an polygon on plan XZ: 
  
    * From edges sides. 
    
    * From radius radius. 
    
    * With offset offset.

  :argument edges: The number of edges from the polygon to generate.
  
  :argument radius: The radius from the polygon to generate.
  
  :argument offset: The offset in degrees to orientate the polygon.
  
  Generate an polygon with the given edges number, radius with even an offset.
  
  In the plan XZ. 
  
  :return: An list of objects from type :obj:`Vertex` composing the polygon.  
  
.. function:: generate_polygon_on_yz_radius(edges,radius,center,offset=0)

  Return an polygon on plan YZ: 
  
    * From edges sides. 
    
    * From radius radius. 
    
    * With offset offset.

  :argument edges: The number of edges from the polygon to generate.
  
  :argument radius: The radius from the polygon to generate.
  
  :argument offset: The offset in degrees to orientate the polygon.
  
  Generate an polygon with the given edges number, radius with even an offset.
  
  In the plan YZ. 
  
  :return: An list of objects from type :obj:`Vertex` composing the polygon.
  
.. function:: generate_polygon_on_xy_side_length(edges,side_length,offset=0) 

  Return an polygon on plan XY: 
  
    * With edges edges.
    
    * From side length side_length.
    
    * With offset offset.
    
  :argument edges: The number of edges from the polygon to generate.
  
  :argument side_length: The side length from the polygon to generate.
  
  :argument offset: The offset in degrees to orientate the polygon.
  
  Generate an polygon with the given edges number, side length with even an offset.
  
  :return: An list of objects from type :obj:`Vertex` composing the polygon.  
  
.. function:: generate_polygon_on_xz_side_length(edges,side_length,offset=0) 

  Return an polygon on plan XZ: 
  
    * With edges edges.
    
    * From side length side_length.
    
    * With offset offset.
    
  :argument edges: The number of edges from the polygon to generate.
  
  :argument side_length: The side length from the polygon to generate.
  
  :argument offset: The offset in degrees to orientate the polygon.
  
  Generate an polygon with the given edges number, side length with even an offset.
  
  :return: An list of objects from type :obj:`Vertex` composing the polygon.
  
.. function:: generate_polygon_on_yz_side_length(edges,side_length,offset=0) 

  Return an polygon on plan YZ: 
  
    * With edges edges.
    
    * From side length side_length.
    
    * With offset offset.
    
  :argument edges: The number of edges from the polygon to generate.
  
  :argument side_length: The side length from the polygon to generate.
  
  :argument offset: The offset in degrees to orientate the polygon.
  
  Generate an polygon with the given edges number, side length with even an offset.
  
  :return: An list of objects from type :obj:`Vertex` composing the polygon.  
  
.. code-block:: text 

    The plans:

	|                      /               | /
	|                     /                |/ 
    ----+----            ----+----             +
	|                   /                 /|
	|    XY plan.      /      XZ plan.   / |   YZ plan. 
	
	
++++++++++++++++++++++
Polyhedrons generators
++++++++++++++++++++++

.. function:: generate_tetrahedron(side_length)

  Generate an tetrahedron in relationship to the given side length.
  
  And return an sequence from triangles composing the tetrahedron.
  
  :argument side_length: The side length of the tetrahedron's sides.
  
  This low-level function does not generate an tetrahedron object but return an sequence of 4 triangles composing the tetrahedron.
  
  :return: An list of triangles, within each triangles is an sequence of 3 objects from type :obj:`Vertex`.
  
.. function:: generate_cube(side_length)

  Generate an cube in relationship to the given side length. 
  
  And return an sequence from quads composing the cube.
  
  :argument side_length: The side length of the cube's sides.
  
  This low-level function does not generate an cube object but return an sequence of 6 quads composing the cube.
  
  :return: An list of quads, within each quad is an sequence of 4 objects from type :obj:`Vertex`.
  
.. function:: generate_octahedron(side_length)

  Generate an octahedron from the given side length. 
  
  And return an sequence from triangles composing the octahedron.
  
  :argument side_length: The side length of the octahedron's sides.
  
  This low-level function does not generate an octahedron object but return an sequence of 8 triangles composing the octahedron.
  
  :return: An list of triangles, within each triangles is an sequence of 3 objects from type :obj:`Vertex`.
  
.. function:: generate_dodecahedron(side_length)

  Generate an dodecahedron in relationship to the argument side_length taken as basis for the dodecahedron generation. 
  
  And return an sequence of pentagons composing the dodecahedron.
  
  :argument side_length: The side length of the icosahedron's sides using for generate the dodecahedron.
  
  This low-level function does not generate an dodecahedron object but return an sequence of 12 pentagons composing the dodecahedron.
  
  :return: An list of pentagons, within each pentagons is an sequence of 5 objects from type :obj:`Vertex`.
  
  .. note:: BUGFIX
  
    This function does not return an exact dodecahedron.
    
    It is based on an icosahedron construction but all issues pentagons have one side which is not equal to the others from the same pentagon.
    
    But the illusion of an dodecahedron is maintain.
    
    If you have an solution thank's to inform me about at: <mrcyberfighter@gmail.com>.
    
.. function:: generate_icosahedron(side_length)

  Generate an icosahedron from the given side length. 
  
  And return an array of 20 triangles component from the icosahedron and 
  
  his construction base quad set.
  
  :argument side_length: The side length of the icosahedron's sides.

  This low-level function does not generate an icosahedron object but return an sequence of 20 triangles composing the icosahedron and an array of the 3 base quads (build with the golden number).
    
  :return: An list of the 3 basis quads and An list of triangles, within each triangle is an sequence of 3 objects from type :obj:`Vertex`.
    
.. function:: generate_fulleren(side_length)

  Generate an fulleren from the given side length and return 2 arrays:
  
    * an sequence containing hexagons,
    
    * an sequence containing pentagons,
    
    composing the fulleren.
    
  an fulleren is an 3D polyhedron likewise an soccer ball.
  
  :argument side_length: The side length of the fulleren's sides.
  
  This low-level function does not generate an fulleren object but return an 2-items array (hexagons,pentagons) composing the fulleren.
  
  :return: An list of hexagons and an list of pentagons within each is composed of objects from type :obj:`Vertex`.
  
.. function:: generate_toros(base,base_radius,toros_radius)

  Generate an toros in relationship to the given settings:
  
    * base:        the toros basis polygon.
    
    * base_radius: the toros basis polygon radius.
    
    * toros_radius: the torod radius (without the base polygon radius.).
    
    and return an sequence of polygons base from the toros.
    
  :argument base: The base polygon edges number, for the toros.
  
  :argument base_radius: The base polygon radius, for the toros.
  
  :argument toros_radius: The toros radius.
  
  This low-level function does not generate an toros object but return the polygons to assembly the toros.
  
  :return: An list of polygons within each is composed of objects from type :obj:`Vertex` composing the toros.
  
.. function:: generate_polyhedron_26_faces(side_length)

  Generate an 26 faces polyhedron from the given side length and return: 
  
    * An sequence of 8 triangles 
    
    * An sequence of 18 quads
    
    composing the 26 faces of the polyhedron.
    
  :argument side_length: The side length of the 26 faces polyhedron.
  
  This low-level function does not generate an 26-faces-polyhedron object but return an 2-item array (triangles,quads) composing the 26 faces polyhedron.
  
  :return: An list of triangles and an list of quads within each is composed of objects from type :obj:`Vertex`.
  
.. function:: generate_polyhedron_32_faces(side_length)

  Generate an 32 faces polyhedron from the given side length and return:
  
    * an sequence of the triangles.
    
    * an sequence of the pentagons.
    
  :argument side_length: The side length of the 32 faces polyhedron.
  
  This low-level function does not generate an 32-faces-polyhedron object but return an 2-item array (triangles,pentagons) composing the 32 faces polyhedron.
  
  :return: An list of triangles and an list of pentagons within each is composed of objects from type :obj:`Vertex`.  
  
++++++++++++++++++
Spheres generators
++++++++++++++++++

.. function:: generate_quad_sphere(basis,radius)

  Generate an quads sphere and return an tuple from 2 arrays: 
 
  (base polygons, quads).
 
  In relationship with the base for the sphere generating:  faces count = basis * basis
 
  and the given sphere radius.
    
  :argument basis: The polygon to take as basis for the quad sphere generation.
                   
                   Must be % 2 == 0.  
  
  :argument radius: The quad sphere radius.
  
  This low-level function does not generate an quad sphere object but return an 2-item array (base polygons, quads) each can be using to display the quad sphere.
  
  :return: An list of polygons and an list of quads within each is composed of objects from type :obj:`Vertex`.
  

.. function:: generate_trigon_sphere(basis,radius)

  Generate an trigon sphere and return an tuple from 2 arrays: 
 
  (base polygons, trigons).
 
  In relationship with the base for the sphere generating:  faces count = basis * basis
 
  and the given sphere radius.
    
  :argument basis: The polygon to take as basis for the trigon sphere generation.
  
		   Must be % 4 == 0.   
  
  :argument radius: The trigon sphere radius.
  
  This low-level function does not generate an trigon sphere object but return an 2-item array (base polygons, trigons) each can be using to display the trigon sphere.
  
  :return: An list of polygons and an list of trigons within each is composed of objects from type :obj:`Vertex`.
  
  