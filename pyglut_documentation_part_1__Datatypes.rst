
================
pyglut datatypes
================

:mod:`pyglut` -- python opengl utilities
========================================

.. module:: pyglut

:platform: `Linux, Windows`
  
:synopsis: `pyopengl programming helper classes and functions set.`

.. moduleauthor:: Eddie Brüggemann <mrcyberfighter@gmail.com>

----------------
pyglut datatypes   
----------------

++++++++++++++
Datatype Color
++++++++++++++

.. class:: Color(ub_v=False,f_v=False)
  
  Color management class implementing the <type 'Color'> datatype.
  
  The color can be encoded either as unsigned bytes or as floats.
  
  To interact with :mod:`pyopengl` color functions.
  
  :argument ub_v: (unsigned bytes vector) [0-255]   rgb(a) color representing sequence.
  
  Initialize the :obj:`Color` with an unsigned bytes rgb(a) sequence.
                
  :argument  f_v: (floats vector)         [0.0-1.0] rgb(a) color representing sequence.

  Initalize the :obj:`Color` with an floats rgb(a) sequence.
                
  .. note:: The sequence must be in the order (Red, Green, Blue (,Alpha)).

  
.. method:: Color.get_float_v()
    
    Color values getting method.
    
    If the color is encoded as unsigned bytes it will be *automaticly convert* in floats.
    
    :return: The color representation as an sequence of floats.
    
.. method:: Color.get_ubyte_v()
    
    Color values getting method.
    
    If the color is encoded as floats it will be *automaticly convert* in unsigned bytes.
    
    :return: The color representation as an sequence of unsigned byte.
    
.. method:: Color.set_in_float_values()
  
    Convert the color unsigned bytes encoded color in floats values.

.. method:: Color.set_in_float_values()
  
    Convert float encoded color in unsigned byte values.  

.. attribute:: Color.r

  Contains the *red* value.
  
.. attribute:: Color.g

  Contains the *green* value.
  
.. attribute:: Color.b

  Contains the *blue* value.
  
.. attribute:: Color.a

  Contains the *alpha* value. 
  
.. attribute:: Color.encoding

  Contains the current color *encoding*.
 
+++++++++++++++
Datatype Vertex
+++++++++++++++

.. class:: Vertex(x=False,y=False,z=False,vertexv=False)

  Vertices management class implementing the <type 'Vertex'> datatype.
  
  Holding the coordinate part x, y and z of an vertice.
  
  :argument x,y,z: Coordinate of the position from the vertice.
  
  The coordinate can be given as an sequence with the parameter:
  
  :argument vertexv: an sequence from the (x, y, z) values.
  
.. method:: Vertex.get_vertex()

  :return: The coordinate as an sequence (x, y, z).
  
.. attribute:: Vertex.wx

  The X coordinate part.
  
.. attribute:: Vertex.wy

  The Y coordinate part.
  
.. attribute:: Vertex.wz

  The Z coordinate part.  
  
+++++++++++++++
Datatype Vector
+++++++++++++++

.. class:: Vector(x=0,y=0,z=0)

  Vector management class implementing the <type 'Vector'> datatype.
  
.. method:: Vector.from_vertices(vertex1,vertex2)

  Initialize an vector from 2 vertices for representing an direction from an vertice to another.
  
  :parameter vertex1: Vector begin.
  
  :parameter vertex2: Vector End.
 
.. method:: Vector.get_magnitude()
  
  Return the length of the :obj:`Vector` object.
  
  :return: The vector length.
  
.. method:: Vector.normalize()

  Normalize the current :obj:`Vector` object and return the resulting unit :data:`vector`.
  
  So as his length is equal to 1.0.
  
  :return: The unit vector, from length 1.0, from the :obj:`Vector` object. 

.. method:: Vector.add_vector(vector)

  Add the given :data:`vector` to the current :obj:`Vector` object.
  
  :return: The direction :data:`vector` from the :obj:`Vector` object.
  
