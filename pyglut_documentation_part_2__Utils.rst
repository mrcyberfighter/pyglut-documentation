
============
pyglut utils
============

:mod:`pyglut` -- python opengl utilities
========================================

.. module:: pyglut

:platform: `Linux, Windows`
  
:synopsis: `pyopengl programming helper classes and functions set.`

.. moduleauthor:: Eddie Brüggemann <mrcyberfighter@gmail.com>

------------
pyglut utils   
------------

++++++++++++++++++
Primary Operations
++++++++++++++++++

.. function:: translate(vertex,value_x,value_y,value_z)

  Translate an vertice from the given offset in every axes directions.

  :argument vertex: an object from type :obj:`Vertex` to translate.
  
  This will be the vertice to translate from his current position (value from X, Y and Z).

  :argument value_x: The translation value on the X axe.
  :argument value_y: The translation value on the Y axe.
  :argument value_z: The translation value on the Z axe.

  The values from this 3 arguments will be added to the current position from the vertice *vertex* given as argument.

  :return: An object from type :obj:`Vertex` within the new position of the vertice.


.. function:: scale(vertex,factor)
  
  Scaling function.

  For scaling an 3D object you must give all his vertices to this function.

  And the center of the 3D object to scale must be linked to the origin.

  So translate all vertices from your 3D object from the values between his center and the origin. You can retranslate it back after.

  :argument vertex: An object from type :obj:`Vertex` to scale.

  :argument factor: The scaling factor.
  
  If the scaling factor is littler than 1.0 the 3D object will be littler than the original, else greater.
  
  :return: An object from type :obj:`Vertex` within the new position of the vertice.

.. function:: rotate_x(vertex,angle)

  Rotate an vertice around the X axe and return the result position vertice.

  :argument vertex: An object from type :obj:`Vertex` to rotate.

  :argument  angle: The rotation angle in degress.

  For rotate an 3D object around his own X axe you must give all his vertices to this function.

  And the center of the 3D object to rotate must correspond to the origin.

  So translate all vertices from your 3D object from the values between his center and the origin. You can retranslate it back after.

  :return: An object from type :obj:`Vertex` within the new position of the vertice.

.. function:: rotate_y(vertex,angle)

  Rotate an vertice around the Y axe and return the result position vertice.

  :argument vertex: An object from type :obj:`Vertex` to rotate.

  :argument  angle: The rotation angle in degress.

  For rotate an 3D object around his own Y axe you must give all his vertices to this function.

  And the center of the 3D object to rotate must correspond to the origin.

  So translate all vertices from your 3D object from the values between his center and the origin. You can retranslate it back after.

  :return: An object from type :obj:`Vertex` within the new position of the vertice.

.. function:: rotate_z(vertex,angle)

  Rotate an vertice around the Z axe and return the result position vertice.

  :argument vertex: An object from type :obj:`Vertex` to rotate.

  :argument  angle: The rotation angle in degress.

  For rotate an 3D object around his own Z axe you must give all his vertices to this function.

  And the center of the 3D object to rotate must correspond to the origin.

  So translate all vertices from your 3D object from the values between his center and the origin. You can retranslate it back after.

  :return: An object from type :obj:`Vertex` within the new position of the vertice.

++++++++++++
Center utils
++++++++++++

.. function:: get_middle_from_segment(vertex1,vertex2)

  Return the middle point of an segment as an object from type :obj:`Vertex`.
  
  :argument vertex1: An object from type :obj:`Vertex`.
  :argument vertex2: An object from type :obj:`Vertex`.
  
  Compute the middle point between vertex1 and vertex2.
  
  :return: The middle from vertex1 and vertex2 as an object from type :obj:`Vertex`.
  
.. function:: get_center_from_polygon(points)

  Return the center of an polygon as an object from type :obj:`Vertex`.
  
  :argument points: Must be a list or a tuple of objects from type :obj:`Vertex` composing the polygon.
  
  Compute the center from the polygon which vertices sequence is given as argument.
  
  :return: The center from the polygon as an object from type :obj:`Vertex`.
  
.. function:: get_center_from_polyhedron(points)

  Return the center of an polyhedron as an object from type :obj:`Vertex`.
  
  :argument points: Must be a list or a tuple of objects from type :obj:`Vertex` composing the polyhedron.
  
  Compute the center from the polyhedron which vertices sequence is given as argument.
  
  :return: The center from the polyhedron as an object from type :obj:`Vertex`.
  
