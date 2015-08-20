
==================
pyglut polyhedrons
==================

:mod:`pyglut` -- python opengl utilities
========================================

.. module:: pyglut

:platform: `Linux, Windows`
  
:synopsis: `pyopengl programming helper classes and functions set.`

.. moduleauthor:: Eddie Brüggemann <mrcyberfighter@gmail.com>

-----------------
Plato polyhedrons
-----------------

+++++++++++
Tetrahedron
+++++++++++

.. class:: Tetrahedron(side_length,display_mode="lined",lines_color=False,faces_color=False,lines_width=1,display_ls=False)

  Generate an tetrahedron object with the given side length settings.
  
  :argument side_length: The side length of the tetrahedron sides.
  
  :argument display_mode: How to display the tetrahedron.
			    
			    * "lined" -> Only the lines will be displayed.
			    
			    * "faced" -> Only the faces will be displayed.
			    
			    * "twice" -> The lines and the faces will be displayed.
  
  :argument lines_color: An objet from type :obj:`Color` representing the lines color.
  
  :argument faces_color: The faces color(s).
			  
			  * An objet from type :obj:`Color` representing the faces color. 
			  
			  * An 4-items-list from objects from type :obj:`Color`. One item per tetrahedron face. 
  
  :argument lines_width: An integer representing the lines width.
  
  :argument display_ls: Define if the localview should be display.
  
.. method:: Tetrahedron.update_pos(matrix)

  Method to apply changing contains in the matrix argument on the tetrahedron object.
  
  :argument matrix: An object from type :obj:`Matrix` configurate to contains the wanted changings.
  
.. method:: Tetrahedron.display()

  Tetrahedron displaying method towards the settings.
  
.. method:: Tetrahedron.set_display_mode(display_mode)

  Change the polyhedron display mode. 
  
  :argument display_mode: can take as value:
                          
			    * "lined" -> Only the lines will be displayed.
			    
			    * "faced" -> Only the faces will be displayed.
			    
			    * "twice" -> The lines and the faces will be displayed.
			    
.. method:: Tetrahedron.set_lines_color(lines_color)

  Change the lines color from the polyhedron.
    
  :argument lines_color: An objet from type :obj:`Color` representing the lines color.
  
.. method:: Tetrahedron.set_faces_color(faces_color)

  Change the faces color(s) from the polyhedron.
        
  :argument faces_color: 
  
			  * An objet from type :obj:`Color` representing the faces color.
			 
			  * An 4-items-list from objects from type :obj:`Color`. One item per tetrahedron face.
			 
.. method:: Tetrahedron.set_lines_width(lines_width)

  Change the lines width from the polyhedron.
  
  :argument lines_width: An integer representing the lines width.
  
.. method:: Tetrahedron.set_display_ls(display_ls) :

  Change the Localview displaying setting.
  
  :argument display_ls: Define if the localview should be display.
  
.. method:: Tetrahedron.set_side_length(side_length) 

  Change the sides length from tetrahedron.
  
  :argument side_length: An float representing the tetrahedron sides length.
  
.. note:: **documentation**

  The Tetrahedron object has an private documentation display method: **Tetrahedron.__doc__()**
  
.. attribute:: Tetrahedron.side_length

  The tetrahedron sides length.

.. attribute:: Tetrahedron.lines_color

  The tetrahedron lines color.

.. attribute:: Tetrahedron.faces_color

  The tetrahedron faces color(s).

.. attribute:: Tetrahedron.polyhedron

  The tetrahedron polygons.

.. attribute:: Tetrahedron.ls
  
  The tetrahedron's localview.
  
.. attribute:: Tetrahedron.center

  The center of the polyhedron as an object from type :obj:`Vertex`.  
  
.. attribute:: Tetrahedron.display_ls

  Tetrahedron localview displaying boolean value.


++++
Cube
++++

.. class:: Cube(side_length,display_mode="lined",lines_color=False,faces_color=False,lines_width=1,display_ls=False)

  Generate an cube object with the given side length settings.
  
  :argument side_length: The side length of the cube sides.
  
  :argument display_mode: How to display the cube.
			    
			    * "lined" -> Only the lines will be displayed.
			    
			    * "faced" -> Only the faces will be displayed.
			    
			    * "twice" -> The lines and the faces will be displayed.
  
  :argument lines_color: An objet from type :obj:`Color` representing the lines color.
  
  :argument faces_color: The faces color(s).
			  
			  * An objet from type :obj:`Color` representing the faces color. 
			  
			  * An 6-items-list from objects from type :obj:`Color`. One item per cube face. 
  
  :argument lines_width: An integer representing the lines width.
  
  :argument display_ls: Define if the localview should be display.
  
.. method:: Cube.update_pos(matrix)

  Method to apply changing contains in the matrix argument on the cube object.
  
  :argument matrix: An object from type :obj:`Matrix` configurate to contains the wanted changings.
  
.. method:: Cube.display()

  Cube displaying method towards the settings.
  