.. method:: Vector.sub_vector(vector)

  Substract the given vector from the current :obj:`Vector` object.
  
  :return: The direction :data:`vector` (opposite direction) from the :obj:`Vector` object.
  
.. method:: Vector.mult_vector(mult,vector=False)

  Multiply the :obj:`Vector` object or the given :data:`vector` with the given :data:`mult` argument what:
  
  Increment the :data:`vector` length and if :data:`mult` is negativ, flip the vector direction.
  
  :return: If the :data:`vector` argument is given, multiply it per the argument :data:`mult`.
           
           If the :data:`vector` argument is not given, multiply the current :obj:`Vector` object per the argument :data:`mult`.
           
.. method:: Vector.div_vector(div,vector=False)

  Divide the :obj:`Vector` object or the given :data:`vector` by the given :data:`div` argument what:
  
  Decrement the :data:`vector` length and if :data:`div` is negativ, flip the vector direction.
  
  :return: If the :data:`vector` argument is given, divide it per the argument :data:`div`.
           
           If the :data:`vector` argument is not given, divide the current Vector object per the argument :data:`div`.
           
.. method:: Vector.negation()

  Negate the current :obj:`Vector` object.
  
.. method:: Vector.add_vertex(vertex,vector=False)

  Add the given :data:`vertex` with, if given, the :data:`vector` argument, else the current :obj:`Vector` object and return the result as an :obj:`Vertex` object.
  
  :return: If the :data:`vector` argument is given, add it to the argument :obj:`vertex` and return the result as an :obj:`Vertex` object. 
           
           If the :data:`vector` argument is not given, add the current :obj:`Vector` object to the argument :data:`vertex` and return the result as an :obj:`Vertex` object. 
 
.. method:: Vector.cross(vector1,vector2)

  Compute the cross product from 2 vectors and return the result as an :obj:`Vector` object.
  
  :return: The cross product from vector1 and vector2.
  
.. note:: Operations placeholders:

  The class :obj:`Vector` implement 5 operations signs placeholder:
  
    * Vector \+ vector
    
    * Vector \- vector
    
    * Vector \* multiplier
    
    * Vector \\ divisor
    
    * -Vector (negation)
 
.. attribute:: Vector.x

  The X coordinate part.
  
.. attribute:: Vector.y

  The Y coordinate part.
  
.. attribute:: Vector.z

  The Z coordinate part.   
 
.. attribute:: Vector.length

  The vector length.
 
++++++++++++++++++
Datatype Localview
++++++++++++++++++

.. class:: Localview(x=0.0,y=0.0,z=0.0)

   Create an localview object with:
   
    * an position represented by an Vertex.
    
    * 3 free axes initialise as the X, Y, Z axes.
    
    :argument x,y,z: Coordinate of the position of the Localview.
   
    An localview is an object representing either an 
    
      * Camera view.
      
      * Local axes (X, Y, Z) of an 3D object.
    
    An locaview is made from:
    
      * An localview position vertex, object from type :obj:`Vertex`.
	  
	  which is the position from:
	  
	    + The camera.
	    
	    + The center from the 3D object.
	
	referenced as an attribute named: Localview.pos
	
      * 3 axes, objects from type :obj:`Vector` Representing either:
	
	+ The camera orientation.
	
	+ The own axes from the 3D object.
	
	
.. method:: Localview.mult_matrix(matrix)

   Multiply the localview with an matrix, given as argument,
   
   which settings change the localview.
   
   :argument matrix: An object from type :obj:`Matrix` to change the position and | or the axes orientation of the :obj:`Localview`.
   
.. method:: Localview.display(factor)

  Display the axes in their current orientation
  
  from the center to the greater values from the axes.
  
  At the current Localview position.

  :note: For debugging purpose.
  
.. attribute:: Localview.pos

  Object from type :obj:`Vertex` representing the current position from the localview.
  
.. attribute:: Localview.right

  Object from type :obj:`Vector` representing the X axe from the localview.
  
.. attribute:: Localview.up

  Object from type :obj:`Vector` representing the Y axe from the localview. 
  
.. attribute:: Localview.sight

  Object from type :obj:`Vector` representing the Z axe from the localview. 
  
