Download Link: https://assignmentchef.com/product/solved-tetris-bucket-full-game
<br>
<p title="Tetris bucket Full game Solution">



<p class="ui header product-top-header" title="Tetris bucket Full game Solution">You have already displayed the Tetris bucket in your previous project assignment. In this assignment, you will need to display and drop the shape. Add plenty of narrative comments. Your program must be compilable and executable.

If you need guidance, you will find some detailed instruction (below) to assist you. This is not the only approach that will work but it will present one possibility. The sample below uses Classes (a little Object oriented programming) but, if you prefer a different approach, you do not have to use classes in your project.

To represent the Tetris shapes, you can create a Class called “TetrisShape”. In the class, declare a 2-D array of chars that is 4×4 in size (you could also use 4×2 but that would require different algorithm). Call the array “shapeArray”. For convenience, declare it as public (but, it should not be your practice when you work in the software industry). You might need more dimensions for the array if you want to statically assign (hard code) all the shape rotations (3-d) for all the shapes (4-d). In this example, the rotation of the shapes is done by value swapping in the 4×4 array.Now, populate or initialize the “shapeArray”. There are three (3) options for doing this:Option 1: Add a function in the class (call it “populateShapeArray(int shapeType)”), that will take an integer which will denote the type of shape.Option 2: Use a non-default constructor. In this case, when you create an object, you will take an integer as the constructor argument, which will denote the type of shape, as shown below.TetrisShape currentShape = new TetrisShape(shapeType);// shapeType is an intOption 3: Use a setter “setShape(int shapeType)” function.Regardless of which option you chose above, you would use a switch statement to assign the 4×4 array values for the specific shape. For example, for ‘L’, it can be something like the following:

shapeArray[0][0] = ‘ ‘; shapeArray[1][0] = ‘X’; shapeArray[2][0] = ‘ ‘; shapeArray[3][0] = ‘ ‘;

shapeArray[0][1] = ‘ ‘; shapeArray[1][1] = ‘X’; shapeArray[2][1] = ‘ ‘; shapeArray[3][1] = ‘ ‘;

shapeArray[0][2] = ‘ ‘; shapeArray[1][2] = ‘X’; shapeArray[2][2] = ‘X’; shapeArray[3][2] = ‘ ‘;

shapeArray[0][3] = ‘ ‘; shapeArray[1][3] = ‘ ‘; shapeArray[2][3] = ‘ ‘; shapeArray[3][3] = ‘ ‘;Always keep record of the top left corner location (x,y dimensions) of the shape that is falling. This record will indicate where to draw the shape in the bucket after the shape moves. Initially, the location should be, (6, 0), which is the top middle of the bucket. Store the coordinates in the “TetrisShape” class as shapeTopLeftX and shapeTopLeftY. Note, x changes horizontally, and y changes vertically.In this step you will generate one shape. To accomplish this, in the main() function, before the while loop (game loop), do the following:Generate a random number from 0 to 6.Use one of the options presented in step 2 above to create a TetrisShape object.Create a global function called “updatebucket(TetrisShape localTetrisShape)” to populate the bucket with values of the “shapeArray”. Here, you will use two nested for loops to go over the shapeArray of 4×4. You need to provide the TetrisShape object (created in step ‘4b’ above) to the function as an argument in order to access its shapeArray. Inside the loop, you will do this.bucket[i+shapeTopLeftX][j+shapeTopLeftY] = localTetrisShape.shapeArray[i][j];You are actually imposing the shape values on to the bucket.

Call the “updatebucket(TetrisShape localTetrisShape)” function from main() using the object created in step 4b.Display the bucket.Inside the while loop (game loop), as the shape falls, the value of y will increase. In order to accomplish this you will have “newShapeTopLeftY = shapeTopLeftY + 1;” so that the shape falls one cell below. Notice that you are storing the new y value in another variable because you need both the old and the new values.Clear (assign spaces to) the current position values of the shape in the bucket using the “old”shapeTopLeftX and shapeTopLeftY. This will ensure that you do not leave any trail of the shape.Call the “updatebucket(TetrisShape localTetrisShape)” function with the “new” shapeTopLeftX and shapeTopLeftY values. This will ensure the shape will be displayed in the new location (newShapeTopLeftX, newShapeTopLeftY).Display the bucket. The shape is displayed in the new location of the bucket.Store the new shapeTopLeftX and shapeTopLeftY values to the old shapeTopLeftX and shapeTopLeftY values to get ready for the next loop.Sleep for a while to slow down the game.Remember, these are guidelines and are only intended to help you, if you need assistance. If you already know what you need to do, then do it your way.

Submit your completed assignment by following the directions linked below. Please check the Course Calendar for specific due dates.

Save your assignment as a Microsoft Word document.

5/5 - (2 votes)