.. method:: Cube.set_display_mode(display_mode)

  Change the polyhedron display mode. 
  
  :argument display_mode: can take as value:
                          
			    * "lined" -> Only the lines will be displayed.
			    
			    * "faced" -> Only the faces will be displayed.
			    
			    * "twice" -> The lines and the faces will be displayed.
			    
.. method:: Cube.set_lines_color(lines_color)

  Change the lines color from the polyhedron.
    
  :argument lines_color: An objet from type :obj:`Color` representing the lines color.
  
.. method:: Cube.set_faces_color(faces_color)

  Change the faces color(s) from the polyhedron.
        
  :argument faces_color: 
  
			  * An objet from type :obj:`Color` representing the faces color.
			 
			  * An 6-items-list from objects from type :obj:`Color`. One item per cube face.
			 
.. method:: Cube.set_lines_width(lines_width)

  Change the lines width from the polyhedron.
  
  :argument lines_width: An integer representing the lines width.
  
.. method:: Cube.set_display_ls(display_ls) :

  Change the Localview displaying setting.
  
  :argument display_ls: Define if the localview should be display.
  
.. method:: Cube.set_side_length(side_length) 

  Change the sides length from cube.
  
  :argument side_length: An float representing the cube sides length.
  
.. note:: **documentation**

  The Cube object has an private documentation display method: **Cube.__doc__()**
  
.. attribute:: Cube.side_length

  The cube sides length.

.. attribute:: Cube.lines_color

  The cube lines color.

.. attribute:: Cube.faces_color

  The cube faces color(s).

.. attribute:: Cube.polyhedron

  The cube polygons.

.. attribute:: Cube.ls
  
  The cube's localview.
 
.. attribute:: Cube.center

  The center of the polyhedron as an object from type :obj:`Vertex`. 
 
.. attribute:: Cube.display_ls

  Cube localview displaying boolean value.

++++++++++
Octahedron
++++++++++

.. class:: Octahedron(side_length,display_mode="lined",lines_color=False,faces_color=False,lines_width=1,display_ls=False)

  Generate an octahedron object with the given side length settings.
  
  :argument side_length: The side length of the octahedron sides.
  
  :argument display_mode: How to display the octahedron.
			    
			    * "lined" -> Only the lines will be displayed.
			    
			    * "faced" -> Only the faces will be displayed.
			    
			    * "twice" -> The lines and the faces will be displayed.
  
  :argument lines_color: An objet from type :obj:`Color` representing the lines color.
  
  :argument faces_color: The faces color(s).
			  
			  * An objet from type :obj:`Color` representing the faces color. 
			  
			  * An 8-items-list from objects from type :obj:`Color`. One item per octahedron face. 
  
  :argument lines_width: An integer representing the lines width.
  
  :argument display_ls: Define if the localview should be display.
  
.. method:: Octahedron.update_pos(matrix)

  Method to apply changing contains in the matrix argument on the octahedron object.
  
  :argument matrix: An object from type :obj:`Matrix` configurate to contains the wanted changings.
  
.. method:: Octahedron.display()

  Octahedron displaying method towards the settings.
  
.. method:: Octahedron.set_display_mode(display_mode)

  Change the polyhedron display mode. 
  
  :argument display_mode: can take as value:
                          
			    * "lined" -> Only the lines will be displayed.
			    
			    * "faced" -> Only the faces will be displayed.
			    
			    * "twice" -> The lines and the faces will be displayed.
			    
.. method:: Octahedron.set_lines_color(lines_color)

  Change the lines color from the polyhedron.
    
  :argument lines_color: An objet from type :obj:`Color` representing the lines color.
  
.. method:: Octahedron.set_faces_color(faces_color)

  Change the faces color(s) from the polyhedron.
        
  :argument faces_color: 
  
			  * An objet from type :obj:`Color` representing the faces color.
			 
			  * An 8-items-list from objects from type :obj:`Color`. One item per octahedron face.
			 
.. method:: Octahedron.set_lines_width(lines_width)

  Change the lines width from the polyhedron.
  
  :argument lines_width: An integer representing the lines width.
  
.. method:: Octahedron.set_display_ls(display_ls) :

  Change the Localview displaying setting.
  
  :argument display_ls: Define if the localview should be display.
  
.. method:: Octahedron.set_side_length(side_length) 

  Change the sides length from octahedron.
  
  :argument side_length: An float representing the octahedron sides length.
  
.. note:: **documentation**

  The Octahedron object has an private documentation display method: **Octahedron.__doc__()**
  
.. attribute:: Octahedron.side_length

  The octahedron sides length.

.. attribute:: Octahedron.lines_color

  The octahedron lines color.

.. attribute:: Octahedron.faces_color

  The octahedron faces color(s).

.. attribute:: Octahedron.polyhedron

  The octahedron polygons.

.. attribute:: Octahedron.ls
  
  The octahedron's localview.
  
.. attribute:: Octahedron.center

  The center of the polyhedron as an object from type :obj:`Vertex`.      
  
.. attribute:: Octahedron.display_ls

  Octahedron localview displaying boolean value.
  
++++++++++++
Dodecahedron
++++++++++++

