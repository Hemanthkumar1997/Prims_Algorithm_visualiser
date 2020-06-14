# Prims Algorithm visualiser
Visualises spanning tree found using prims algorithm using openGL


### How to run
* install openGL libraries
* if you are using linux based os use "g++ filename.cpp -o gl -lGL -lGLU - lglut" to compile and ./a.out for running program

### Note 
* if nothing appears after welcome screen 
  - change glutInitDisplayMode(GLUT_DOUBLE) to glutInitDisplayMode(GLUT_SINGLE) 
  - replace all glutswapbuffer() with glFlush()
  - this might change shape of point to rectangle than circle thus you can define your own function to draw circle instead of point in place of draw edge function
* if you are unable to draw vertices increase center_difference_error value in the code.

## Features
- Run
- Undo
- Redo
- Draw Nodes
- Draw Edges
- Print cost matrix
- Spanning Tree calculation

# Algorithm used

## Prims Algorithm
  The algorithm may informally be described as performing the following steps:

  1. Initialize a tree with a single vertex, chosen arbitrarily from the graph.
  2. Grow the tree by one edge: of the edges that connect the tree to vertices not yet in the tree, find the minimum-weight 
     edge,and transfer it to the tree.
  3. Repeat step 2 (until all vertices are in the tree).
  

## Functions
#### 1. int_str()

  ##### signature:
   void int_str(int rad,char r[]) 
   
  ##### Description:
  This functions writes the integer into char array

#### 2. push()
  
  ##### signature:
  void push(int n)
  
  ##### Description:
  whenever undo function is called the cost is pushed into the stack
  
#### 3. pop()

  ##### signature:
  int pop()
  
  ##### Description:
  when redo function is called the cost is popped out

#### 4. drawpoint()
  
  ##### signature:
  void drawpoint()
  
  ##### Description:
  this function creates nodes using location stored in oldx[][] array
  
#### 5. bitmap_output()
  
  ##### signature:
  void bitmap_output(int x, int y, char *string, void *font)
  
  ##### Description:
  This function prints text in graphics window
  
#### 6. delay()

  ##### signature:
  void delay()
  
  ##### Description:
  this delays out execution of next instruction

#### 7. frontpage()

  ##### signature:
  void frontpage()
  
  ##### Description:
  this function displays staring window

#### 8. Instructions()

  ##### signature:
  void Instructions()
  
  ##### Description:
  this function displays text instructions in grpahics windwow
  
#### 9. drawline()

  ##### signature:
  void drawline()
  
  ##### Description:
  this function draws edges using location stored in linex array

#### 10. blinking_lines()

  ##### signature:
  void blinking_lines()
  
  ##### Description:
  this function does animation of lines connecting after calculating spanning tree

#### 11. drawPointAt()

  ##### signature:
  void drawPointAt(float x,float y)
  
  ##### Description:
  this displays a point when mouse clicked for first time in draw edge mode

#### 12. loadpage()

  ##### signature:
  void loadpage()
  
  ##### Description:
  this function mimics loading animation

#### 13. output()

  ##### signature:
  void output()
  
  ##### Description:
  this function displays text output after calculating spanning tree
  
#### 14. display()

  ##### signature:
  void display()
  
  ##### Description:
  this is callback function called by OpenGL 
  
#### 15. reshape()

  ##### signature:
  void reshape(int w, int h)
  
  ##### Description:
  this is reshape callback function called by OpenGL whenever window is resized
  
#### 16. input()

  ##### signature:
  void input()
  
  ##### Description:
  this function takes cost input from user during edge drawing
  
#### 17. mousefun()

  ##### signature:
  void mousefun(int button,int state,int x,int y)
  
  ##### Description:
  this is mouse callback function called by OpenGL whenever mouse event occurs
  
#### 18. printmatrix()

  ##### signature:
  void printmatrix()
  
  ##### Description:
  this function will print matrix constructed
  
#### 19. isconnected()
 
  ##### signature:
  bool isconnected()
  
  ##### Description:
  this checks if the graph is connected or not
  
#### 20. undo()

  ##### signature:
  void undo()
  
  ##### Description:
  this undo the drawing in the order the graph was drawn
  
#### 21. redo()

  ##### signature:
  void redo()
  
  ##### Description:
  this redo the drawing in the order the graph was drawn
  
#### 22. find()

  ##### signature:
  void find()
  
  ##### Description:
  this will call find_spanning_tree function if graph is connected

#### 23. selectedge() 

  ##### signature:
  void selectedge()
  
  ##### Description:
  this will select edge draw mode 

#### 24. selectnode()

  ##### signature:
  void selectnode()
  
  ##### Description:
  this will select node draw mode 

#### 25. keyboardfun()

  ##### signature:
  void keyboardfun(unsigned char key,int x,int y)
  
  ##### Description:
  this is keyboard callback function called by OpenGL whenever keyboard event occurs
  
#### 26. menu()

  ##### signature:
  void menu(int id)
  
  ##### Description:
  this is menu callback function called by OpenGL as menu function

#### 27. find_spanning_tree()

  ##### signature:
  void find_spanning_tree()
  
  ##### Description:
  this function calculates spanning tree using Prim's algorithm
  
#### 28. main()

  ##### signature:
  int main(int argc,char** argv)
  
  ##### Description:
  Program execution starts from here
























