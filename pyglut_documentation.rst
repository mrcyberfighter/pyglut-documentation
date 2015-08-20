
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
  
  Class for the color management:
  
  The color can be encoded either as unsigned bytes or as floats.
  
  To interact with :mod:`pyopengl` color functions.
  
  :argument ub_v: (unsigned bytes vector) [0-255]   rgb(a) color representing sequence.
  
  Initialize the :class:`Color` with an unsigned bytes rgb(a) sequence.
                
  :argument  f_v: (floats vector)         [0.0-1.0] rgb(a) color representing sequence.

  Initalize the :class:`Color` with an floats rgb(a) sequence.
                
  .. note:: The sequence must be in the order (Red, Green,Blue (,Alpha)).

  
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

  Vertices management datatype class.
  
  Holding the coordinate part x, y and z of an vertice.
  
  :argument x,y,z: Coordinate of the position from the vertice.
  
  The coordinate can be given as an sequence with the parameter:
  
  :argument vertexv: an sequence from the (x, y, z) values.
  
.. method:: Vertex.get_vertex()

  :return: The coordinate as an sequence (x, y, z).
  
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
  
  Return the length of the vector object.
  
  :return: The vector length.
  
.. method:: Vector.normalize()

  Normalize the current vector object and return the resulting unit vector.
  
  So as his length is equal to 1.0.
  
  :return: The unit vector, from length 1.0, from the vector object. 

.. method:: Vector.add_vector(vector)

  Add The Vector object to the given vector.
  
  :return: The direction vector from the vector object.
  
.. method:: Vector.sub_vector(vector)

  Substract the given vector from the current Vector object.
  
  :return: The direction vector (opposite direction) from the vector object.
  
.. method:: Vector.mult_vector(mult,vector=False)

  Multiply the vector object or the given vector with the given :data:`mult` argument what:
  
  Increment the vector length and if :data:`mult` is negativ flip the vector direction.
  
  :return: If the vector argument is given, multiply it per the argument :data:`mult`.
           
           If the vector argument is not given, multiply the current Vector object per the argument :data:`mult`.
           
.. method:: Vector.div_vector(div,vector=False)

  Divide the vector object or the given vector by the given :data:`div` argument what:
  
  Decrement the vector length and if :data:`div` is negativ flip the vector direction.
  
  :return: If the vector argument is given, divide it per the argument :data:`div`.
           
           If the vector argument is not given, divide the current Vector object per the argument :data:`div`.
           
.. method:: Vector.negation()

  Negate the current Vector object.
  
.. method:: Vector.add_vertex(vertex,vector=False)

  Add the given vertex with, if given, the vector argument, else the current Vector object and return the result as an Vertex object.
  
  :return: If the vector argument is given, add it to the argument :class:`vertex` and return the result as an :class:`Vertex` object. 
           
           If the vector argument is not given, add the current Vector object to the argument :class:`vertex` and return the result as an :class:`Vertex` object. 
 
.. method:: Vector.cross(vector1,vector2)

  Compute the cross product from 2 vectors and return the result as an Vector object.
  
  :return: The cross product from vector1 and vector2.
  
.. note:: Operations placeholders:

  The class :class:`Vector` implement 5 operations signs placeholder:
  
    * Vector \+ vector
    
    * Vector \- vector
    
    * Vector \* multiplier
    
    * Vector \\ divisor
    
    * -Vector (negation)
 
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
    
      * An localview position vertex, object from type :class:`Vertex`.
	  
	  which is the position from:
	  
	    + The camera.
	    
	    + The center from the 3D object.
	
	referenced as an attribute named: Localview.pos
	
      * 3 axes, objects from type :class:`Vector` Representing either:
	
	+ The camera orientation.
	
	+ The own axes from the 3D object.
	
	
.. method:: Localview.mult_matrix(matrix)

   Multiply the localview with an matrix, given as argument,
   
   which settings change the localview.
   
   :argument matrix: An object from type :class:`Matrix` to change the position and | or the axes orientation of the :class:`Localview`.
   
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

  Object from type :class:`Vector` representing the Y axe from the localview. 
  
.. attribute:: Localview.sight

  Object from type :class:`Vector` representing the Z axe from the localview. 
  
  
  
  