.. class:: Dodecahedron(side_length,display_mode="lined",lines_color=False,faces_color=False,lines_width=1,display_ls=False)

  Generate an dodecahedron object with the given side length settings.
  
  :argument side_length: The side length of the dodecahedron sides.
  
  :argument display_mode: How to display the dodecahedron.
			    
			    * "lined" -> Only the lines will be displayed.
			    
			    * "faced" -> Only the faces will be displayed.
			    
			    * "twice" -> The lines and the faces will be displayed.
  
  :argument lines_color: An objet from type :obj:`Color` representing the lines color.
  
  :argument faces_color: The faces color(s).
			  
			  * An objet from type :obj:`Color` representing the faces color. 
			  
			  * An 12-items-list from objects from type :obj:`Color`. One item per dodecahedron face. 
  
  :argument lines_width: An integer representing the lines width.
  
  :argument display_ls: Define if the localview should be display.
  
.. method:: Dodecahedron.update_pos(matrix)

  Method to apply changing contains in the matrix argument on the dodecahedron object.
  
  :argument matrix: An object from type :obj:`Matrix` configurate to contains the wanted changings.
  
.. method:: Dodecahedron.display()

  Dodecahedron displaying method towards the settings.
  
.. method:: Dodecahedron.set_display_mode(display_mode)

  Change the polyhedron display mode. 
  
  :argument display_mode: can take as value:
                          
			    * "lined" -> Only the lines will be displayed.
			    
			    * "faced" -> Only the faces will be displayed.
			    
			    * "twice" -> The lines and the faces will be displayed.
			    
.. method:: Dodecahedron.set_lines_color(lines_color)

  Change the lines color from the polyhedron.
    
  :argument lines_color: An objet from type :obj:`Color` representing the lines color.
  
.. method:: Dodecahedron.set_faces_color(faces_color)

  Change the faces color(s) from the polyhedron.
        
  :argument faces_color: 
  
			  * An objet from type :obj:`Color` representing the faces color.
			 
			  * An 12-items-list from objects from type :obj:`Color`. One item per dodecahedron face.
			 
.. method:: Dodecahedron.set_lines_width(lines_width)

  Change the lines width from the polyhedron.
  
  :argument lines_width: An integer representing the lines width.
  
.. method:: Dodecahedron.set_display_ls(display_ls) :

  Change the Localview displaying setting.
  
  :argument display_ls: Define if the localview should be display.
  
.. method:: Dodecahedron.set_side_length(side_length) 

  Change the sides length from dodecahedron.
  
  :argument side_length: An float representing the dodecahedron sides length.
  
.. note:: **documentation**

  The Dodecahedron object has an private documentation display method: **Dodecahedron.__doc__()**
  
.. attribute:: Dodecahedron.side_length

  The dodecahedron sides length.

.. attribute:: Dodecahedron.lines_color

  The dodecahedron lines color.

.. attribute:: Dodecahedron.faces_color

  The dodecahedron faces color(s).

.. attribute:: Dodecahedron.polyhedron

  The dodecahedron polygons.

.. attribute:: Dodecahedron.ls
  
  The dodecahedron's localview.

.. attribute:: Dodecahedron.center

  The center of the polyhedron as an object from type :obj:`Vertex`.    
  
.. attribute:: Dodecahedron.display_ls

  Dodecahedron localview displaying boolean value.
  
+++++++++++
Icosahedron
+++++++++++

.. class:: Icosahedron(side_length,display_mode="lined",lines_color=False,faces_color=False,lines_width=1,display_ls=False)

  Generate an icosahedron object with the given side length settings.
  
  :argument side_length: The side length of the icosahedron sides.
  
  :argument display_mode: How to display the icosahedron.
			    
			    * "lined" -> Only the lines will be displayed.
			    
			    * "faced" -> Only the faces will be displayed.
			    
			    * "twice" -> The lines and the faces will be displayed.
  
  :argument lines_color: An objet from type :obj:`Color` representing the lines color.
  
  :argument faces_color: The faces color(s).
			  
			  * An objet from type :obj:`Color` representing the faces color. 
			  
			  * An 20-items-list from objects from type :obj:`Color`. One item per icosahedron face. 
  
  :argument lines_width: An integer representing the lines width.
  
  :argument display_ls: Define if the localview should be display.
  
.. method:: Icosahedron.update_pos(matrix)

  Method to apply changing contains in the matrix argument on the icosahedron object.
  
  :argument matrix: An object from type :obj:`Matrix` configurate to contains the wanted changings.
  
.. method:: Icosahedron.display()

  Icosahedron displaying method towards the settings.
  
.. method:: Icosahedron.set_display_mode(display_mode)

  Change the polyhedron display mode. 
  
  :argument display_mode: can take as value:
                          
			    * "lined" -> Only the lines will be displayed.
			    
			    * "faced" -> Only the faces will be displayed.
			    
			    * "twice" -> The lines and the faces will be displayed.
			    
.. method:: Icosahedron.set_lines_color(lines_color)

  Change the lines color from the polyhedron.
    
  :argument lines_color: An objet from type :obj:`Color` representing the lines color.
  
