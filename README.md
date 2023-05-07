Download Link: https://assignmentchef.com/product/solved-lab-5-using-arrays-and-while-loops
<br>
<strong><em>Objectives:</em> </strong>

<ol>

 <li>To practice using one-dimensional arrays in Java.</li>

 <li>To practice using while loops in Java.</li>

 <li>To practice changing pixel colours.</li>

 <li>To learn about collages for Assignment 2.</li>

</ol>

<strong><em>Preparation:</em> </strong>

<ol>

 <li>Go over the Lecture Notes: Topic 5, Topic 6</li>

 <li>Textbook reading (optional): Chapter 4</li>

</ol>

<h1>Exercise 1: Loops and Arrays of Integers</h1>

<ol>

 <li>In this part of the exercise, you will practice writing while loops.

  <ol>

   <li>In the Interactions pane, type the following: int counter = 1; while (counter &lt;= 10 )</li>

  </ol></li>

</ol>

{

System.out.print(“*”);    counter = counter + 1;

}

System.out.println();

How many asterisks are printed?




<ol start="2">

 <li>Reset the Interactions pane. Type statements that print exactly the same thing as the code from step 1, except start the counter at 0.</li>

</ol>




<ol>

 <li>In this part of the exercise, you will practice initializing and working with an array of integers.

  <ol>

   <li>In the Interactions pane, type the following:</li>

  </ol></li>

</ol>




int[] nums = {1,2,3,4,5}; System.out.println(nums[0]);




<ol start="2">

 <li>How would you now print the rest of the items in the array nums?</li>

</ol>




<ol start="3">

 <li>As you probably noticed, this is somewhat tedious (and would get worse if the array contained more items!) We can use a while loop to print all the items in this array. Type the following statements, filling in the blanks with the appropriate numeric values:</li>

</ol>




int index = _____; while (index &lt; _____ )

{

System.out.println(nums[index]);    index = index + 1;

}




<ol start="4">

 <li>Recall that array objects have a public variable called length, which contains the number of items in the array. Type the following statements, filling in the blanks so that it prints all the items in the array:</li>

</ol>




index = _____;

while (index ___ nums.length )

{

System.out.println(nums[index]);    index = index + 1;

}




<ol start="5">

 <li>Now type the following statement:</li>

</ol>




System.out.println(nums[nums.length]);

What happens? Why?




<ol start="6">

 <li>Now suppose we want to initialize an array moreNums of size 100 that contains the integers 1 to 100. It is impractical to do so by using a statement that lists all the values in the array, for example:</li>

</ol>

