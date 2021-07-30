
### Developed by Sai Teja Macharla 
#### *Email: macharlasaiteja@gmail.com*  

<br>

#### Test Results (Total Tests: 40+)
#### ALL TESTS PASSED
**==================== 16 passed in 0.40s =====================**

#  Session 12 - Iterables and Iterators - II
## Topics Covered 
- Lazy Iterables
- In-Built Iterables
- Sorting Iterables
- The iter() function
- Iterating Callables
- Delegating Iterators
- Reversed Iteration
- Using Iterators as function arguments


## **Project: Description** 
- The starting point for this project is the Polygon class and the Polygons sequence type we created in the previous project.
- The code for these classes along with the unit tests for the Polygon class are below if you want to use those as your starting point. But use whatever you came up with in the last project.

We have two goals:

#### **Goal 1**
- Refactor the Polygon class so that all the calculated properties are lazy properties, i.e. they should still be calculated properties, but they should not have to get recalculated more than once (since we made our Polygon class "immutable").

#### **Goal 2**
- Refactor the Polygons (sequence) type, into an iterable. Make sure also that the elements in the iterator are computed lazily - i.e. you can no longer use a list as an underlying storage mechanism for your polygons.
- You'll need to implement both an iterable, and an iterator.



![text](/image.jpeg "")

## **Function created based on Assignment**
### Part -1 Functions (class : Polygon)
- A Polygon class which will generate regular polygon of desired vertex and circumradius
###  __repr__  
- This function is used to display the output of the class object.

###  __gt__ 
-  This class is to check greater than. It checks the self.no_edges and circumradius with the ones of the other passed in as argument

###  __eq__ 
-  This class is to check equality. It checks the self.no_edges and circumradius  with the ones of the other passed in as argument

###  **interior_angle**
-  (edges - 2) * (180 / edges)

###  **edge_length** 
-  2 * circumradius * math.sin(math.pi / edges)

###  **apothem** 
-  circumradius * math.cos(math.pi / edges)

###  **area**
-  0.5 * edges * edge_length * apothem

###  **perimeter** 
-  edges *  edge_length

###  **__iter__** 
-  iter method is used to create iterator .

###  **__next__** 
-  next method used over iterator to get the next element.


### Part -2 Functions (class : PolygonSequence)
- This is a polygon sequence class used to develop a custom sequence

###  **__len__** 
-  _edges - 2

###  **__getitem__** 
where initializer takes in:
- number of vertices for largest polygon in the sequence
- common circumradius for all polygons

###  **efficient_polygon** 
-  This function calculates the efficient_polygon based on area/ perimeter ration  and returns the string displaying the output

###  **class PolygonIter** 
-  This is a polygon ITERATOR (next method callable only with iterator : lazily produce next value )t

###  **circumradius** 

###  **vertices** 


## **Functions used in Test File**
### test_readme_exists 
- checks if Readme files exists

### test_readme_contents  
- checks the content length of  Readme file , if it has more than 500 words then only test will be passed

### test_readme_proper_description 
- checks the content length of  Readme file

### test_readme_file_for_formatting 
- checks the formatting of  Readme file

### test_indentations 
- checks if the Assignment code is properly formatted

### test_function_name_had_cap_letter 
- checks if the Assignment code is function has capital letters

### test_Polygon_1 
- tests Polygon class outputs 
### test_Polygon_2
- tests Polygon class outputs 
### test_Polygon_gt
- tests Polygon greater than function outputs
### test_Polygon_eq
- tests Polygon equality function outputs
### test_polygon_size
- tests Polygon size function outputs
### test_PolygonSequence
- tests PolygonSequence class outputs
### test_PolygonSequence_efficient
- tests PolygonSequence efficient_polygon function outputs
### test_PolygonSequence_next
- tests PolygonSequence next method outputs
### test_polygon
- tests Polygon class outputs