.. method:: Icosahedron.set_faces_color(faces_color)

  Change the faces color(s) from the polyhedron.
        
  :argument faces_color: 
  
			  * An objet from type :obj:`Color` representing the faces color.
			 
			  * An 20-items-list from objects from type :obj:`Color`. One item per icosahedron face.
			 
.. method:: Icosahedron.set_lines_width(lines_width)

  Change the lines width from the polyhedron.
  
  :argument lines_width: An integer representing the lines width.
  
.. method:: Icosahedron.set_display_ls(display_ls) :

  Change the Localview displaying setting.
  
  :argument display_ls: Define if the localview should be display.
  
.. method:: Icosahedron.set_side_length(side_length) 

  Change the sides length from icosahedron.
  
  :argument side_length: An float representing the icosahedron sides length.
  
.. note:: **documentation**

  The Icosahedron object has an private documentation display method: **Icosahedron.__doc__()**
  
.. attribute:: Icosahedron.side_length

  The icosahedron sides length.

.. attribute:: Icosahedron.lines_color

  The icosahedron lines color.

.. attribute:: Icosahedron.faces_color

  The icosahedron faces color(s).

.. attribute:: Icosahedron.polyhedron

  The icosahedron polygons.

.. attribute:: Icosahedron.ls
  
  The icosahedron's localview.
  
.. attribute:: Icosahedron.center

  The center of the polyhedron as an object from type :obj:`Vertex`.  
  
.. attribute:: Icosahedron.display_ls

  Icosahedron localview displaying boolean value. 
  
-----------------
Other polyhedrons
----------------- 

++++++++++++++++++++++++
Polyhedron with 26 faces
++++++++++++++++++++++++

.. class:: Poly26Hedron(side_length,display_mode="lined",lines_color=False,quads_color=False,triangles_color=False,lines_width=1,display_ls=False)

  Generate an polyhedron with 26 faces, 18 quads and 8 triangles, object with the given side length settings.
  
  :argument side_length: The side length of the polyhedron with 26 faces sides.
  
  :argument display_mode: How to display the polyhedron with 26 faces.
			    
			    * "lined" -> Only the lines will be displayed.
			    
			    * "faced" -> Only the faces will be displayed.
			    
			    * "twice" -> The lines and the faces will be displayed.
  
  :argument lines_color: An objet from type :obj:`Color` representing the lines color.
  
  :argument quads_color: The quads color(s).
			  
			  * An objet from type :obj:`Color` representing the faces color. 
			  
			  * An 18-items-list from objects from type :obj:`Color`. One item per polyhedron quads face. 
			  
  :argument triangles_color: The triangles color(s).
			  
			  * An objet from type :obj:`Color` representing the faces color. 
			  
			  * An 8-items-list from objects from type :obj:`Color`. One item per polyhedron triangle face. 			  
  
  :argument lines_width: An integer representing the lines width.
  
  :argument display_ls: Define if the localview should be display.
  
.. method:: Poly26Hedron.update_pos(matrix)

  Method to apply changing contains in the matrix argument on the polyhedron with 26 faces object.
  
  :argument matrix: An object from type :obj:`Matrix` configurate to contains the wanted changings.
  
.. method:: Poly26Hedron.display()

  polyhedron with 26 faces displaying method towards the settings.
  
.. method:: Poly26Hedron.set_display_mode(display_mode)

  Change the polyhedron display mode. 
  
  :argument display_mode: can take as value:
                          
			    * "lined" -> Only the lines will be displayed.
			    
			    * "faced" -> Only the faces will be displayed.
			    
			    * "twice" -> The lines and the faces will be displayed.
			    
.. method:: Poly26Hedron.set_lines_color(lines_color)

  Change the lines color from the polyhedron.
    
  :argument lines_color: An objet from type :obj:`Color` representing the lines color.
  
.. method:: Poly26Hedron.set_quads_color(quads_color)

  Change the quads faces color(s) from the polyhedron.
        
  :argument quads_color: 
  
			  * An objet from type :obj:`Color` representing the faces color.
			 
			  * An 18-items-list from objects from type :obj:`Color`. One item per polyhedron quads face.
	
.. method:: Poly26Hedron.set_triangles_color(triangles_color)

  Change the triangles faces color(s) from the polyhedron.
        
  :argument triangles_color: 
  
			  * An objet from type :obj:`Color` representing the faces color.
			 
			  * An 8-items-list from objects from type :obj:`Color`. One item per polyhedron triangle face.	
	
.. method:: Poly26Hedron.set_lines_width(lines_width)

  Change the lines width from the polyhedron.
  
  :argument lines_width: An integer representing the lines width.
  
.. method:: Poly26Hedron.set_display_ls(display_ls) :

  Change the Localview displaying setting.
  
  :argument display_ls: Define if the localview should be display.
  
.. method:: Poly26Hedron.set_side_length(side_length) 

  Change the sides length from polyhedron with 26 faces.
  
  :argument side_length: An float representing the polyhedron with 26 faces sides length.
  