++++++++++++
Length utils
++++++++++++ 

.. function:: get_distance_vertices(vertex1,vertex2)

  Return the distance between 2 vertices vertex1 and vertex2.
  
  :argument vertex1: An object from type :obj:`Vertex`.
  :argument vertex2: An object from type :obj:`Vertex`.
  
  Compute the distance between the vertices vertex1 and vertex2.
  
  :return: The distance between vertex1 and vertex2 as an float.
  
.. function:: get_perimeter_from_polygon(points)

  Return the length of the perimeter of the polygon which vertex sequence is given as argument.
  
  :argument points: Must be a list or a tuple of objects from type :obj:`Vertex` composing the polygon.
  
  Compute the perimeter from the polygon which vertices are given as argument.
  
  :return: The perimeter of the polygon as an float.
  
.. function:: get_perimeter_from_polyhedron(points)

  Return the length of the perimeter from the polyhedron which polygon sequence is given as argument.
  
  :argument points: An list containing lists or tuples representing every polygon from the polyhedron, which contains objects from type :obj:`Vertex`.
  
  Compute the polyhedron perimeter without take into account superimpose segments.
  
  :return: The perimeter of the polyhedron as an float.
  
++++++++++++++  
Rotation utils
++++++++++++++

.. function:: rotate_on_xy(center,angle,vertex)

  Function to rotate the argument :data:`vertex` around a center :data:`vertex` in the XY plan from the value angle in clock sens.
      
  Return the rotated :data:`vertex` as an object from type :obj:`Vertex`.
  
  :argument center: An object from type :obj:`Vertex` representing the rotation center.
  :argument  angle: The rotation angle in degrees.
  :argument vertex: An object from type :obj:`Vertex` to rotate in the XY plan.
  
  The rotation taking place in the XY plan, so that the Z coordinate component des not change.
  
  :return: An object from type :obj:`Vertex` rotated around center from angles degrees.
  
.. function:: rotate_on_xz(center,angle,vertex)

  Function to rotate the argument :data:`vertex` around a center :data:`vertex` in the XZ plan from the value angle in clock sens.
      
  Return the rotated :data:`vertex` as an object from :obj:`'Vertex`.
  
  :argument center: An object from type :obj:`Vertex` representing the rotation center.
  :argument  angle: The rotation angle in degrees.
  :argument vertex: An object from type :obj:`Vertex` to rotate in the XZ plan.
  
  The rotation taking place in the XZ plan, so that the Y coordinate component des not change.
  
  :return: An object from type :obj:`Vertex` rotated around center from angles degrees.  
  
.. function:: rotate_on_yz(center,angle,vertex)

  Function to rotate the argument :data:`vertex` around a center :data:`vertex` in the YZ plan from the value angle in clock sens.
      
  Return the rotated :data:`vertex` as an object from :obj:`'Vertex`.
  
  :argument center: An object from type :obj:`Vertex` representing the rotation center.
  :argument  angle: The rotation angle in degrees.
  :argument vertex: An object from type :obj:`Vertex` to rotate in the YZ plan.
  
  The rotation taking place in the YZ plan, so that the X coordinate component des not change.
  
  :return: An object from type :obj:`Vertex` rotated around center from angles degrees.    
  
  
.. code-block:: text 

    The plans:

	|                      /               | /
	|                     /                |/ 
    ----+----            ----+----             +
	|                   /                 /|
	|    XY plan.      /      XZ plan.   / |   YZ plan.
      
      
+++++++++++++++++++
Miscellaneous utils
+++++++++++++++++++

.. function:: div_segment_into_vertices(vertex1,vertex2,divider)

  Return an sequence from vertices between vertex1 and vertex2. 
  
  Which divide the segment (vertex1,vertex2) in the given number of vertices.
  
  :argument vertex1: An object from type :obj:`Vertex` representing the segment start point.
  :argument vertex2: An object from type :obj:`Vertex` representing the segment end point.
  :argument divider: The number of vertices between vertex1 and vertex2 (excluded).
  
  The function divide the segment (vertex1,vertex2) into divider vertices.
  
  :return: An sequence of divider + 2 vertices objects from type :obj:`Vertex` dividing the segment (vertex1,vertex2).