int [] moreNums = {1, 2, 3, 4, 5, 6, …




We can do this by creating the array, and then using a loop in which we initialize each element with an assignment statement.




Reset the Interactions pane and type the following statements, filling in the blanks. Hint: What integer should be stored in moreNums[0]? in moreNums[1]?




int[] moreNums = new int[ ___ ]; int index = _____; while (index &lt; ______)

{

moreNums[index] = __________;    index = index + 1;

}




<ol start="7">

 <li>Type the statements to print only the first 10 items in the array moreNums, using a while loop. If you did not get the numbers 1 to 10 printed, go back to step 6 and fix your initialization, and then try printing again.</li>

</ol>

<strong> </strong>

<h1>Exercise 2: Changing the Color of Pixels</h1>

In the Interactions pane, make a variable pictureObj refer to a picture that contains the image in the file <em>caterpillar.jpg</em> that is in your mediaSources folder. (Refer back to Lab 4 Exercise 1 if you need to).




We have seen the following methods:

<ul>

 <li>getPixel(x,y) of the Picture class, which allows you to access one of the pixels in a picture</li>

 <li>setColor(aColor) of the Color class, which can be used to change the colour of a pixel.</li>

</ul>

We can use these methods to change the colour of the following pixels of the caterpillar picture to black:




(100,100), (101,101), (102,102), (103,103), (104,104), (105,105), (106,106)




One way to do this is to type the following sequence of Java statements in the Interactions Pane (note that you can repeat the previous line in the Interactions pane by using the up-arrow key, and then edit the line before hitting Enter for that line – this saves a lot of typing!)




import java.awt.Color;

pictureObj.getPixel(100,100).setColor(Color.black); pictureObj.getPixel(101,101).setColor(Color.black); pictureObj.getPixel(102,102).setColor(Color.black); pictureObj.getPixel(103,103).setColor(Color.black); pictureObj.getPixel(104,104).setColor(Color.black); pictureObj.getPixel(105,105).setColor(Color.black); pictureObj.getPixel(106,106).setColor(Color.black); pictureObj.repaint();




How does the above sequence change the image?

<h1>Exercise 3: Using a Loop to Change the Color of Pixels</h1>

Setting the colour for a series of pixels as in the previous exercise is tedious.  It is also repetitive, so we have an opportunity to use a loop construct here!




In this exercise, you will write a complete program that draws a line in a picture. Enter the following code in the Definitions pane, filling in the missing statements as specified by the comments within the code.




import java.awt.Color; public class DrawLine

{

public static void main (String[] args) {




/* add code here to choose a filename of an image,     create a Picture object from the image (referenced by    the variable pictureObj), and then display the picture    on the screen */

int i = 0;

while(i&lt;25)

{

pictureObj.getPixel(100+i,100+i).setColor(Color.black);          i++;       }

pictureObj.explore();

}

}




Save it as the file <em>DrawLine.java,</em> compile it, fix any errors, and run the program, choosing the file <em>caterpillar.jpg   </em>How does it change the image you got from <em>caterpillar.jpg</em>?




Try using the <em>Zoom</em> feature of the Picture Explorer (button in top left corner). You will be able to see individual pixels in lines in the image.

<h1>Exercise 4: Adapting Your Program to Change More Pixels</h1>

Now, add code to your DrawLine program to also draw a magenta vertical line of 25 pixels and a white horizontal line of 25 pixels in the caterpillar image, both starting at (100,100).  Compile and run your modified program.

<h1>Exercise 5: Creating a Collage</h1>

A <em>collage </em>is a collection of pictures copied to some background image.  The purpose of this exercise is to have you create a simple collage, in preparation for Assignment 2.

<ol>

 <li>Download the file <em>java</em> from the Labs link (under Lab 5), open it in DrJava and compile it. It is a modified version of the<em> Picture.java</em> provided by the textbook, with an added method called copyPictureTo() which has the following header:</li>

</ol>




public copyPictureTo(Picture sourcePicture, int xStart, int yStart)




This method will copy the <em>source picture</em> that is passed in as a parameter, into the <em>target picture</em> (the picture object on which the method is invoked). The parameters xStart and yStart are the (x,y) positions at which to start the copy into the target picture. You will be invoking this method in steps c) and d) below.   <em> </em>

<ol>

 <li>Reset the Interactions pane. To create and view a “blank” picture (which will be the background for our collage, and which we will call the “canvas”), type the following sequence of statements in the Interactions pane:</li>

</ol>

Picture canvas = new Picture(640,480);    canvas.show();

<ol>

 <li>In your mediaSources folder there are two images of flowers, each 100 pixels per side. You will be copying them onto the canvas, one at a time, using the copyPictureTo() First type in the following statements, choosing the file <em>flower1.jpg</em>. (Note that sometimes the FileChooser window comes up hidden behind DrJava.)</li>

</ol>

String fileName1 = FileChooser.pickAFile();     Picture picFlower1 = new Picture(fileName1);     canvas.copyPictureTo(picFlower1,100,0);     canvas.repaint();

<ol start="2">

 <li>Now type in statements to copy the image in <em>jpg</em> onto the canvas, at the position</li>

</ol>

(300,0). Hint: first create a Picture object, as in step c), perhaps using the variable names fileName2 and picFlower2 for your reference variables.




<ol>

 <li>Save the canvas to a file by typing the following statement:</li>

</ol>




canvas.write(“Z:/collageLab5.jpg”);




<ol>

 <li>Check the image in your new JPEG file by opening it with the Picture Explorer (the explore method):</li>

</ol>




String fileName = FileChooser.pickAFile();

Picture pictureObj = new Picture(fileName); pictureObj.explore();







<strong>  </strong>