.. note:: **documentation**

  The Poly26Hedron object has an private documentation display method: **Poly26Hedron.__doc__()**
  
.. attribute:: Poly26Hedron.side_length

  The 26 faces polyhedron  sides length.

.. attribute:: Poly26Hedron.lines_color

  The polyhedron lines color.

.. attribute:: Poly26Hedron.triangles_color

  The polyhedron triangles color(s).

.. attribute:: Poly26Hedron.quads_color

  The polyhedron quads color(s).  
  
.. attribute:: Poly26Hedron.quads

  The polyhedron quads container.
  
.. attribute:: Poly26Hedron.triangles

  The polyhedron triangles container.  

.. attribute:: Poly26Hedron.ls
  
  The 26 faces polyhedron 's localview.
  
.. attribute:: Poly26Hedron.center

  The center of the polyhedron as an object from type :obj:`Vertex`.
  
.. attribute:: Poly26Hedron.display_ls

  The 26 faces polyhedron localview displaying boolean value.
  
++++++++++++++++++++++++
Polyhedron with 32 faces
++++++++++++++++++++++++  
  
.. class:: Poly32Hedron(side_length,display_mode="lined",lines_color=False,pentagons_color=False,triangles_color=False,lines_width=1,display_ls=False)

  Generate an polyhedron with 32 faces, 20 triangles and 12 pentagons, object with the given side length settings.
  
  :argument side_length: The side length of the polyhedron with 32 faces sides.
  
  :argument display_mode: How to display the polyhedron with 32 faces.
			    
			    * "lined" -> Only the lines will be displayed.
			    
			    * "faced" -> Only the faces will be displayed.
			    
			    * "twice" -> The lines and the faces will be displayed.
  
  :argument lines_color: An objet from type :obj:`Color` representing the lines color.
  
  :argument triangles_color: The triangles color(s).
			  
			  * An objet from type :obj:`Color` representing the faces color. 
			  
			  * An 20-items-list from objects from type :obj:`Color`. One item per polyhedron triangles face. 
			  
  :argument pentagons_color: The pentagons color(s).
			  
			  * An objet from type :obj:`Color` representing the faces color. 
			  
			  * An 12-items-list from objects from type :obj:`Color`. One item per polyhedron triangle face. 			  
  
  :argument lines_width: An integer representing the lines width.
  
  :argument display_ls: Define if the localview should be display.
  
.. method:: Poly32Hedron.update_pos(matrix)

  Method to apply changing contains in the matrix argument on the polyhedron with 32 faces object.
  
  :argument matrix: An object from type :obj:`Matrix` configurate to contains the wanted changings.
  
.. method:: Poly32Hedron.display()

  polyhedron with 32 faces displaying method towards the settings.
  
.. method:: Poly32Hedron.set_display_mode(display_mode)

  Change the polyhedron display mode. 
  
  :argument display_mode: can take as value:
                          
			    * "lined" -> Only the lines will be displayed.
			    
			    * "faced" -> Only the faces will be displayed.
			    
			    * "twice" -> The lines and the faces will be displayed.
			    
.. method:: Poly32Hedron.set_lines_color(lines_color)

  Change the lines color from the polyhedron.
    
  :argument lines_color: An objet from type :obj:`Color` representing the lines color.
  
.. method:: Poly32Hedron.set_triangles_color(triangles_color)

  Change the triangles faces color(s) from the polyhedron.
        
  :argument triangles_color: 
  
			  * An objet from type :obj:`Color` representing the faces color.
			 
			  * An 20-items-list from objects from type :obj:`Color`. One item per polyhedron triangle face.
	
.. method:: Poly32Hedron.set_pentagons_color(pentagons_color)

  Change the pentagons faces color(s) from the polyhedron.
        
  :argument pentagons_color: 
  
			  * An objet from type :obj:`Color` representing the faces color.
			 
			  * An 12-items-list from objects from type :obj:`Color`. One item per polyhedron pentagon face.	
	
.. method:: Poly32Hedron.set_lines_width(lines_width)

  Change the lines width from the polyhedron.
  
  :argument lines_width: An integer representing the lines width.
  
.. method:: Poly32Hedron.set_display_ls(display_ls) :

  Change the Localview displaying setting.
  
  :argument display_ls: Define if the localview should be display.
  
.. method:: Poly32Hedron.set_side_length(side_length) 

  Change the sides length from polyhedron with 32 faces.
  
  :argument side_length: An float representing the polyhedron with 32 faces sides length.
  
.. note:: **documentation**

  The Poly32Hedron object has an private documentation display method: **Poly32Hedron.__doc__()**
  
.. attribute:: Poly32Hedron.side_length

  The 32 faces polyhedron  sides length.

.. attribute:: Poly32Hedron.lines_color

  The polyhedron lines color.

.. attribute:: Poly26Hedron.triangles_color

  The polyhedron triangles color(s).

.. attribute:: Poly26Hedron.pentagons_color

  The polyhedron pentagons color(s).  

.. attribute:: Poly32Hedron.triangles

  The polyhedron triangles container.
  