+++++++++++++++
Datatype Matrix
+++++++++++++++

.. class:: Matrix(vertex=False)

  Create an matrix object to process move, scaling, matrix, vectors, localviews and vertex operations.
  
  The Matrix computing is the heart of the 3D programmation.
  
  You can configure the matrix to apply changing to your 3D object with the primary operations:
    
    * Scaling
    
    * Translating
    
    * Rotation around the X, Y, Z axes.
    
    and others for matrix, vectors, localviews and vertex operations.
    
    And finally for replacing or mutiply the OpenGL MODELVIEW matrix with the matrix containing the desire settings for views implementing per example.
    
  And many others usage...
    
  :argument vertexv: initialize the matrix with an sequence (x, y, z) **! not recommended**
  
.. method:: Matrix.translate(vector)

  Configure the matrix to perform an translation movement.
  
  :argument vector: An sequence (x, y, z) to apply the translation.
  
.. method:: Matrix.scale(factor)

  Configure the matrix to perform an scaling operation.
  
  :argument factor: Scaling factor.
  
.. method:: Matrix.rotate_x(degrees)

  Configure the matrix to perform an rotation around the X axe from the given angle in degrees.
  
  :argument degrees: Angle value for the rotation movement.
  
.. method:: Matrix.rotate_y(degrees)

  Configure the matrix to perform an rotation around the Y axe from the given angle in degrees.
  
  :argument degrees: Angle value for the rotation movement.
  
.. method:: Matrix.rotate_z(degrees)

  Configure the matrix to perform an rotation around the Z axe from the given angle in degrees.
  
  :argument degrees: Angle value for the rotation movement.
  
.. method:: Matrix.rows(vector_a,vector_b,vector_c) 

  Build an row matrix with the given vectors.
  
  :argument vector_a: :obj:`Vector` to set in the first row.
  
  :argument vector_b: :obj:`Vector` to set in the second row.
  
  :argument vector_c: :obj:`Vector` to set in the third row.
  
.. method:: Matrix.columns(vector_a,vector_b,vector_c) 

  Build an column matrix with the given vectors.
  
  :argument vector_a: :obj:`Vector` to set in the first column.
  
  :argument vector_b: :obj:`Vector` to set in the second column.
  
  :argument vector_c: :obj:`Vector` to set in the third column. 
  
.. method:: Matrix.load_hardware()

  Load the current matrix as the internal OpenGL MODELVIEW matrix.
  
  :note: All vertices will be multiply with the new matrix.
  
.. method:: Matrix.multiply_hardware()

  Multiply the current matrix with the internal OpenGL MODELVIEW matrix.
  
  :note: All vertices will be multiply with the resulting matrix.
  
.. method:: Matrix.get_hardware()

  Retrieve the OpenGL internal MODELVIEW matrix.
  
  :return: The current internal OpenGL MODELVIEW matrix.
  
.. method:: Matrix.mult_vertex(vertex)

  Multiply the current main matrix with the given vertex. 
        
  And return the result as an Vertex.
  
  :note: You have to multiply all the vertices from your 3D object with the matrix to apply the settings (movements) to your 3D object.
  
.. method:: Matrix.mult_vector(vector)

  Multiply the current main matrix with the given vector. 
  
  And return the result as an Vector.
  
.. method:: Matrix.rotate_vector(angle,vector)

  Rotate around the given vector (representing an axe) from the given angle.
  
.. method:: Matrix.mult_localview(localview)

  Multiply an given localview with the current main matrix.
  
  :return: The resulting :obj:`Localview`.
  
.. method:: Matrix.get_result()

  :return: An vertex issue from the main matrix multiplying.
  
.. note:: multiply sign placeholder

  The :obj:`Matrix` class implement an \* sign placeholder what permit to multiply the matrix with:
  
    * Matrix \* :obj:`Vertex`.
    
    * Matrix \* :obj:`Vector`.
    
    * Matrix \* :obj:`Localview`.
    
    
  
  
  
  
  
  
  
  
  