.. attribute:: Poly32Hedron.pentagons

  The polyhedron pentagons container.  

.. attribute:: Poly32Hedron.ls
  
  The 32 faces polyhedron 's localview.
  
.. attribute:: Poly32Hedron.center

  The center of the polyhedron as an object from type :obj:`Vertex`.
  
.. attribute:: Poly32Hedron.display_ls

  The 32 faces polyhedron  localview displaying boolean value.
  
------------------
Fulleren and toros
------------------

++++++++
Fulleren
++++++++

.. class:: Fulleren(side_length,display_mode="lined",lines_color=False,pentagons_color=False,hexagons_color=False,lines_width=1,display_ls=False)

  Generate an fulleren, 20 hexagons and 12 pentagons, object with the given side length settings.
  
  :argument side_length: The side length of the fullerens sides.
  
  :argument display_mode: How to display the fulleren.
			    
			    * "lined" -> Only the lines will be displayed.
			    
			    * "faced" -> Only the faces will be displayed.
			    
			    * "twice" -> The lines and the faces will be displayed.
  
  :argument lines_color: An objet from type :obj:`Color` representing the lines color.
  
			  
  :argument pentagons_color: The pentagons color(s).
			  
			  * An objet from type :obj:`Color` representing the faces color. 
			  
			  * An 12-items-list from objects from type :obj:`Color`. One item per polyhedron pentagon face. 			  
  
  :argument hexagons_color: The hexagons color(s).
			  
			  * An objet from type :obj:`Color` representing the faces color. 
			  
			  * An 20-items-list from objects from type :obj:`Color`. One item per polyhedron hexagon face. 
  
  :argument lines_width: An integer representing the lines width.
  
  :argument display_ls: Define if the localview should be display.
  
.. method:: Fulleren.update_pos(matrix)

  Method to apply changing contains in the matrix argument on the fulleren object.
  
  :argument matrix: An object from type :obj:`Matrix` configurate to contains the wanted changings.
  
.. method:: Fulleren.display()

  fulleren displaying method towards the settings.
  
.. method:: Fulleren.set_display_mode(display_mode)

  Change the polyhedron display mode. 
  
  :argument display_mode: can take as value:
                          
			    * "lined" -> Only the lines will be displayed.
			    
			    * "faced" -> Only the faces will be displayed.
			    
			    * "twice" -> The lines and the faces will be displayed.
			    
.. method:: Fulleren.set_lines_color(lines_color)

  Change the lines color from the polyhedron.
    
  :argument lines_color: An objet from type :obj:`Color` representing the lines color.
  
.. method:: Fulleren.set_hexagons_color(hexagons_color)

  Change the hexagons faces color(s) from the polyhedron.
        
  :argument hexagons_color: 
  
			  * An objet from type :obj:`Color` representing the faces color.
			 
			  * An 20-items-list from objects from type :obj:`Color`. One item per polyhedron hexagons face.
	
.. method:: Fulleren.set_pentagons_color(pentagons_color)

  Change the pentagons faces color(s) from the polyhedron.
        
  :argument pentagons_color: 
  
			  * An objet from type :obj:`Color` representing the faces color.
			 
			  * An 12-items-list from objects from type :obj:`Color`. One item per polyhedron pentagon face.	
	
.. method:: Fulleren.set_lines_width(lines_width)

  Change the lines width from the polyhedron.
  
  :argument lines_width: An integer representing the lines width.
  
.. method:: Fulleren.set_display_ls(display_ls) :

  Change the Localview displaying setting.
  
  :argument display_ls: Define if the localview should be display.
  
.. method:: Fulleren.set_side_length(side_length) 

  Change the sides length from fulleren.
  
  :argument side_length: An float representing the fulleren sides length.
  
.. note:: **documentation**

  The Fulleren object has an private documentation display method: **Fulleren.__doc__()**
  
.. attribute:: Fulleren.side_length

  The fulleren sides length.

.. attribute:: Fulleren.lines_color

  The fulleren lines color.

.. attribute:: Fulleren.faces_color

  The fulleren faces color(s).

.. attribute:: Fulleren.hexagons

  The fulleren hexagons container.
  
.. attribute:: Fulleren.pentagons

  The fulleren pentagons container.  

.. attribute:: Fulleren.ls
  
  The fulleren's localview.
  
.. attribute:: Fulleren.center

  The center of the polyhedron as an object from type :obj:`Vertex`.
  
.. attribute:: Fulleren.display_ls

  Fulleren localview displaying boolean value.
  
+++++
Toros
+++++  
  
.. class:: Toros(base_polygon,base_radius,toros_radius,display_mode="lined",lines_color=False,faces_color=False,lines_width=1,display_ls=False)
  
  Generate an toros object with the given radius and basis polygone settings.
  
  :argument base: The base polygon edges number, for the toros generation.
  
  :argument base_radius: The base polygon radius, for the toros generation.
  
  :argument toros_radius: The toros radius (without the base polygon radius). 
  
  :argument display_mode: How to display the toros.
			    
			    * "lined" -> Only the lines will be displayed.
			    
			    * "faced" -> Only the faces will be displayed.
			    
			    * "twice" -> The lines and the faces will be displayed.
  
  :argument lines_color: An objet from type :obj:`Color` representing the lines color.
  
  :argument faces_color: The faces color(s). An objet from type :obj:`Color` representing the faces color.   
  
  :argument lines_width: An integer representing the lines width.
  
  :argument display_ls: Define if the localview should be display.
  
.. method:: Toros.update_pos(matrix)

  Method to apply changing contains in the matrix argument on the toros object.
  
  :argument matrix: An object from type :obj:`Matrix` configurate to contains the wanted changings.
  
.. method:: Toros.display()

  Toros displaying method towards the settings.
  
.. method:: Toros.set_display_mode(display_mode)

  Change the polyhedron display mode. 
  
  :argument display_mode: can take as value:
                          
			    * "lined" -> Only the lines will be displayed.
			    
			    * "faced" -> Only the faces will be displayed.
			    
			    * "twice" -> The lines and the faces will be displayed.
			    
.. method:: Toros.set_lines_color(lines_color)

  Change the lines color from the polyhedron.
    
  :argument lines_color: An objet from type :obj:`Color` representing the lines color.
  
.. method:: Toros.set_faces_color(faces_color)

  Change the faces color(s) from the polyhedron.
        
  :argument faces_color: An objet from type :obj:`Color` representing the faces color.
 
.. method:: Toros.set_lines_width(lines_width)

  Change the lines width from the polyhedron.
  
  :argument lines_width: An integer representing the lines width.
  
.. method:: Toros.set_display_ls(display_ls) :

  Change the Localview displaying setting.
  
  :argument display_ls: Define if the localview should be display.
  
.. method:: Toros.set_base_polygon(base_polygon)

  Change the toros basis polygon.
  
  :argument base_polygon: The base polygon edges number, for the toros generation.
  
.. method:: Toros.set_base_radius(base_radius)

  Change the toros base polygon radius.
  
  :argument base_radius: The base polygon radius, for the toros generation.
  
.. method:: Toros.set_toros_radius(toros_radius)
 
  Change the toros radius (without the base polygon radius).
  
  :argument toros_radius: The toros radius (without the base polygon radius). 
  
.. note:: **documentation**

  The Toros object has an private documentation display method: **Toros.__doc__()**
  
.. attribute:: Toros.base_polygon

  The base polygon edges number, for the toros generation.

.. attribute:: Toros.base_radius

  The base polygon radius, for the toros generation.

.. attribute:: Tors.toros_radius

  The toros radius (without the base polygon radius). 

.. attribute:: Toros.lines_color

  The toros lines color.

.. attribute:: Toros.faces_color

  The toros faces color(s).

.. attribute:: Toros.toros

  The toros polygons container.
  
.. attribute:: Toros.ls
  
  The toros's localview.
  
.. attribute:: Toros.center

  The center of the polyhedron as an object from type :obj:`Vertex`.      
  
.. attribute:: Toros.display_ls

  Toros localview displaying boolean value. 
  
-------
Spheres
-------

+++++++++++
Quad_Sphere
+++++++++++

.. class:: Quad_Sphere(radius,basis,display_mode="lined",lines_color=False,faces_color=False,lines_width=1,display_ls=False)

  Generate an quad sphere object with the given radius and polygone basis.
  
  :argument radius: The radius of the sphere to generate.
  
  :argument basis: The basis polygon for the sphere generation.
  
	           The basis must be: basis % 2 == 0.		    
  
  :argument display_mode: How to display the sphere.
			    
			    * "lined" -> Only the lines will be displayed.
			    
			    * "faced" -> Only the faces will be displayed.
			    
			    * "twice" -> The lines and the faces will be displayed.
  
  :argument lines_color: An objet from type :obj:`Color` representing the lines color.
  
  :argument faces_color: An objet from type :obj:`Color` representing the faces color.  
  
  :argument lines_width: An integer representing the lines width.
  
  :argument display_ls: Define if the localview should be display.
  
.. method:: Quad_Sphere.update_pos(matrix)

  Method to apply changing contains in the matrix argument on the sphere object.
  
  :argument matrix: An object from type :obj:`Matrix` configurate to contains the wanted changings.
  
.. method:: Quad_Sphere.display()

  Quad_Sphere displaying method towards the settings.
  
.. method:: Quad_Sphere.set_display_mode(display_mode)

  Change the sphere display mode. 
  
  :argument display_mode: can take as value:
                          
			    * "lined" -> Only the lines will be displayed.
			    
			    * "faced" -> Only the faces will be displayed.
			    
			    * "twice" -> The lines and the faces will be displayed.
			    
.. method:: Quad_Sphere.set_lines_color(lines_color)

  Change the lines color from the sphere.
    
  :argument lines_color: An objet from type :obj:`Color` representing the lines color.
  
.. method:: Quad_Sphere.set_faces_color(faces_color)

  Change the faces color(s) from the sphere.
        
  :argument faces_color: An objet from type :obj:`Color` representing the faces color.

.. method:: Quad_Sphere.set_lines_width(lines_width)

  Change the lines width from the sphere.
  
  :argument lines_width: An integer representing the lines width.
  
.. method:: Quad_Sphere.set_display_ls(display_ls) :

  Change the Localview displaying setting.
  
  :argument display_ls: Define if the localview should be display.
  
.. method:: Quad_Sphere.set_basis(basis) 

  Change sphere basis polygon.
  
  :argument basis: An integer representing the sphere base polygon edges number.
  
.. method:: Quad_Sphere.set_radius(radius) 

  Change sphere radius.
  
  :argument radius: An float representing the sphere radius.  
  
.. note:: **documentation**

  The Quad_Sphere object has an private documentation display method: **Quad_Sphere.__doc__()**
  
.. attribute:: Quad_Sphere.radius

  The sphere radius.
  
.. attribute:: Quad_Sphere.basis

  The sphere basis polygon. 

.. attribute:: Quad_Sphere.lines_color

  The sphere lines color.

.. attribute:: Quad_Sphere.faces_color

  The sphere faces color.

.. attribute:: Quad_Sphere.polygons

  The sphere polygons.

.. attribute:: Quad_Sphere.ls
  
  The sphere's localview.
  
.. attribute:: Quad_Sphere.center

  The center of the sphere as an object from type :obj:`Vertex`.  
  
.. attribute:: Quad_Sphere.display_ls

  Quad_Sphere localview displaying boolean value. 
  
+++++++++++++
Trigon_Sphere
+++++++++++++  
  
.. class:: Trigon_Sphere(radius,basis,display_mode="lined",lines_color=False,faces_color=False,lines_width=1,display_ls=False)

  Generate an quad sphere object with the given radius and polygone basis.
  
  :argument radius: The radius of the sphere to generate.
  
  :argument basis: The basis polygon for the sphere generation.
  
	           The basis must be: basis % 4 == 0.		    
  
  :argument display_mode: How to display the sphere.
			    
			    * "lined" -> Only the lines will be displayed.
			    
			    * "faced" -> Only the faces will be displayed.
			    
			    * "twice" -> The lines and the faces will be displayed.
  
  :argument lines_color: An objet from type :obj:`Color` representing the lines color.
  
  :argument faces_color: An objet from type :obj:`Color` representing the faces color.  
  
  :argument lines_width: An integer representing the lines width.
  
  :argument display_ls: Define if the localview should be display.
  
.. method:: Trigon_Sphere.update_pos(matrix)

  Method to apply changing contains in the matrix argument on the sphere object.
  
  :argument matrix: An object from type :obj:`Matrix` configurate to contains the wanted changings.
  
.. method:: Trigon_Sphere.display()

  Trigon_Sphere displaying method towards the settings.
  
.. method:: Trigon_Sphere.set_display_mode(display_mode)

  Change the sphere display mode. 
  
  :argument display_mode: can take as value:
                          
			    * "lined" -> Only the lines will be displayed.
			    
			    * "faced" -> Only the faces will be displayed.
			    
			    * "twice" -> The lines and the faces will be displayed.
			    
.. method:: Trigon_Sphere.set_lines_color(lines_color)

  Change the lines color from the sphere.
    
  :argument lines_color: An objet from type :obj:`Color` representing the lines color.
  
.. method:: Trigon_Sphere.set_faces_color(faces_color)

  Change the faces color(s) from the sphere.
        
  :argument faces_color: An objet from type :obj:`Color` representing the faces color.

.. method:: Trigon_Sphere.set_lines_width(lines_width)

  Change the lines width from the sphere.
  
  :argument lines_width: An integer representing the lines width.
  
.. method:: Trigon_Sphere.set_display_ls(display_ls) :

  Change the Localview displaying setting.
  
  :argument display_ls: Define if the localview should be display.
  
.. method:: Trigon_Sphere.set_basis(basis) 

  Change sphere basis polygon.
  
  :argument basis: An integer representing the sphere base polygon edges number.
  
                   The basis must be: basis % 4 == 0.	
  
.. method:: Trigon_Sphere.set_radius(radius) 

  Change sphere radius.
  
  :argument radius: An float representing the sphere radius.  
  
.. note:: **documentation**

  The Trigon_Sphere object has an private documentation display method: **Trigon_Sphere.__doc__()**
  
.. attribute:: Trigon_Sphere.radius

  The sphere radius.
  
.. attribute:: Trigon_Sphere.basis

  The sphere basis polygon. 

.. attribute:: Trigon_Sphere.lines_color

  The sphere lines color.

.. attribute:: Trigon_Sphere.faces_color

  The sphere faces color.

.. attribute:: Trigon_Sphere.trigons

  The sphere trigons.

.. attribute:: Trigon_Sphere.ls
  
  The sphere's localview.
  
.. attribute:: Trigon_Sphere.center

  The center of the sphere as an object from type :obj:`Vertex`.  
  
.. attribute:: Trigon_Sphere.display_ls

  Trigon_Sphere localview displaying boolean value.     